# AnaMedis 🩺

> **Carteira digital de histórico clínico** — o prontuário do paciente organizado, confiável e disponível na tela do médico.

[![Live Demo](https://img.shields.io/badge/demo-anamedis.replit.app-0d9488?style=for-the-badge)](https://anamedis.replit.app)
[![Hackathon](https://img.shields.io/badge/Replit_%C3%97_startups.com.br-Hackathon_2026-7c3aed?style=for-the-badge)](https://hackathon-startups.replit.app)

---

## Sobre o projeto

O AnaMedis resolve um problema silencioso e cotidiano: **o paciente chega ao consultório sem os documentos certos**. Resultados de exames em papel, receitas perdidas, histórico fragmentado em vários sistemas. O médico recomeça do zero — e o paciente repete exames que já fez.

Com o AnaMedis, o paciente centraliza todo o seu histórico de saúde em um único lugar. Quando vai a uma consulta, **gera um código temporário** e compartilha exatamente o que quiser com o médico — com controle total sobre o que é exibido e por quanto tempo.

---

## Demo ao vivo

🔗 **[anamedis.replit.app](https://anamedis.replit.app)**

---

## Funcionalidades

### Para o paciente

| Tela | O que faz |
|---|---|
| **Início** | Painel com resumo do histórico, alertas de saúde e atalho rápido para gerar código |
| **Documentos** | Lista de laudos, exames e receitas com filtro por tipo |
| **Consultas** | Histórico de consultas com data, especialidade e resumo |
| **Compartilhar** | Geração de código `SAUDE-XXXX-XX` com temporizador de expiração |
| **Minha Saúde** | Métricas de saúde, alergias, medicamentos em uso e histórico familiar |
| **Perfil** | Dados pessoais, tipo sanguíneo e contato de emergência |
| **Dispositivos** | Conexão com wearables (relógio, cinta, outros apps) |
| **Acessos** | Log de quem acessou o histórico e quando |
| **Conta** | Configurações de segurança e notificações |
| **Assinatura** | Planos disponíveis |

### Para o médico

- Recebe o código do paciente
- Visualiza exatamente o que o paciente autorizou exibir
- Vê análise de IA com resumo dos dados relevantes para a consulta

---

## Fluxo principal

```
Paciente abre o AnaMedis
        ↓
Clica em "Gerar código para o médico"
        ↓
Sistema gera código único: SAUDE-XXXX-XX
        ↓
Código expira em 15 minutos
        ↓
Médico insere o código no terminal
        ↓
Acessa histórico autorizado + resumo de IA
```

---

## Stack técnica

- **Frontend:** HTML5 + Tailwind CSS (via CDN)
- **JavaScript:** Vanilla JS — SPA com renderização client-side via `innerHTML`
- **Estilo:** Design system próprio com tokens de cor teal/slate
- **Hospedagem:** Replit Static Pages
- **Repositório:** GitHub (`isaarauj0/anamedis`)

### Tokens de design

```
Sidebar background:  #111827
Nav item ativo:      #134e4a
Primary teal:        #0d9488
Hero gradient:       135deg → #134e4a → #0d9488 → #0891b2
Main background:     #f8fafc
```

---

## Estrutura do projeto

```
anamedis/
└── index.html   # Aplicação completa — 917 linhas, single-file SPA
```

---

## Como rodar localmente

```bash
# Clone o repositório
git clone https://github.com/isaarauj0/anamedis.git
cd anamedis

# Abra direto no navegador
open index.html
# ou
python3 -m http.server 8080
# → http://localhost:8080
```

Sem dependências de build. Sem `npm install`. Funciona offline.

---

## Dados de demonstração

A versão atual roda com dados simulados:

- **Paciente:** Maria Aparecida
- **Documentos:** 6 itens (laudos, exames, receitas)
- **Consultas:** 3 registros
- **Alertas:** Alergia a Dipirona e Penicilina
- **Medicamentos:** 2 em uso contínuo

---

## Hackathon

Este projeto foi desenvolvido para o **Hackathon Replit × startups.com.br 2026**.

> **Tema:** Construir um produto real, hospedado no Replit, que resolva um problema concreto.

**Tagline do projeto:**
> *"O histórico clínico do paciente organizado, confiável e disponível na tela do médico."*

---

## Próximos passos (roadmap)

- [ ] Autenticação real com biometria / Face ID
- [ ] Upload e OCR de documentos em PDF/foto
- [ ] Integração com laboratórios via API
- [ ] Conexão com sistemas hospitalares (HL7/FHIR)
- [ ] Versão mobile (PWA)
- [ ] Portal do médico com histórico persistente

---

## Licença

MIT © 2026 AnaMedis
