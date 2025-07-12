# NLW Agents

Projeto desenvolvido durante o evento **NLW (Next Level Week)** da Rocketseat, focado em criar uma aplicação de agentes inteligentes.

## 🚀 Tecnologias

### Backend
- **Fastify** - Framework web rápido para Node.js
- **TypeScript** - Linguagem tipada
- **Drizzle ORM** - ORM moderno para TypeScript
- **PostgreSQL** - Banco de dados relacional
- **pgvector** - Extensão para vetores no PostgreSQL
- **Zod** - Validação de schemas

### Ferramentas
- **Biome** - Linter e formatter
- **Docker** - Containerização
- **Node.js** - Runtime JavaScript

## 📋 Pré-requisitos

- Node.js 18+
- Docker e Docker Compose
- PostgreSQL (via Docker)

## ⚙️ Setup

### 1. Clone o repositório
```bash
git clone <url-do-repositorio>
cd server
```

### 2. Instale as dependências
```bash
npm install
```

### 3. Configure o banco de dados
```bash
# Inicie o PostgreSQL com Docker
docker-compose up -d
```

### 4. Configure as variáveis de ambiente
Crie um arquivo `.env` na raiz do projeto:
```env
DATABASE_URL="postgresql://docker:docker@localhost:5432/agents"
PORT=3333
```

### 5. Execute as migrações
```bash
npm run db:seed
```

### 6. Inicie o servidor
```bash
# Desenvolvimento (com hot reload)
npm run dev

# Produção
npm start
```

## 🛠️ Scripts Disponíveis

- `npm run dev` - Inicia o servidor em modo desenvolvimento com hot reload
- `npm start` - Inicia o servidor em modo produção
- `npm run db:seed` - Executa o seed do banco de dados

## 📁 Estrutura do Projeto

```
src/
├── db/           # Configurações do banco de dados
├── http/         # Rotas e controllers
├── env.ts        # Configurações de ambiente
└── server.ts     # Arquivo principal do servidor
```

## 🔧 Configurações

### TypeScript
- Target: ES2022
- Module: NodeNext
- Strict mode habilitado

### Biome
- Configurado com preset Ultracite
- Linting e formatação automática

### Drizzle
- Dialect: PostgreSQL
- Casing: snake_case
- Migrations: `./src/db/migrations`

## 🌐 Endpoints

- `GET /health` - Health check
- `GET /rooms` - Lista de salas (implementado)

## 📝 Padrões de Projeto

- **Clean Architecture** - Separação clara de responsabilidades
- **Type Safety** - Uso extensivo de TypeScript e Zod
- **Environment Variables** - Configurações via variáveis de ambiente
- **Docker** - Containerização para desenvolvimento
- **ORM Modern** - Drizzle ORM para queries type-safe

## 🚀 Deploy

O projeto está configurado para rodar com Node.js usando a flag `--experimental-strip-types` para execução direta de arquivos TypeScript.

---

Desenvolvido com 💜 durante o NLW da Rocketseat 