# Back End, Api e MySQL
Vamos se aprofundar nos assuntos citados, com objetivo de armazenar o conhecimento recebido relacionado a esses temas.
Vamos nessa!

![alt text](backend-dev.jpg)
# Introdução
Imagine um site ou aplicativo como um iceberg. A parte que você vê e interage (botões, imagens, textos) é o front-end. Mas o que acontece por trás, como os dados são armazenados e processados, é o back-end.
## Exemplo de back end no Node Js com Mysql
1 - Crie uma pasta.

2- Abra o cmd e abra essa pasta no VSCode

3- Crie um arquivo index.js

4- Instale os módulos:
myaql2 e express.
- npm i express
- npm i mysql2

## Coding
Comece seu index declarando as seguintes variáveis:
- const express = require('express')
- const app = express()
- const mysql = require('mysql2/promise')
- const conexao = mysql.createPool({

   database:"cloudflix",

   host:"localhost",

   password:"senai",

   user:"root"
   
})

--------------------
Insira os seguintes comandos:

(Mostra a tabela mysql.)
- app.get('/filmes',async function(req, res){

   var dados = await conexao.query('select * from filmes')

   console.log(dados[0])

   res.send(dados[0])

})

----
Finalizando:

(Abra a porta de acesso)
- app.listen(3000)

# API
- Uma interface de programação de aplicativos (em inglês, Application Programming Interface).
- É como uma porta: Permite que diferentes programas se comuniquem entre si.
- É um conjunto de regras: Define como os programas devem se conectar e trocar informações.

# MySQL
O MySQL é como um superorganizador para seus dados. Ele te ajuda a encontrar as informações que você precisa de forma rápida e fácil. É como ter uma biblioteca particular dentro do seu computador! É usado como linguagem também.

## Códigos:
- CREATE DATABASE name;
- CREATE TABLE name; (

    teste int primary key auto_increment not null

    teste2 varchar(40) not null
)

- CREATE USER name;
- SHOW DATABASES/TABLES;
- SELECT * FROM database WHERE table = 'class';
- DELETE FROM database WHERE table = 'name';
- UPDATE database SET table = 'Name' WHERE class = 'Name';
- INSERT INTO database (name, name, name..) VALUES ('value',....);
- DESCRIBE table;
