# Angular 09 (Funcionalidades)

## ETAPA 01 (Construindo o Backend)

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

### 1.1 - Testando o Back com o Postman

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

2 - Importar os módulos do material design que utilizaremos na aplicação. Arquivo (app,module.ts)

```
import { MatToolbarModule } from '@angular/material/toolbar';

imports: [
  ...
  MatToolbarModule
]
```

3 - Gerar o componente Footer. No terminal digite:

```
ng g c components/template/footer
```

3 - Criando estilos para ser utilizados globalmente. Na pasta raiz do projeto arquivo style.css

4 - Criando o componente de Navegação. No terminal digite:

```
ng g c components/template/nav
```

5 - Importar os componentes sidebar e list do material design

```
import { MatSidenavModule } from '@angular/material/sidenav';
import { MatListModule } from '@angular/material/list';

imports: [
  ...
  MatSidenavModule,
  MatListModule
]
```

## Etapa 05

01 - Componentes são chamados pelo seletor:

```
// Arquivo TS
@Component({
  selector: 'app-nav',
  templateUrl: './nav.component.html',
  styleUrls: ['./nav.component.css']
})

// Arquivo html
<app-nav></app-nav>
```

02 - Diretivas de atributos (Altera a aparência ou comportamento de um elemento, componente ou outra diretiva)

```
// Aparência (EX: Modifica o css, uma cor de um elemento.)
// Cria com o CLI do angular
@Directive({
  selector: '[appRed]'
})
export class RedDirective{
  construtor(el: ElementRef){
    el.nativeElement.style.color = 'red',
  }
}
// No html
<i class = "material-icons" appRed>
  home
</i>
```

03 - Diretiva Estrutural (Altera o layout adicionando ou removendo elementos da DOM)
EX: *ngIf | *ngFor

04 - Decorator: É um padrão de projeto que tem como objetivo evitar herança trabalhando com composição para extender um determinado objeto.

```
@Component // Determina que é um componente
@Directive // Determina que é uma diretiva

// Comportamento (EX: modifica um botão que faz um achamada ao backend )
```

05 - Property binding (Vinculação de Propriedade)
Ligar o seu TS com o html - Colchetes []

```
// No arquivo TS
products: Praduct[];

// No html
<table [dataSource]="products">
</table>
```

06 - Event binding (Vinculação de Eventos)
Ligar um evento do TS com um método no html - Parenteses ()

```
// No arquivo TS
createProducts(): void{
  ......
}

// No html
<button mat-raised button
(click)= "createProducts">
</button>
```

07 - One Way data binding (Vinculação de um sentido)
Olhar item 05

```
// No arquivo TS
nome: "Rafael"

// No html
<imput [value]="nome"> // Receberá "Rafael">
```

08 - Two Way data binding (Vinculação nos dois sentidos)
Mudança feita no formulário vai alterar o back e vice-versa.

```
// No arquivo TS
nome: "Rafael"

// No html
<imput [(ngMOdel)]="nome"> // Receberá "Rafael">
// caso modifique o valor no formulario (front) altera o back.

HTML <=> TS
```

09 - Pipe (Formata o valor recebido)

## Etapa 06

01 - Programação Reativa (ReativeX)

02 - Callback

03 - Promises - Consegue encadear vãrias chamadas - Consegue utilizar somente uma vez

04 - Observables (reusável - stream de dados - operadores) O padrão observer é a base da programação reativa.

## Etapa 07

01 - Service - São Classes que tem como principal objetivo organizar e compartilhar métodos e dados entre os componentes. Posso utilizar services dentro de diretivas. Tudo que diz respeito ao "visual" da aplicação são componentes; regras que não diz respeito a parte visual (encapsular a api - backend da aplicação)

02 - Injeção de dependência - É um padrão no qual a clase recebe as dependências de uma fonte externa ao invés de criar por conta própria.

03 - Singletons - Apenas uma instância - Os services são singletons do escopo de um injector.

04 - Injector - possuimos 2 tipos o injector de módulo (ModuleInjector - @NgModule | @Injectable) ou in injector de elemento (ElementInjector - @Directive | @Component).
