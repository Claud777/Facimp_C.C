### Requisitos Zabbix
Para a instalação do Zabbix, primeiro é necessário certificar que a maquina virtual atenda os requisitos de configuração mínima para a boa operação do Zabbix
- [ ] 128MB de memória
- [ ] 256MB de armazenamento
- [ ] CPU - 1Ghz

Precauções de uso por parte do cliente ou operador devem ser ter acesso a um navegador web com cookies e Scripts habilitados.
	Obs. Tenha em vista que a quantidade de memoria e armazenamento necessários podem variar de acordo com o numero de hosts que serão monitorados pelo Zabbix

### Requisitos NginX
Para a instalação do NginX, primeiro é necessário certificar que a maquina virtual atenda os requisitos de configuração mínima para a boa operação do NginX
- [ ] 512MB de memória
- [ ] 50MB de armazenamento
- [ ] CPU - 1Ghz

Precauções devem ser tomadas por parte do operador, como a configuração do *Firewall* (caso existente) para que permita a funcionalidade plena do NginX
	Obs. Tenha em vista que a quantidade de memoria e armazenamento necessários podem variar de acordo com o numero de hosts que serão monitorados pelo Zabbix

### Instalação e configuração do Zabbix e NginX no Debian 12

*É recomendável que sejam implementadas melhorias no bash do Debian para executar os comandos de instalação que serão executados no artigo a seguir.*

Acesse o terminal e execute o seguinte comando:
	`1 # apt -y install nginx`
	`2 # sed -i 's/# server_tokens/server_tokens/' /etc/nginx/nginx.conf`
	`3 # systemctl restart nginx`

Agora para a instalação do Zabbix, é necessário primeiro instalar um banco de dados compatível com o software, nesse exemplo utilizaremos o PHP8
No terminal execute o codigo:
	`1 #  apt -y install --no-install-recommends \`
	`2 # php php-{fpm,cli,mysql,pear,gd,gmp,bcmath,mbstring,curl,xml,zip,json,pgsql}`

O comando abaixo aumenta o limite de tempo maximo de Upload no PHP

	 `1 # vim /etc/php/8.2/fpm/php.ini`

Pode se fazer necessário encontrar a linha *max_execution_time* e alterá-la para o valor 600 e a linha *upload_max_filesize* para o valor 100MB

Após realizados os passos, reinicie o PHP com o seguinte comando:

	`1  # systemctl restart php8.2-fpm`

### Instalação do PostGreSQL

Para instalar os pacotes do postgreSQL execute os comandos abaixo:

	´1 # apt -y install postgresql postgresql-contrib´

Altere para o usuário postgres.

	´1 # su - postgres´

Acesse o terminal de comando do banco de dados

	´$ psql´

Defina a senha de usuário postgres e instale o adminpack

	´1 # postgres=# \password postgres
	´2 # Digite nova senha para postgres: ´
	´3 # Digite-a novamente:´
	´4 # postgres=# CREATE EXTENSION adminpack;´
	´5 # CREATE EXTENSION´
	´6 # postgres=# \q ´
	´7 # $ exit´

Realize ajustes no arquivo pg_hba.conf para autenticação com senha.

	´1 # sed -1 '/postgres.*peer/s/peer/md5/' /etc/postgresql/15/main/pg_hba.conf´
	´2 # sed -1 '0,/local\s*all\s*all\s*peer/s/peer/md5/' /etc/postgresql/15/main/pg_hba.conf´

Ajuste as configurações padrões do PostgreSQL conforme a memória disponivel

	´1 vim /etc/postgresql/15/main/postgresql.conf´

    -----------------------------------------
	2 # 4GB de Memoria RAM
	-----------------------------------------
	´4 max_connections = 500´
	´5 shared_buffers = 1GB´
	´6 work_mem = 16MB´
	´7 maintenance_work_mem = 128MB´
	´8 max_wal_size = 1GB´
	´9 min_wal_size = 256MB´
	´10 effective_cache_size = 2GB´
	-----------------------------------------
	´8GB de Memoria RAM´
	-----------------------------------------
	´max_connections = 1000´
	´shared_buffers = 2GB´
	´work_mem = 32MB´
	´maintenance_work_mem = 512MB´
	´max_wal_size = 2GB´
	´min_wal_size = 512MB´
	´effective_cache_size = 4GB´ 
	-----------------------------------------
	´16GB de Memoria RAM´
	-----------------------------------------
	´max_connections = 2000´
	´shared_buffers = 4GB´
	´work_mem = 64MB´
	´maintenance_work_mem = 1GB´
	´max_wal_size = 4GB´
	´min_wal_size = 1GB´
	´effective_cache_size = 8GB´

Após realizadas as configurações, reinicie o serviço:

	´1 # systemctl  restart postgresql´

Para a instalação do Zabbix 7 LTS siga as instruções do site oficial do Zabbix:
	[Documentação Zabbix](https://www.zabbix.com/br/download)
