# prueba
PROPUESTAS DE PROYECTOS ESCOLARES ARDUINO
Fichas Técnicas para Documentos de Google

Propuesta N.º 1: Alerta Sísmica Arduino
N.º de propuesta
1
Nombre del proyecto
Alerta Sísmica Arduino
Problema o necesidad
Mejorar la seguridad dentro del liceo mediante un sistema que detecte vibraciones fuertes y genere una alerta sonora y visual.
Aplicación
Podría utilizarse en salas de clases, laboratorios, talleres u otras dependencias del liceo para realizar una demostración educativa de detección de vibraciones.
Funcionamiento
El sensor de vibración detecta movimientos. Arduino Uno recibe la señal y, cuando detecta una vibración, activa el buzzer y el LED rojo. Cuando no hay vibración, mantiene encendido el LED verde y la alarma permanece apagada.
Arduino
Arduino Uno
Sensores
Sensor de vibración SW-420
Actuadores
Buzzer, LED rojo y LED verde
Otros componentes
Resistencias de 220 Ω, protoboard y cables jumper.
Materiales
Arduino Uno, sensor SW-420, buzzer, 1 LED rojo, 1 LED verde, resistencias de 220 Ω, protoboard y cables jumper.
Programación
El programa debe leer constantemente el sensor. Si detecta una vibración, debe apagar el LED verde, encender el LED rojo y activar el buzzer. Si no detecta vibración, debe mantener el LED verde encendido y la alarma apagada.
Viabilidad
Sí, es altamente viable. Es un proyecto de bajo costo y fácil implementación para el entorno escolar. Desglose estimado de componentes en pesos chilenos (CLP):
• Arduino Uno Rev3 (Compatible): $5.000 - $7.000 CLP
• Sensor de vibración SW-420: $1.200 - $1.800 CLP
• Buzzer pasivo/activo: $500 - $800 CLP
• LEDs (Rojo y Verde) + Resistencias 220Ω: $500 CLP
• Protoboard 400 puntos + Cables Jumper: $2.500 CLP
Costo total aproximado: $9.700 - $12.600 CLP. Accesible para presupuesto escolar o trabajo en equipo.
Integrantes
[Nombres de los integrantes del equipo]


Propuesta N.º 2: Lavamanos Inteligente Automatizado con Arduino
N.º de propuesta
2
Nombre del proyecto
Lavamanos Inteligente Automatizado con Arduino
Problema o necesidad
Permitir el lavado de manos sin necesidad de tocar una llave, ayudando a mejorar la higiene y evitar el desperdicio de agua en el liceo.
Aplicación
Baños de estudiantes, profesores y zonas de alimentación del liceo.
Funcionamiento
Un sensor detecta cuando una persona acerca las manos. La información es enviada al Arduino, que procesa los datos y activa una bomba de agua mediante un relé. Cuando las manos se alejan, la bomba se apaga.
Arduino
Arduino Uno o Arduino Nano
Sensores
Sensor ultrasónico HC-SR04 (detecta presencia y distancia de las manos)
Actuadores
Mini bomba de agua (impulsa el agua). Indicador opcional con LED o Buzzer.
Otros componentes
Módulo relé de 1 canal, protoboard, cables Dupont y fuente de alimentación.
Materiales
Arduino Uno o Nano, sensor HC-SR04, módulo relé, mini bomba de agua, mangueras, recipiente para agua, cables, protoboard y materiales de maqueta (cartón, plástico o madera).
Programación
Se programa en Arduino IDE (C/C++). Mide la distancia con el sensor HC-SR04 y, si las manos están dentro del rango establecido, activa el relé para encender la bomba.
Viabilidad
El proyecto es totalmente viable para realizar como maqueta escolar. Utiliza componentes comerciales de muy bajo costo y fácil adquisición en tiendas de electrónica locales.
Integrantes
[Nombres de los integrantes del equipo]


