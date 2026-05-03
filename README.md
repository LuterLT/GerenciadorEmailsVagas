# 📩 Automação de Triagem de Vagas do LinkedIn

Automação desenvolvida com n8n para filtrar, classificar e organizar e-mails de vagas recebidos do LinkedIn com foco em **oportunidades de estágio (internship)**.

---

## ⚙️ Como funciona

- Executa automaticamente todos os dias às **23:40**
- Filtra e-mails enviados por:
  - `jobalerts-noreply@linkedin.com`
  - `jobs-listings@linkedin.com`
  - `jobs-noreply@linkedin.com`
- Usa IA (Gemini + Groq) para separar as vagas já filtradas pelos Nodes em Javascript
- Identifica palavras-chave relacionadas a **estágio (internship)** (ex: “estágio”, “internship”)
- Marca e-mails relevantes com o rótulo **`vagasLinkedin`**
- Registra automaticamente as informações no Google Sheets

---

## 📊 Dados coletados

Para cada vaga identificada, são armazenados:

- **Título da vaga**
- **Nome da empresa**
- **Localização**
- **Data do e-mail**
- **Link da vaga**

---

## 🧰 Tecnologias utilizadas

- n8n  
- Gmail API  
- Google Sheets API  
- Gemini API  
- Groq API  
- Docker (self-hosted)

---

## 🚀 Setup do ambiente

### 1. Subir o n8n com Docker

Utilize Docker caso queira rodar localmente.

---

### 2. Configurar Google Cloud

1. Acesse o Google Cloud Console  
2. Crie um novo projeto  
3. Ative as APIs:
   - Gmail API
   - Google Sheets API  
4. Crie uma credencial **OAuth 2.0**
5. Copie:
   - Client ID  
   - Client Secret  

---

### 3. Configurar credenciais no n8n

- Configure OAuth2 para:
  - Gmail
  - Google Sheets  
- Faça login com sua conta Google  
- Insira o **Client ID** e **Client Secret**

---

### 4. Configurar APIs de IA

- Adicione no n8n:
  - Chave da API do Gemini  
  - Chave da API da Groq  

---

### 5. Importar e ajustar o workflow

- Importe o fluxo no n8n  
- Configure:
  - Credenciais  
  - Lista de palavras-chave relacionadas a **estágio (internship)**  

---

## ⏱️ Agendamento

Execução automática diária às:

23:40
