# ASSETANA QUANT-PRO V23 — Cloud Intelligence Engine

> Auto trade engine for Deriv platform (binary options / synthetic indices / forex)

## 🚀 Deploy na Vercel

### Pré-requisitos
- Conta na [Vercel](https://vercel.com) (gratuita)
- Repositório GitHub com este código

### Passos

1. **Fork / clone** este repositório no GitHub
2. No painel da Vercel: **Add New Project → Import Git Repository**
3. Selecione este repositório
4. Configurações de build:
   - **Framework Preset:** Other
   - **Build Command:** *(deixar vazio)*
   - **Output Directory:** `.` (ponto)
5. Clique **Deploy**

O site ficará disponível em `https://seu-projeto.vercel.app`

---

## 📁 Estrutura do Projeto

```
/
├── index.html          # App principal (ASSETANA V23)
├── vercel.json         # Configuração Vercel (headers, rewrites)
└── README.md           # Este arquivo
```

> **Imagem de fundo opcional:** Para usar o background cyberpunk customizado,
> adicione o arquivo `cyberpunk_trading_bg.png` na raiz do projeto.
> Sem ele, o app usa um background CSS gerado automaticamente.

---

## ⚙️ Configuração do App

Após o deploy, acesse a URL e configure:

| Campo | Onde encontrar |
|-------|---------------|
| **TwelveData API Key** | [twelvedata.com/apikey](https://twelvedata.com/apikey) |
| **Deriv App ID** | [developers.deriv.com](https://developers.deriv.com) |
| **Token DEMO** | [app.deriv.com/account/api-token](https://app.deriv.com/account/api-token) |
| **Token REAL** | Mesmo link acima |
| **Ably Key** (Cloud V23) | [ably.com](https://ably.com) |
| **Supabase URL + Key** | [supabase.com](https://supabase.com) |

---

## 🔌 WebSocket & CORS

O Vercel serve o app em **HTTPS**, o que desbloqueia automaticamente:
- WebSocket Deriv (`wss://ws.derivws.com`)
- API TwelveData (REST)
- Ably Realtime

> Se abrir o `index.html` localmente via `file://`, o WebSocket ficará bloqueado.
> Use sempre a URL da Vercel ou um servidor local: `python3 -m http.server 8080`

---

## 🧠 Módulos V23

- **ANALYZER** — Gráfico candlestick + indicadores em tempo real
- **DASHBOARD** — Equity curve + métricas de risco
- **BACKTEST** — Walk-Forward IS70%/OOS30% + slippage model
- **BRAIN V21** — Asset IQ + K-Means clusters + Monte Carlo + SHAP
- **PREDICTOR** — Logistic Regression online (Light Predictor)
- **OTIMIZADOR** — Grid Search + Algoritmo Genético
- **SUPERVISOR IA** — Agent Lightning + Supabase + Ably
- **CLOUD V23** — Broadcast/recepção de sinais via Ably

---

## ⚠️ Aviso Legal

Este software é para fins educacionais. Trading envolve risco de perda de capital.
Use sempre a conta **DEMO** até ter confiança nos resultados.
