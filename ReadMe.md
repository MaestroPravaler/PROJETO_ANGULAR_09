# Angular 09 (Funcionalidades)

## ETAPA 01
1 - Criação do arquivo package.json (Pasta backend) pelo terminal digite:
```
npm init -y
```
2 - Criação do ambiente (server)
```
npm i json-server
```
3 - Criação do nosso objeto que terá todos os endpoints da nossa api (Arquivo db.json)
4 - Inicializar o db.json (Arquivo package.json)
```
"scripts": {
    "start": "json-server --watch db.json --port 3001"
  },
```
5 - Start no serviço: No diretório backend rodar o comando.
```
npm start
```

## ETAPA 02
1 - Instalando o CLI do Angular
```
sudo npm i -g @angular/cli
```
2 - Criando um novo projeto (-- minimal instala os componentes básicos)
```
ng new nome_do_projeto --minimal
```
3 - Start da aplicação: No diretório nome_da_aplicação rodar o comando:
```
npm start
```

## ETAPA 03
1 - Modificar o arquivo angular.json | O arquivo de css, html, e TS serão arquivos separados e não inline como o padrão que seria todos eles em um arquivo único. 
```
"@schematics/angular:component": {
          "inlineTemplate": false,
          "inlineStyle": false,
```
2 - Separar o html que esta no arquivo .ts criando o arquivo "app.component.html"
```
@Component({
  selector: 'app-root',
  templateUrl: 'app.component.html'
})
```
3 - Instalar os componentes do Material Design. No terminal digite:
```
ng add @angular/material
```

## Etapa 04
1 - Gerar o componente header. No terminal digite:
```
ng g c components/template/header
```

2 - Gerar o componente Footer. No terminal digite:
```
ng g c components/template/footer
```

3 - Criando estilos para ser utilizados globalmente. Na pasta raiz do projeto arquivo style.css

4 - Criando o componente de Navegação. No terminal digite:
```
ng g c components/template/nav
```

5 - Menu lateral com icones 