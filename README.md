# Caja-de-arena-PWM

Lugar para desarrollar un control PWM PID retroalimentado por un sensor de presión para el control de una bomba de desplazamiento positivo de CC.

## Requisitos de software

Se utilizan las siguientes bibliotecas de Arduino:

- [TFT_eSPI](https://github.com/Bodmer/TFT_eSPI) para manejar la pantalla TFT.
- **Wire** (incluida en el entorno de Arduino).

## Conexiones de hardware

- **ESP32 a BTS7960**
  - `LPWM_PIN` (GPIO16) → pin `L_PWM` del BTS7960
  - `L_EN_PIN` (GPIO17) → pin `L_EN` del BTS7960
  - Conectar la bomba a las salidas de potencia del BTS7960.
- **Pantalla TFT**
  - Cablear según la configuración de `TFT_eSPI` en `User_Setup.h` (SPI, `CS`, `DC`, `RST`, `MOSI`, `MISO`, `CLK`).

## Compilación para ESP32

1. Instalar el **Arduino IDE** (o PlatformIO) con soporte para ESP32.
2. Instalar la biblioteca **TFT_eSPI** desde el gestor de librerías.
3. Copiar el archivo `SRC` como `src/main.cpp` (o abrirlo como sketch `.ino`).
4. Seleccionar la placa *ESP32 Dev Module* y compilar el proyecto.
5. Subir el programa al ESP32 conectado con la configuración de pines indicada.

## Licencia

Este repositorio no incluye un archivo de licencia. Consulta con los autores antes de reutilizar o distribuir el código.
