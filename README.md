# cybersecurity-phishing-lab
Laboratório prático de simulação de Credential Harvesting utilizando Kali Linux e Zphisher para estudos de Engenharia Social.

# 🛡️ Simulador de Credential Harvesting - Lab de Cibersegurança

## 📋 Visão Geral
Este projeto faz parte da formação de Cybersecurity da plataforma DIO. O objetivo é demonstrar a mecânica de um ataque de **Phishing** do tipo *Credential Harvesting* (colheita de credenciais), simulando a criação de uma página de login falsa para capturar dados de autenticação.

## 🎯 Objetivos de Aprendizagem
- Compreender a anatomia de um ataque de engenharia social.
- Manipular ferramentas de teste de intrusão em ambiente controlado (Kali Linux).
- Analisar a eficácia de diferentes ferramentas de clonagem de sites.
- Documentar processos técnicos para fins de auditoria e estudo.

## 🛠️ Stack Técnica
- **Sistema Operacional:** Kali Linux (VM)
- **Ferramenta de Ataque:** Zphisher
- **Serviço de Hospedagem:** Servidor local PHP (Porta 1111)
- **Dependências:** Git, PHP, Bash

## 🚀 Metodologia de Execução

### Passo a Passo:
1. **Setup do Ambiente:** Atualização do sistema e instalação de dependências necessárias via `apt`.
2. **Deploy da Ferramenta:** Clonagem do repositório Zphisher e execução do script de automação.
3. **Configuração do Alvo:** Seleção do template de login do Facebook e configuração do servidor em modo Localhost.
4. **Validação:** Acesso ao IP local via navegador e simulação de envio de credenciais.

## 🧠 Análise Técnica e Decisões
Durante a fase de implementação, foi testado inicialmente o **Social-Engineer Toolkit (SET)**. No entanto, observou-se que o servidor do Facebook implementa proteções de *Anti-Scraping* que impedem a clonagem em tempo real por scripts automatizados.

**Decisão Técnica:** Para contornar essa barreira, a ferramenta foi alterada para o **Zphisher**. 
**Justificativa:** O Zphisher utiliza templates estáticos pré-renderizados. Isso elimina a necessidade de fazer a requisição ao servidor real do alvo no momento do ataque, garantindo 100% de disponibilidade da página falsa e eficácia na captura dos dados via requisições HTTP POST.

## 📸 Evidências do Lab
| Etapa | Captura de Tela |
| :--- | :--- |
| **Configuração do Zphisher** | ![Configuração](./images/configuracao.png) |
| **Página de Login Falsa** | ![Página Falsa](./images/pagina_falsa.png) |
| **Captura de Dados (HIT)** | ![Captura](./images/captura_senha.png) |

## ⚠️ Isenção de Responsabilidade (Disclaimer)
Este repositório possui fins estritamente **educacionais**. A realização de ataques de phishing contra sistemas ou pessoas sem consentimento explícito é crime previsto na legislação brasileira (Lei Carolina Dieckmann) e em normas internacionais.
