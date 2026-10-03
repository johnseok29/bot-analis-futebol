# Bot Analis Futebol

Plataforma completa para acompanhar partidas reais, gerar análise de pressão e sugerir mercados com base em dados públicos e em regras de lógica esportiva.

## Stack
- Node.js + Express
- React + Vite
- Fetch para APIs públicas
- Fallback para dados locais caso a API externa falhe

## Requisitos
- Node.js 18+
- npm

## Instalação

```bash
npm install
```

## Execução em desenvolvimento

```bash
npm run dev
```

O frontend roda em: http://localhost:5173
O backend roda em: http://localhost:4000

## Endpoints

- GET `/api/health`
- GET `/api/fixtures?date=YYYY-MM-DD`
- GET `/api/summary?date=YYYY-MM-DD`

## Observação sobre dados reais

O projeto busca partidas públicas do ESPN e normaliza os resultados em uma base comum. Para odds e dados mais profundos (xG, posse, stats, bookmakers), é recomendável conectar APIs de terceiros com chave de acesso, como:
- API-Football
- The Odds API
- Sportradar
- Football Data

Sem essas chaves, o painel usa dados reais de fixtures + lógica derivada localmente para manter o sistema funcional.
