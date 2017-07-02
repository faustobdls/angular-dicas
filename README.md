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

## Para os comandos abaixo é importante ter na maquina:
node
npm
@angular/cli `npm install -g @angular/cli`


# Comandos na ordem vão ajudar

```
    ng new projeto --routing --style=scss (cria o novo projeto usando o @angular/cli pra acelerar, o --routing e pra ja adcionar o arquivo de roteamento da aplicação, e o --style=scss é pra setar o estilo como scss como padrão)
    
    cd projeto (navega até a pasta do projeto)
    
    ng g module login --routing (usa o @angular/cli para criar o modulo e o --routing para adcionar o roteamento nele) 
        ng g component login/login (usa o @angular/cli para criar um component e como existe um modulo ja criado, o component ja é adicionado ao modulo como parte dele)
        ng g component login/register (opcional, usa o @angular/cli para criar um component e como existe um modulo ja criado, o component ja é adicionado ao modulo como parte dele)
    
    ng g module user --routing
        ng g component user/createuser
        ng g component user/readuser
        ng g component user/updateuser
        ng g component user/listuser
    
    ng g module core
        ng g component core/header
        ng g component core/footer
    
    ng g module shared
        ng g component shared/componentName * para todos os components reusáveis
```
