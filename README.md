# API de Anotações

Esta é uma API para gerenciar anotações, permitindo criar, buscar, atualizar e deletar notas. O projeto foi desenvolvido utilizando Node.js, TypeScript e Prisma ORM.

## Requisitos

Antes de começar, certifique-se de ter os seguintes itens instalados em sua máquina:

- [Node.js](https://nodejs.org/) (versão 16 ou superior)
- [npm](https://www.npmjs.com/) 
- Banco de dados compatível com Prisma (ex.: PostgreSQL, MySQL, SQLite)

## Instalação

1. Clone este repositório:
   ```bash
   git clone https://github.com/Vinipereir/API_anotacoes_pessoais.git
   cd seu-repositorio
   ```

2. Instale as dependências:
   ```bash
   npm install



3. Configure o banco de dados:
   - Renomeie o arquivo `.env.example` para `.env`.
   - Edite o arquivo `.env` e configure a variável `DATABASE_URL` com a URL de conexão do seu banco de dados.

4. Gere o cliente Prisma:
   ```bash
   npx prisma generate
   ```

5. Execute as migrações para criar as tabelas no banco de dados:
   ```bash
   npx prisma migrate dev
   ```

## Uso

Para iniciar o servidor de desenvolvimento, execute:

```bash
npm run dev


A API estará disponível em `http://localhost:3000`.

### Endpoints

- **GET /notas**: Retorna todas as notas.
- **POST /notas**: Cria uma nova nota.
- **GET /notas/:id**: Retorna uma nota específica.
- **PUT /notas/:id**: Atualiza uma nota existente.
- **DELETE /notas/:id**: Deleta uma nota.

### Exemplo de busca por termo id

Endpoint: `GET http://localhost:3000/notas/2`

Este endpoint permite buscar notas pelo id ou conteúdo que contenham o termo especificado.

## Estrutura do Projeto

```plaintext
src/
├── controllers/    # Lógica dos controladores
├── routes/         # Definição das rotas
├── models/         #organizar e estruturar os dados da aplicação
├── server.js       # Configuração principal do servidor
```

## Arquivo .gitignore

Certifique-se de que o arquivo `.gitignore` inclua os seguintes itens:

```
node_modules/
.env

```

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests.

## Licença

Este projeto está licenciado sob a licença MIT. Consulte o arquivo `LICENSE` para mais detalhes.