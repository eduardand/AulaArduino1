# Ponderada Semana 01

Este projeto documenta o aprendizado do ambiente de desenvolvimento Arduino e na prática do circuito básico "Blink" (pisca-pisca) em duas partes: LED Interno (simulação do hardware físico) e LED Externo (simulação de circuito).

## Parte 1: Blink do LED Interno 

A Parte 1 demonstra o controle do LED embutido (`LED_BUILTIN`, que corresponde ao Pino 13 no Uno). A simulação foi usada como evidência.

###  Lógica Implementada

O programa utiliza a função `pinMode` para configurar o LED interno como uma **saída** (`OUTPUT`) e, em seguida, a função `digitalWrite` com uma cadência de tempo única no loop.

| Estado | Comando | Duração (Tempo X/Y) |
| :--- | :--- | :--- |
| **Ligado** | `digitalWrite(LED_BUILTIN, HIGH)` | 3000 milissegundos (3 segundo) |
| **Desligado** | `digitalWrite(LED_BUILTIN, LOW)` | 1000 milissegundos (1 segundo) |

### 🔗 Código da Parte 1

```cpp
const int ledPin = LED_BUILTIN; 

void setup() {
  pinMode(ledPin, OUTPUT);
  Serial.begin(9600);
}

void loop() {
  digitalWrite(ledPin, HIGH); 
  delay(1000); 

  digitalWrite(ledPin, LOW);  
  delay(500); 
}
```
## Parte 2
A Parte 2 foca na montagem do circuito externo, introduzindo o uso do Resistor de Limitação de Corrente.

O circuito foi montado no Tinkercad, conectando um LED externo a um pino digital (6).

###  Lógica Implementada
```cpp
int ledExterno = 6; 

void setup() {
  pinMode(ledExterno, OUTPUT); 
}

void loop() {
  digitalWrite(ledExterno, HIGH);
  delay(3000); 

  digitalWrite(ledExterno, LOW);
  delay(1000); 
}
```

## Links de entrega
Link do Projeto no Tinkercad (Blink Interno):
[Blink](https://www.tinkercad.com/things/56TSMnm1dt6-blink-interno)

(Blink Externo):
[Blink Externo](https://www.tinkercad.com/things/3SKuckeThWH-blink-externo)

Link do vídeo demosntrativo: [Vídeo de Demonstração](https://drive.google.com/file/d/13VW-Ag4GP6Rz6YUrFoQ_EsGijkVrhMNI/view?usp=sharing)