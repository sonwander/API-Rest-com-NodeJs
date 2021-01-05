# Uma API REST simples para consumo de dados

Você precisará adicionar uma secret key no arquivo `.env`:

```
TOKEN_SECRET='sua_secret_key_aqui'
```

Execute os comandos abaixo:

```
npm i
npx sequelize db:migrate
npx sequelize db:seed:all
npm run dev
```

A API deverá estará rodando no endereço http://127.0.0.1:3001/.


As configurações começando com `process.env.` vem do arquivo `.env`.

Os dados de usuário e senha dos arquivos de seed são:

- email = admin@email.com
- senha = 123456

Você pode obter o token JWT na rota `/tokens`, passando os dados JSON:

```json
{
	"email": "admin@email.com",
	"password": "123456"
}
```

Headers:

```
Content-Type	application/json; charset=utf-8
```
