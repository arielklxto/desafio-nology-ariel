# Sistema de Cálculo de Cashback

Aplicação web para cálculo de cashback com base em regras de desconto, tipo de cliente (VIP ou normal) e valor final da compra, incluindo registro de histórico em banco de dados.

---

![Desafio Nology](https://github.com/arielklxto/desafio-nology-ariel/blob/main/print-app.jpg)


## Acesso ao Projeto

🔗 **Frontend (Aplicação):**  
https://desafio-nology-gamma.vercel.app/

🔗 **API (Documentação Swagger):**  
https://desafio-nology-6mlb.onrender.com/docs

🔗 **Repositório:**  
https://github.com/arielklxto/desafio-nology-ariel

---

## Funcionalidades

- Cálculo de cashback com base em:
  - Valor da compra
  - Desconto aplicado
  - Tipo de cliente (VIP ou normal)
- Bônus adicional para clientes VIP
- Multiplicador para compras acima de R$ 500
- Registro de consultas no banco de dados
- Visualização de histórico por IP

---

## Regras de Negócio

- Cashback base: **5%**
- Cliente VIP: +**10%** sobre o cashback base
- Compras acima de R$ 500: **cashback dobrado**
- O desconto é aplicado antes do cálculo do cashback

---

## Arquitetura

O sistema foi estruturado de forma desacoplada:

- **Frontend:** HTML, CSS e JavaScript (Vercel)
- **Backend:** FastAPI (Render)
- **Banco de Dados:** MySQL (Railway)

A comunicação entre frontend e backend ocorre via **API REST** utilizando requisições HTTP.

---

## Tecnologias Utilizadas

- Python (FastAPI)
- MySQL
- HTML, CSS, JavaScript
- Render (deploy backend)
- Vercel (deploy frontend)
- Railway (banco de dados)

---

## Fluxo da Aplicação

1. O usuário insere os dados no frontend  
2. O frontend envia uma requisição para a API  
3. O backend processa o cálculo do cashback  
4. O resultado é salvo no banco de dados  
5. A API retorna o valor calculado ao frontend  

---

## Como Executar Localmente

### Backend

```bash
pip install -r requirements.txt
uvicorn main:app --reload
