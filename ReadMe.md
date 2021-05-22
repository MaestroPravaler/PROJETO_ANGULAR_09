# Angular 09 (Funcionalidades)

## Commit 01
- criação do arquivo package.json (Pasta backend) pelo terminal digite:
```
npm init -y
```
- criação do ambiente (server)
```
npm i json-server
```
- Criação do nosso objeto que terá todos os endpoints da nossa api (Arquivo db.json)
- Inicializar o db.json (Arquivo package.json)
```
"scripts": {
    "start": "json-server --watch db.json --port 3001"
  },
```
- Start no serviço (Diretório backend)
```
npm start
```
