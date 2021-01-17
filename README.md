## Criar API REST utilizando NodeJS + pacote json-server.

O proposito do projeto é criar uma API REST utilizando o NodeJS + pacote json-server para subir a API e disponibilizar todas as rotas de uma API REST (GET, POST, PUT, DELETE). Link de Referencia: 

```
https://www.npmjs.com/package/json-server#getting-started
```


## Requisitos:

Dentro do diretorio do projeto, inicie o projeto com o comando abaixo. Será criado o arquivo 'package.json', onde constará as dependencias do projeto.

```
$  npm init
```


Dentro do diretorio do projeto, instale o pacote json-server na opção global. Execute o comando abaixo no terminal. Será criado a pasta 'node-modules' e tambem será registrado a dependencia do json-server no arquivo 'package.json'.

```
$  npm install -g json-server
```


Crie um arquivo db.json com a estrutura que a sua API terá. Abaixo um modelo como sugestão, para fins de testes.

```javascript
{
    "livros": [
		{ "id": 1, "titulo": "javascript", "autor": "autor1", "ano": 2020 },
     		{ "id": 2, "titulo": "sql","autor": "autor2", "ano": 2019 },
		{ "id": 3, "titulo": "react", "autor": "autor3", "ano": 2020 }, 
		{ "id": 4, "titulo": "react native", "autor": "autor4", "ano": 2019 }
    ],
    "animais": [
		{ "id": 1, "tipo": "cachorro", "nome": "lulu" },
		{ "id": 2, "tipo": "gato", "nome": "nina" }
    ]
}

```


Depois inicie o json-server, para subir a API. Utilize o comando abaixo. Detalhe: caso a porta esteja em uso com alguma aplicação, utilize outra porta que esteja disponivel.

```
$  json-server --watch db.json --port 3000
```


Com o json-server ativado, é possivel fazer manipulações no arquivo db.json, utilizando o PostMan ou utilize outro programa de preferencia (como por exemplo o SoapUI, Katalon Studio, Rest-Assured....). A API estará disponivel no endereço abaixo:

```
http://localhost:3000 
```


Para acessar uma rota, como por exemplo, a rota 'animais', informe o endereço no formato abaixo:

```
http://localhost:3000/animais
```


Ou se caso queira acessar um objeto especifico de uma rota, como por exemplo, o 'id: 1' de 'livros', informe a rota abaixo.

```
http://localhost:3000/livros?id=1
```


Caso fizer alguma alteração direto nos arquivos do projeto usando a IDE, assim que salvar as alterações o json-server será reiniciado automaticamente (ação parecida com o nodemon, o nodemom é outro utilitário que monitora todas as alterações nos arquivos de sua aplicação e reinicia automaticamente o servidor quando for necessário). 
