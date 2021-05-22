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

## ETAPA 03
- Modificar o arquivo angular.json | O arquivo de css, html, e TS serão arquivos separados e não inline como o padrão que seria todos eles em um arquivo único. 
```
"@schematics/angular:component": {
          "inlineTemplate": false,
          "inlineStyle": false,
```
- Separar o html que esta no arquivo .ts criando o arquivo "app.component.html"
```
@Component({
  selector: 'app-root',
  templateUrl: 'app.component.html'
})
```
- Instalar os componentes do Material Design. No terminal digite:
```
ng add @angular/material
```