# WorganicTabV1 / v23 ! Table/Multiple

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 16.1.1.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.


## Development server json

Run `json-server --watch db.json` for a dev server. Navigate to `http://localhost:3000/`.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Get clone 
> https://github.com/worganic/TutoTab-St23-tableMultiple.git
> npm install
> cd .\worganic-tab-v23\
> ng serve

## Project :
v23 - Tableau -> multiple

    - On ajoute une section au menu : multiple
        - On ajoute un component multiple
            ~ ng generate c /component/multiple --skip-import  
        - On le rajoute dans le router :
            \src\main.ts
                >> path: 'multiple',...
        - On le rajoute dans le menu :
            \src\app\app.component.html
                >> <a  class="menu-item" routerLink="/multiple"> Multiple </a>
        - On n'oubli pas de mettre le composant en standalone :
            \src\app\component\multiple\multiple.component.ts
                >> standalone: true
    
    - On crait les tableaux de base :
        \src\app\component\multiple\multiple.component.html
            >> <div class="container">

    - On rajoute le component mère users :
        \src\app\component\multiple\multiple.component.html
            >> <app-users ></app-users>
        et l'import : 
       \src\app\component\multiple\multiple.component.ts
            >> import { UsersComponent } from 'src/app/component/users/users.component';

    - On crait une option pour modifié les options de base de user :
        \src\app\component\multiple\multiple.component.ts
            >> option2: any = {...
    - On rajoute l'option dans la vue :
        \src\app\component\multiple\multiple.component.html
            >>  <app-users [optionRecup]="option2"></app-users>
    - On récupère les options envoyé au component mère :
        \src\app\component\users\users.component.ts
            >> @Input() optionRecup!: any[];
            >> async ngOnInit(): Promise<void> {...
                 if(this.optionRecup != null){...

    - On peux modifié le scss car la taille des tableaux sont différentes :
        \src\app\component\multiple\multiple.component.scss
        [On pourrais changer les priorité des colonnes pour amélioré l'affichage]

## Problème à résoudre :
    

## Infos plus :
   
## Update

## Historique :
Avant -> v22 - Tableau -> Add
Après -> v24 - Tableau -> 
## Ressource :
    - 

## Abouts
created by Johann Loreau
create at 2023/08/18
Le project évolura suivant les remarques et conseils des visiteurs.