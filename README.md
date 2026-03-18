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

## 🔌 Guia de Montagem (Hardware)
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

# Desafio Web: Interface de Análise Termo-higrométrica

Este repositório contém as especificações para o desenvolvimento de um painel web estático. O objetivo é introduzir conceitos de desenvolvimento Front-end focados na visualização de dados de sensores (temperatura e umidade), preparando a base de interface para futuras integrações de hardware e software do laboratório.

##  Objetivo
Desenvolver a estrutura (HTML) e a estilização (CSS) de um dashboard de monitoramento. A página deve conter um cabeçalho de identificação e dois *cards* centrais exibindo valores representativos de Temperatura e Umidade.

## Requisitos de Ambiente
* **IDE:** [Visual Studio Code (VS Code)](https://code.visualstudio.com/).
* **Ambiente de Teste Local:** Instalar a extensão **Live Server** no VS Code para atualização automática do navegador durante o desenvolvimento.

## Competências Desenvolvidas
* **HTML5:** Estruturação semântica da página (`<header>`, `<main>`, `<div>`, `<p>`, `<h1>`).
* **CSS3:** Separação do escopo de apresentação e conteúdo. Aplicação de propriedades visuais e tipográficas.
* **Layout:** Aplicação do modelo **Flexbox** para alinhamento dinâmico e centralização de múltiplos elementos (*cards*) no DOM.

---

## Especificações do Projeto

### 1. Estruturação (HTML)
No arquivo `index.html`:
* Estruture um documento HTML5 válido.
* Realize a importação do arquivo `style.css` na tag `<head>`.
* Crie uma tag `<header>` contendo o título principal do dashboard.
* Crie um contêiner principal (`<main>` ou `<div>`) que englobará os dados.
* Dentro do contêiner, crie dois *cards* separados (`<div>`): um destinado à exibição da Temperatura (ex: 26°C) e outro para a Umidade (ex: 55%).

### 2. Estilização e Layout (CSS)
No arquivo `style.css`, implemente os seguintes requisitos visuais:
* **Contraste:** Defina uma cor de fundo para a página (`body`) que garanta contraste com os *cards* centrais.
* **Componentização:** Configure os *cards* de dados com uma cor de fundo distinta, aplicando `border-radius` (bordas arredondadas) e `box-shadow` (sombra) para criar hierarquia e separação visual do fundo.
* **Alinhamento:** Utilize `display: flex;` no contêiner principal. Configure as propriedades do Flexbox para alinhar os dois *cards* lado a lado e centralizá-los horizontal e verticalmente na tela.

---

##  Execução
1. Clone ou baixe este repositório.
2. Abra a pasta no VS Code.
3. Com o arquivo `index.html` ativo, inicie o **Live Server**. O navegador abrirá a porta local para visualização em tempo real das alterações.
