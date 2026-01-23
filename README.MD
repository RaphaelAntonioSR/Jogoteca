# 🎮 Jogoteca

Uma aplicação web para gerenciar sua coleção pessoal de jogos. Organize seus jogos por categoria, console e adicione capas personalizadas.

## ✨ Funcionalidades

### 🔄 Operações CRUD

Este projeto implementa todas as operações **CRUD** (Create, Read, Update, Delete):

- **C**reate - ✅ **Criar Novo Jogo** - Adicione um novo jogo com capa personalizada
- **R**ead - ✅ **Listar Jogos** - Visualize todos os jogos da sua biblioteca
- **U**pdate - ✅ **Editar Jogo** - Modifique as informações e capa do jogo
- **D**elete - ✅ **Deletar Jogo** - Remova jogos da sua biblioteca

### Recursos Adicionais

- ✅ **Sistema de Login** - Autenticação de usuários
- ✅ **Gerenciamento de Capas** - Upload e atualização de capas dos jogos
- ✅ **Proteção CSRF** - Segurança em formulários
- ✅ **Banco de Dados Relacional** - Persistência com SQLAlchemy

## 🛠️ Tecnologias Utilizadas

- **Backend:** Flask
- **Banco de Dados:** SQLAlchemy
- **Autenticação:** Flask-Bcrypt
- **Formulários:** Flask-WTF
- **Proteção CSRF:** Flask-WTF CSRF
- **Frontend:** Bootstrap, jQuery, HTML/CSS

## 📁 Estrutura do Projeto

```
Jogoteca-C1/
├── config.py              # Configurações da aplicação
├── app.py            # Inicialização do Flask
├── models.py              # Modelos do banco de dados
├── views.py               # Rotas e controllers
├── helpers.py             # Funções auxiliares e formulários
├── prepara_banco.py       # Script para preparar o banco de dados
├── static/                # Arquivos estáticos
│   ├── app.css
│   ├── app.js
│   ├── bootstrap.css
│   └── jquery.js
├── templates/             # Templates HTML
│   ├── template.html      # Template base
│   ├── lista.html         # Página de listagem
│   ├── novo.html          # Formulário novo jogo
│   ├── editar.html        # Formulário editar jogo
│   └── login.html         # Página de login
└── uploads/               # Capas dos jogos

```

## 🚀 Como Executar

### Pré-requisitos
- Python 3.7+
- pip (gerenciador de pacotes Python)

### Instalação

1. Clone o repositório
```bash
git clone <url-do-repositorio>
cd Jogoteca-C1
```

2. Instale as dependências
```bash
pip install flask flask-sqlalchemy flask-wtf flask-bcrypt
```

3. Prepare o banco de dados
```bash
python prepara_banco.py
```

4. Execute a aplicação
```bash
python app.py
```

5. Acesse no navegador
```
http://localhost:5000
```

## 📝 Uso

### Adicionar um Novo Jogo
1. Clique em "+ Novo Jogo"
2. Preencha o nome, categoria e console
3. Selecione a capa do jogo
4. Clique em "Salvar"

### Editar um Jogo
1. Clique em "Editar" na capa do jogo
2. Modifique as informações desejadas
3. Se quiser atualizar a capa, selecione uma nova imagem
4. Clique em "Salvar"

### Deletar um Jogo
1. Clique em "Deletar" na capa do jogo
2. Confirme a exclusão
3. O jogo e sua capa serão removidos

### Fazer Login
1. Clique em "Login"
2. Digite seu nickname e senha
3. Clique em "Login"

## 🔒 Autenticação

- Sistema de login com criptografia de senha
- Rotas protegidas que requerem autenticação
- Logout disponível após login

## 📸 Gerenciamento de Capas

- Upload de capas ao criar ou editar jogos
- As capas são automaticamente nomeadas como `capa{id}.jpg`
- Capas antigas são automaticamente deletadas ao atualizar
- Uma capa padrão é exibida se nenhuma capa for fornecida

## 🐛 Resolução de Problemas

### Capa não aparece ao editar
- Verifique se o arquivo foi salvo corretamente na pasta `uploads/`
- Certifique-se de que a extensão do arquivo é `.jpg`

### Erro ao deletar jogo
- Verifique se a pasta `uploads/` existe
- Verifique permissões de escrita na pasta

### Erro de banco de dados
- Execute `python prepara_banco.py` para reinicializar o banco

## 📄 Licença

Este projeto é um trabalho educacional da Alura com modificações e algumas implementações pessoais.

## 👨‍💻 Autor

Desenvolvido como projeto de aprendizado em Flask.

---


