# 🎉 Sistema de Gerenciamento de Eventos

![Node](https://img.shields.io/badge/Node.js-18+-green)
![MySQL](https://img.shields.io/badge/MySQL-Database-blue)
![Status](https://img.shields.io/badge/Status-Acadêmico-orange)
![Curso](https://img.shields.io/badge/Curso-ADS-00599C)

---

# 📌 1. Visão Geral do Projeto

O **Sistema de Gerenciamento de Eventos** é uma aplicação Web Full Stack desenvolvida com o objetivo de aplicar conceitos de desenvolvimento web moderno utilizando arquitetura cliente-servidor e API REST.

O sistema permite:

- Cadastro de usuários
- Gerenciamento de eventos
- Comunicação entre interface e servidor
- Persistência de dados em banco relacional
- Organização modular do código

---

# 🏗 2. Arquitetura do Sistema

O projeto é dividido em duas aplicações independentes:

```text
📦 gerenciador-eventos
 ┣ 📂 gerenciador-eventos-BackEnd
 ┗ 📂 gerenciador-eventos-FrontEnd
```

## 🧱 Modelo Arquitetural

- Arquitetura Cliente-Servidor
- API REST
- Padrão MVC (Backend)
- Separação de Responsabilidades
- Modularização por camadas

---

# 🔙 3. Backend

Responsável por:

- Regras de negócio
- Processamento de requisições
- Persistência de dados
- Comunicação com banco MySQL

## 📂 Estrutura

```text
BackEnd
 ┣ 📂 models
 ┣ 📂 controllers
 ┣ 📂 routes
 ┣ 📂 config
 ┣ 📄 index.js
 ┗ 📄 .env
```

## 🛠 Tecnologias Utilizadas

- Node.js
- Express
- Sequelize (ORM)
- MySQL
- Dotenv
- Cors

## 🔎 Funcionamento Interno

1. O cliente envia uma requisição HTTP.
2. A rota direciona para o Controller.
3. O Controller executa a regra de negócio.
4. O Model interage com o banco via Sequelize.
5. O Backend retorna resposta em JSON.

---

# 🔜 4. Frontend

Responsável por:

- Interface gráfica
- Captura de dados
- Envio de requisições HTTP
- Renderização de dados recebidos

## 📂 Estrutura

```text
FrontEnd
 ┣ 📂 css
 ┣ 📂 js
 ┣ 📄 index.html
 ┗ 📄 demais páginas
```

## 🛠 Tecnologias Utilizadas

- HTML5
- CSS3
- JavaScript
- Bootstrap

---

# 🔗 5. Comunicação entre Frontend e Backend

Fluxo completo de execução:

```text
[Usuário]
    ↓
[Frontend]
    ↓  HTTP Request (GET | POST | PUT | DELETE)
[Backend - Express]
    ↓
[Controller]
    ↓
[Model - Sequelize]
    ↓
[MySQL]
    ↓
[Resposta JSON]
    ↓
[Frontend atualiza interface]
```

---

# 📬 6. Endpoints da API

| Método | Rota | Descrição |
|--------|------|-----------|
| GET | `/eventos` | Listar eventos |
| POST | `/eventos` | Criar evento |
| PUT | `/eventos/:id` | Atualizar evento |
| DELETE | `/eventos/:id` | Remover evento |

---

# 🗄 7. Banco de Dados

Banco relacional MySQL.

### Conceitos Aplicados:

- Entidade-Relacionamento
- Chaves Primárias
- Chaves Estrangeiras
- Relacionamentos 1:N
- Integridade Referencial

---

# ⚙️ 8. Requisitos do Sistema

- Node.js 18+
- MySQL Server
- Git
- VSCode (opcional)
- Navegador atualizado

---

# 🚀 9. Guia Completo de Execução

## 9.1 Clonar o Repositório

```bash
git clone <URL_DO_REPOSITORIO>
```

---

## 9.2 Criar Banco de Dados

```sql
CREATE DATABASE gerenciador_eventos;
```

---

## 9.3 Configurar Variáveis de Ambiente

Criar arquivo `.env` dentro da pasta Backend:

```env
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=sua_senha
DB_NAME=gerenciador_eventos
PORT=3000
```

---

## 9.4 Instalar Dependências (Backend)

```bash
cd gerenciador-eventos-BackEnd
npm install
```

---

## 9.5 Iniciar Servidor

```bash
npm start
```

Servidor disponível em:

```text
http://localhost:3000
```

---

## 9.6 Executar Frontend

```bash
cd gerenciador-eventos-FrontEnd
```

Abrir:

```text
index.html
```

Ou usar Live Server no VSCode.

---

# 🧠 10. Conceitos de Engenharia Aplicados

- Arquitetura em camadas
- Modularização
- CRUD
- API RESTful
- ORM
- Versionamento com Git
- Uso de variáveis de ambiente
- Separação entre lógica e interface

---

# 📊 11. Diagrama Conceitual Simplificado

```text
[Usuário]
     ↓
[Frontend]
     ↓
[API Express]
     ↓
[Controllers]
     ↓
[Models]
     ↓
[MySQL]
```

---

# 📚 12. Informações Acadêmicas

**Instituição:** Instituto Federal do Piauí – IFPI  
**Curso:** Análise e Desenvolvimento de Sistemas – ADS  
**Professor:** Anderson Barros  

---

# 👥 13. Autores

- Autor 1: Antonio Hittalo Ramyres P. R. Macedo
- Autor 2: Bento Kauê de Sousa Lima
- Autor 3: João Manuel da Silva Paulo
- Autor 4: José Nillo Marques Martins

---

# 🎯 14. Objetivo Acadêmico

Este projeto foi desenvolvido com fins educacionais para:

- Aplicar conceitos de desenvolvimento Full Stack
- Trabalhar integração entre camadas
- Desenvolver organização modular
- Aplicar modelagem de banco de dados
- Praticar boas práticas de desenvolvimento

---

# 🔒 15. Segurança e Boas Práticas

- Uso de `.env`
- Separação MVC
- Organização por pastas
- Padronização REST
- Tratamento básico de erros

---

# 📈 16. Melhorias Futuras

- Implementação de JWT
- Criptografia com bcrypt
- Deploy em ambiente cloud
- Testes automatizados
- Docker
- Documentação Swagger

---

# 📦 17. Status do Projeto

🟢 Em desenvolvimento acadêmico  
🟢 Funcional em ambiente local  

---

# 📄 18. Licença

Projeto desenvolvido exclusivamente para fins acadêmicos no IFPI.
