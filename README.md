# Los Calipsos Sistema de Monitoreo de Cisterna

Prototipo académico que mide el nivel y la temperatura de un recipiente con agua, muestra alertas mediante LED y buzzer, y permite visualizar vehículos, ubicación y recorridos desde una plataforma web.

## Componentes principales

- Arduino Leonardo o Uno.
- Sensor ultrasónico HC-SR04.
- Sensor de temperatura DS18B20.
- Potenciómetro en A0 para ajustar la referencia.
- LED verde, amarillo y rojo, buzzer activo.
- Computadora con Chrome o Edge y celular con GPS.
- Firebase Authentication y Realtime Database.

## Ejecución rápida

1. Instalar en Arduino IDE las librerías `OneWire` y `DallasTemperature`.
2. Abrir `LosCalipsos_WebUSB.ino`, seleccionar la tarjeta y el puerto COM, y cargar el programa.
3. Copiar la configuración del proyecto Firebase en `firebase-config.js`.
4. Publicar las reglas de `database.rules.json` con el UID autorizado.
5. Abrir la web mediante HTTPS e iniciar sesión.
6. En el celular, registrar o elegir una placa y pulsar **Iniciar recorrido**; autorizar la ubicación.
7. En la computadora, elegir la misma placa para observar el mapa. Para leer el Arduino, cerrar el Monitor Serial y pulsar **Conectar Arduino**.

## Estados del nivel

- Verde: nivel bajo o recipiente casi vacío.
- Amarillo: nivel intermedio.
- Rojo y buzzer: nivel alto o recipiente lleno.

## Estructura sugerida

```text
arduino/       código INO
web/           panel y acceso del transportista
docs/          informe, diagramas y evidencias
tests/         registro de pruebas y errores
README.md      instrucciones del proyecto
```

## Seguridad y limitaciones

El montaje se prueba únicamente con agua. No debe colocarse electrónica común en gasolina, diésel ni otros combustibles. El GPS pertenece al celular y puede detenerse si el navegador pierde permisos, Internet o queda suspendido. No subir contraseñas, cuentas personales ni coordenadas privadas al repositorio.

## Equipo

- David Limachi Poma: integración y organización.
- Ronaldo Quispe Tarqui: plataforma web.
- Daniel Ruiz Vargas: pruebas y monitoreo.
- Flavio Zambrana Bacarreza: maqueta y conexiones.
- Integrante 5: pendiente de registrar.
- Integrante 6: pendiente de registrar, si corresponde.

## Repositorio

Enlace: `PENDIENTE_DE_COLOCAR`

Cada integrante debe realizar commits propios y describir su aporte. Antes de la entrega se deben adjuntar capturas o enlaces de la demostración, pruebas, bitácora y dos revisiones docentes.
