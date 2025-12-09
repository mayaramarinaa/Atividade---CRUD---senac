# Atividade-CRUD-SENAC
🎮 Jogoteca – Documentação Oficial
Este repositório contém apenas o README com a documentação completa da Jogoteca, pensado para ser enviado junto ao arquivo ZIP enviado pelo Teams. Aqui estão todas as informações necessárias para entender, instalar, rodar e revisar o projeto.

📘 Sobre o Sistema
A Jogoteca é um sistema web desenvolvido em Flask (Python) para gerenciar um catálogo de jogos. Ele permite que usuários autenticados cadastrem, editem, excluam e visualizem jogos. O projeto foi construído com foco em aprendizado de desenvolvimento web usando Flask, MySQL e templates Jinja2.

🚀 Funcionalidades
Cadastro e login de usuários
Autenticação com sessão
Listagem de jogos cadastrados
Cadastro de novos jogos
Edição de jogos existentes
Exclusão de jogos
Organização em templates HTML com Jinja2
Integração com MySQL
Script automático para criação do banco

🛠️ Tecnologias Utilizadas
Python 3.10+
Flask
MySQL
Werkzeug (senhas)
Jinja2 (templates)
Bootstrap (layout)
Flask-WTF (caso usado para formulários)

⚙️ Requisitos para Rodar o Projeto
Para que o sistema funcione corretamente, é necessário ter:

✔ Python 3.10 ou superior
✔ MySQL instalado e em execução
✔ Pip instalado
✔ Virtualenv (opcional)
✔ Script de criação do banco presente em preparabanco/

📁 Estrutura Geral do Projeto (ZIP)
A versão compactada do sistema contém pastas semelhantes a esta estrutura:

/jogoteca
│
├── app.py
├── models.py
├── helpers.py
├── preparabanco/
│   └── prepara_banco.py  # cria o banco automaticamente
├── static/
│   └── imagens/
├── templates/
│   ├── lista.html
│   ├── novo.html
│   ├── login.html
│   └── editar.html
└── README.md

🗄️ Estrutura do Banco de Dados
O banco é criado automaticamente pelo script da pasta preparabanco. Ele gera as seguintes tabelas:

🔹 Tabela usuarios
Campo	Tipo	Descrição
id	INT (PK)	ID do usuário
nome	VARCHAR	Nome completo
nickname	VARCHAR	Apelido utilizado para login
senha	VARCHAR	Senha hasheada

🔹 Tabela jogos
Campo	Tipo	Descrição
id	INT (PK)	ID do jogo
nome	VARCHAR	Nome do jogo
categoria	VARCHAR	Gênero/categoria
console	VARCHAR	Console/plataforma

📦 Como Rodar o Sistema
Abaixo está um passo a passo completo para quem baixar o ZIP pelo Teams.

1️⃣ Instalar dependências
No terminal, na pasta do projeto:

pip install -r requirements.txt

2️⃣ Criar o banco de dados automaticamente
Dentro da pasta do projeto, execute:

python preparabanco/prepara_banco.py
O script criará o banco, tabelas e dados iniciais.

3️⃣ Rodar o servidor Flask
flask run

4️⃣ Abrir no navegador
http://127.0.0.1:5000

📌 Observações Importantes
O script já cria o banco no MySQL — não é necessário criar manualmente.
Se o MySQL pedir usuário e senha diferentes, ajuste dentro do script prepara_banco.py.
Recomenda-se rodar em ambiente virtual (venv).

🧑‍💻 Melhorias Futuras
Adicionar upload real de imagens
Criar API REST
Implementar paginação
Tornar o layout mais moderno

Dupla: Flávio Gonçalves e Mayara Marina
