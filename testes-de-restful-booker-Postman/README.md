# Testes da API Restful-booker Ultilizando o Postman

Este projeto realiza o teste de uma API de Reservas de Hotel, se trata de uma API de Estudos com opção de Listar (GET), Criar (POST), Editar (PUT), Atualizar usuário (PATCH) e Deletar (DEL) reservas de usuários, alem de gerar Token. O ambiente utiliza o Postman e o navegador (Chrome).

## Cenários de Teste

## 1.**Listagem de Reservas do Hotel - GET**

- Listar todas as Reservas já criadas no Hotel e realizar testes de Status Code e Resposta.

## **Resposta:**
 - Mensagem: Reserva encontrada, atraves do "bookingid".
 - Mensagem: Status code é (200).

#
<div align="Center">
    <img width="1920" src="Sprints.status/Screenshot 2024-11-26 084541.png">
</div>

<div align="Center">
    <img width="1920" src="Sprints.status/Screenshot 2024-11-26 084549.png">
</div>


## 2.**Criar Reservas no Hotel - POST**
 - Criar uma reserva no hotel contendo "firstname", "lastname", "totalprice", "depositpaid", "bookingdates", "checkin", "checkout", "additionalneeds", "additionalneeds" e realizar testes de Status Code e Resposta.

## **Resposta:**
 - Mensagem: Nova Reserva  Criada por Ismael Gabriel, atravez do "bookingid".
 - Mensagem: Primeiro nome do hóspede que fez a reserva, atavez do "firstname".
 - Mensagem: Status code é (200).

#
   <div align="Center">
     <img width="1920" src="Sprints.status/Screenshot 2024-11-26 084600.png">
   </div>

   <div align="Center">
     <img width="1920" src="Sprints.status/Screenshot 2024-11-26 084608.png">
   </div>


## 3.**Atualizar Reserva já criada - PUT**
- Editar uma reserva no hotel usando o id da reserva e mudando alguma informação da reserva, trocando o "firstname", ou "lastname", "totalprice", "depositpaid", "bookingdates", "checkin", "checkout", "additionalneeds", "additionalneeds" e realizar testes de Status Code e Resposta.

## **Resposta:**
 - Mensagem: Atualizou a Reserva Criada por Ismael, atravez do "firstname".
 - Mensagem: Primeiro nome do hóspede que fez a reserva, atavez do "firstname".
 - Mensagem: Status code é (200).
#
<div align="Center">
    <img width="1920" src="Sprints.status/Screenshot 2024-11-26 084734.png">
</div>
<div align="Center">
    <img width="1920" src="Sprints.status/Screenshot 2024-11-26 084747.png">
</div>


## 4.**Atualizar um Usuário da Reserva - PATCH**
 - Editar o nome e sobrenome de um Usuário em uma reserva já criada usando o id usando o "firstname" e "lastname", depois realizar testes de Status Code e Resposta.

## **Resposta:**
 - Mensagem: Atualizou Usuário para Joeli Donelia, atravez do "fistname".
 - Mensagem: Primeiro nome do hóspede que fez a reserva, atavez do "firstname".
 - Mensagem: Status code é (200).

#
<div align="Center">
    <img width="1920" src="Sprints.status/Screenshot 2024-11-26 084830.png">
</div>
<div align="Center">
    <img width="1920" src="Sprints.status/Screenshot 2024-11-26 084838.png">
</div>

## 5.**Deletar uma Reserva do Hotel - DEL**
- Deletar uma reserva de um usuário já criada usando o id e realizar testes de Status Code e Resposta.

## **Resposta:**
 - Mensagem: Reserva deletada com sucesso, atravez do "Created".
 - Mensagem: Status code é (201).

#
<div align="Center">
    <img width="1920" src="Sprints.status/Screenshot 2024-11-26 084853.png">
</div>
<div align="Center">
    <img width="1920" src="Sprints.status/Screenshot 2024-11-26 084904.png">
</div>

## Cenário nagativos

