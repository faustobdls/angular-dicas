# angular-dicas

  Como estruturar um projeto em Angular 2/4 de mateira que os components/modules possam ser reusáveis, e q ele se mantenha facil de dar manuntenção 

# Estrutura

```
    app
        user
            createuser
            readuser
            updateuser
            listuser
        login
            login
            register
        core
            header
            footer
        shared
            *components q queira q seja reusado em todo o projeto
```

# Comandos na ordem vão ajudar

```
    ng new projeto --routing --style=scss

    ng g module login --routing
        ng g component login/login
        ng g component login/register (opcional)
    ng g module user --routing
        ng g component user/createuser
        ng g component user/readuser
        ng g component user/updateuser
        ng g component user/listuser
    ng g module core
        ng g component header
        ng g component footer
    ng g module shared
        ng g component shared/componentName * para todos os components reusáveis
```
