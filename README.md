# 🌦 Assistente de Eventos com Clima - n8n + IA + Twilio

## Descrição
Automação criada no n8n (orquestrador via Docker) que verifica o clima e envia um relatório curto por WhatsApp para indicar se é viável realizar um evento ao ar livre.

Tecnologias utilizadas
n8n (workflow automation)

## Docker
- Twilio (API WhatsApp)
- OpenWeatherMap API
- Groq (query language)

## Arquivos principais
- workflow-anon.json  — workflow anonimizado para importar no n8n
- .env.example        — exemplo das variáveis de ambiente
- docker-compose.yml  — para subir o n8n localmente
- .gitignore

## Como usar (resumo)
1. Copie `.env.example` → `.env` e preencha com suas chaves reais.
2. Rode `docker-compose up -d`.
3. Acesse `http://localhost:5678`, importe `workflow-anon.json`.
4. Configure as credenciais em *Credentials* (OpenWeatherMap, Groq, Twilio).
5. Ative o workflow e teste.

Importante: Não commite o arquivo .env pois ele está listado no .gitignore para proteger suas credenciais.

## O que aprendi
- Automação de workflows usando n8n e Docker
- Integração de APIs externas (OpenWeatherMap, Twilio)
- Configuração e gerenciamento de variáveis de ambiente de forma segura
- Conceitos de segurança evitando expor dados sensíveis no repositório
