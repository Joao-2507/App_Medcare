
<div align="center">

# 💊 MedCare

### Sistema de Gerenciamento e Acompanhamento de Medicamentos

![React Native](https://img.shields.io/badge/React_Native-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Expo](https://img.shields.io/badge/Expo-000020?style=for-the-badge&logo=expo&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Node.js](https://img.shields.io/badge/Node.js-5FA04E?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=for-the-badge&logo=supabase&logoColor=white)

</div>

---

## 📖 Sobre o projeto

O **MedCare** é um aplicativo desenvolvido com o objetivo de auxiliar no gerenciamento e acompanhamento do uso de medicamentos.

A aplicação oferece funcionalidades para organizar horários, registrar medicamentos e acompanhar a administração das doses.

O sistema possui dois perfis de utilização:

- **Paciente:** responsável pelo gerenciamento dos medicamentos e acompanhamento de sua rotina.
- **Familiar:** permite acompanhar informações relacionadas aos medicamentos de um paciente vinculado.

O projeto utiliza React Native com Expo para a interface, Node.js e Express para a API e Supabase para autenticação e armazenamento de dados.

---

## 🎯 Objetivos

- Facilitar a organização de medicamentos.
- Auxiliar no acompanhamento dos horários de administração.
- Disponibilizar lembretes por notificações.
- Registrar o cumprimento da rotina de medicação.
- Permitir o acompanhamento por familiares.
- Integrar aplicativo, backend e banco de dados.

---

## ⚙️ Funcionalidades

### 👤 Autenticação e gerenciamento de usuários

- Cadastro de usuários.
- Login e autenticação.
- Perfis de paciente e familiar.
- Gerenciamento de informações de perfil.
- Vinculação entre pacientes e familiares.

### 💊 Gerenciamento de medicamentos

- Cadastro de medicamentos.
- Definição de doses e horários.
- Edição de informações.
- Remoção de medicamentos.
- Organização dos medicamentos cadastrados.

### ⏰ Lembretes e notificações

- Configuração de lembretes de medicamentos.
- Notificações locais em dispositivos compatíveis.
- Agendamento baseado nos horários cadastrados.

### ✅ Checklist de medicação

- Visualização das doses programadas.
- Registro de medicamentos tomados.
- Acompanhamento diário.
- Consulta ao histórico de administração.

### 👨‍👩‍👧 Acompanhamento familiar

- Cadastro e vinculação de familiares.
- Acesso a informações dos medicamentos.
- Visualização do checklist do paciente.
- Acompanhamento da rotina de medicação.

---

## 🛠️ Tecnologias utilizadas

### Frontend

- **React Native:** desenvolvimento da interface do aplicativo.
- **Expo:** ambiente de desenvolvimento e execução.
- **JavaScript:** implementação da lógica.
- **React Navigation:** navegação entre telas.
- **Expo Notifications:** gerenciamento de notificações.

### Backend

- **Node.js:** ambiente de execução JavaScript.
- **Express.js:** desenvolvimento da API REST.
- **Supabase:** autenticação e persistência de dados.
- **JWT:** autenticação de requisições.
- **Dotenv:** gerenciamento de variáveis de ambiente.

---

## 🏗️ Arquitetura do sistema

O MedCare utiliza uma arquitetura composta por três camadas principais:

**1. Aplicativo (Frontend)**

Interface desenvolvida em React Native, responsável pela interação com pacientes e familiares.

**2. API REST (Backend)**

Servidor Node.js com Express, responsável pelo processamento das requisições, autenticação e operações do sistema.

**3. Banco de Dados e Autenticação**

Supabase, utilizado para armazenamento e gerenciamento das informações dos usuários e medicamentos.

### Fluxo de comunicação

```text
         Aplicativo MedCare
          React Native
               |
               v
            API REST
        Node.js + Express
               |
               v
            Supabase
      Autenticação e Dados
```

---

## 📂 Estrutura do projeto

```text
MedCare/
│
├── App.js
├── index.js
├── package.json
├── app.json
│
├── assets/
│
├── src/
│   ├── components/
│   │
│   ├── screens/
│   │   ├── LoginScreen.js
│   │   ├── CadastroScreen.js
│   │   ├── HomeScreen.js
│   │   ├── RemediosScreen.js
│   │   ├── ChecklistScreen.js
│   │   ├── FamiliaScreen.js
│   │   └── ...
│   │
│   └── services/
│       ├── api.js
│       ├── authservice.js
│       ├── Remedioservice.js
│       ├── Checklistservice.js
│       └── Lembreteservice.js
│
└── MedCareBackend/
    ├── server.js
    └── src/
        ├── middleware/
        ├── routes/
        └── supabase.js
```

---

## 🚀 Como executar o projeto

### Pré-requisitos

- Node.js e npm instalados.
- Expo Go ou ambiente de desenvolvimento compatível.
- Projeto Supabase configurado.
- Variáveis de ambiente do backend.

### 1. Clonar o repositório

```bash
git clone https://github.com/Joao-2507/MedCare.git
```

### 2. Acessar o diretório

```bash
cd MedCare
```

### 3. Instalar as dependências

```bash
npm install
```

### 4. Configurar o backend

Crie o arquivo `MedCareBackend/.env` com as variáveis necessárias:

```env
PORT=3000
SUPABASE_URL=SUA_URL
SUPABASE_ANON_KEY=SUA_CHAVE_PUBLICA
SUPABASE_SERVICE_KEY=SUA_CHAVE_PRIVILEGIADA
```

**Atenção:** não publique o arquivo `.env` nem compartilhe suas credenciais.

O projeto também depende de tabelas e configurações apropriadas no Supabase.

### 5. Iniciar o backend

```bash
npm run api
```

### 6. Configurar o endereço da API

Configure a variável `EXPO_PUBLIC_API_URL` com o endereço acessível pelo aplicativo.

Para executar em um dispositivo físico, utilize o endereço IP local do computador que executa o backend.

### 7. Iniciar o aplicativo

Em outro terminal:

```bash
npm start
```

Utilize o Expo Go ou um ambiente compatível para executar a aplicação.

---

## 🔐 Segurança

O projeto utiliza autenticação e rotas protegidas para controlar o acesso às informações.

As credenciais de acesso ao Supabase devem ser armazenadas em variáveis de ambiente, sem exposição no código-fonte público.

O aplicativo é um projeto de software e não substitui orientações médicas ou farmacêuticas.

---

## 📌 Considerações finais

O desenvolvimento do MedCare permitiu aplicar conhecimentos de desenvolvimento mobile, integração de APIs, autenticação de usuários e gerenciamento de dados.

A aplicação reúne diferentes funcionalidades em uma solução voltada à organização de medicamentos e ao acompanhamento da rotina de administração.

O projeto também proporcionou experiência prática com arquitetura cliente-servidor, desenvolvimento colaborativo e integração entre frontend e backend.

---

## 👥 Desenvolvimento

Projeto desenvolvido em equipe.

**Integrantes:**

- João Victor Salústio
- [Adicionar os demais integrantes]

**Repositório original:**

[Adicionar link do repositório original]

---

## 👨‍💻 Contato

**João Victor Salústio**

Estudante de Engenharia da Computação — UFRN

[GitHub](https://github.com/Joao-2507) |
[Currículo Lattes](http://lattes.cnpq.br/7048388853999078)

