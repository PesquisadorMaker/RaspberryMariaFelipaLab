# RaspberryMariaFelipaLab

Projeto: Implementação de um Servidor Web Multifuncional com Raspberry Pi 3

Introdução:
No mundo atual, a demanda por servidores web flexíveis e de baixo custo está em constante crescimento, especialmente para pequenas empresas, projetos pessoais e fins educacionais. Nesse contexto, o Raspberry Pi 3 se destaca como uma opção acessível e versátil para a criação de servidores web. Este projeto visa demonstrar como configurar um servidor web completo utilizando o Raspberry Pi 3, oferecendo suporte para uma variedade de tecnologias, incluindo PHP, MySQL, JavaScript, Python e HTML.

Objetivo:
O objetivo principal deste projeto é auxiliar o aluno, criar um servidor web multifuncional utilizando o Raspberry Pi 3 para serem aplicados as atividades sugeridas. Este servidor será capaz de hospedar sites dinâmicos das atividades interativas, como também da possibilidade de criaqr aplicações web com bancos de dados

Componentes Necessários:

    Raspberry Pi 3 (com fonte de alimentação, cartão microSD e caixa para proteção)
    Cabo de rede Ethernet ou apenas configurando o Wi-Fi interno
    Monitor HDMI, teclado, mouse e caixa de som
    Acesso à internet para instalação dos programas

Passos do Projeto:

    Instalação do Sistema Operacional:
        Baixe e instale o sistema operacional Raspberry pi e instale utilizando um balena etcher para o cartão microSD.
        Insira o cartão microSD no Raspberry Pi 3 e inicie o sistema.

    Configuração da Rede:
        Conecte o Raspberry Pi 3 à sua rede local através de um cabo Ethernet ou adaptador Wi-Fi.
        Configure as opções de rede no sistema operacional para garantir conectividade com a internet.

    Instalação dos Componentes do Servidor:
        Utilize o terminal para instalar os seguintes componentes:
            Servidor Apache: Para hospedar páginas web.
            PHP: Para processamento de scripts do lado do servidor.
            MySQL: Para gerenciamento de banco de dados.
            Python: Para suporte a aplicativos e scripts.
            Node.js: Para execução de aplicativos JavaScript no servidor.

+ No terminal linux, faça este comando conforme abaixo e aperte enter para confirmar
sudo apt update && sudo apt upgrade -y

+ No terminal linux, faça este comando conforme abaixo e aperte enter para confirmar
sudo apt install apache2 -y

+ No terminal linux, faça este comando conforme abaixo e aperte enter para confirmar
cd /var/www/html

+ No terminal linux, faça este comando conforme abaixo e aperte enter para confirmar
ls -al index.html

+ No terminal linux, faça este comando conforme abaixo e aperte enter para confirmar
/var/www/html $ hostname -I	

+ No terminal linux, faça este comando conforme abaixo e aperte enter para confirmar
sudo apt install php -y

+ No terminal linux, faça este comando conforme abaixo e aperte enter para confirmar
sudo service apache2 restart

+ No terminal linux, faça este comando conforme abaixo e aperte enter para confirmar
+banco de dados

+ No terminal linux, faça este comando conforme abaixo e aperte enter para confirmar
sudo apt install mariadb-server php-mysql -y

+ No terminal linux, faça este comando conforme abaixo e aperte enter para confirmar
sudo service apache2 restart

+ No terminal linux, faça este comando conforme abaixo e aperte enter para confirmar
sudo mysql_secure_installation

+ No terminal linux, faça este comando conforme abaixo e aperte enter para confirmar
sudo mysql --user=root --password

+ No terminal linux, faça este comando conforme abaixo e aperte enter para confirmar
create user admin@localhost identified by 'sua_senha_aqui';

+ No terminal linux, faça este comando conforme abaixo e aperte enter para confirmar

+ No terminal linux, faça este comando conforme abaixo e aperte enter para confirmar
grant all privileges on *.* to admin@localhost;

+ No terminal linux, faça este comando conforme abaixo e aperte enter para confirmar
FLUSH PRIVILEGES;
+ No terminal linux, faça este comando conforme abaixo e aperte enter para confirmar
exit;

+ No terminal linux, faça este comando conforme abaixo e aperte enter para confirmar
sudo apt install phpmyadmin -y

    Selecione Apache2 quando aparecer como opção e depois aperte a tecla ENTER
    Configurando phpmyadmin? OK
    Configurando database para phpmyadmin com dbconfig-common? Yes
    Coloque a senha desejada e afirma com a tecla ENTER


+ No terminal linux, faça este comando conforme abaixo e aperte enter para confirmar
sudo phpenmod mysqli

+ No terminal linux, faça este comando conforme abaixo e aperte enter para confirmar
sudo service apache2 restart

+ No terminal linux, faça este comando conforme abaixo e aperte enter para confirmar
+Teste em um browser da internet (firefox)

http://localhost/phpmyadmin


+No terminal linux, faça este comando
sudo ln -s /usr/share/phpmyadmin /var/www/html/phpmyadmin

ls
phpmyadmin


ls -lh /var/www/

sudo chown -R pi:www-data /var/www/html/

sudo chmod -R 770 /var/www/html/

ls -lh /var/www/

  

Conclusão:
O Raspberry Pi 3 oferece uma solução econômica e poderosa para a criação de servidores web multifuncionais. Com a configuração adequada e a escolha dos componentes certos, é possível criar um servidor capaz de atender às demandas de hospedagem web, desenvolvimento de aplicativos e gerenciamento de bancos de dados. Este projeto proporciona uma oportunidade para explorar e aprender sobre tecnologias de servidor web de uma maneira prática e acessível.

