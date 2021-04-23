# api
1. Criar uma pasta: segundo-fetch
2. Abrir esta pasta no visual studio code
3. Acessar o site:  https://jsonplaceholder.typicode.com/
4. Clicar no link:  My JSON Server
5. Criar um repositório no github: <your-username>/<your-repo>
            
7. Neste novo repositório criar um arquivo: db.json
```
{
  "disciplinas": [
    { "id": 1, "titulo": "Programação Web Front-end", "codigo": "PWFE" },
    { "id": 2, "titulo": "Programação Web Back-end", "codigo": "PWBE" },
    { "id": 3, "titulo": "Banco de Dados", "codigo": "BCD" },
    { "id": 4, "titulo": "Interfaces para Dispositivos Móveis", "codigo": "INDMO" }
  ]
}
```
6. Criar dois arquivos: <br />
  6.1. index.html
  6.2.  index.js

7. index.html
```
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta namedisciplinas="viewport" content="width=device-width, initial-scale=1.0">
    <title>Minha API</title>
</head>
<body>
    <div id="conteudo"></div>
    <script src="index.js"></script>   
</body>
</html>
```

7.1. index.js
```
fetch('https://my-json-server.typicode.com/Jefferson1202/api/disciplinas')
  .then(response => response.json())
  .then(json => {
    const div = document.getElementById("conteudo");
    div.innerText = JSON.stringify(json)
    //div.innerText = JSON.stringify(json.title)
  })
 ```

6. Salvar e rodar a partir do index.html
