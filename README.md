Aplicação **full stack** desenvolvida em **Spring Boot** e **React/Vite**, criada para listar vendas e **simular o envio de SMS** (mock no backend + *toast* no frontend).

---

## 🚀 Tecnologias utilizadas

**Backend**
- Java 17  
- Spring Boot 2.7  
- Banco em memória H2  

**Frontend**
- React + Vite + TypeScript  
- Axios, Datepicker e React-Toastify  

---

## ⚙️ Como rodar o projeto

# Acesse: https://tccraissa.netlify.app/


### 🖥️ Backend
\`\`\`bash
cd backend
./mvnw clean spring-boot:run
# Acesse http://localhost:8080
\`\`\`

### 💻 Frontend
\`\`\`bash
cd frontend
npm install
npm run dev
# Acesse http://127.0.0.1:5173
\`\`\`

---

## 🧱 Arquitetura do Sistema

Fluxo geral de funcionamento do projeto:

📘 **Diagrama Arquitetural:**
![Diagrama Arquitetural](docs/Diagrama%20Arquitetural%20do%20DS%20Meta.png)

---

## 🧮 Modelo de Dados

O sistema utiliza uma única tabela chamada **tb_sales**, responsável por armazenar os registros de vendas.

📗 **Diagrama de Dados:**
![Modelo de Dados](docs/Modelo%20de%20Dados%20do%20DS%20Meta%20Raissa.png)

**Campos:**
| Campo | Tipo | Descrição |
|-------|------|------------|
| id | Long | Identificador único |
| seller_name | String | Nome do vendedor |
| visited | Integer | Visitas realizadas |
| deals | Integer | Negócios fechados |
| amount | Double | Valor total (R$) |
| date | Date | Data da venda |

---

## 🧩 Diagrama de Classes

Representa a entidade principal do projeto, **Sale**.

📙 **Diagrama de Classe:**
![Diagrama de Classe](docs/Diagrama%20de%20Classe%20entidade%20principal%20ds%20meta.png)

---

## 🔁 Diagrama de Sequência — Ação “Notificar”

Mostra o fluxo da ação de notificação simulada no sistema:

📒 **Diagrama de Sequência:**
![Diagrama de Sequência](docs/Diagrama%20de%20sequencia%20notificar%20o%20vendedor.png)

Fluxo:
1. O **usuário** clica no botão **Notificar** no frontend.  
2. O **frontend** envia uma requisição `POST` para o backend (`/sales/{id}/notification`).  
3. O **backend** processa a requisição e retorna sucesso.  
4. O **frontend** exibe um **toast de confirmação** (“SMS enviado com sucesso”).  
5. O **backend** imprime no console logs simulando o envio.

---

## 📩 Notificações simuladas

- O botão **“Notificar”** exibe um *toast* de sucesso no frontend  
- No backend, é impresso no console:
  \`\`\`
  [MOCK] SMS SIMULADO com sucesso!
  [MOCK] Mensagem: O vendedor X foi destaque...
  \`\`\`
- O envio real via Twilio foi **desativado** para evitar custos.

---

## 🏁 Objetivo

Projeto utilizado como **Trabalho de Conclusão de Curso**, demonstrando domínio de:
- Integração entre front e back-end  
- Consumo de API REST  
- Uso de ORM (JPA/Hibernate) e banco em memória  
- Deploy local e versionamento no GitHub
- 
