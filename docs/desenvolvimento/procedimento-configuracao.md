# Procedimento de Configuração do Ambiente de Desenvolvimento

## 1. Configuração Inicial do Projeto

### 1.1. Estrutura de Pastas
```bash
# Criar estrutura de pastas
mkdir -p AgendVluma/{frontend,backend,docs,scripts}
```

### 1.2. Inicialização do Git
```bash
cd AgendVluma
git init
echo "node_modules/" >> .gitignore
echo ".env" >> .gitignore
echo ".next/" >> .gitignore
```

## 2. Configuração do Frontend (Next.js)

### 2.1. Criar Projeto Next.js
```bash
cd frontend
npx create-next-app@latest . --typescript --eslint --tailwind --src-dir --import-alias "@/*"
```

### 2.2. Dependências Adicionais
```bash
npm install @supabase/supabase-js @supabase/auth-helpers-nextjs @hookform/resolvers zod react-hook-form axios socket.io-client
```

## 3. Configuração do Backend (Node.js + Express)

### 3.1. Inicialização do Projeto
```bash
cd ../backend
npm init -y
npm install express typescript ts-node @types/node @types/express --save-dev
npx tsc --init
```

### 3.2. Dependências Principais
```bash
npm install @supabase/supabase-js cors dotenv express-validator jsonwebtoken socket.io
npm install --save-dev @types/cors @types/jsonwebtoken @types/node @types/express ts-node-dev
```

## 4. Configuração do Supabase

### 4.1. Criar Projeto
1. Acessar https://supabase.com
2. Criar novo projeto
3. Configurar banco de dados
4. Obter URL e chave anônima

### 4.2. Configurar Tabelas
```sql
-- Exemplo de tabela de usuários
CREATE TABLE users (
  id UUID REFERENCES auth.users NOT NULL,
  email TEXT NOT NULL,
  full_name TEXT,
  created_at TIMESTAMPTZ DEFAULT NOW(),
  updated_at TIMESTAMPTZ DEFAULT NOW(),
  PRIMARY KEY (id)
);
```

## 5. Configuração da Vercel

### 5.1. Deploy do Frontend
1. Conectar repositório na Vercel
2. Configurar variáveis de ambiente
3. Configurar domínio personalizado
4. Habilitar HTTPS

## 6. Configuração da VPS

### 6.1. Instalação do OrionSetup
1. Acessar a VPS via SSH
2. Executar script de instalação do OrionSetup
3. Configurar domínio e SSL

### 6.2. Configuração do N8N
1. Acessar o Portainer
2. Verificar instância do N8N
3. Configurar autenticação
4. Configurar webhooks

## 7. Variáveis de Ambiente

### 7.1. Frontend (.env.local)
```env
NEXT_PUBLIC_SUPABASE_URL=seu-projeto-supabase-url
NEXT_PUBLIC_SUPABASE_ANON_KEY=sua-supabase-anon-key
NEXT_PUBLIC_API_URL=https://api.seudominio.com
```

### 7.2. Backend (.env)
```env
NODE_ENV=development
PORT=3001
SUPABASE_URL=seu-projeto-supabase-url
SUPABASE_KEY=sua-supabase-service-role-key
JWT_SECRET=seu-jwt-secreto
```

## 8. Scripts Úteis

### 8.1. Iniciar Desenvolvimento
```bash
# Frontend
cd frontend
npm run dev

# Backend (em outro terminal)
cd backend
npm run dev
```

## 9. Verificações Finais

### 9.1. Frontend
- [ ] Acessar http://localhost:3000
- [ ] Verificar se a página carrega
- [ ] Verificar erros no console

### 9.2. Backend
- [ ] Acessar http://localhost:3001/health
- [ ] Verificar logs do servidor
- [ ] Testar conexão com o banco de dados

## 10. Solução de Problemas

### 10.1. Erros de Conexão
- Verificar se as portas estão abertas
- Verificar variáveis de ambiente
- Verificar logs de erro

### 10.2. Problemas com o Supabase
- Verificar credenciais
- Verificar permissões
- Verificar políticas de segurança

---
**Última Atualização**: 25/11/2025

Este documento deve ser atualizado sempre que houver mudanças significativas na configuração do ambiente.
