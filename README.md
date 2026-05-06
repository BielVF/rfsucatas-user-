# RF Sucatas - Backend (Railway + PostgreSQL + Prisma)

## Variáveis de ambiente (Railway)
- `DATABASE_URL` (Railway PostgreSQL fornece automaticamente)
- `API_KEY` = `0838@RFSucatas2026!`
- `PORT` = `3000`

## Rodar local
```bash
npm install
npx prisma generate
npx prisma migrate dev --name init
npm run dev
```

## Deploy Railway
Railway vai executar:
- `npm install`
- `npm start`

### Rodar migrations no Railway
Depois do deploy, no Railway -> Service -> Deployments -> Run Command:
```bash
npx prisma migrate deploy
```

## Autenticação
Todas as rotas exigem header:

`x-api-key: 0838@RFSucatas2026!`