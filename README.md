🚀 Como Executar o Projeto
Pré-requisitos:
Certifique-se de ter instalados:

Node.js (v14 ou superior)

MySQL (configurado com as credenciais do arquivo .env)

Passo a Passo:
Clone o repositório:

bash
git clone <URL_DO_REPOSITORIO>
cd snoopy-petshop
Instale as dependências:

bash
npm install
Configure o arquivo .env com as credenciais do banco de dados:

DATABASE_URL="mysql://usuario:senha@localhost:3306/snoopy_petshop"
Inicialize o Prisma:

bash
npx prisma generate
Execute as migrações para criar as tabelas no banco:

bash
npx prisma migrate dev --name init
Inicie o servidor:

bash
npm run dev
Teste as rotas usando o Insomnia ou outra ferramenta de sua preferência.

📂 Estrutura de Pastas
snoopy-petshop/
├── prisma/
│   ├── schema.prisma     # Modelo do banco de dados
├── src/
│   ├── controllers/      # Lógica das rotas (CRUD de motoristas e pedidos)
│   ├── routes/           # Arquivo para definir as rotas
│   └── server.js         # Configuração do servidor
├── .env                  # Configuração de variáveis de ambiente
├── package.json          # Configurações e scripts do projeto
📋 Endpoints Principais
Motoristas
Método	Rota	Descrição
POST	/motoristas	Cadastrar motorista
GET	/motoristas	Listar todos os motoristas
GET	/motoristas/:id	Buscar motorista pelo ID
PUT	/motoristas/:id	Atualizar motorista pelo ID
DELETE	/motoristas/:id	Excluir motorista pelo ID
Pedidos
Método	Rota	Descrição
POST	/pedidos	Cadastrar pedido
GET	/pedidos	Listar todos os pedidos
GET	/pedidos/:id	Buscar pedido pelo ID
PUT	/pedidos/:id	Atualizar pedido pelo ID
DELETE	/pedidos/:id	Excluir pedido pelo ID
🧪 Exemplos de Testes (Insomnia)
Cadastrar Motorista (POST /motoristas)
json
{
  "email": "motorista@email.com",
  "nome": "Carlos dos Santos",
  "telefones": "(11) 98765-4321"
}
Cadastrar Pedido (POST /pedidos)
json
{
  "motoristaId": 1,
  "data": "2025-04-15T14:30:00.000Z",
  "produto": "Casinha",
  "valor": 40.50,
  "endereco": "Rua dos Anjos",
  "numero": "163",
  "cep": "12345-978",
  "complemento": "Bloco A"
}
📌 Contribuição
Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests.



![Captura de tela 2025-04-15 165949](https://github.com/user-attachments/assets/2b84dfae-cfa5-498d-a164-14f9b6fc554c)

