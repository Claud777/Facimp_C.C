
Foi trabalhada a possibilidade de usar o software Proxmox para o gerenciamento do servidor porém, a partir de uma analise de caso de uso, foi concluído que o mesmo só seria viável no ramo empresarial por trabalhar melhor com servidores dedicados e que permanecem ligados o tempo todo, relatado em detalhes no arquivo a seguir:

O Proxmox é uma distro Linux de código aberto com a funcionalidade voltada para a virtualização e integração de sistemas de containers, sendo muito usada no ramo profissional para a criação de maquinas AVS e servidores, com ele é possível criar, gerenciar e utilizar varias maquinas virtuais alocadas em um único computador, possibilitando uma praticidade na utilização das maquinas virtuais, sua instalação é relativamente fácil, sendo necessários apenas um pen-drive bootavel com o software do proxmox, após a instalação, o único momento em que se faz necessário o uso de uma interface gráfica na maquina onde está sendo instalada o Proxmox, é no momento em que será necessário obter o IP do servidor para acesso ao Dashboard.

Em uma analise de caso de uso, se torna perceptível que apesar de ser uma ferramenta util para a criação de maquinas virtuais, o Proxmox tem seu uso mais efetivo em maquinas com destino exclusivamente voltado para função de servidores, no caso de nosso exercicio, onde iremos criar uma maquina virtual em um computador de uso pessoal, o Proxmox se torna desnecessário, já que as configurações da maquina podem ser feitas pelo proprio software virtualizador como VmWare ou OracleVB.

Outro fator que torna inviável o uso do Proxmox no projeto é o custo gerado pela necessidade de uma maquina especifica para a função de servidor, a mesma precisaria ficar ligada o tempo todo para receber as requisições de usuários, e no nosso caso tal maquina serviria apenas para fins didaticos, sendo desnecessário a sua existência após o termino do projeto.

Fica claro a capacidade da ferramenta e da possibilidade de uso da mesma em maquinas para uso de ambientes profissionais, o conhecimento e aprendizado adquirido sobre a mesma poderá ser util futuramente em ambientes empresariais ou ainda ser utilizado na criação de servidores NAS para uso pessoal.

<iframe
		  id="inlineFrameExample"
		  title="Inline Frame Example"
		  width="800"
		  height="400"
		  src="https://diolinux.com.br/video/crie-seu-servidor-em-casa-com-proxmox.html#:~:text=O%20PROXMOX%20é%20uma%20distro,que%20já%20apresentamos%20por%20aqui!">
</iframe>	

Pesquisa:
1. Requisitos para a instalação do Proxmox
	1. Necessário saber as preparações à serem feitas antes de instalar o Proxmox
	2. Ex: Configurações da VM para suportar o Proxmox
2. Requisitos para uso do Proxmox
	1. Necessário saber as configurações necessárias para o bom funcionamento do Proxmox na VM
	2. Configuração de vídeo (se existente) capacidade de armazenamento e de memoria
3. Como é feita a instalação do Proxmox na VM
4. Como utilizar o Proxmox
5. Estrutura de VM's do Proxmox
	1. Previa organização das VM's armazenadas dentro do Proxmox
6. Configurações ativadas no Proxmox
	1. Ferramentas de proteção e configurações á serem ativadas dentro do Proxmox
7. Serviços integrados no Proxmox
	1. Pesquisa aprofundada sobre as integrações de serviços do Proxmox sejam estes adicionados pela equipe ou pré-existentes
8. Threat Hunter da implementação e uso do Proxmox
	1. Caça aos possíveis erros e dificuldades que podem surgir durante o processo de instalação e uso do Proxmox