# 🛡️ Projeto de Auditoria de Força Bruta: Kali Linux e Medusa

## 👤 Autor

* **Seu Nome/GitHub Username**: Gabriel matias
* **Desafio Original**: dio santander

## ✨ Descrição do Projeto

Este projeto consiste na implementação de um laboratório de segurança para simular e documentar ataques de **força bruta** contra serviços comuns (FTP, SMB e Web) utilizando o sistema operacional **Kali Linux** e a ferramenta **Medusa**.

O objetivo principal é exercitar a configuração de ambientes controlados, aplicar conhecimentos de *pentesting* e, crucialmente, propor medidas eficazes de **mitigação** para as vulnerabilidades exploradas.

---

## 🎯 Objetivos de Aprendizagem Atingidos

* [x] Compreensão de ataques de força bruta em diferentes serviços (FTP, Web, SMB).
* [x] Utilização do **Kali Linux** e do **Medusa** para auditoria de segurança em ambiente controlado.
* [x] Documentação de processos técnicos de forma clara e estruturada.
* [x] Reconhecimento de vulnerabilidades comuns e proposta de medidas de mitigação.
* [x] Utilização do GitHub como portfólio técnico.

---

## ⚙️ 1. Configuração do Ambiente de Testes

O ambiente foi configurado com duas Máquinas Virtuais (VMs) no VirtualBox, isoladas da rede externa para garantir a ética e a segurança dos testes.

### 1.1 Topologia de Rede

| Máquina Virtual | Sistema Operacional/Aplicação | Endereço IP (Host-Only) | Função |
| :--- | :--- | :--- | :--- |
| **VM Atacante** | Kali Linux | `192.168.56.10` | Execução do Medusa e Nmap. |
| **VM Alvo** | Metasploitable 2 | `192.168.56.20` | Alvo com serviços vulneráveis (FTP, SMB, DVWA). |

> **Nota**: As máquinas foram configuradas com adaptadores de rede **Host-Only** (Rede Interna) no VirtualBox, garantindo que o ataque ficasse restrito ao laboratório.

### 1.2 Reconhecimento Inicial (Nmap)

Antes dos ataques, foi realizado um *scan* inicial para confirmar os serviços ativos e as portas abertas na VM alvo.

**Comando:**

```bash
nmap -sV 192.168.56.20
