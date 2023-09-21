# Projeto 01 - Projeto de Administração de Redes usando Vagrant com 3 VMs

### Proposta

Você é responsável por configurar um ambiente de laboratório de administração de redes com 3 máquinas virtuais (VMs) usando o Vagrant. Este ambiente de laboratório será usado para fins educacionais e de treinamento em administração de redes. As três VMs devem ser configuradas da seguinte forma:

1. VM1 - Servidor Web (Privado)
   - Sistema Operacional: Ubuntu Server 20.04 LTS
   - Interface de Rede 1 (eth0): IP Privado Estático (192.168.56.10)
   - Função: Servidor Web (instalar o Apache)
   - Pasta Compartilhada: `/var/www/html` na máquina host deve ser compartilhada com `/var/www/html` na VM1.

2. VM2 - Servidor de Banco de Dados (Privado)
   - Sistema Operacional: Ubuntu Server 20.04 LTS
   - Interface de Rede 1 (eth0): IP Privado Estático (192.168.56.11)
   - Função: Servidor de Banco de Dados (instalar o MySQL ou PostgreSQL)

3. VM3 - Gateway (Privado DHCP e Pública)
   - Sistema Operacional: Ubuntu Server 20.04 LTS
   - Interface de Rede 1 (eth0): IP Privado Estático (192.168.56.12)
   - Interface de Rede 2 (eth1): IP Público DHCP
   - Função: Gateway de Rede
   - Deve fornecer acesso à Internet para as VMs1 e VM2.

Seu objetivo é criar um ambiente de laboratório onde VM1 e VM2 podem se comunicar através da rede privada (192.168.56.0/24) e VM3 atua como um gateway, fornecendo acesso à Internet para VM1 e VM2 através de sua interface de rede pública.

### Subindo as VM'S

1. Primeiramente escolha a pasta você irá manipular esse ambiente.
2. Abra com o terminal no local e clone este repositorio.
3. Ainda no terminal utilize o comando `cd VM[subtiuir pelo numero da VM que irá ser manipulada]`. Exemplo:`cd VM1`.
4. Dentro do diretorio você deverá digitar e rodar os seguintes comandos:
   - `vagrant up`
     - comando acima é responsável por colocar a vm provisionada no **Vagrantfile** em funcionamento.
   - `vagrant provision`
     - O comando acima é só uma garantia de que as linhas de comando configuradas no Vagrantfile rodem e termine a configuração da máquina.
5. Realize o processo em todas as pastas onde estão as VM1, VM2 E VM3 e seu ambiente de laboratório estará configurado e pronto para uso. Lembrando que a internet e a conexão com a vm3 só funcionarão quando as 3 VM's forem provisionadas.

:exclamation: **IMPORTANTE**: Lembrando que a internet e a conexão com a vm3 só funcionarão quando as 3 VM's forem provisionadas.

:notebook: **NOTA**: Caso encontre algum erro e queira contribuir, coloque um pull request :) .
