# Configuração do Ambiente de Desenvolvimento

## 1. Pré-requisitos

### 1.1. Na Máquina Local
- Node.js 18+
- npm 9+
- Git
- Conta na Vercel
- Acesso à VPS

### 1.2. Na VPS
- Docker e Docker Compose
- Portainer (via OrionSetup)
- N8N (via OrionSetup)
- Domínio configurado com SSL

## 2. Configuração Inicial

### 2.1. Clonar o Repositório
```bash
git clone https://github.com/VlumaOficial/agendvluma.git
cd agendvluma
```

### 2.2. Instalar Dependências
```bash
# Frontend
cd frontend
npm install

# Backend
cd ../backend
npm install
```

## 3. Configuração do Supabase

1. Criar um novo projeto no Supabase
2. Configurar autenticação
3. Criar tabelas necessárias
4. Obter as credenciais da API

## 4. Configuração da Vercel (Frontend)

1. Fazer deploy do frontend na Vercel
2. Configurar variáveis de ambiente
3. Configurar domínio personalizado
4. Configurar SSL

## 5. Configuração da VPS

### 5.1. Backend
1. Instalar Node.js e PM2
2. Configurar Nginx como reverse proxy
3. Configurar SSL com Let's Encrypt

### 5.2. N8N via OrionSetup
1. Acessar o Portainer
2. Verificar se o N8N está rodando
3. Configurar domínio e SSL
4. Configurar autenticação

## 6. Variáveis de Ambiente

Criar um arquivo `.env` baseado no `.env.example`:

```bash
cp .env.example .env
```

## 7. Iniciando o Desenvolvimento

### Frontend (Vercel)
```bash
cd frontend
npm run dev
```

### Backend (Local para desenvolvimento)
```bash
cd backend
npm run dev
```

## 8. Configuração do CI/CD

### 8.1. Vercel (Frontend)
- Configurar integração contínua
- Configurar deploy automático na branch `main`

### 8.2. Backend (VPS)
- Configurar ações do GitHub para deploy automático
- Configurar PM2 para gerenciamento de processos

## 9. Monitoramento

### 9.1. Frontend (Vercel)
- Usar o painel da Vercel para monitoramento
- Configurar alertas

### 9.2. Backend (VPS)
- Configurar PM2 para monitoramento
- Configurar logs
- Configurar alertas

## 10. Backup

### 10.1. Banco de Dados (Supabase)
- Configurar backup automático
- Testar restauração

### 10.2. Aplicação
- Manter backup do código no GitHub
- Manter backup das configurações da VPS

## Solução de Problemas Comuns

### Frontend não consegue acessar a API
- Verificar CORS
- Verificar se o backend está rodando
- Verificar as variáveis de ambiente

### Problemas com N8N
- Verificar logs do container
- Verificar se as portas estão abertas
- Verificar configuração do domínio

### Problemas com o Banco de Dados
- Verificar conexão com o Supabase
- Verificar permissões
- Verificar logs do Supabase
