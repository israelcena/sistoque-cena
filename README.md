# Sistema de Gerenciamento de Produtos

Sistema completo de gerenciamento de estoque com backend NestJS e frontend Next.js.

## Tecnologias

### Backend
- NestJS 11
- TypeScript
- Class Validator para validação de dados
- CORS habilitado para comunicação com frontend

### Frontend
- Next.js 15.3
- React 19
- TypeScript
- Tailwind CSS 4
- Dark mode support

## Funcionalidades

- Criar novos produtos
- Listar todos os produtos
- Editar produtos existentes
- Excluir produtos
- Validação de dados no backend
- Interface responsiva com dark mode
- Armazenamento em memória (pode ser substituído por banco de dados)

## Estrutura do Projeto

```
.
├── backend/              # API NestJS
│   └── src/
│       ├── products/     # Módulo de produtos
│       │   ├── entities/        # Entidades
│       │   ├── dto/             # Data Transfer Objects
│       │   ├── products.controller.ts
│       │   ├── products.service.ts
│       │   └── products.module.ts
│       ├── app.module.ts
│       └── main.ts
│
└── frontend/             # Interface Next.js
    └── src/
        └── app/
            └── page.tsx  # Página principal
```

## Como Executar

### Backend

```bash
cd backend
npm install
npm run start:dev
```

O servidor estará rodando em `http://localhost:3000`

### Frontend

```bash
cd frontend
npm install
npm run dev
```

A aplicação estará disponível em `http://localhost:3001`

## API Endpoints

- `GET /products` - Listar todos os produtos
- `GET /products/:id` - Buscar produto por ID
- `POST /products` - Criar novo produto
- `PATCH /products/:id` - Atualizar produto
- `DELETE /products/:id` - Excluir produto

### Exemplo de Produto

```json
{
  "name": "Notebook",
  "description": "Notebook para desenvolvimento",
  "price": 3500.00,
  "quantity": 10,
  "category": "Eletrônicos"
}
```

## Próximas Melhorias

- [ ] Integração com banco de dados (PostgreSQL, MongoDB, etc.)
- [ ] Autenticação e autorização
- [ ] Paginação na listagem de produtos
- [ ] Filtros e busca
- [ ] Upload de imagens
- [ ] Relatórios e exportação de dados
- [ ] Histórico de movimentações de estoque
- [ ] Notificações de estoque baixo

## Licença

Este projeto foi desenvolvido para fins educacionais.
