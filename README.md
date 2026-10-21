## Instalação do uv no windows:
Acesse o site: https://docs.astral.sh/uv/getting-started/installation/
Copiar link do site e rodar no terminal PowerShell: powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
 
### Inicialização do uv na pasta:
Para versionar a sua pasta em uv (no terminal *PowerShell*):
- uv init;
 
Para criar um ambiente virtual isolado em Python:
- uv venv
 
Instalação da versão mais recente de Python:
- uv python install 3.15.0
 
No arquivo ".python-version" no IDE, altere a versão padrão, caso não esteja, para *3.15.0*
E em seguida sincronize o ambiente virtual com as suas dependências listadas, use no terminal:
- uv sync
 
Para verificar a versão do Python e garantir que tudo saiu como desejado, no terminal use:
- python -V
 
Para adicionar o recurso Flask no seu projeto python, no terminal use:
- uv add Flask
 
Para mudarmos o arquivo para a branch desejada, usamos o comando git:
- git branch -M main
 
Após isso configuramos as informações iniciais para a sequência do commit, usando:
- git config user.name -nome do usuário-
- git config user.email -email@gmail.com-;
 
---------------------------------------------------------------------------------------------------------------------------------------
## Criação do repositório no Github e git push
---------------------------------------------------------------------------------------------------------------------------------------
Crie o repositório no Github com o nome desejado
Para direcionar os arquivos para o repositório local, utilize o comando git:
- git remote add origin URL
 
Adicionamos todas as informações desejadas e preparamos os arquivos para o commit com:
- git add .
 
Commite sua tarefa, usando:
- git commit -m "nome do commit"
 
Levando as alterações e os novos arquivos para o repositório remoto com o comando git:
- git push -u origin main
 
Para verificar o funcionamento e o andamento da aplicação, use o comando uv (no terminal PowerShell):
- uv run Flask run
 
Os snippets, são blocos de código reutilizáveis, nao sendo necessário usar para repetir, agilizando o trabalho e escrita, existindo dois tipos:
- O snippet de linha, representado com {snippet} ou {{snippet}}.
- O snippet de bloco,referindo-se a um trecho de código estruturados, funcionando como um "módulo" que carrega um script ou layout específico.
- --
------------------------------------------------------------------------------------------------------------------------------------------------------
Em python é comum as importações, como no exemplo criado, aonde são feitas importações para construir uma aplicação web básica em Python utilizando o framework Flask:
-- From flask import Flask, render_template, request
-- from markupsafe import escape
 
- Flask: Classe usada para cirar instâncias da sua aplicação na web;
- render_template: Função utilizada para carregar e renderizar arquivos HTML (geralmente localizados numa pasta chamada "templates").
- request: Objeto global que gerencia os dados das aquisições do HTTP enviadas pelo usuário, como parâmetros do URL.
- escape: É uma ferramenta de segurança do pacote markupsafe que converte caracteres especiais como: "<" e  ">" em entidades seguras.
 
Para não ser dependente do comando "uv run flask run", e ser possível correr a aplicação através do próprio Python, usar uma linha de código para configurar e iniciar o servidor de desenvolvimento local:
- if __ nome __ == "__ main __"
 
Assim garantindo que o servidor seja iniciado apenas se o script Python for executado diretamente pelo usuário.
 
- app.run(...)
O método do Flask que coloca a aplicação no ar para escutar requisições HTTP recebidas
 
- debug = True
Ativa o *Modo de Depuração (Debug Mode)*, que traz dois grandes benefícios no desenvolvimento.
- Auto reload
- Depurador Interativo