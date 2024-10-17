##### O primeiro passo após realizar a instalação da maquina virtual é criar uma nova VM e definir qual sistema operacional utilizar, no caso, utilizaremos a distribuição Linux Debian.
#### clicando em "Novo", aparecerá 
##### ![[Pasted image 20240930003429.png]] - defina um nome e escolha o local da imagem ISO da distribuição Linux 
##### - após definir essas duas etapas, automaticamente o tipo e a versão ja irão aparecer.
##### - aperte em pular instalação desassistida e aperte em próximo![[Pasted image 20240930003758.png]]
##### - Aqui definimos o hardware da nossa máquina virtual. Como é apenas um teste, utilizaremos 4g de memória RAM e 3 processadores
![[Pasted image 20240930004056.png]]
 ##### - Aqui colocamos quantidade de armazenamento da VM. Colocarei 20GB mesmo![[Pasted image 20240930004507.png]]
 ##### - Nessa parte é informada as configurações que acabamos de definir.
![[Pasted image 20240930004640.png]]
##### - Após clicar em finalizar... aparecerá a nossa VM na tela inicial do VirtualBox.
![[Pasted image 20240930004745.png]]
##### - clicando com o botão direto do mouse e apertando em "Configurações"
![[Pasted image 20240930005033.png]]
##### - Vamos modificar as configurações da rede para que o Proxmox reconheça nossa rede e consiga hospedar o servidor.
![[Pasted image 20240930005246.png]]
##### - Clicando em "Placa em modo Bridge", estaremos fazendo com que a maquina virtual fique conectada com a nossa rede.
##### - Clicando em "Avançado" e modificando o "Modo Promíscuo" para "Permitir tudo", estaremos autorizando a maquina virtual utilizar vms, entre outros.![[Pasted image 20240930005645.png]]
##### agora vamos adicionar a ISO do proxmox no debian diretamento pela configuração para facilitar. Aperte na ISO do proxmox-ve
![[Pasted image 20241002195723.png]]

##### Após adicionar, aperte em "OK" e ja poderemos iniciar a máquina virtual
![[Pasted image 20241002195904.png]]

##### Após deixarmos iniciar, aparecerá a interface do proxmox. Aperte na primeira opção.
![[Pasted image 20241002200107.png]]

### Aceite os termos
![[Pasted image 20241002200302.png]]

Aqui definimos o armazenamento do Proxmox. deixarei padrão
![[Pasted image 20241002200521.png]]

Aqui definimos a localização(Definição errada poderá ocorrer instabilidades  )
![[Pasted image 20241002200700.png]]

Aqui definimos o email e senha do nosso proxmox. Utilizaremos mais tarde.
![[Pasted image 20241002200927.png]]

Nessa parte é definido hostname(pode ser um aleatório) e o IP local para a utilização do proxmox. Como configuramos no começo a rede, não será necessário modificar a parte do ip
![[Pasted image 20241002201300.png]]

Aqui mostra todas as configurações que você fez. aperter em "Install"
![[Pasted image 20241002201606.png]]


![[Pasted image 20241002204130.png]]
