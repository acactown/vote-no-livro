#Vote no Livro Project, AKA 'VNL'

#TODO

    - [X] Create base project structure
    - [X] README: Main repo
    - [ ] README: Model Layer
    - [ ] README: Service Layer
    - [ ] README: View Layer
    - [ ] Implement unit tests
        - [ ] Model layer
        - [ ] Service layer
        - [ ] Web Layer
            - [ ] API
            - [ ] Client
    - [ ] Implement main logic
        - [ ] Model layer
        - [ ] Service Layer
        - [ ] Web Layer
            - [ ] API
            - [ ] Client
    - [ ] Client Front-end visual improvements                 

# Notes

## What does the APP do?

Email specifications:   

> Ao entrar na página inicial em http://localhost:8080/vote-no-livro, você deverá exibir dois livros para o usuário e perguntar qual deles ele gosta mais. Digamos que o usuário clique no livro “Harry Potter”. Você então deverá computar o voto dele e perguntar sobre outros livros.  Você deverá ter apenas 5 livros diferentes em seu banco de dados. Depois de computar todos os votos necessários, você deverá exibir dois campos para que o usuário preencha: um para o e-mail e outro para o nome dele. Ao confirmar, você deverá exibir o ranking geral dos livros considerando todos os votos inclusive dos outros usuário, e o ranking dele.

## Run

#### Simplest

The simplest method to run this web app is just execute inside Jetty Web Container using gradle wrapper task, in root path execute:

```
./gradlew :vnl-web:jettyRun
```

**Expected result:**

```
 > Building 93% > :vnl-web:jettyRun > Running at http://localhost:8080/vnl-view
```

# Artifacts

##vnl-model

This is a main share model mapping objects. (Entities, pogos, constants, etc...)

##vnl-service

This is a main service layer that contains all the relevant business logic. (DAOs, services, utils, etc...).

##vnl-web

The web layer, in this case (test :) ) both API and Web Client are running inside the same context.

###vnl-api

This is a RESTful, HATEOAS compliant, webservices application. (Controllers, cache layer, resources, etc...).

###vnl-client

This is the web application that manages the VNL app. It's essentially a web UI that consumes REST services from vnl-api. (Client Web App, front-end, etc...)