##  🎀✨ cadEcommerce ✨🎀
 
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

# 🎀✨ form_cadEndereco ✨🎀

## 📌 Introdução
**form_cadEndereco** é um sistema de pedido de compra desenvolvido como parte da disciplina de Programação Web II, ministrada pelo professor Leonardo Rocha. Nosso objetivo é oferecer uma plataforma intuitiva para gerenciar categorias, marcas e produtos, além de proporcionar uma experiência de compra fluida e eficiente.

## 📖 Descrição
O **form_cadEndereco** é uma aplicação web que visa simplificar o gerenciamento de produtos e pedidos. Com uma interface amigável e funcionalidades robustas, os usuários podem adicionar e gerenciar produtos, categorias e marcas, além de gerenciar seu carrinho de compras e visualizar resumos detalhados dos pedidos.

## 🌼 Sobre a Atividade
Este projeto foi desenvolvido dentro de sala de aula, com o apoio e orientação do professor Leonardo Rocha. O desafio foi colocar em prática o que aprendemos na disciplina de Programação Web II.

**O projeto teve como foco principal:**
- **Integração entre Frontend e Backend:** Aprendemos a conectar a interface que os usuários veem com a lógica que roda nos bastidores, garantindo que tudo funcione de maneira coesa. 
- **Gerenciamento de Banco de Dados:** Trabalhamos na organização e armazenamento eficiente dos dados, assegurando que o sistema possa lidar com informações de maneira eficaz.
- **Desenvolvimento de Funcionalidades Dinâmicas:** Implementamos características interativas para tornar a experiência do usuário mais envolvente e intuitiva.

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
- 📝 **Criar novas categorias**: Adicione categorias para organizar seus produtos.
- ✏️ **Editar e excluir categorias**: Modifique ou remova categorias existentes conforme necessário.
- 📋 **Visualizar categorias**: Consulte a lista de todas as categorias cadastradas.

### 📂 Cadastro de Marcas
- 📝 **Adicionar novas marcas**: Registre marcas para associar aos produtos.
- ✏️ **Atualizar e remover marcas**: Edite ou exclua marcas quando necessário.
- 📋 **Visualizar marcas**: Acesse a lista completa de marcas.

### 📂 Cadastro de Produtos
- 📝 **Inserir novos produtos**: Adicione produtos com informações detalhadas.
- ✏️ **Editar e excluir produtos**: Atualize ou remova produtos existentes.
- 📋 **Visualizar produtos**: Consulte a lista de todos os produtos cadastrados.

### 🛒 Gerenciamento de Carrinho
- ➕ **Adicionar produtos ao carrinho**: Inclua itens ao seu carrinho de compras.
- 🔄 **Atualizar quantidades e remover itens**: Modifique quantidades ou remova produtos do carrinho.
- 🛒 **Visualizar o conteúdo do carrinho**: Confira todos os itens no carrinho.

### 📄 Resumo do Pedido
- 🧾 **Exibir um resumo detalhado**: Veja um resumo completo do pedido antes da finalização.
- 👀 **Revisar a seleção de produtos**: Confirme os produtos escolhidos antes de completar a compra.

## 📋 Exemplo de Uso


### Adição ao Carrinho
1. Vá para a lista de produtos.
2. Clique em "Adicionar ao Carrinho" ao lado do produto desejado.

### Visualização do Pedido
1. Acesse o carrinho de compras.
2. Revise os itens e clique em "Finalizar Pedido" para visualizar o resumo.

## 📝 Exemplos Auxiliares de Uso dos Métodos PHP

### Cadastro de Categoria (PHP)
1. Acesse a página de categorias e clique em "Adicionar Nova Categoria".
2. Preencha o formulário com o nome da categoria e clique em "Salvar".

```
php
=======

### Cadastro de Categoria:
- Acesse a página de categorias e clique em "Adicionar Nova Categoria".
- Preencha o formulário com o nome da categoria e clique em "Salvar".

```
php
>>>>>>> 410f7d46fbeac7e1b9415465da3ffd5bde19bb86
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
```
### Inserção de Marca
```
<?php
include('controller/conexao.php');

