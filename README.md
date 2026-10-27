# Dio-Cyber
Auditoria de segurança e ataques de força bruta (FTP, SMB, Web) utilizando Kali Linux, Medusa e Hydra em ambiente controlado (Metasploitable 2).

# 🛡️ Bootcamp DIO - Cybersecurity: Auditoria de Força Bruta com Kali Linux

Este repositório contém a documentação e as evidências do projeto prático de auditoria de segurança desenvolvido durante o Bootcamp de Cybersecurity da DIO.

## 🎯 Objetivo
Simular cenários de ataque de força bruta e password spraying em um ambiente controlado, utilizando o **Kali Linux** e a ferramenta **Medusa**, além de validar a segurança de um formulário web (DVWA) com o **Hydra**. O objetivo é demonstrar o entendimento das fases de um teste de intrusão (PTES) e propor medidas de mitigação.

## 🖥️ Ambiente do Laboratório
- **Atacante:** Kali Linux (Live USB com persistência) - `192.168.0.105`
- **Reconhecimento/Apoio:** Ubuntu 26.04 LTS - `192.168.0.106`
- **Alvo:** Metasploitable 2 - `192.168.1.106`
- **Rede:** Isolada e roteada via firewall Fortigate.

## 🛠️ Ferramentas Utilizadas
- **Nmap:** Reconhecimento de portas e serviços.
- **Enum4linux:** Enumeração de usuários e políticas do Samba/SMB.
- **Medusa:** Ataques de força bruta (FTP e SMB).
- **Hydra:** Automação de tentativas de login no formulário web (DVWA).
- **HTML/CSS/JS:** Criação de um dashboard interativo para documentação e geração do relatório em PDF.

## 📊 Resultados Obtidos (Resumo)

| Serviço | Ferramenta | Técnica (MITRE ATT&CK) | Resultado |
| :--- | :--- | :--- | :--- |
| **FTP (21)** | Medusa | T1110.001 - Brute Force | ✅ Sucesso (`msfadmin:msfadmin`) |
| **SMB (445)** | Medusa | T1110.003 - Password Spraying | ✅ Sucesso (`msfadmin:msfadmin` com acesso ADMIN$) |
| **HTTP (80)** | Hydra | T1110 - Brute Force | ✅ Sucesso (`admin:password`) |

## 📄 Documentação Completa
- O relatório técnico completo, estruturado com o framework **PTES** e com todas as evidências e mitigações, está disponível no arquivo: **[Relatorio_Pentest_DIO.pdf](./Relatorio_Pentest_DIO.pdf)**.
- Os logs brutos das ferramentas estão na pasta `/logs`.

## 🛡️ Mitigação
O relatório detalha as recomendações de segurança, incluindo:
- Implementação de políticas de senhas fortes e bloqueio de contas (Account Lockout).
- Desativação do SMBv1 e aplicação do Princípio do Menor Privilégio.
- Uso de CAPTCHA, Rate Limiting e MFA em formulários web.

---
*Projeto desenvolvido para fins educacionais no Bootcamp DIO - Cybersecurity.*
