# 🤖 Proyectos Arduino — Soluciones Tecnológicas Escolares

Repositorio que reúne una serie de **proyectos escolares desarrollados con Arduino**, orientados a resolver problemas reales dentro de un establecimiento educacional mediante automatización, sensores y sistemas de alerta.

Los proyectos están pensados para ser desarrollados inicialmente como **prototipos y maquetas educativas**, utilizando componentes de bajo costo y herramientas de simulación como **Tinkercad**.

---

## 📋 Proyectos

| # | Proyecto                  | Área                           |
| - | ------------------------- | ------------------------------ |
| 1 | 🚨 Alerta Sísmica Arduino | Seguridad                      |
| 2 | 🚰 Lavamanos Inteligente  | Higiene y automatización       |
| 3 | 🔐 Cerradura Inteligente  | Seguridad y acceso             |
| 4 | 🔥 Detector de Humo       | Seguridad y prevención         |
| 5 | 🌱 EcoRiego               | Medioambiente y automatización |

---

# 🚨 1. Alerta Sísmica Arduino

Sistema diseñado para detectar **vibraciones fuertes** y generar una alerta sonora y visual.

### 🎯 Objetivo

Mejorar la seguridad dentro del establecimiento mediante un sistema capaz de detectar vibraciones y alertar a los usuarios.

### ⚙️ Funcionamiento

El sensor **SW-420** detecta vibraciones y envía la señal al Arduino Uno.

Cuando se detecta una vibración:

* 🔴 Se enciende el LED rojo.
* 🟢 Se apaga el LED verde.
* 🔊 Se activa el buzzer.

Cuando no existe vibración:

* 🟢 El LED verde permanece encendido.
* 🔴 El LED rojo permanece apagado.
* 🔇 El buzzer permanece desactivado.

### 🔧 Componentes

* Arduino Uno
* Sensor de vibración SW-420
* Buzzer
* LED rojo
* LED verde
* Resistencias de 220 Ω
* Protoboard
* Cables jumper

### 💻 Programación

El programa monitorea constantemente el sensor y cambia el estado de los LEDs y del buzzer dependiendo de la presencia de vibraciones.

### 💰 Costo estimado

**$9.700 – $12.600 CLP**

---

# 🚰 2. Lavamanos Inteligente Automatizado

Sistema de lavado de manos automático que permite activar el suministro de agua **sin tocar una llave**.

### 🎯 Objetivo

Mejorar la higiene y reducir el desperdicio de agua mediante automatización.

### ⚙️ Funcionamiento

Un sensor ultrasónico **HC-SR04** detecta la presencia de las manos.

Cuando las manos se encuentran dentro del rango configurado:

1. Arduino procesa la información.
2. Se activa el módulo relé.
3. El relé enciende la bomba.
4. La bomba suministra agua.

Cuando las manos se alejan, la bomba se apaga.

### 🔧 Componentes

* Arduino Uno o Nano
* Sensor ultrasónico HC-SR04
* Módulo relé de 1 canal
* Mini bomba de agua
* Manguera
* Recipiente para agua
* Protoboard
* Cables Dupont
* Fuente de alimentación

### 💻 Programación

Desarrollado mediante **Arduino IDE utilizando C/C++**.

El programa mide continuamente la distancia detectada por el HC-SR04 y controla la bomba según el rango configurado.

---

# 🔐 3. Cerradura Inteligente — Smart Lock

Sistema de control de acceso mediante **clave numérica**, servomotor y pantalla LCD.

### 🎯 Objetivo

Mejorar la seguridad de salas, laboratorios y espacios donde se almacenan equipos tecnológicos.

### ⚙️ Funcionamiento

El usuario introduce una clave mediante un **teclado matricial 4x4**.

Si la clave es correcta:

* ✅ Se muestra "Acceso Concedido".
* 🟢 Se enciende el LED verde.
* 🔓 El servomotor abre el mecanismo.
* ⏱️ La cerradura permanece abierta durante 5 segundos.

Si la clave es incorrecta:

* ❌ Se muestra "Clave Incorrecta".
* 🔴 Se enciende el LED rojo.
* 🔊 Se activa el buzzer.

### 🔧 Componentes

* Arduino Uno
* Teclado matricial 4x4
* Servomotor SG90
* Buzzer pasivo
* Pantalla LCD 16x2
* Módulo I2C
* LED verde
* LED rojo
* Resistencias de 220 Ω
* Protoboard
* Cables jumper

### 📚 Librerías

```cpp
#include <Keypad.h>
#include <Servo.h>
```

### 🧪 Simulación

El proyecto puede ser desarrollado y probado previamente mediante **Tinkercad**, antes de construir el prototipo físico.

---

# 🔥 4. Sistema de Detección Temprana de Humo

Sistema de monitoreo diseñado para detectar la presencia de humo o gases y generar una alerta.

