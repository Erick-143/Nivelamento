# Radar de Estacionamento (Sensor de Ré) com Arduino
---

## O Problema
Ter noção de espaço ao estacionar é difícil e arriscado para o para-choque. Os carros modernos usam sensores ultrassônicos para medir a distância até os obstáculos e avisar o motorista com bipes e luzes que se intensificam com a proximidade. Nós vamos recriar exatamente a lógica desse sistema.

## O Que Você Vai Aprender
* **Controle de Saídas (Outputs):** Acender LEDs e gerar tons sonoros usando um Piezo (Buzzer).
* **Leitura de Entradas (Inputs):** Capturar dados do ambiente com um Sensor Ultrassônico.
* **Física no Código:** O sensor emite um som inaudível e "escuta" o eco. O código calcula a distância usando a equação $d = \frac{v \cdot t}{2}$ (onde a distância é a velocidade do som multiplicada pelo tempo, dividida por dois, já que o som precisa ir e voltar).
* **Lógica de Decisão:** Criar regras em programação C++ (`if` / `else if`) para mudar o comportamento do alarme dependendo da faixa de distância.
* **Monitor Serial:** Aprender a debugar o código lendo os valores em centímetros diretamente na tela.

---

##  Componentes Necessários (Tinkercad)
* 1x Placa Arduino Uno R3
* 1x Placa de Ensaio (Protoboard pequena)
* 1x Sensor Ultrassônico (Modelo HC-SR04 - versão de 4 pinos)
* 1x Piezo (Buzzer)
* 3x LEDs (1 Verde, 1 Amarelo, 1 Vermelho)
* 3x Resistores de 220 Ω (para proteger os LEDs)

---

## Guia de Montagem (Hardware)
1.  **Energia:** Conecte o pino `5V` do Arduino na linha positiva (+) da protoboard e o `GND` na linha negativa (-).
2.  **Sensor Ultrassônico:** * Pino `VCC` no positivo (+).
    * Pino `GND` no negativo (-).
    * Pino `Trig` (Gatilho) no pino digital **7** do Arduino.
    * Pino `Echo` (Eco) no pino digital **6** do Arduino.
3.  **LEDs (Sinalização Visual):**
    * Conecte o lado negativo (cátodo, perna reta) dos 3 LEDs na linha negativa da protoboard.
    * Conecte um resistor de 220 Ω no lado positivo (ânodo, perna torta) de cada LED.
    * Ligue o pino do LED **Verde** no pino digital **10**, o **Amarelo** no **9**, e o **Vermelho** no **8**.
4.  **Buzzer (Sinalização Sonora):**
    * Pino negativo no GND.
    * Pino positivo no pino digital **11** do Arduino.

---

## Código-Fonte (Software)
*Você cria a lógica*

---

## Como Rodar a Simulação
1. Crie uma conta gratuita no [Tinkercad](https://www.tinkercad.com/).
2. No painel, vá em **Projetos > Circuitos > Novo Circuito**.
3. Arraste os componentes do menu lateral e faça as ligações confome o **Guia de Montagem** acima.
4. Clique na aba **Código** (canto superior direito), mude a visualização de "Blocos" para "Texto" e cole o código-fonte deste repositório.
5. Clique no botão **Iniciar Simulação**. 
6. Clique em cima do Sensor Ultrassônico durante a simulação para mover a bolinha (que representa o obstáculo) e veja o seu sistema reagindo em tempo real!
