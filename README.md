cat << 'EOF' > README.md
# DSCommerce

[![NPM](https://img.shields.io/npm/l/react)](https://github.com/git/git-scm.com/blob/main/MIT-LICENSE.txt) 

O **DSCommerce** é um sistema de e-commerce completo desenvolvido durante o Bootcamp Spring da [DevSuperior](https://devsuperior.com.br), ministrado pelo professor Nélio Alves. 

A aplicação consiste em um sistema onde usuários podem visualizar produtos, gerenciar um carrinho de compras, realizar pedidos e efetuar pagamentos. O sistema possui dois perfis de acesso: **Clientes** (com permissões de compra e visualização) e **Administradores** (responsáveis pelo gerenciamento do catálogo de produtos e usuários).

## 🛠️ Tecnologias Utilizadas

### Back-end
- **Java 25**
- **Spring Boot 3**
- **Spring Data JPA**
- **Spring Security** (OAuth2 com JWT para autenticação e autorização)
- **Banco de dados:** H2 (Testes/Desenvolvimento) e PostgreSQL (Produção)
- **Validation** (Bean Validation para regras de negócio nos DTOs)

### Ferramentas & Padrões
- Padrão arquitetural **DDD** (Camadas: Controller, Service, Repository, DTO, Entity)
- Tratamento global de exceções customizadas
- Migrações de banco de dados
- Postman (para testes automatizados das rotas)

---

## 📐 Modelo de Domínio (ORM)
A estrutura do banco de dados e as relações entre as entidades seguem o modelo da aplicação.

---

## 🚀 Como Executar o Projeto

### Pré-requisitos
Antes de começar, você vai precisar ter instalado em sua máquina:
- Java JDK (versão 17 ou superior)
- Git
- Uma IDE de sua preferência (IntelliJ IDEA, Eclipse, VS Code)

### Passo a Passo

1. **Clonar o repositório:**
\`\`\`bash
git clone https://github.com/ujoaofreitas/dscommerce.git
\`\`\`

2. **Entrar na pasta do projeto:**
\`\`\`bash
cd dscommerce
\`\`\`

3. **Executar a aplicação:**
Você pode rodar diretamente pela sua IDE (executando a classe \`DscommerceApplication.java\`) ou via terminal utilizando o Maven Wrapper:
\`\`\`bash
./mvnw spring-boot:run
\`\`\`

4. **Acessar a aplicação:**
Por padrão, a API estará rodando no endereço: \`http://localhost:8080\`

O banco de dados H2 pode ser acessado em: \`http://localhost:8080/h2-console\`
- **JDBC URL:** \`jdbc:h2:mem:testdb\`
- **User Name:** \`sa\`
- **Password:** *(deixe em branco)*

---

## 🛣️ Endpoints Principais (API)

### Rotas Públicas
- \`GET /products\` - Retorna a listagem paginada de produtos.
- \`GET /products/{id}\` - Retorna os detalhes de um produto específico.

### Rotas Protegidas (Requer Autenticação)
- \`POST /products\` - Cadastra um novo produto (Apenas ADMIN).
- \`PUT /products/{id}\` - Atualiza um produto existente (Apenas ADMIN).
- \`DELETE /products/{id}\` - Deleta um produto (Apenas ADMIN).
- \`POST /orders\` - Registra um novo pedido (CLIENT / ADMIN).
- \`GET /orders/{id}\` - Busca os detalhes de um pedido (CLIENT dono do pedido / ADMIN).

---

## 🧑‍💻 Autor

Desenvolvido por **João Freitas**. Entre em contato comigo!

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/ujoaofreitas)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/ujoaofreitas)

---
Criado durante o treinamento de Spring Boot da DevSuperior.
EOF
