##  🎀✨ form_cadEndereco ✨🎀
 
[Introdução](#-introdu%C3%A7%C3%A3o)

[Descrição](#-descri%C3%A7%C3%A3o)

[Sobre a Atividade](#-sobre-a-atividade)

[Tecnologias Utilizadas](#-tecnologias-utilizadas)

[Funcionalidades](#%EF%B8%8F-funcionalidades)

[Exemplo de Uso](#-exemplo-de-uso)

[Fontes Consultadas](#-fontes-consultadas )

[Autores](#-autores)

![SanrioSanrioCharactersGIF](https://github.com/user-attachments/assets/784a0d6e-f24e-4394-a6e6-2624bbaa0541)


![Capa do projeto]()

## 📌 Introdução
**form_cadEndereco** é um sistema de pedido de compra desenvolvido como parte da disciplina de Programação Web II, ministrada pelo professor Leonardo Rocha. Nosso objetivo é oferecer uma plataforma intuitiva para gerenciar categorias, marcas e produtos, além de proporcionar uma experiência de compra fluida e eficiente.

## 📖 Descrição
O **form_cadEndereco** é uma aplicação web que visa simplificar o gerenciamento de produtos e pedidos. Com uma interface amigável e funcionalidades robustas, os usuários podem adicionar e gerenciar produtos, categorias e marcas, além de gerenciar seu carrinho de compras e visualizar resumos detalhados dos pedidos.

## 🌼 Sobre a Atividade
Este projeto foi desenvolvido em sala de aula, com o apoio e orientação do professor Leonardo Rocha. O desafio foi colocar em prática o que aprendemos na disciplina de Programação Web II.

### Foco Principal
- **Integração entre Frontend e Backend:** Conectando a interface com a lógica de backend para garantir coesão.
- **Gerenciamento de Banco de Dados:** Organização e armazenamento eficiente dos dados.
- **Desenvolvimento de Funcionalidades Dinâmicas:** Implementação de características interativas para uma experiência de usuário envolvente e intuitiva.

## 💻 Tecnologias Utilizadas
| Tecnologia         | Descrição                         |
|--------------------|-----------------------------------|
| **VS Code**        | Editor de código-fonte            |
| **GitHub**         | Plataforma de hospedagem de código|
| **HTML**           | Linguagem de marcação             |
| **CSS**            | Folhas de estilo em cascata       |
| **JSS**            | Lib de estilo em JavaScript       |
| **JavaScript**     | Linguagem de programação para web |
| **jQuery**         | Biblioteca JavaScript             |
| **PHP**            | Linguagem de script no servidor   |
| **MySQL**          | Sistema de gerenciamento de banco de dados|

## 🛠️ Funcionalidades

### 📂 Cadastro de Categorias
- 📝 **Criar novas categorias:** Adicione categorias para organizar seus produtos.
- ✏️ **Editar e excluir categorias:** Modifique ou remova categorias existentes conforme necessário.
- 📋 **Visualizar categorias:** Consulte a lista de todas as categorias cadastradas.

### 📂 Cadastro de Marcas
- 📝 **Adicionar novas marcas:** Registre marcas para associar aos produtos.
- ✏️ **Atualizar e remover marcas:** Edite ou exclua marcas quando necessário.
- 📋 **Visualizar marcas:** Acesse a lista completa de marcas.

### 📂 Cadastro de Produtos
- 📝 **Inserir novos produtos:** Adicione produtos com informações detalhadas.
- ✏️ **Editar e excluir produtos:** Atualize ou remova produtos existentes.
- 📋 **Visualizar produtos:** Consulte a lista de todos os produtos cadastrados.

### 🛒 Gerenciamento de Carrinho
- ➕ **Adicionar produtos ao carrinho:** Inclua itens ao seu carrinho de compras.
- 🔄 **Atualizar quantidades e remover itens:** Modifique quantidades ou remova produtos do carrinho.
- 🛒 **Visualizar o conteúdo do carrinho:** Confira todos os itens no carrinho.

### 📄 Resumo do Pedido
- 🧾 **Exibir um resumo detalhado:** Veja um resumo completo do pedido antes da finalização.
- 👀 **Revisar a seleção de produtos:** Confirme os produtos escolhidos antes de completar a compra.

## 📋 Exemplo de Uso

### Cadastro de Categoria
1. Acesse a página de categorias e clique em "Adicionar Nova Categoria".
2. Preencha o formulário com o nome da categoria e clique em "Salvar".

### Cadastro de Produto
1. Navegue até a página de produtos e clique em "Adicionar Novo Produto".
2. Insira os detalhes do produto, selecione a categoria e a marca, e clique em "Salvar".

### Adição ao Carrinho
1. Vá para a lista de produtos.
2. Clique em "Adicionar ao Carrinho" ao lado do produto desejado.

### Visualização do Pedido
1. Acesse o carrinho de compras.
2. Revise os itens e clique em "Finalizar Pedido" para visualizar o resumo.

## 📝 Exemplos Auxiliares de Uso dos Métodos PHP
Aqui estão alguns exemplos dos métodos PHP utilizados no cadastro:

### Cadastro de Categoria (PHP)
```php
<?php
// Função para adicionar nova categoria
function adicionarCategoria($nomeCategoria) {
    $conn = new mysqli('localhost', 'usuario', 'senha', 'banco');
    $sql = "INSERT INTO categorias (nome) VALUES ('$nomeCategoria')";
    if ($conn->query($sql) === TRUE) {
        echo "Categoria adicionada com sucesso";
    } else {
        echo "Erro: " . $sql . "<br>" . $conn->error;
    }
    $conn->close();
}
?>
