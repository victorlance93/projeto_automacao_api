# Projeto de Automação de API com Postman

## Descrição do Projeto

Este projeto tem como objetivo realizar a automação de testes de API utilizando o Postman, concentrando-se na API do hunter.io. A estrutura organizacional do projeto é baseada em recursos, sendo eles "Lead" e "Lead List". Cada recurso possui subpastas dedicadas a diferentes tipos de requisição, tais como GET, PUT, POST e DELETE. A parametrização foi implementada para permitir a execução dos testes com massas de dados provenientes de arquivos externos, localizados na pasta `DADOS`.

## Documetação do Projeto

Para obter mais informações sobre como usar o meu projeto, consulte a [documentação completa](https://documenter.getpostman.com/view/19539264/2s9YymGjLj).

## Estrutura de Pastas

- **Lead**

  - `GET`: Testes relacionados à obtenção de leads e lead list.
  - `PUT`: Testes relacionados à atualização de leads e lead list.
  - `POST`: Testes relacionados à criação de novos leads e lead list.
  - `DELETE`: Testes relacionados à exclusão de leads e lead list.

- **Lead List**
  - Subpastas para diferentes tipos de operações similares às do recurso "Lead".

## Execução dos Testes

Os testes podem ser executados de forma automatizada utilizando o Newman, a ferramenta de linha de comando do Postman.

## Capturas de Tela

Aqui estão algumas capturas de tela do meu projeto:

![Projeto](/Users/victorlance93/Desktop/postman.png)

![report HTML com Newman Terminal](/Users/victorlance93/Desktop/terminal.png)

![report HTML com Newman HTML](/Users/victorlance93/Desktop/html_report.png)

### Comandos do Newman

`Gerar relatório no prompt de comando`
newman run HunterIO.postman_collection.json -e Teste.postman_environment.json --iteration-data dados/massa_hunter_leads.csv

`Gerar relatório HTML`
newman run HunterIO.postman_collection.json -e Teste.postman_environment.json --iteration-data dados/massa_hunter_leads.csv -r html

`Gerar com Template mas visual`
newman run HunterIO.postman_collection.json -e Teste.postman_environment.json --iteration-data dados/massa_hunter_leads.csv -r htmlextra

### Instalação do Newman

```bash
npm install -g newman
npm install -g newman-reporter-htm
npm install -g newman-reporter-htmlextra















```
