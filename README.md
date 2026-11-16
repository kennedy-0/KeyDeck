# KeyDeck

**Dispositivo portátil de automação USB HID utilizando RP2040.**

## Sobre o projeto

O KeyDeck é um dispositivo desenvolvido com RP2040 que utiliza a funcionalidade USB HID para simular um teclado conectado ao computador.

O projeto possui uma interface própria com display OLED e botões físicos, permitindo navegar por um menu e executar diferentes funções programadas.

O objetivo é explorar conceitos de automação, programação embarcada, comunicação USB e desenvolvimento de interfaces físicas.

## Funcionalidades

- Emulação de teclado USB HID.
- Interface gráfica utilizando display OLED.
- Menu interativo com navegação por botões.
- Execução de funções personalizadas.
- Controle de ativação e desativação de funções.
- Possibilidade de expansão com novas funcionalidades.

## Hardware utilizado

| Componente | Descrição |
|---|---|
| Raspberry Pi Pico | Microcontrolador RP2040 |
| OLED SSD1306 | Display 128x64 |
| Botão 1 | Executar função selecionada |
| Botão 2 | Ativar/desativar função |
| Botão 3 | Navegar pelo menu |

## Ligações

| Componente | Pino RP2040 |
|---|---|
| OLED SDA | SDA |
| OLED SCL | SCL |
| Botão 1 | GPIO 20 |
| Botão 2 | GPIO 21 |
| Botão 3 | GPIO 22 |

O display utiliza comunicação I2C no endereço `0x3C`.

## Bibliotecas

- Wire
- Adafruit GFX
- Adafruit SSD1306
- PluggableUSBHID
- USBKeyboard

## Organização do código

O projeto utiliza funções independentes para organizar as funcionalidades.

- `setup()`: inicialização dos componentes.
- `loop()`: gerenciamento dos botões.
- `drawMenu()`: atualização da interface OLED.
- `carregando()`: tela inicial.
- `voltarMenu()`: retorno ao menu principal.
- `menuFunctions[]`: array de ponteiros para funções.

## Segurança

O KeyDeck foi desenvolvido para estudos de USB HID e automação em ambientes próprios e autorizados.

As funcionalidades devem ser utilizadas somente em computadores sob autorização do responsável.

Rotinas destrutivas, alterações indevidas no sistema operacional e execução massiva de comandos não fazem parte da versão segura do projeto.

## Objetivos de aprendizagem

- Programação em C++.
- Sistemas embarcados.
- Comunicação USB HID.
- Interface I2C.
- Manipulação de GPIO.
- Desenvolvimento de menus interativos.

## Status

Em desenvolvimento.

Novas funcionalidades e melhorias na interface serão adicionadas durante a evolução do projeto.

---

**KeyDeck — Hardware, automação e programação embarcada.**
