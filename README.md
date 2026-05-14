# Sistema Inteligente de Monitoramento Residencial com Arduino e Arquitetura ARM

[![License: Apache-2.0](https://img.shields.io/badge/License-Apache--2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Target: ARM Cortex-M0+](https://img.shields.io/badge/Target-ARM%20Cortex--M0%2B-orange.svg)]()
[![Platform: Arduino](https://img.shields.io/badge/Platform-Arduino-00979D.svg)]()

## 📝 Descrição do Projeto

Este projeto consiste no desenvolvimento de um sistema embarcado de alto desempenho para monitoramento e automação residencial. Utilizando a plataforma **Arduino Nano 33 IoT**, equipada com o microcontrolador **SAMD21 (ARM Cortex-M0+)**, o sistema integra múltiplos sensores para aquisição de dados ambientais em tempo real.

O diferencial acadêmico deste projeto reside na utilização da arquitetura **ARM de 32 bits** para o processamento de algoritmos de **Inteligência Artificial (Edge AI)** de baixa densidade, como lógica adaptativa de histerese e detecção de anomalias, permitindo uma gestão eficiente da iluminação, climatização e segurança patrimonial com baixa latência e alta precisão.

## 🚀 Funcionalidades Principais

- **Monitoramento de Climatização**: Aquisição de temperatura e umidade via sensor DHT22 com alta precisão.
- **Eficiência Energética**: Controle de iluminação inteligente baseado em luminosidade (LDR) e detecção de presença (PIR).
- **Segurança Patrimonial**: Detecção de intrusão com ativação automática de alarmes e logs de segurança.
- **IA Embarcada**: Algoritmos de processamento local que reduzem falsos positivos e otimizam o consumo energético.
- **Telemetria Serial**: Interface de usuário via terminal serial (115200 baud) para depuração e análise de dados em tempo real.

## 🛠️ Lista de Componentes

| Item | Componente | Função |
| :--- | :--- | :--- |
| **MCU** | Arduino Nano 33 IoT | Processamento central (ARM Cortex-M0+) |
| **Sensor 1** | DHT22 (AM2302) | Temperatura e Umidade Relativa |
| **Sensor 2** | Sensor PIR HC-SR501 | Detecção de Presença/Movimento |
| **Sensor 3** | LDR 5mm | Medição de Luminosidade Ambiente |
| **Atuador 1** | Módulo Relé 5V (2 Canais) | Controle de Lâmpadas e Ar Condicionado |
| **Atuador 2** | Buzzer Ativo/Passivo | Alerta Sonoro de Segurança |
| **Outros** | Resistores, Protoboard e Jumpers | Conexão e Proteção de Circuito |

## 📍 Pinagem Recomendada (Hardware)

| Componente | Pino Arduino | Tipo de Sinal |
| :--- | :--- | :--- |
| **DHT22** | D3 | Digital (One-Wire) |
| **PIR HC-SR501** | D2 | Digital (Interrupt-ready) |
| **LDR** | A0 | Analógico (ADC) |
| **Relé 01 (Luzes)** | D4 | Saída Digital |
| **Relé 02 (AC)** | D5 | Saída Digital |
| **Buzzer** | D6 | Saída PWM |

## ⚙️ Instalação e Execução

1.  **Pré-requisitos**: Tenha o [Arduino IDE](https://www.arduino.cc/en/software) instalado (versão 2.3.0 ou superior recomendada).
2.  **Gerenciador de Placas**: Vá em `Arquivo > Preferências`, adicione as placas via `Gerenciador de Placas` procurando por "Arduino SAMD Boards".
3.  **Bibliotecas Necessárias**: No Gerenciador de Bibliotecas, instale:
    -   `DHT sensor library` by Adafruit.
    -   `Adafruit Unified Sensor`.
    -   `WiFiNINA` (para conectividade IoT, se aplicável).
4.  **Upload**: Conecte o Arduino Nano 33 IoT ao PC, selecione a porta correta e clique em `Upload`.
5.  **Monitoramento**: Abra o **Monitor Serial** e configure a velocidade para **115200 baud**.

## 📂 Estrutura de Pastas

```text
├── assets/             # Imagens do circuito e logos
├── docs/               # Artigos Acadêmicos (PDF/Markdown)
├── simulation/         # Pseudocódigo e logs do Simulador ARM
├── src/                # Código fonte principal (.ino)
└── README.md           # Documentação do projeto
