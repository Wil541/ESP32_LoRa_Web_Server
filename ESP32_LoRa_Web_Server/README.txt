# Silo Bag IoT System - Código do Emissor e Receptor

Este repositório contém o código para um sistema IoT que monitora um silo bag, incluindo sensores de temperatura, umidade e gás. O sistema é composto por dois componentes: o Emissor (SENDER) e o Receptor (RECEIVER). O Emissor envia dados para o Receptor usando comunicação LoRa.

## Componente Emissor (SENDER)

O componente Emissor é responsável por ler os sensores e enviar dados via LoRa. Ele consiste em:

- Sensor DHT11 para medição de temperatura e umidade.
- Sensor de gás (MQ-135) para detectar vazamentos de gás.
- Display OLED SSD1306 para exibir informações.
- Comunicação LoRa para enviar dados ao Receptor.

### Configuração

Antes de usar o componente Emissor, você deve configurar:

- Conexões de hardware (sensores, LoRa, display).
- Frequência de rádio (BAND) para comunicação LoRa.

### Funcionamento

O código do Emissor lê os sensores, verifica se há vazamentos de gás e envia os dados para o Receptor via LoRa. O estado do gás é exibido no display OLED.

## Componente Receptor (RECEIVER)

O componente Receptor é responsável por receber dados via LoRa e exibi-los em uma página da web. Ele consiste em:

- Comunicação LoRa para receber dados do Emissor.
- Display OLED SSD1306 para exibir informações.
- Um servidor web para exibir os dados em uma página.

### Configuração

Antes de usar o componente Receptor, você deve configurar:

- Conexões de hardware (LoRa, display).
- Frequência de rádio (BAND) para comunicação LoRa.
- Configurações da rede Wi-Fi (SSID e senha).

### Funcionamento

O código do Receptor aguarda a recepção de dados LoRa do Emissor. Quando os dados são recebidos, eles são exibidos na página da web e no display OLED. Os dados incluem temperatura, umidade, nivel de gás e informações de RSSI.

## Como Usar

1. Carregue o código do Emissor e do Receptor em dois dispositivos ESP32 separados.
2. Conecte os componentes de hardware conforme as instruções de configuração.
3. Acesse o servidor web do Receptor a partir de um navegador para visualizar os dados. (Certifique-se de que esteja conectados à mesma rede Wi-Fi)

### Observações

- O Emissor deve estar em um local próximo aos sensores e ao silo bag.
- O Receptor deve estar em um local com acesso à rede Wi-Fi.
- Certifique-se de configurar corretamente os pinos, conexões e credenciais de rede Wi-Fi nos códigos.

## Autor

Nome: [Willian Cardoso]
