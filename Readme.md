# 📦 Gerenciador de Estoque em Console (C# / .NET 8)

## 🎯 Visão Geral
Este projeto consiste no desenvolvimento de um **Gerenciador de Estoque em Console**, utilizando **C# com .NET 8.0**, com o objetivo de simular uma **arquitetura de software real**, próxima da utilizada em ambientes profissionais.

Mais do que um exercício de lógica, o sistema foi pensado para aplicar **boas práticas de organização, separação de responsabilidades e escalabilidade**, servindo como um projeto sólido para **portfólio profissional**.

---

## 🛠️ Tecnologias Utilizadas
- **Linguagem:** C#
- **Framework:** .NET 8.0
- **Tipo de Aplicação:** Console Application
- **Versionamento:** Git & GitHub
- **Arquitetura:** Separação em camadas (Entities, Repositories, Services, Views e Controllers)

---

## 📌 Objetivo do Produto
Criar um sistema leve em **Console (C#)** que permita ao usuário gerenciar produtos de um estoque.

### Funcionalidades (CRUD)
- **Create:** Cadastrar novos produtos
- **Read:** Listar todos os produtos ou buscar por ID
- **Update:** Alterar preço e/ou quantidade
- **Delete:** Remover produtos do estoque

---

## 🧱 Estrutura Técnica do Projeto
O projeto é organizado em **5 responsabilidades bem definidas**, garantindo um código limpo e de fácil manutenção:

### 1️⃣ Entities (O quê)
Responsável por definir **o formato dos dados**.  
Exemplo:
- Classe `Produto` com `Id`, `Nome`, `Preco` e `Quantidade`.

### 2️⃣ Repositories (Onde)
Responsável pelo **armazenamento dos dados**.
- Simula um banco de dados utilizando uma `List<Produto>`.
- Executa apenas operações de salvar, buscar, atualizar e remover.

### 3️⃣ Services (As regras)
Responsável pelas **regras de negócio e validações**.
- Não permitir preço menor ou igual a zero
- Não permitir nome vazio
- Atua como intermediário seguro entre Controller e Repository

### 4️⃣ Views (A interface)
Responsável pela **interação com o usuário**.
- Exibe menus e mensagens
- Solicita entradas via `Console.ReadLine()`
- Não contém regras de negócio

### 5️⃣ Controllers (O maestro)
Responsável por **orquestrar o fluxo do sistema**.
- Recebe dados da View
- Chama o Service apropriado
- Retorna respostas para a View

---

## 🔄 Fluxo de Funcionamento (Exemplo Prático)
### Cadastro de Produto
1. **View:** Solicita nome, preço e quantidade ao usuário
2. **Controller:** Recebe os dados e envia ao Service
3. **Service:** Valida as informações
4. **Repository:** Armazena o produto na lista
5. **Controller:** Retorna sucesso
6. **View:** Exibe mensagem de confirmação

Esse fluxo garante que cada camada tenha uma única responsabilidade.

---

## 📂 Estrutura de Pastas
```text
📂 GerenciadorEstoque
│── 📂 Controllers
│── 📂 Entities
│── 📂 Repositories
│── 📂 Services
│── 📂 Views
│── Program.cs
│── README.md
│── .gitignore
```

---


**Contribuidores Principais**

- [Gabriel Oliveira dos Santos](https://github.com/gabrielods14)
- [Thiago Almeida Ribeiro](https://github.com/Thiagoalmeida74)

---

📜 Licença

Este projeto está licenciado sob a Licença MIT, permitindo uso, modificação e distribuição livre para fins educacionais e profissionais.