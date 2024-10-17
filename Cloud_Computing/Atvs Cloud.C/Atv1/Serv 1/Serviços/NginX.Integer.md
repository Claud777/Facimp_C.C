[NGINX](https://www.hostinger.com.br/tutoriais/o-que-e-nginx#:~:text=NGINX%2C%20pronunciado%20“engine-ex,lançado%20em%20Outubro%20de%202004.) A ideia de usar o Nginx no servidor apareceu a partir do network com outros desenvolvedores, o NginX é um software para servidores que disponibiliza varias ferramentas para uso em controle de servidores web, sendo ideal para lidar com um grande fluxo de requisições em um site, além de possibilitar uma otimização do acesso web do servidor ele também fornece ferramentas de segurança para o mesmo.

<iframe
		  id="inlineFrameExample"
		  title="Inline Frame Example"
		  width="800"
		  height="400"
		  src="https://blog.eveo.com.br/nginx">
	</iframe>

O Nginx fornece ferramentais para monitoramento de acessos ao servidor, como Log de acessos e de erros, obtendo informações sobre o requisitante e o requisito, quanto aos logs de erros, pode se obter informações como o código do erro e o arquivo de origem. A partir de uma analise dos logs de acesso e dos logs de erros, pode-se obter uma boa informação sobre as tentativas de invasão ao seu servidor e as principais brechas exploradas, se tornando assim uma ferramenta importante de auxilio no monitoramento do servidor

<iframe
		  id="inlineFrameExample"
		  title="Inline Frame Example"
		  width="800"
		  height="400"
		  src="https://pt.linkedin.com/advice/1/how-can-you-use-nginx-logs-detect-mitigate-opgae?lang=pt">
</iframe>

Pesquisa:
1. Requisitos para a instalação do NginX
	1. Necessário saber as preparações à serem feitas antes de instalar o NginX
	2. Ex: Configurações da VM para suportar o NginX
2. Requisitos para uso do NginX
	1. Necessário saber as configurações necessárias para o bom funcionamento do Docker na VM
	2. Configuração de vídeo (se existente) capacidade de armazenamento e de memoria
3. Como é feita a instalação do NginX no Debian
4. Como utilizar o NginX
5. Configurações ativadas no NginX
	1. Ferramentas de proteção e configurações á serem ativadas dentro do NginX
6. Threat Hunter da implementação e uso do NginX
	1. Caça aos possiveis erros e dificuldades que podem surgir durante o processo de instalação e uso do NginX

O NginX pode se comunicar com o Apache para executar um controle de acesso a sites estáticos e dinâmicos, funcionando como um semelhante ao firewall mas ainda sendo um proxy-reverso

"O NginX exercendo sua função de proxy reverso requisita o IP do firewall onde está hospedado o host para disponibilizar o site, cabe ao firewall disponibilizar ou não o IP, caso seja fornecido, o IP e a localização do firewall onde o mesmo está hospedado será armazenado no Proxy reverso, caso não, apenas o local será armazenado e cabe ao firewall reter e se responsabilizar pelas informações acessadas pelo host."