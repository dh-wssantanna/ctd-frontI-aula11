# Formulário 1/2
## Qual a diferença das tag(s) de formulário, comparado com as demais?
Os campos, ou `inputs` permitem recolher dados do usuário, em outras palavras, é uma ponte de comunicação do usuário com o sistema.
É importante observar que os dados por vezes precisam se modificados para se encaixar perfeitamente com o que o sistema necessita. Apelidamos esse processo de modificação de **tratamento**.
## Como normalmente os dados são tratados?
A princícpio não iremos aprofundar nossa abordagem sobre arquitetura de sistemas, porém é fundamental comepreender que os formulários que trabalharemos enviarão as informações para um sistemna a partir de um serviço disponilizado via API - Interface de programação de aplicações. O processo é simples, a partir de um formulário coletamos os dados e enviamos para o sistema a partir de um link seguindo um **método de envio**.
## Métodos de envio
É possível emular dois métodos de envio a partir de um documento HTML, são eles `GET` e `POST`.
```html
<html>
  <head>
    ...
    <title>...<title>
  </head>
  <body>
    <form action="https://api.sistema.com/cadastrar" method="GET">
      ...
    </form>
  </body>
</html>
```
### GET
Enviar os dados do formulário via URI, ou seja, os dados são enviados como parametro na URL.
### POST
Enviar os dados do formulário no corpo de uma requisição HTTP.
## Tipos de campos de formulário
### `<input>`
```html
<input name="nome" type="text">
```
## Validações
### `required`
```html
<input name="cpf" type="text" required>
```
### `type=""`
```html
<input name="nome" type="nome">
<input name="email" type="email">
<input name="telefone" type="tel">
<input name="senha" type="password">
```
## Semântica
### `<label for="">`
```html
<label for="nome">Nome completo</label>
<input id="nome" name="nome" type="text">
```
**Nota:** Para associar a `label` ao `input` deve-se utilizar o atributo **id**. 
### `placeholder=""`
```html
<label for="nome">Nome</label>
<input id="nome" name="nome" type="text" placeholder="Digite seu nome completo">
```
