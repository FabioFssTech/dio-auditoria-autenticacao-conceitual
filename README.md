# 🧪 Estudo Conceitual Auditoria de Autenticação com Kali Linux e Medusa (DIO)

> ⚠️ **Aviso Ético**
> Este projeto é **estritamente educacional** e foi desenvolvido como **documentação conceitual**, sem execução prática de ataques.
> Os cenários descritos referem-se exclusivamente a **ambientes controlados e intencionalmente vulneráveis**, como Metasploitable 2 e DVWA.
> Não é permitido realizar testes de força bruta em sistemas reais sem autorização formal.

---

## 🎯 Objetivo do Projeto

Este projeto tem como objetivo **demonstrar o entendimento conceitual** sobre:
- Ataques de força bruta em serviços de autenticação;
- Uso do Kali Linux e da ferramenta Medusa em ambientes controlados;
- Principais riscos associados a credenciais fracas;
- Medidas de mitigação, prevenção e detecção;
- Relação desses ataques com a rotina de **Operações de Rede (NOC)**.

Não houve execução prática de ataques neste desafio, apenas **análise, estudo e documentação**.

---

## 🧰 Ferramentas e Ambientes Estudados

### 🔹 Kali Linux
Distribuição Linux voltada para testes de segurança e auditoria, amplamente utilizada para estudos defensivos e ofensivos em ambientes controlados.

### 🔹 Medusa
Ferramenta de auditoria de autenticação que realiza tentativas repetidas de login em serviços de rede.
Seu uso em ambientes de laboratório permite compreender:
- Como ataques de força bruta funcionam;
- Como serviços mal configurados se comportam;
- Como detectar padrões suspeitos de autenticação.

### 🔹 Metasploitable 2
Máquina virtual **intencionalmente vulnerável**, utilizada para treinamento em segurança da informação.
Nunca deve ser exposta a redes reais ou à internet.

### 🔹 DVWA (Damn Vulnerable Web Application)
Aplicação web vulnerável criada para estudo de falhas comuns de segurança, incluindo autenticação fraca e ausência de mecanismos de proteção.

---

## 🧱 Topologia do Laboratório (Conceitual)

- Duas máquinas virtuais (VMs):
  - Kali Linux (atacante/auditor)
  - Metasploitable 2 / DVWA (alvo)
- Rede isolada (Host-only ou rede interna)
- Ambiente sem acesso externo

Este isolamento garante que qualquer estudo permaneça seguro, controlado e ético.

---

## 🧪 Cenários Estudados (Conceitualmente)

### 🔐 1. Força Bruta em FTP
**Descrição:**
Serviços FTP sem limitação de tentativas permitem que ferramentas automatizadas testem diversas combinações de usuário/senha.

**Riscos:**
- Comprometimento de contas
- Vazamento de arquivos
- Uso do serviço como ponto inicial de ataque

---

### 🌐 2. Autenticação Web (DVWA)
**Descrição:**
Aplicações web sem:
- Rate limiting
- CAPTCHA
- Bloqueio após falhas
podem ser alvo de tentativas automatizadas de login.

**Riscos:**
- Acesso indevido
- Enumeração de usuários
- Comprometimento da aplicação

---

### 🗂️ 3. Password Spraying em SMB (Conceito)
**Descrição:**
Técnica que testa uma senha comum em múltiplas contas, reduzindo chances de bloqueio.

**Riscos:**
- Comprometimento silencioso
- Dificuldade de detecção sem correlação de eventos

---

## 🛡️ Mitigações Estudadas

As principais contramedidas contra ataques de força bruta incluem:

✅ Rate limiting  
✅ Atraso progressivo entre tentativas  
✅ Bloqueio temporário de contas  
✅ Uso de MFA (Autenticação Multifator)  
✅ Políticas fortes de senha  
✅ Desativação de serviços legados (ex.: FTP)  
✅ Monitoramento e correlação de eventos de autenticação  

---

## 📊 Visão Operacional (NOC)

Do ponto de vista de **Operações e Monitoramento**, ataques de força bruta podem ser identificados por:

- Pico de falhas de autenticação
- Tentativas repetidas em curto intervalo
- Variação de usuários ou serviços
- Horários incomuns de acesso

A atuação do NOC envolve:
- Registro de eventos
- Correlação de alertas
- Escalonamento conforme severidade
- Comunicação com times de segurança

---

## ✅ Conclusão

Este desafio permitiu compreender:
- Como ataques de força bruta funcionam;
- Por que ambientes mal protegidos são vulneráveis;
- A importância da prevenção e detecção;
- O papel essencial da operação (NOC) na identificação e resposta a incidentes de autenticação.

Mesmo sem execução prática, o estudo conceitual demonstra domínio dos temas, responsabilidade ética e entendimento do impacto operacional desses ataques.

---

## 👤 Autor
Fabio Santos  
Profissional de Tecnologia da Informação  
Foco em Operações de Rede (NOC)
``
---
Este projeto foi desenvolvido como estudo conceitual, com texto autoral, sem uso de comandos ou execução prática de ataques, focando em entendimento, mitigação e visão operacional.
---