## 1.**Listar Reservas de Hotel Inexistentes - GET**
 - Testar a listagem de reservas de um Hotel Inexistente, usando /bookingi e realizar testes de Status Code e Resposta.

## **Resposta:**
 - Mensagem: Lista de Reserva do Hotel não encontrada, atravez do "Not Found".
 - Mensagem: Status code é (401).

#
<div align="Center">
    <img width="1920" src="Sprints.status/Screenshot 2024-11-26 084514.png">
</div>

## 2.**Gerar Token Inválido - POST**
- Testar gerar o token de criação de reservas com usuarios e senha inválidos e realizando testes de Status Code e Resposta.

## **Resposta:**
- Mensagem: Credenciais Inválidas, atravez do "reason".
- Mensagem: Status code é (200).

#
<div align="Center">
    <img width="1920" src="Sprints.status/Screenshot 2024-11-26 084502.png">
</div>


## 3.**Criar Reserva já Existente - POST**
 - Testar realizar a criação de uma reserva já existente usando dados com id da reserva e realizar testes de Status Code e Resposta.

## **Resposta:**
 - Mensagem: Erro no Servidor Interno, atravez do "Internal Server Error".
 - Mensagem: Reserva já Criada, atravez do "Internal Server Error".
 - Mensagem: Status code é (500).
#
<div align="Center">
    <img width="1920" src="Sprints.status/Screenshot 2024-11-26 084452.png">
</div>


## 4.**Atualizar Reserva não Criada - PUT**
- Testar realizar a atualização  de uma reserva não criada usando id inválido e relizar testes de Status Code e Resposta.
   
## **Resposta:**
 - Mensagem: Não é possivel a auteração , atravez do "Method Not Allowed".
 - Mensagem: Status code é (405).
#

<div align="Center">
    <img width="1920" src="Sprints.status/Screenshot 2024-11-26 084433.png">
</div>


## 5.**Atualizar Usuário da Reserva Inexistente - PATCH**
- Testar a atualização de um usuario em uma reserva inexistente usando um id inválido e realizar testes de Status Code e Resposta.

## **Resposta:**
 - Mensagem: Não é possivel alteração, reserva Inexistente , atravez do "Method Not Allowed".
 - Mensagem: Status code é (405).

#
<div align="Center">
    <img width="1920" src="Sprints.status/Screenshot 2024-11-26 084411.png">
</div>


## 6.**Deleta Reserva Inexistente - DEL**
 - Testar a exclusão de uma reserva inexistente usando um id inválido e realizar testes de Status Code e Resposta.

## **Resposta:**
 - Mensagem: Reserva não pode ser Deletado (Inexistente), atravez do "Method Not Allowed".
 - Mensagem: Status code é (405).

#
<div align="Center">
    <img width="1920" src="Sprints.status/Screenshot 2024-11-26 084349.png">
</div>


## Filtros e Buscas

## 1.**Buscar Reservas pelo Nome - GET**
 - Buscar reservas do Hotel pelo nome, utilizando o parametro "Josh" entre outros e  realizar testes de Status Code e Resposta.

## **Resposta:**
 - Mensagem: Reserva de Josh, atravez do "bookingid".
 - Mensagem: ID de uma reserva especifica que corresponde aos critérios de pesquisa" atarvez do "bookingid".
 - Mensagem: Status code é (200).

#
<div align="Center">
    <img width="1920" src="Sprints.status/Screenshot 2024-11-26 084312.png">
</div>

<div align="Center">
    <img width="1920" src="Sprints.status/Screenshot 2024-11-26 084322.png">
</div>


## 2.**Buscar Reservas especificas pelo id - GET**
 - Buscar reservas do Hotel pelo id, de uma pessoa ou reserva com informações que precisa recolher, atraves do id da reserva e realizar testes de Status Code e Resposta.

 ## **Resposta:**
 - Mensagem: Usuário encontrado, atravez do "firstname".
 - Mensagem: Status code é (200).

