# MÓDULO - 5

# Documentação da Base de Dados

## 1. Introdução

Este Miniprojeto é parte da componente avaliativa no módulo de competências para o mercado de trabalho, do curso de Administração de Sistemas da Faculdade de Ciências da Universidade de Lisboa, inserido no âmbito do programa UPskill.

## 2. Instalação da Base de Dados

- ### Pré-requisito
Possuir instalado o MySQL, disponível em [MySQL] ou equivalente, como por exemplo o [XAMPP], de acordo com o sistema operacional em uso no computador. 

- ### Acesso a Base de Dados
Abrir o ficheiro do projeto (.sql) por meio de duplo clique 
ou alternativamente após aceder a aplicação MySQL > File > Open SQL Script.

## 3. Objetivos e Elementos da Base de Dados

- A Base de Dados têm como objetivo auxiliar na gestão, controlo e tomada de decisão em um departamento de informática em uma empresa. 

- Esta Base de Dados é composta por 6 tabelas (utilizador, dispositivos, permissões, serviços, acessos, logins das actividades), possuem dados que são capazes de informar qual utilizador realizou o acesso, actividade feita, assim como o respetivo dispositivo. Para além de outras consultas quem sejam de interesse comum.

## 4. Salvaguarda da Base de Dados

Para salvaguarda da Base de Dados recomenda-se adoptar o seguintes práticas, (1) backup completo da Base de Dados,
(2) apenas da estrutura  e (3) apenas dos dados, as quais são condutas  : 

``````console
(1)

mysqldump-u <USER> -p <DBNAME> > <DESTFILE.SQL>
 

(2)

 mysqldump--no-data -u <USER> -p <DBNAME> > <DESTFILE.SQL>
 

(3)

mysqldump--no-create-info-u <USER> -p <DBNAME> > <DESTFILE.SQL>

``````

Onde:
 
- < USER>: Substituir pelo nome do usuário com permissões.
- < DBNAME> : Substituir pelo nome da base de dados.
- < DESTFILE.SQL> : Arquivo backup gerado.

Exemplo: 

mysqldump -u root -p controlopermissoes > C:\backup\controlopermissoesBD.sql

## 5. Restauro da Base de Dados

São boas práticas de restauro da Base de Dados: (1) criar a Base de Dados, caso não exista
(2) importar o ficheiro dump em formato .sql



``````console
 (1)

mysql-u <USER> -p –e "CREATE DATABASE destination_db"



(2)

mysql-u <USER> -p < <SOURCEFILE.SQL>

``````
Onde:
 
- < SOURCEFILE.SQL>: Arquivo a ser importado.

## 6. Créditos

Elaborador por Waltemberg Dantas



[MySQL]: https://dev.mysql.com/downloads/installer/
[XAMPP]: https://www.apachefriends.org/
