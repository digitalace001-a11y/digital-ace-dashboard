# Digital Ace - Dashboard com Google Sheets

## Fluxo
```
Google Sheets (você edita) → Dashboard (lê em tempo real) → Vercel (hospeda)
```
Sem banco de dados, sem backend, sem API key. Só uma planilha pública e um HTML.

---

## PASSO 1: Criar o Google Sheets

1. Abra [sheets.google.com](https://sheets.google.com) → Nova planilha
2. Renomeie para: **Digital Ace - Dashboard**
3. Crie **3 abas** com os nomes EXATOS abaixo:

### Aba 1: `revenue`
| data | mes | conta | produto | usd | cotacao |
|------|-----|-------|---------|-----|---------|
| 2025-06-04 | Jun 2025 | TTK Shop 001 | YIANNA Faja | 18.37 | 5.50 |

### Aba 2: `contas`
| conta | status |
|-------|--------|
| TTK Shop 001 | Ativo |

### Aba 3: `config`
| chave | valor |
|-------|-------|
| meta_bronze | 7500 |
| meta_silver | 10000 |
| meta_gold | 15000 |
| meta_diamond | 25000 |

---

## PASSO 2: Publicar o Google Sheets

1. **Arquivo → Compartilhar → Publicar na Web**
2. Documento inteiro → formato CSV → Publicar
3. Copie o ID da URL: `https://docs.google.com/spreadsheets/d/`**ID_AQUI**`/edit`

---

## PASSO 3: Configurar o Dashboard

Abra `index.html`, encontre e substitua:
```js
const SHEET_ID = 'COLE_SEU_SHEET_ID_AQUI';
```

---

## PASSO 4: Deploy na Vercel

1. [vercel.com/new](https://vercel.com/new) → Upload
2. Arraste a pasta com index.html + vercel.json
3. Dashboard online

---

## Uso diário
- Abra o Google Sheets (celular ou PC)
- Adicione linhas na aba `revenue`
- Dashboard atualiza ao dar refresh
