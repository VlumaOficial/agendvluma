# AgendVluma

Sistema de agendamento e CRM unificado para diversos segmentos, com foco em atendimento via WhatsApp e painel web responsivo.

## 🚀 Recursos Principais

- **Agendamento Inteligente**
  - Múltiplos canais de agendamento
  - Lembretes automáticos
  - Gestão de recursos (salas, equipamentos, profissionais)

- **Atendimento Híbrido**
  - Integração com WhatsApp Business
  - Chat em tempo real
  - Painel web responsivo

- **Conformidade LGPD**
  - Gestão de consentimento
  - Proteção de dados sensíveis
  - Relatórios de conformidade

## 📚 Documentação

- [Visão Geral do Projeto](/docs/projeto/visao-geral.md)
- [Requisitos](/docs/projeto/requisitos/funcionais.md)
- [Arquitetura](/docs/desenvolvimento/arquitetura.md)
- [LGPD e Privacidade](/docs/projeto/lgpd/politica-privacidade.md)

## 🛠️ Configuração do Ambiente

### Pré-requisitos

- Node.js 18+
- PostgreSQL 14+
- NPM 9+

### Instalação

1. Clone o repositório:
   ```bash
   git clone https://github.com/VlumaOficial/agendvluma.git
   cd agendvluma
   ```

2. Instale as dependências:
   ```bash
   # Backend
   cd src/backend
   npm install
   
   # Frontend
   cd ../frontend
   npm install
   ```

3. Configuração do ambiente:
   - Copie `.env.example` para `.env`
   - Configure as variáveis de ambiente necessárias

4. Inicie os serviços:
   ```bash
   # Em terminais separados
   cd src/backend && npm run dev
   cd src/frontend && npm run dev
   ```

## 🤝 Contribuição

1. Faça um Fork do projeto
2. Crie uma Branch para sua Feature
3. Adicione suas mudanças
4. Envie um Pull Request

## 📄 Licença

Este projeto está sob a licença [MIT](LICENSE).

## 📞 Contato

Equipe Vluma - contato@vluma.com.br

---

<div align="center">
  Desenvolvido com ❤️ por <a href="https://vluma.com.br">Vluma</a>
</div>