#
<div align="Center">
    <img width="1920" src="Sprints.status/Screenshot 2024-11-26 084240.png">
</div>

<div align="Center">
    <img width="1920" src="Sprints.status/Screenshot 2024-11-26 084249.png">
</div>


## 2.**Buscar Reservas pelo Sobrenome - GET**
 - Buscar reservas do Hotel pelo sobrenome, utilizando o parametro "Josh Smith" entre outros e  realizar testes de Status Code e Resposta.

## **Resposta:**
 - Mensagem: Reserva de Josh, atravez do "bookingid".
 - Mensagem: Status code é (200).

#
<div align="Center">
    <img width="1920" src="Sprints.status/Screenshot 2024-11-26 084136.png">
</div>

<div align="Center">
     <img width="1920" src="Sprints.status/Screenshot 2024-11-26 084223.png">
</div>


## 3.**Buscar Reservas por check-in - GET**
 - Buscar reservas do Hotel pelo checkin da reserva, utilizando o parametro "check-in" contendo a data do registro e  realizar testes de Status Code e Resposta.

## **Resposta:**
 - Mensagem: Todas as Reservas de 02/03/2018, atravez do "bookingid".
 - Mensagem: Status code é (200).

#
<div align="Center">
    <img width="1920" src="Sprints.status//Screenshot 2024-11-26 084037.png>
</div>

<div align="Center">
    <img width="1920" src="Sprints.status/Screenshot 2024-11-26 084057.png">
</div>


## 4.**Buscar Reservas por check-out - GET**
 - Buscar reservas do Hotel pelo checkin da reserva, utilizando o parametro "check-out" contendo a data do registro e  realizar testes de Status Code e Resposta.

## **Resposta:**
 - Mensagem: Todas as Reservas de 14/06/2001, atravez do "bookingid".
 - Mensagem: Status code é (200).

#
<div align="Center">
    <img width="1920" src="Sprints.status/Screenshot 2024-11-26 084011.png">
</div>

<div align="Center">
    <img width="1920" src="Sprints.status/Screenshot 2024-11-26 084001.png">
</div>


## Token

## 1.**Gerar Token Valido - POST**
 - Gerar o Token de autorização para podermos Criar, Editar, Atualizar e Deletar reservas no Hotel de forma fácil e realizar testes de Status Code e Resposta.

## **Resposta:**
 - Mensagem: Token pa usar em solicitações futuras, atravez do "token".
 - Mensagem: Status code é (200).


#
<div align="Center">
    <img width="1920" src="Sprints.status/Screenshot 2024-11-26 083922.png">
</div>

<div align="Center">
    <img width="1920" src="Sprints.status/Screenshot 2024-11-26 083935.png">
</div>

## Realizacão de Testes com Postman

<br>

Este projeto realiza testes de uma API, cobrindo o fluxo completo de Token, Busca, Edicão ou atualização de reservas, criação da reserva, atualização de nome, sobrenome, cenarios negativos e invalidos.O ambiente utiliza Navegador (Chrome) e programa de API Postman.

## Pré-requisitos

Certifique-se de que você possui as seguintes ferramentas instaladas:

 - **Postman** (Ultima versão recomendada)
 - **Navegador (ex:Chrome)** (Ultima versão recomendada)
   
<br>

## Instalação

1. **Ambiente de Testes**

 - Abrir o Postman.
 - Criar uma Collection.
 - Ou usar a Collection já criada neste repositório usando a opção Menu, file, dentro do Postman.
 - Escolher a opção import para adicionar o arquivo baixado.
 - Ou arrastar o arquivo para dentro da área.
 - Selecionar a pasta e abrir.

<br>

2. **Execução de testes**

 - Abrir o Postman e selecionar a Collection.
 - Abrir o documento da API e realizar os testes no Postman.

<br>

## **Tecnologias Utilizadas**
  
 - **Postman:** Framework para testes de API.
 - **Navegador:** Ferramenta de navegação Web.
 - **GitHub:** Ferramenta de desenvolvimento colaborativo.
