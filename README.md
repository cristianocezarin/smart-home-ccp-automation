# 🏠 CCP Automation - Home Control System

![Status](https://img.shields.io/badge/Status-Publicado%20na%20Play%20Store-success)
![Plataforma](https://img.shields.io/badge/Plataforma-Android%20%7C%20ESP32%20%7C%20ESP8266-blue)
![Comunicação](https://img.shields.io/badge/Comunicação-HTTP%20%2F%20WiFi-orange)

## 📌 Visão Geral
O **CCP Automation** é um ecossistema completo de automação residencial (Hardware + Software + Aplicativo Mobile) publicado comercialmente na Google Play Store.

O projeto permite controlar dispositivos conectados a relés por meio de uma rede Wi-Fi local, sem depender de servidores externos em nuvem. A solução abrange o aplicativo mobile (front-end), o firmware dos microcontroladores e a integração com a montagem eletrônica (hardware).

## 💡 O Problema e a Solução
Muitas soluções de automação no mercado param de funcionar se a internet cair, pois dependem de servidores em nuvem. 

**A Solução:** Desenvolvi um sistema com comunicação direta e local (App <-> Microcontrolador) que garante:
*   **Baixíssima latência:** Resposta imediata aos comandos.
*   **Independência externa:** Funciona apenas com o roteador local, sem internet.
*   **Custo acessível:** Utiliza componentes de baixo custo (ESP32/ESP8266 e módulos relés).

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
Componentes Principais
Camada	Tecnologia / Componente
Aplicativo Mobile	Android (MIT App Inventor)
Firmware	C++ (Arduino IDE)
Microcontroladores	ESP32 e ESP8266 / NodeMCU
Comunicação	HTTP sobre Wi-Fi local
Saídas	Portas digitais e Módulos de Relé
🚀 Funcionalidades Principais
☑ Controle individual de até 11 portas digitais (On/Off).
☑ Personalização visual de ícones e nomes dos dispositivos.
☑ Configuração dinâmica de IP (Conexão local).
☑ Programação de Timers (Hora de início/fim e dias da semana).
☑ Acionamento de lâmpadas, portões, ventiladores e câmeras.
☑ Pacote comercial com manual de instalação e diagramas.
📱 Publicação Comercial
O aplicativo foi publicado na Google Play Store e é vendido como um pacote completo (App + Firmware + Tutorial de Montagem).

Link da Play Store: Clique aqui para acessar o App

🎥 Demonstração
https://img.youtube.com/vi/wjYDkZ-SsI0/0.jpg

📸 Interface do Aplicativo
https://cole_o_link_da_sua_imagem_aqui/
(Não esqueça de colocar o link da sua imagem que você subiu, no lugar de COLE_O_LINK...)

🔒 Código-Fonte e Materiais
Como este é um produto comercial, o código-fonte integral, os materiais comerciais e os detalhes de implementação podem não estar disponíveis publicamente. Este repositório funciona como uma apresentação técnica e documentação do produto.

🎓 Principais Aprendizados
Este projeto envolveu práticas essenciais de engenharia:

Desenvolvimento de interface mobile para controle de hardware.

Comunicação App <-> Microcontrolador via rede local.

Programação de ESP32 e ESP8266 em C++.

Modelagem de tarefas agendadas (Timers).

Publicação e manutenção na Google Play Store.

Integração entre software, firmware e componentes físicos.

👨‍💻 Autor
Cristiano Cezarino Pereira

GitHub: @cristianocezarin

YouTube: CCP Automation (ajuste o link se necessário)