$descricao = $_POST['descricao'];

echo "<h3> Descrição: $descricao </h3></br>";

$cad_marca = "INSERT INTO marca(DESCRICAO) VALUES ('$descricao')";

if(mysqli_query($mysqli,$cad_marca)){
    echo "<h1>Nova marca cadastrada com sucesso</h1></br>";
}else{
    echo "Erro: " . $cad_marca . "</br>" . mysqli_error($mysqli);
}

mysqli_close($mysqli);
?>
```
### Cadastro de Produto
1. Navegue até a página de produtos e clique em "Adicionar Novo Produto".
2. Insira os detalhes do produto, selecione a categoria e a marca, e clique em "Salvar".

```
<?php
include_once('controller/conexao.php');

$categoria = $_POST['seleciona_categoria'];
$marca = $_POST['seleciona_marca'];
$nome_produto = $_POST['nome'];
$descricao = $_POST['descricao'];
$estoque = $_POST['estoque'];
$preco = $_POST['preco'];

$grava_produto="INSERT INTO produtos (IDCATEGORIA, IDMARCA, NOME, DESCRICAO, ESTOQUE, PRECO) VALUES ('$categoria', '$marca', '$nome_produto', '$descricao', '$estoque', '$preco')";

$resute_gravacao = mysqli_query($mysqli, $grava_produto);
if(mysqli_affected_rows($mysqli) != 0){
    echo "
    <META HTTP-EQUIV=REFRESH CONTENT = 'O;URL=produtos.php'>
    <script type=\"text/javascript\">
      alert('produto cadastrado com sucesso');
    </script>
    ";
}else{
    echo"
    <META HTTP-EQUIV=REFRESH CONTENT = 'O;URL=produto.php'>
    <script type=\"text/javascript\">
    alert('Produto não cadastrado, tente novamente');
    </script>
    ";
}
?>
<<<<<<< HEAD
```

=======
>>>>>>> 410f7d46fbeac7e1b9415465da3ffd5bde19bb86
```
### **``Adição ao Carrinho:``**
   - Vá para a lista de produtos.
   - Clique em "Adicionar ao Carrinho" ao lado do produto desejado.
```
if (isset($_POST['produto_id']) && isset($_POST['quantidade'])) {
    $produto_id = $_POST['produto_id'];
    $quantidade = $_POST['quantidade'];
    $_SESSION['carrinho'][$produto_id] = $quantidade;
    echo "Produto adicionado ao carrinho!";
}
?>
```

### **``Visualização do Pedido:``**
 - Acesse o carrinho de compras.
 - Revise os itens e clique em "Finalizar Pedido" para visualizar o resumo.
```
$total = 0;
foreach ($_SESSION['carrinho'] as $produto_id => $quantidade) {
    $sql = "SELECT nome, preco FROM produtos WHERE id = '$produto_id'";
    $result = mysqli_query($mysqli, $sql);
    if (mysqli_num_rows($result) > 0) {
        while($row = mysqli_fetch_assoc($result)) {
            echo "Produto: " . $row['nome'] . " - Quantidade: " . $quantidade . " - Preço: " . $row['preco'] . "<br>";
            $total += $row['preco'] * $quantidade;
        }
    }
}
echo "Total do Pedido: " . $total;
?>
```
![Capa do projeto]()
 
## 🔗 Fontes Consultadas 
- [Leonardo Rocha](https://github.com/LeonardoRochaMarista)
- [chatGPT](https://openai.com/chatgpt/)
 
## 💖 Autores
- [Verônica Borges](https://github.com/okayVeronica)
- [Leonardo Rocha](https://github.com/LeonardoRochaMarista)
 
![TaylorTaylorSwiftGIF (3)](https://github.com/user-attachments/assets/55504d1b-18a2-4f11-8ed3-ec2b4853ec09)
