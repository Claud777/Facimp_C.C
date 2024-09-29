#ADS 

[[VM em C.C]]

- O projeto:
	O plano é criar dois servidores: Um servidor alocado em uma Maquina Virtual (VM) utilizando a plataforma de virtualização VmWare e o sistema Linux Debian, dentro do servidor colocaremos um Docker e um contêiner.
	Foi sugerida a hospedagem de um site dentro deste servidor para ser usado na apresentação do projeto.
	
	Obs:
	Como o objetivo final desse projeto é a realização de uma atividade conjunta entre as turmas de CloudCom e CyberSec, o servidor deve estar preparado para receber ataques realizados pela classe de red-team

- Segurança:
	Eu, o encarregado pela segurança do servidor fui incumbido de compreender e aplicar camadas de segurança e monitoramento de acesso no mesmo, as camadas de segurança seguem um embasamento em normas de cyber segurança divulgadas por órgãos competentes, tendo como referencia um TCC feito por estudantes em 2002, eu redigi os mesmos padrões de segurança e irei adapta-los para nosso uso: ![[Segurança e monitoramento de servidores Linux]]
	Referencia: -> [[MONOGRAFIA_Segurança computacional segurança em servidores linux em camadas.pdf]]

- Sugestões:
- Firewalld: Ferramenta utilizada para proteção do Linux: Partindo do pressuposto uso de ferramentas para melhoria da segurança de servidores linux, o Firewalld é mais uma ferramenta para controle de acesso a servidores linux, atuando como firewall, como seu proprio nome já diz
	[Firewalld](https://hackmd.io/@RATM/BJBJkZmZ3?utm_source=preview-mode&utm_medium=rec)