### 🎯 Objetivo

Implementar un sistema educativo de prevención ante posibles situaciones de humo o amago de incendio.

### ⚙️ Funcionamiento

El sensor **MQ-2** monitorea constantemente la concentración de humo/gases.

Cuando el valor supera el umbral configurado:

* 🔴 Se activa el LED rojo.
* 🔊 Se activa el buzzer.
* 📺 La pantalla LCD muestra una advertencia.
* ⚠️ Se indica el estado de alerta.

En condiciones normales:

* 🟢 El LED verde permanece activo.
* 🔇 La alarma permanece apagada.

### 🔧 Componentes

* Arduino Uno o Nano
* Sensor MQ-2
* Buzzer
* LED rojo
* LED verde
* Pantalla LCD 16x2
* Módulo I2C
* Resistencias de 220 Ω
* Protoboard
* Cables jumper

### 💻 Lógica principal

```text
Leer sensor MQ-2
       ↓
¿Supera el umbral?
    ↙       ↘
  SÍ         NO
  ↓           ↓
Alarma      Estado
LED rojo    normal
LCD         LED verde
Buzzer
```

---

# 🌱 5. EcoRiego — Sistema de Riego Automatizado

Sistema de riego automático capaz de determinar cuándo una planta necesita agua.

### 🎯 Objetivo

Reducir el desperdicio de agua y automatizar el riego de áreas verdes, jardines o huertos escolares.

### ⚙️ Funcionamiento

El sensor de humedad mide constantemente las condiciones del suelo.

Cuando la humedad se encuentra por debajo del umbral establecido:

1. Arduino detecta que el suelo está seco.
2. Activa el módulo relé.
3. El relé enciende la bomba.
4. La bomba suministra agua.
5. La pantalla LCD muestra el estado del sistema.

Cuando el suelo presenta suficiente humedad, el sistema permanece en reposo.

### 🔧 Componentes

* Arduino Uno R3
* Sensor de humedad de suelo
* Módulo relé de 1 canal
* Mini bomba de agua
* Buzzer
* Pantalla LCD 16x2
* Módulo I2C
* Resistencias de 220 Ω
* Protoboard
* Cables jumper
* Manguera de silicona
* Depósito de agua
* Tierra y plantas para pruebas

### 💻 Lógica principal

```text
Leer humedad del suelo
        ↓
¿Suelo seco?
    ↙          ↘
  SÍ            NO
  ↓              ↓
Activar        Mantener
bomba          reposo
  ↓
Actualizar LCD
```

---

# 🛠️ Tecnologías utilizadas

* **Arduino UNO / Nano**
* **Arduino IDE**
* **C/C++**
* **Tinkercad Circuits**
* Sensores digitales y analógicos
* Actuadores
* Relés
* Servomotores
* Pantallas LCD
* Electrónica básica

---

# 🎓 Enfoque educativo

Estos proyectos están diseñados para desarrollar competencias relacionadas con:

* Programación de microcontroladores.
* Electrónica básica.
* Lectura de sensores.
* Control de actuadores.
* Automatización.
* Resolución de problemas reales.
* Diseño y construcción de prototipos.
* Trabajo colaborativo.
* Pensamiento lógico y algorítmico.

---

# 📁 Estructura recomendada del repositorio

```text
arduino-proyectos/
│
├── README.md
│
├── 01-alerta-sismica/
│   ├── alerta-sismica.ino
│   ├── README.md
│   └── img/
│
├── 02-lavamanos-inteligente/
│   ├── lavamanos-inteligente.ino
│   ├── README.md
│   └── img/
│
├── 03-cerradura-inteligente/
│   ├── cerradura-inteligente.ino
│   ├── README.md
│   └── img/
│
├── 04-detector-humo/
│   ├── detector-humo.ino
│   ├── README.md
│   └── img/
│
└── 05-ecoriego/
    ├── ecoriego.ino
    ├── README.md
    └── img/
```

---

# 👨‍🎓 Integrantes

Los integrantes de cada proyecto serán definidos por los respectivos equipos de trabajo.

| Proyecto              | Integrantes |
| --------------------- | ----------- |
| Alerta Sísmica        | Por definir |
| Lavamanos Inteligente | Por definir |
| Cerradura Inteligente | Por definir |
| Detector de Humo      | Por definir |
| EcoRiego              | Por definir |

---

# ⚠️ Aviso

Estos proyectos tienen un **propósito educativo y de prototipado**. Los sistemas de detección de humo, seguridad y alerta sísmica no deben considerarse reemplazos de sistemas profesionales certificados.

---

# 📄 Licencia

Proyecto desarrollado con fines **educativos y académicos**.

Puedes adaptar, modificar y mejorar los proyectos para actividades de aprendizaje, prototipado y experimentación con Arduino.
