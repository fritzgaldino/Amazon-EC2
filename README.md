# Amazon EC2 - Elastic Compute Cloud

O Amazon Elastic Compute Cloud (Amazon EC2) é um serviço web que oferece capacidade computacional segura e escalável na nuvem. Com o EC2, é possível provisionar servidores virtuais, conhecidos como instâncias EC2. Você pode criar uma ou várias instâncias e pagar apenas pelo tempo de uso, conforme o tipo de instância selecionado. Quando não precisar mais de uma instância, é possível pará-la ou encerrá-la, evitando cobranças adicionais.

Para criar uma instância EC2, é essencial conhecer alguns serviços importantes:

1. AMI - Amazon Machine Image
A primeira configuração ao iniciar uma instância EC2 é definir o sistema operacional desejado (Windows, Linux, entre outros) utilizando uma Amazon Machine Image (AMI). A AMI contém todas as informações necessárias para executar uma instância.

2. Tipo de Instância
As instâncias EC2 variam em capacidade. É crucial escolher o tipo de instância adequado às suas necessidades. Por exemplo, as instâncias T2 são de uso geral e podem ser usadas para diversas cargas de trabalho.

3. Amazon VPC - Virtual Private Cloud
A Amazon VPC oferece uma rede virtual isolada. Se não for especificado, a instância EC2 é executada em uma VPC padrão, eliminando a necessidade de criar e configurar uma rede manualmente.

4. Security Group - Grupo de Segurança
Um grupo de segurança atua como um firewall virtual para instâncias EC2, controlando o tráfego de entrada e saída. Se não especificado, o Amazon EC2 usa o grupo de segurança padrão da VPC ao iniciar uma instância.

5. Key Pair - Par de Chaves
Um par de chaves consiste em uma chave pública e uma chave privada, usadas como credenciais de segurança para se conectar a uma instância EC2. Para instâncias Windows, a chave privada é necessária para descriptografar a senha do administrador usada na conexão com a instância.

Compreender esses serviços é essencial para utilizar o Amazon EC2 de forma eficaz e segura, aproveitando ao máximo sua flexibilidade e escalabilidade na nuvem.

Feito a compreensão, então vamos lá, mão na massa. Vamos criar Instância EC2 Windows Server.


1 - Após acessar o console da AWS, pesquise por EC2
![image](https://github.com/fritzgaldino/Amazon-EC2/assets/87190206/0bee6475-4f4a-46f1-b84f-13da140fb4d2)

2 - Clique em iniciar instâncias (Launch Instance)
![image](https://github.com/fritzgaldino/Amazon-EC2/assets/87190206/bcc8551a-c59e-4e42-a6c3-d411d1786744)

3 - Adicione um nome para a instância
![image](https://github.com/fritzgaldino/Amazon-EC2/assets/87190206/cd7b22f1-3551-4214-8d5e-84e9ca621d72)

4 - Defina o sistema operacional por meio da AMI – Amazon Machine Image
* importante verificar a elegibilidade (nível gratuito), escolhi o Sistema operacional Windows Server
![image](https://github.com/fritzgaldino/Amazon-EC2/assets/87190206/4c60360c-7394-42bc-b885-1a21cdb5ddf3)

5 - Escolha o tipo de instância – t2 (nível gratuito)
![image](https://github.com/fritzgaldino/Amazon-EC2/assets/87190206/b8414191-7592-4ab8-9acc-e822d86a4322)

6 - Clique em Criar um novo par de chaves – para poder conectar à máquina virtual
![image](https://github.com/fritzgaldino/Amazon-EC2/assets/87190206/9dde825d-f0e0-4620-bac7-cb5d60415179)

7 - Adicione um nome a seu par de chaves, clique no formato “. pem” via SSH, clique para criar par de chaves
![image](https://github.com/fritzgaldino/Amazon-EC2/assets/87190206/326bf111-2f5d-4835-a9c9-a5e015ea5a32)

8 - Arquivo gerado
![image](https://github.com/fritzgaldino/Amazon-EC2/assets/87190206/f2a087e7-c443-4db7-aa45-a9a482526694)

9 - Configurações de rede – VPC
* Marcar onde está azul (trafego de rede), as outras configurações com relação a vpc e grupos de segurança permaneceram com as configurações padrão.
![image](https://github.com/fritzgaldino/Amazon-EC2/assets/87190206/292e68dd-c0c6-4de7-b8de-f0c1c06c1fb4)

10 - Defina o armazenamento padrão - Permanecer no nível gratuito e clicar em iniciar instância
![image](https://github.com/fritzgaldino/Amazon-EC2/assets/87190206/8ba9839c-6667-4b22-bb18-dcb496e00d17)

11 - Instância criada
![image](https://github.com/fritzgaldino/Amazon-EC2/assets/87190206/dfd41595-74cf-435e-ba65-1de3ddb8199b)

12 - Configuração da Instância EC2 finalizada, hora de conectar...
![image](https://github.com/fritzgaldino/Amazon-EC2/assets/87190206/88b9d8b5-54a1-47c1-aaed-37a48e0170cd)

13 - Clique em RDP e clicar para fazer download. O Protocolo de Desktop Remoto (RDP) é um protocolo, ou padrão técnico, que permite utilizar um computador desktop remotamente
![image](https://github.com/fritzgaldino/Amazon-EC2/assets/87190206/ae018cc7-9b37-4716-b7ca-e6bf70e73930)

14 - Clique no download
![image](https://github.com/fritzgaldino/Amazon-EC2/assets/87190206/23e0ca61-f3c5-4498-a223-d1100ec48a50)
![image](https://github.com/fritzgaldino/Amazon-EC2/assets/87190206/4ec7ffa6-ccc0-4a87-9298-068985867c89)

15 - Em seguida clique em obter senha para conectar ao servidor
![image](https://github.com/fritzgaldino/Amazon-EC2/assets/87190206/f6d567ee-e638-4f8c-a0a6-2691453c7024)

16 - Faça o upload do par de chaves que criamos anteriormente
![image](https://github.com/fritzgaldino/Amazon-EC2/assets/87190206/e64be610-0ca3-4977-aea0-f7756d17d465)

17 - Descriptografe o par de chaves que criamos
![image](https://github.com/fritzgaldino/Amazon-EC2/assets/87190206/eeb9ff10-8de1-4670-9adb-a1804ca72213)

18 - Copiar a senha e conectar ao servidor
![image](https://github.com/fritzgaldino/Amazon-EC2/assets/87190206/a624b723-7ce9-4cf1-aede-3aabd2a528e6)

19 - Pronto, acesso feito
![image](https://github.com/fritzgaldino/Amazon-EC2/assets/87190206/3b408fab-7f75-4e8f-921b-c02832203516)

## Referência

 - [skillbuilder](https://explore.skillbuilder.aws/learn/course/aws-technical-essentials)
 - [Docs AWS](https://docs.aws.amazon.com/pt_br/ec2/)








