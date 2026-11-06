# 🏠 CCP Automation - Home Control System

![Status](https://img.shields.io/badge/Status-Publicado%20na%20Play%20Store-success)
![Plataforma](https://img.shields.io/badge/Plataforma-Android%20%7C%20ESP32%20%7C%20ESP8266-blue)
![Linguagem](https://img.shields.io/badge/Linguagem-C%2B%2B%20%7C%20MIT%20App%20Inventor-orange)

## 📌 Visão Geral
O **CCP Automation** é um ecossistema completo de automação residencial (Hardware + Software + Aplicativo Mobile) publicado comercialmente na Google Play Store. 

O projeto permite controlar dispositivos conectados a relés por meio de uma rede Wi-Fi local, sem depender de servidores externos em nuvem. A solução abrange o aplicativo mobile (front-end), o firmware dos microcontroladores e a integração com a montagem eletrônica (hardware).

## 💡 O Problema e a Solução
A maioria das soluções de automação residencial no mercado depende de servidores em nuvem (se a internet cai, o sistema para) ou possui um custo elevado. 

**A Solução:** Desenvolvi um aplicativo Android que se comunica diretamente com o microcontrolador via rede local (IP), garantindo:
*   **Baixíssima latência:** Resposta imediata aos comandos.
*   **Independência externa:** Funciona apenas com o roteador local, sem internet.
*   **Custo acessível:** Utiliza componentes de baixo custo (ESP8266/ESP32 e módulos relés).

## ⚙️ Arquitetura do Sistema

```text
+---------------------+          Wi-Fi / HTTP          +----------------------+
|  Aplicativo Android | -----------------------------> |   ESP32 ou ESP8266   |
|  (MIT App Inventor) | <----------------------------- | (Firmware em C++)    |
+---------------------+            respostas           +----------+-----------+
                                                                  |
                                                                  | sinais digitais
                                                                  v
                                                       +----------------------+
                                                       | Módulos de Relé e    |
                                                       | Dispositivos Elétricos|
                                                       +----------------------+
```

### Componentes Principais
| Camada | Tecnologia / Componente |
| :--- | :--- |
| **Aplicativo Mobile** | Android (MIT App Inventor) |
| **Firmware** | C++ (Arduino IDE) |
| **Microcontroladores** | ESP32 e ESP8266 / NodeMCU |
| **Comunicação** | HTTP sobre Wi-Fi local |
| **Saídas** | Portas digitais e Módulos de Relé |

## 🚀 Funcionalidades Principais
- [x] Controle individual de até 11 portas digitais (On/Off).
- [x] Personalização visual de ícones e nomes dos dispositivos.
- [x] Programação de Timers (Hora de ligar/desligar e dias da semana).
- [x] Configuração dinâmica de IP para conexão local.
- [x] Acionamento de lâmpadas, portões, ventiladores e câmeras.
- [x] Pacote comercial incluindo manual de instalação e diagramas elétricos.

## 📱 Publicação Comercial
O aplicativo foi publicado na **Google Play Store** e o pacote completo (App + Código Fonte + Tutorial de Montagem do Circuito) é vendido para entusiastas de automação.
*   **Link da Play Store:** [Clique aqui para acessar o App](https://play.google.com/store/apps/details?id=appinventor.ai_cristiano_cta_pr.MasterAPP_ESP32_S)

## 🎥 Demonstração
[![Assista ao vídeo do sistema funcionando](https://img.youtube.com/vi/wjYDkZ-SsI0/0.jpg)](https://youtube.com/shorts/wjYDkZ-SsI0?si=89hJTj7HKS-c9i2h)

## 📸 Galeria do Projeto
![Interface do App CCP Automation](https://github.com/cristianocezarin/smart-home-ccp-automation/blob/main/WhatsApp%20Image%202026-09-25%20at%2020.35.30.jpeg)

## 🔒 Código-Fonte e Materiais
Como este é um produto comercial, o código-fonte integral, os materiais comerciais e os detalhes de implementação podem não estar disponíveis publicamente. **Este repositório funciona como uma apresentação técnica e documentação do produto.**

## 🎓 Principais Aprendizados
Este projeto envolveu práticas essenciais de engenharia:
*   Desenvolvimento de interface mobile para controle de hardware.
*   Comunicação App <-> Microcontrolador via rede local.
*   Programação de ESP32 e ESP8266 em C++.
*   Modelagem de tarefas agendadas (Timers).
*   Publicação e manutenção na Google Play Store.
*   Integração entre software, firmware e componentes físicos.

---
**Autor:** Desenvolvido por Cristiano Cezarin (CCP Automation)
*   **GitHub:** [@cristianocezarin](https://github.com/cristianocezarin)
*   **YouTube:** [CCP Automation](https://youtube.com/shorts/wjYDkZ-SsI0)

* 📄 **Licença:**
Este repositório contém documentação e materiais relacionados ao projeto CCP Automation. Os direitos sobre o aplicativo, o código-fonte, a marca, os materiais comerciais e os demais componentes do produto permanecem com seus respectivos autores e proprietários.

