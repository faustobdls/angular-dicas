# angular-dicas
Como estruturar um projeto em Angular 2/4 de maneira que os components/modules possam ser reusáveis e possibilite a fácil manuntenção.
# Estrutura
```
new-angular-app/
│-- app/
│    |-- user/
│    |    ├──  create-user/
│    |    └──  read-user/
│    │    └──  update-user/
│    │    └──  list-user/
│    │
│    │-- login/
|    │    ├── login/
|    │    ├──  register/ 
│    │-- core/
|    │    ├──  header
|    │    ├──  footer
|    │-- shared/                         * Components que queira reutilizar em todo o projeto.
|    │
│
├── .editorconfig                       * Define estilo de código entre editores
├── .gitignore                          * Exemplo de arquivo para 
├── package.json                        * Define dependências do projeto
```

## Para os comandos abaixo é importante ter na maquina:
- node
- npm
- @angular/cli `npm install -g @angular/cli`


# Comandos na ordem vão ajudar

 - `ng new projeto --routing --style=scss`:  cria o novo projeto usando o `@angular/cli`. O comando `--routing` adiciona os arquivo de roteamento da aplicação, e o --style=scss seta o scss como pré-processador padrão para a aplicação. 
### Dentro da pasta do projeto:
- `ng g module login --routing`: usa o `@angular/cli` para criar o modulo e o `--routing` para adcionar o roteamento nele;
- `ng g component login/login`: usa o @angular/cli para criar um component e como o modulo ja foi criado, o component é adicionado ao modulo como parte dele;
- `ng g component login/register`: opcional, usa o @angular/cli para criar um component e como existe um modulo ja criado, o component é adicionado ao modulo como parte dele.

```
├── ng g module user --routing
    ├──     ng g component user/createuser
    ├──     ng g component user/readuser
    ├──     ng g component user/updateuser
    ├──     ng g component user/listuser
│
├── ng g module core
    ├── ng g component core/header
    ├── ng g component core/footer
│
├── ng g module shared
    ├── ng g component shared/componentName *  para todos os components reusáveis
```
