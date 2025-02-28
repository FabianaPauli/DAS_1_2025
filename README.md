# Design e Arquitetura de Software

## Aula 26/02/25
[Livro Eng Soft Moderna - Cap 7](https://engsoftmoderna.info/cap7.html)

Software normalemte tem a arquitetura de:
Frontend
Backend
Banco de Dados

No java, pacotes (package) são pastas e são extremamente nessessarios para a organização de um projeto

COMPONETE -> UMA FUNÇÃO PRONTA QUE USASSE PARA FACILITAR O TRABALHO, COMO O @GETMAPPING, @CONTROLLER, @ENTITY NO JAVA

MODULOS -> COMO SE SEPARA O SOFTWARE, E COMO ESSAS AREAS, FUNÇÕES, SE CONVERSAM POR MEIO DE UMA INTERFACE, (UMA CHAMADA DE API REST)

SERIÇOS -> SÃO OS CASOS DE USO

## Aula 27/06/25

MODEL-VIEW-CONTROLLER 
uma arquitetura de software 
model
  "dados que vao aparecer na tela"

view 
  tela/interface 

controller
  controla(intermedia) onde vai os dados na interface

entidade classe que representa os dados processados e armazenados no banco
model classe que representa os dados que chegam do banco e apresenta na tela

Selenium -> software para teste de tela

MICROSSERVIÇO -> DIVISÃO EM MODULOS
MONOLITO -> REPOSITORIO UNICO DE CÓDIGO (TUDO NO MESMO LUGAR), USO DE UMA ÚNICA TÉCNOLOGIA, COMPILADO E TESTADO GERANDO UM ÚNICO PACOTE, EXECUTADO COMO UM ÚNICO PROCESSO NO SISTEMA OPERACIONAL,*UM ÚNICO BANCO DE DADOS*