# 🏠 CCP Automation - Home Control System

![Status](https://img.shields.io/badge/Status-Publicado%20na%20Play%20Store-success)
![Plataforma](https://img.shields.io/badge/Plataforma-Android%20%7C%20ESP32%20%7C%20ESP8266-blue)
![Linguagem](https://img.shields.io/badge/Linguagem-C%2B%2B%20%7C%20MIT%20App%20Inventor-orange)

## 📌 Visão Geral
Sistema de automação residencial desenvolvido com aplicativo Android e microcontroladores ESP32/ESP8266. O projeto permite controlar dispositivos conectados a relés por meio de uma rede Wi-Fi local, sem depender de um servidor externo para executar os comandos.

O **CCP Automation** foi publicado na Google Play Store e desenvolvido como uma solução completa, envolvendo aplicativo mobile, firmware, comunicação em rede e montagem eletrônica.

## 💡 O Problema e a Solução
Soluções de automação residencial que dependem exclusivamente de serviços em nuvem podem deixar de responder quando a conexão com a internet é interrompida. O CCP Automation foi projetado para executar a comunicação diretamente entre o aplicativo e o microcontrolador dentro da rede local.

Essa abordagem oferece:
*   **Comunicação direta por Wi-Fi:** Baixa latência para comandos de acionamento.
*   **Independência:** Funcionamento sem dependência de uma conexão externa com a internet.
*   **Custo acessível:** Possibilidade de utilização com componentes de baixo custo (ESP32, ESP8266 e módulos de relé).

## 🚀 Funcionalidades
*   Controle individual de dispositivos conectados a portas digitais.
*   Acionamento de lâmpadas, portões, ventiladores, câmeras e outros equipamentos compatíveis com a instalação elétrica.
*   Personalização dos nomes e ícones dos dispositivos.
*   Configuração do endereço IP do microcontrolador.
*   Programação de tarefas por horário e dia da semana (Timers).
*   Controle local por meio da rede Wi-Fi.
*   Compatibilidade com placas ESP32 e ESP8266.

*(Nota: A quantidade de dispositivos controlados depende da placa, do firmware e da configuração elétrica utilizada. A versão publicada do aplicativo informa suporte a até 11 portas digitais).*

## ⚙️ Arquitetura do Sistema

```text
+----------------------+       Wi-Fi / HTTP       +----------------------+
|                      |  ---------------------> |                      |
|  Aplicativo Android  |                         |  ESP32 ou ESP8266    |
|  MIT App Inventor    |  <--------------------- |  Firmware em C++      |
|                      |       respostas         |                      |
+----------------------+                           +----------+-----------+
                                                               |
                                                               | sinais digitais
                                                               v
                                                     +----------------------+
                                                     | Módulos de relé e    |
                                                     | dispositivos elétricos|
                                                     +----------------------+
Componentes principais
Camada	Tecnologia ou componente
Aplicativo mobile	Android desenvolvido no MIT App Inventor
Firmware	C++ com Arduino IDE
Microcontroladores	ESP32 e ESP8266/NodeMCU
Comunicação	HTTP sobre Wi-Fi local
Saídas	Portas digitais e módulos de relé
🔄 Fluxo Básico de Funcionamento
O microcontrolador é conectado à rede Wi-Fi local.

O aplicativo recebe ou configura o endereço IP do dispositivo.

O usuário seleciona um dispositivo no aplicativo.

O aplicativo envia um comando ao microcontrolador pela rede local.

O firmware interpreta o comando e altera o estado da porta digital correspondente.

O módulo de relé aciona o equipamento conectado.

🔌 Requisitos de Hardware
A montagem pode variar de acordo com a aplicação, mas normalmente envolve:

Uma placa ESP32 ou ESP8266/NodeMCU.

Módulos de relé compatíveis com a tensão e a corrente da aplicação.

Fonte de alimentação adequada.

Roteador ou rede Wi-Fi local.

Dispositivos elétricos compatíveis com a instalação.

Cabos, conectores e materiais de montagem.

⚠️ Atenção: Instalações elétricas podem envolver risco de choque, curto-circuito e incêndio. A montagem de circuitos ligados à rede elétrica deve ser feita por uma pessoa qualificada, seguindo as normas de segurança aplicáveis. Nunca conecte cargas diretamente ao microcontrolador sem utilizar o circuito de acionamento adequado.

🛠️ Instalação e Configuração
Aplicativo
Instale o aplicativo pela Google Play Store.

Conecte o celular à mesma rede Wi-Fi do ESP32 ou ESP8266.

Informe no aplicativo o endereço IP do microcontrolador.

Verifique a conexão apresentada no aplicativo.

Configure os nomes, ícones e dispositivos que serão controlados.

Para automações, configure o horário de início, o horário de término e os dias da semana.

Firmware e Hardware
O firmware e o circuito devem ser configurados de acordo com a placa e o módulo de relé utilizados. Antes de publicar instruções definitivas, inclua neste repositório: o modelo exato da placa testada, o mapeamento das portas digitais, o diagrama de ligação, a versão da Arduino IDE utilizada, as bibliotecas necessárias, o procedimento para configurar a rede Wi-Fi e as limitações conhecidas do firmware.

📱 Publicação Comercial
O aplicativo foi publicado na Google Play Store e o pacote completo (App + Código Fonte + Tutorial de Montagem do Circuito) é vendido para entusiastas de automação.

🎥 Demonstração
https://img.youtube.com/vi/wjYDkZ-SsI0/0.jpg

📸 Galeria do Projeto
https://github.com/cristianocezarin/smart-home-ccp-automation/blob/main/WhatsApp%20Image%202026-09-25%20at%2020.35.30.jpeg

🔒 Código-Fonte e Materiais Proprietários
O CCP Automation foi publicado e comercializado como um produto completo. Por esse motivo, o código-fonte integral, os materiais comerciais e alguns detalhes de implementação podem não estar disponíveis publicamente neste repositório.

Este repositório funciona como uma apresentação técnica do projeto. Caso exemplos não proprietários sejam adicionados, eles serão organizados separadamente do produto comercial original.

📂 Organização do Repositório
text
smart-home-ccp-automation/
├── README.md
├── screenshots/
│   ├── app-overview.jpg
│   ├── device-control.png
│   ├── timer-configuration.png
│   └── ip-configuration.png
├── docs/
│   ├── architecture.md
│   ├── wiring-diagram.png
│   └── communication-protocol.md
├── examples/
│   └── http-command-example.md
└── LICENSE
🎓 Principais Aprendizados
Este projeto envolveu práticas importantes de desenvolvimento de software e sistemas embarcados:

Desenvolvimento de uma interface mobile para controle de hardware.

Comunicação entre aplicativo e microcontrolador por rede local.

Programação de placas ESP32 e ESP8266.

Controle de dispositivos por portas digitais e relés.

Modelagem de tarefas agendadas por horário e dia da semana.

Configuração de rede e identificação de dispositivos por endereço IP.

Publicação e manutenção de um aplicativo Android na Google Play Store.

Integração entre software, firmware e componentes físicos.

🔮 Próximas Melhorias
□ Publicar um diagrama de arquitetura mais detalhado.
□ Adicionar screenshots individuais das principais telas.
□ Documentar o protocolo de comunicação utilizado pelo firmware.
□ Adicionar exemplos de configuração para ESP32 e ESP8266.
□ Criar testes para validar comandos e estados dos dispositivos.
□ Substituir a configuração manual de IP por descoberta automática na rede local.
□ Avaliar autenticação e proteção dos comandos dentro da rede Wi-Fi.
□ Adicionar registro de eventos e tratamento de falhas de comunicação.
👨‍💻 Autor
Desenvolvido por Cristiano Cezarin.

GitHub: @cristianocezarin

YouTube: CCP Automation

LinkedIn: (Adicione o link do seu perfil aqui)

📄 Licença
Este repositório contém documentação e materiais relacionados ao projeto CCP Automation. Os direitos sobre o aplicativo, o código-fonte, a marca, os materiais comerciais e os demais componentes do produto permanecem com seus respectivos autores e proprietários.

Se você decidir disponibilizar parte do código como software livre, substitua esta seção por uma licença adequada, como MIT, Apache-2.0 ou GPL-3.0, e confirme que todos os arquivos publicados podem ser distribuídos sob essa licença.
