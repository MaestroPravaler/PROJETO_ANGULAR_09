# Angular 09 (Funcionalidades)

## ETAPA 01
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
- Start no serviço: No diretório backend rodar o comando.
```
npm start
```
## ETAPA 02
- Instalando o CLI do Angular
```
sudo npm i -g @angular/cli
```
- Criando um novo projeto (-- minimal instala os componentes básicos)
```
ng new nome_do_projeto --minimal
```
- Start da aplicação: No diretório nome_da_aplicação rodar o comando:
```
npm start
```