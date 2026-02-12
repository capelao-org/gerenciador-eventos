# 🎉 Sistema de Gerenciamento de Eventos

![Node](https://img.shields.io/badge/Node.js-18+-green)
![MySQL](https://img.shields.io/badge/MySQL-Database-blue)
![Status](https://img.shields.io/badge/Status-Acadêmico-orange)
![Curso](https://img.shields.io/badge/Curso-ADS-00599C)

---

# 📌 1. Visão Geral do Projeto

O **Sistema de Gerenciamento de Eventos** é uma aplicação Web Full Stack desenvolvida com arquitetura Cliente-Servidor utilizando API REST, banco de dados relacional e autenticação baseada em JWT.

O sistema permite:

- Cadastro e autenticação de usuários
- Gerenciamento de eventos
- Upload de arquivos
- Controle de acesso via token
- Persistência de dados em banco relacional

---

# 🏗 2. Arquitetura do Sistema

```text
📦 gerenciador-eventos
 ┣ 📂 gerenciador-eventos-BackEnd
 ┗ 📂 gerenciador-eventos-FrontEnd
```

## Modelo Arquitetural

- Arquitetura Cliente-Servidor
- API REST
- Padrão MVC
- Autenticação JWT
- Upload de arquivos
- Integração com Amazon S3

---

# 🔙 3. Backend

Responsável por:

- Regras de negócio
- Autenticação e autorização
- Upload e armazenamento de arquivos
- Persistência de dados
- Comunicação com banco MySQL

---

## 📂 Estrutura

```text
BackEnd
 ┣ 📂 models
 ┣ 📂 controllers
 ┣ 📂 routes
 ┣ 📂 config
 ┣ 📂 middlewares
 ┣ 📄 index.js
 ┗ 📄 .env
```

---

# 🛠 4. Tecnologias e Dependências Utilizadas

## 🔹 Principais Dependências

### express
Framework principal para criação da API REST em Node.js.  
Responsável por gerenciar rotas, requisições e respostas HTTP.

---

### sequelize
ORM (Object Relational Mapping) utilizado para:

- Criar models
- Executar consultas no banco
- Gerenciar migrations
- Abstrair comandos SQL

---

### mysql2
Driver MySQL utilizado para conexão e execução de consultas no banco de dados.

---

### dotenv
Carrega variáveis de ambiente a partir do arquivo `.env`, permitindo proteger dados sensíveis como:

- Senhas
- Tokens
- Credenciais de banco
- Chaves da AWS

---

### cors
Permite configurar acesso da API por aplicações externas (Cross-Origin Resource Sharing), garantindo que o Frontend consiga acessar o Backend mesmo estando em portas diferentes.

---

### bcrypt
Responsável por:

- Criptografar senhas usando hash seguro
- Comparar senha digitada com hash armazenado

Utilizado para aumentar a segurança da autenticação.

---

### jsonwebtoken
Utilizado para:

- Gerar tokens JWT
- Validar tokens
- Implementar autenticação baseada em token

Fluxo:

```text
Login → Geração de Token → Cliente armazena Token → 
Requisições protegidas enviam Token → Backend valida Token
```

---

### multer
Middleware responsável por:

- Upload de arquivos via formulário (`multipart/form-data`)
- Manipulação temporária de arquivos no servidor

---

### @aws-sdk/client-s3
Integração com o serviço **Amazon S3**, permitindo:

- Upload de arquivos para nuvem
- Gerenciamento de objetos armazenados
- Armazenamento seguro e escalável

Fluxo de upload:

```text
Frontend envia arquivo →
Multer processa →
Backend envia para Amazon S3 →
Arquivo armazenado na nuvem →
URL salva no banco de dados
```

---

# 🔗 5. Comunicação entre as Camadas

```text
[Usuário]
    ↓
[Frontend]
    ↓ HTTP Request (GET | POST | PUT | DELETE)
[Express]
    ↓
[Controller]
    ↓
[Sequelize]
    ↓
[MySQL]
    ↓
[Resposta JSON]
```

Para rotas protegidas:

```text
Login →
Geração de JWT →
Token enviado no Header →
Middleware valida token →
Acesso autorizado
```

---

# 📬 6. Endpoints da API (Exemplo)

| Método | Rota | Protegida | Descrição |
|--------|------|-----------|------------|
| POST | `/login` | ❌ | Autenticação |
| GET | `/eventos` | ✅ | Listar eventos |
| POST | `/eventos` | ✅ | Criar evento |
| PUT | `/eventos/:id` | ✅ | Atualizar evento |
| DELETE | `/eventos/:id` | ✅ | Remover evento |

---

# 🗄 7. Banco de Dados

Banco relacional MySQL.

Conceitos aplicados:

- Entidade-Relacionamento
- Integridade Referencial
- Relacionamentos 1:N
- Normalização
- Persistência com ORM

---

# ⚙️ 8. Requisitos do Sistema

- Node.js 18+
- MySQL Server
- Conta AWS (para S3)
- Git
- VSCode (opcional)

---

# 🚀 9. Guia Completo de Execução

## 9.1 Clonar Repositório

```bash
git clone <URL_DO_REPOSITORIO>
```

---

## 9.2 Criar Banco

```sql
CREATE DATABASE gerenciador_eventos;
```

---

## 9.3 Configurar `.env`

```env
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=sua_senha
DB_NAME=gerenciador_eventos
PORT=3000

JWT_SECRET=sua_chave_secreta

AWS_ACCESS_KEY_ID=sua_access_key
AWS_SECRET_ACCESS_KEY=sua_secret_key
AWS_REGION=sua_regiao
AWS_BUCKET_NAME=nome_do_bucket
```

---

## 9.4 Instalar Dependências

```bash
cd gerenciador-eventos-BackEnd
npm install
```

---

## 9.5 Iniciar Servidor

```bash
npm start
```

Servidor:

```text
http://localhost:3000
```

---

# 🧠 10. Conceitos Técnicos Aplicados

- API REST
- JWT Authentication
- Upload de arquivos
- Integração com Cloud (Amazon S3)
- ORM
- Hash de senha
- Middleware
- Arquitetura MVC
- Variáveis de ambiente
- Separação de responsabilidades

---

# 📚 11. Informações Acadêmicas

**Instituição:** Instituto Federal do Piauí – IFPI  
**Curso:** Análise e Desenvolvimento de Sistemas – ADS  
**Professor:** Anderson Barros  

---

# 👥 12. Autores

- Autor 1: Antonio Hittalo Ramyres P. R. Macedo
- Autor 2: Bento Kauê de Sousa Lima
- Autor 3: João Manuel da Silva Paulo
- Autor 4: José Nillo Marques Martins

---

# 📈 13. Melhorias Futuras

- Deploy em produção
- Docker
- Testes automatizados
- CI/CD
- Monitoramento
- Documentação Swagger

---

# 📄 14. Licença

Projeto desenvolvido exclusivamente para fins acadêmicos.
