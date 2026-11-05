# 🏠 CCP Automation - Home Control System

![Status](https://img.shields.io/badge/Status-Publicado%20na%20Play%20Store-success)
![Plataforma](https://img.shields.io/badge/Plataforma-Android%20%7C%20ESP32%20%7C%20ESP8266-blue)
![Linguagem](https://img.shields.io/badge/Linguagem-C%2B%2B%20%7C%20MIT%20App%20Inventor-orange)

## 📌 Visão Geral
O **CCP Automation** é um ecossistema completo de automação residencial (Hardware + Software + Aplicativo Mobile) publicado comercialmente na Google Play Store. 

O sistema permite o controle local (via Wi-Fi) de dispositivos como lâmpadas, portões, câmeras e ar-condicionado, além de contar com um sistema de agendamento de tarefas (Timers) por dia da semana.

## 💡 O Problema e a Solução
A maioria das soluções de automação residencial no mercado depende de servidores em nuvem (se a internet cai, o sistema para) ou possui um custo elevado. 

**A Solução:** Desenvolvi um aplicativo Android que se comunica diretamente com o microcontrolador via rede local (IP), garantindo:
*   Baixíssima latência (resposta imediata).
*   Independência de internet externa (funciona apenas com o roteador local).
*   Baixo custo de implementação (utilizando ESP8266/ESP32).

## 🛠️ Tecnologias e Arquitetura
*   **Front-End (App Mobile):** Desenvolvido no MIT App Inventor (Android).
*   **Back-End (Firmware):** C++ programado via Arduino IDE.
*   **Hardware:** Microcontroladores ESP8266 (NodeMCU) e ESP32, Módulos Relés.
*   **Comunicação:** Protocolo HTTP (Rede Local / Wi-Fi).

## 🚀 Funcionalidades Principais
- [x] Controle individual de até 12 dispositivos (On/Off).
- [x] Personalização visual de ícones (lâmpadas, portões, câmeras, etc.).
- [x] Programação de Timers (Hora de ligar/desligar e dias da semana).
- [x] Configuração dinâmica de IP para conexão local.
- [x] Pacote comercial incluindo manual de instalação e diagramas elétricos.

## 📱 Publicação Comercial
O aplicativo foi publicado na **Google Play Store** e o pacote completo (App + Código Fonte + Tutorial de Montagem do Circuito) é vendido para entusiastas de automação.
*   **Link da Play Store:** [Clique aqui para acessar o App na Play Store](https://play.google.com/store/apps/details?id=appinventor.ai_cristiano_cta_pr.MasterAPP_ESP32_S)

## 📸 Galeria do Projeto
*[Interface do App CCP Automation](https://github.com/cristianocezarin/smart-home-ccp-automation/blob/main/WhatsApp%20Image%202026-09-25%20at%2020.35.30.jpeg)*

---
*Desenvolvido por Cristiano Cezarin (CCP Automation)*