Propuesta N.º 3: Cerradura Inteligente (Smart Lock)
N.º de propuesta
3
Nombre del proyecto
Cerradura Inteligente (Smart Lock)
Problema o necesidad
Seguridad de uso y cuidado de las pantallas, además de la pérdida/olvido constante de llaves físicas en salas compartidas del liceo, generando interrupciones.
Aplicación
Puertas de salas con pantallas, laboratorios de computación y casilleros de profesores.
Funcionamiento
El usuario ingresa una clave numérica a través de un teclado matricial. Si coincide, el servomotor retrae el pestillo por 5 segundos y enciende un LED verde. Si es incorrecto, suena una alarma con el buzzer y se enciende un LED rojo.
Arduino
Arduino UNO
Sensores
Teclado matricial 4x4 (interfaz táctil / entrada digital)
Actuadores
Servomotor (SG90) y Buzzer pasivo
Otros componentes
Pantalla LCD 16x2 (con módulo I2C), 1 LED verde, 1 LED rojo, 2 resistencias de 220 Ω y protoboard con cables jumper.
Materiales
Maqueta de puerta con cartón, fuente de alimentación (batería 9V o adaptador de 5V), cables y protoboard.
Programación
Lee teclas con Keypad.h, compara con claveCorrecta, controla el servomotor mediante Servo.h (0° cerrado, 90° abierto) y muestra mensajes ('Acceso Concedido' / 'Clave Incorrecta') en la pantalla LCD.
Viabilidad
Muy alta. Todos los componentes son de bajo costo, altamente accesibles en el mercado local y 100% compatibles en Tinkercad para simulación previa.
Integrantes
[Nombres de los integrantes del equipo]


Propuesta N.º 4: Sistema de Detección Temprana de Humo y Alerta Escolar
N.º de propuesta
4
Nombre del proyecto
Sistema de Detección Temprana de Humo y Alerta Escolar
Problema o necesidad
Riesgo de incendios o amagos de fuego en zonas con material inflamable o de difícil supervisión constante en el liceo.
Aplicación
Laboratorios de computación, bodegas de almacenamiento, salas de clases y baños.
Funcionamiento
El sensor monitorea constantemente la concentración de humo/gases. Si supera un umbral seguro, activa un buzzer y un LED rojo intermitente, desplegando una advertencia de peligro en la pantalla LCD.
Arduino
Arduino UNO (o Arduino Nano)
Sensores
Sensor de humo y gas MQ-2
Actuadores
Buzzer pasivo/activo (alarma sonora) y LED rojo (indicador visual)
Otros componentes
Pantalla LCD 16x2 (con I2C), LED verde, resistencias de 220 Ω, potenciómetro 10k Ω (opcional) y protoboard.
Materiales
Cables jumper, caja protectora (impresa o cortada), cable USB o batería de 9V con conector jack.
Programación
Lee el valor analógico del sensor MQ-2. Si supera el límite fijado (if), activa la frecuencia del buzzer, enciende el LED rojo y escribe 'ALERTA HUMO' en el LCD. En estado normal mantiene LED verde activo.
Viabilidad
Altamente viable. Componentes económicos, ampliamente disponibles en el comercio local y compatibles con la plataforma de simulación Tinkercad.
Integrantes
[Nombres de los integrantes del equipo]


Propuesta N.º 5: (EcoRiego) Sistema de Riego Automatizado e Inteligente
N.º de propuesta
5
Nombre del proyecto
(EcoRiego) Sistema de Riego Automatizado e Inteligente
Problema o necesidad
Áreas verdes o jardines del liceo sufren por falta de riego constante, desperdicio de agua por riego manual ineficiente o descuido durante períodos de vacaciones.
Aplicación
Áreas verdes principales, jardineras del patio central y huertos escolares.
Funcionamiento
Mide constantemente la humedad de la tierra. Si el suelo está seco, activa una bomba de agua mediante un relé durante un tiempo determinado y muestra datos en el LCD. Si está húmedo, permanece en reposo.
Arduino
Arduino Uno R3
Sensores
Sensor de humedad de suelo (capacitivo o resistivo FC-28)
Actuadores
Mini bomba de agua sumergible (5V-12V) y Buzzer activo (alerta de tanque vacío)
Otros componentes
Módulo Relé de 1 canal (5V), pantalla LCD 16x2 con I2C, resistencias de 220Ω, protoboard y cables jumper (M-M, M-H).
Materiales
Manguera de silicona fina, depósito de agua (contenedor plástico), estructura o base protectora y tierra/plantas para pruebas.
Programación
Lee el valor analógico del sensor de humedad. Evalúa si está bajo el umbral crítico para enviar señal HIGH al relé, activar la bomba y actualizar la pantalla LCD con el estado actual.
Viabilidad
Totalmente viable. Componentes muy económicos, fáciles de conseguir y estándar en kits educativos de Arduino.
Integrantes
[Nombres de los integrantes del equipo]


