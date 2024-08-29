# Instala-o-rede-TrueNAS
Instalando e Configurando Rede - Servidor de Arquivos TrueNAS

![Title](imagens/LOGO.jfif)

Faça o Download do True NAS CORE - LINK

**INSTALANDO TrueNAS**

1º - Crie um Pendriver bootavel, no caso, utilizei o RUFUS.

 2º - Coloque o Pendriver no Servidor e escolha ele na opção de boot.

![Title](imagens/2.jfif)

3º - Essa é a tela inicial de instalação, aperte ENTER para escolher a 1º opção ou espere 10 segundos. O Kernel de instalação será carregado.

![Title](imagens/3.jfif)

4º - Escolha a opção 1 - Install/Upgrade

![Title](imagens/4.jfif)

5º - Se seu servidor estiver com menos de 8 GB de memória RAM, ele exibirá essa mensagem de aviso, escolha Yes para continuar.

![Title](imagens/5.jfif)

6º - Escolha o disco onde o TrueNAS será instalado.

![Title](imagens/6.jfif)

7º - Neste tela de aviso sobre o dispositivo de armazenamento, escolha Yes.

![Title](imagens/7.jfif)

8º - Escolha sua senha do usuário root.

![Title](imagens/8.jfif)

9º - Escolha a opção BIOS ou UEFI ( veja qual sistema o seu servidor possui )

![Title](imagens/9.jfif)

10º - Escolha Create Swap para criar automaticamente uma partição de troca.

![Title](imagens/10.jfif)

11º - TrueNAS será instalado.

![Title](imagens/11.jfif)

12º - Instalação Concluída com Sucesso, aperte ENTER.

![Title](imagens/12.jfif)

13º - Escolha a opção 3 - Reboot System e retire o Pendriver.

![Title](imagens/13.jfif)

14º - Tecle Enter para bootar o TrueNAS

![Title](imagens/14.jfif)

15º - TrueNAS será carregado.

![Title](imagens/15.jfif)

16º - TrueNAS carregado e instalado. 
Note que ele pegou ip do meu DHCP (192.168.50.13), você pode acessar via web com este ip. 

![Title](imagens/16.jfif)

**CONFIGURANDO REDE NO TrueNAS**

Para saber se o server está conectado a rede, entre no Shell com a opção 9 e faça um teste de ping.

ping www.google.com
se pingar, prossiga configurando um IP estático. 

![Title](imagens/17.jfif)

Aperte CTRL + C para parar o ping e de um EXIT para voltar ao MENU.

1º - Aperte 1 e tecle ENTER para escolher a primeira opção - Configure Network Interfaces

![Title](imagens/18.jfif)

2º - O sistema vai mostrar suas interfaces disponíveis, escolha a 1 e tecle ENTER.

![Title](imagens/19.jfif)

3º - escolha a opção N

![Title](imagens/20.jfif)

4º - Ele nos perguntará se queremos configurar DHCP neste interface, escolha N.

![Title](imagens/21.jfif)

5º - escolha Y para configurar o IPv4.

![Title](imagens/22.jfif)

6º - Vamos mudar o nome da Interface para eth0.

![Title](imagens/23.jfif)

7º - Escolha um ip dentro da sua faixa de rede, eu coloquei 192.168.10.132.

![Title](imagens/24.jfif)

8º - Escolha a mascara da sua rede, ex: 255.255.255.0

![Title](imagens/25.jfif)

9º - Escolha N para não configurar um IPv6, o sistema vai salvar e retorna ao menu principal.

![Title](imagens/26.jfif)

10º - Vamos configurar nosso Gateway, escolha a opção 4 - Configure Default Route

![Title](imagens/27.jfif)

11º - Escolha Y para configurar o IPv4 do seu Gateway ( Roteador ).

![Title](imagens/28.jfif)

12º - Coloque o IP do seu Roteador.

![Title](imagens/29.jfif)

12º - Escolha N para não configurar um IPv6.

![Title](imagens/30.jfif)

Agora vamos configurar um DNS para nosso servidor.

Se você possui um DNS server na sua rede, pode utiliza-lo, caso contrario, você pode utilizar o DNS do Google.

DNS Primário: 8.8.8.8

1º - Escolha a opção 6 - Configure DNS

![Title](imagens/31.jfif)

2º - Coloque o IP do servidor DNS.

![Title](imagens/32.jfif)

3º - Você pode colocar o nome do Servidor DNS ou deixar em branco apertando ENTER.

![Title](imagens/33.jfif)

Pronto, IP, Gateway e DNS Configurado. 

Vamos testar!

Entre no Shell com a opção 9 e faça um ping para o seu roteador, se pingar, faça novamente um ping para a rede externa, como o www.google.com.

![Title](imagens/34.jfif)

![Title](imagens/35.jfif)

Servidor pingando corretamente. 

Agora use um computador na mesma rede e faça um acesso via Web usando o ip do seu servidor. 

Faça login com usuário root e a senha que você escolheu durante a instalação.

![Title](imagens/36.jfif)

Até a próxima!!!
