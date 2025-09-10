# Desafio CodeGirls Santander - EC2 e EBS na AWS

Para este desafio, decidi integrar o conhecimento adquirido no módulo de instâncias da AWS ao meu projeto da faculdade, que consiste em um sistema de e-commerce para venda de camisetas de time colecionáveis.

# Entendendo o Desafio

O desafio propôs duas possibilidades de arquitetura:

- Utilizar EC2 + EBS
(EC2 se trata de uma máquina virtual, enquanto o EBS é um tipo de armazenamento em blocos, que se conecta à EC2)

- Utilizar S3 + Lambda
(S3 é um armazenamento por objetos, como fotos, documentos ou arquivos estáticos, e o Lambda é a execução de código sem servidor)

Escolhi a arquitetura **EC2 + EBS**, pois ela se conecta diretamente ao modelo de e-commerce desenvolvido, permitindo hospedar o site, armazenar dados de forma persistente e gerenciar informações de usuários e pedidos de camisetas em um banco de dados relacional.

# Arquitetura Proposta

A arquitetura foi desenhada no draw.io e representa os principais conceitos abordados no módulo:

- Usuário acessa o site hospedado em uma instância **EC2**.
- A instância **EC2** está conectada a volumes **EBS**, garantindo **armazenamento persistente**.
- O sistema utiliza **RDS** para gerenciar dados relacionais (usuários, pedidos, produtos).
- Uma **AMI** foi criada para permitir **replicação e recuperação rápida** da instância.
- Foram utilizadas duas regiões (São Paulo e Oregon), destacando a importância de **Availability Zones** para resiliência.

# Diagrama com a arquitetura

`/diagramas/arquitetura.drawio`

### Insights Técnicos

- **EBS**: armazenamento em bloco acoplado à EC2, garantindo persistência dos dados.
- **RDS**: facilita a administração do banco de dados e oferece maior disponibilidade.
- **AMI**: permite criar cópias da instância e manter um plano de recuperação.
- **Availability Zones**: reforça conceitos de latência, custo e disponibilidade das regiões.

# Conclusão
Desenvolvi esse projeto, pensando na melhor performance e custos para meu software de camisetas colecionáveis. 
Seguindo essa abordagem, percebi a importancia de utilizar a instancias EC2 e EBS, em um sistema que precisa de um monitoramento contínuo e que tem a possibilidade de crescer. Então quis destacar as regiões São Paulo oferecendo menor latência ao acesso dos usuários e a região Oregon nos Estados Unidos, como menor custo para o sistema.



  
