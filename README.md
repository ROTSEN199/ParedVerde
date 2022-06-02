# ParedVerde

## Justificación 

En la vida diaria se puede encontrar que los espacios verdes dentro de los diferentes establecimientos escasean por la falta de espacio, la dificultad que genera la humedad de las areas verdes por el riego y por que en la velocidad en la que se vive diariamente resulta dificil mantener las plantas vivas y sanas.
Una de las razones por las que las plantas suelen no sobrevivir es que no recordamos el riego, las mejores horas para regarse y el sobre riego. Por ende es necesario ser más meticulosos.

## Objetivo

Implementar un dispositivo que nos permita monitorear plantas dentro de un prototipo plano que se instale en la pared, aprovechando los espacios reducidos, el dispositivo nos permite estar calculando la humendad y la temperatura para automatizar el riego.

## Descripción general

El dispotisivo contará con una aplicación donde mostrará el estado de humedad y temperatura, el registro de riego, permitiendo un control del mismo.

## Material de uso  //Sergio

|Componente|Imagen|Descripción|Cantidad|
|---|---|---|---|
|Raspberry pi| ![raspberry-pi-](https://user-images.githubusercontent.com/90642664/171302620-60e77d6f-04f1-4e92-abd3-60c3bd514649.jpg)| <p>***Especificaciones de la Raspberry Pi 4***<br><ol><li>Sistema en un chip: Broadcom BCM2711</li><li>CPU: Procesador de cuatro núcleos a 1,5 GHz con brazo Cortex-A72</li><li>GPU: VideoCore VI</li><li>Memoria: 1/2/4GB LPDDR4 RAM</li><li>Conectividad: 802.11ac Wi-Fi/Bluetooth 5.0, Gigabit Ethernet</li><li>Vídeo y sonido: 2 x puertos micro-HDMI que admiten pantallas de 4K@60Hz a través de HDMI 2.0, puerto de pantalla MIPI DSI, puerto de cámara MIPI CSI, salida estéreo de 4 polos y puerto de vídeo compuesto.</li><li>Puertos: 2 x USB 3.0, 2 x USB 2.0</li><li>Alimentación: 5V/3A vía USB-C, 5V vía cabezal GPIO</li><li>Expansión: Cabezal GPIO de 40 pines</li></ol></p> | 1 |
|Sensores de temperatura|![infrarrojos-sin-contacto-sensor-temperatura-termopila](https://user-images.githubusercontent.com/90642664/171306773-0cac1e63-c131-40b0-aae6-fee378396b77.jpg)| <p>**Sensor de Temperatura por Radiación de Infrarrojos**<br><p><ol><li>Estos compactos sensores son económicos per de alta calidad, tienen la capacidad de medir la variación de la temperatura en materiales y objetos en movimiento o con dificultad de acceso, son consistentes precisos y oportuna respuesta en el tiempo.</li><li>Tienen un rango de medición considerable, ya que pueden registrar valores que van desde los 200º centígrados hasta los -20 ºC, además suelen ser muy compatibles con vaios tipos de instrumentos.</li></ol></p> | 2 o tal vez 3|
|Sensor de temperatura y humedad | ![sensor de temperatura](https://user-images.githubusercontent.com/90642664/171311674-c51042c7-e5e5-43f9-862f-56726043b1ab.jpg) | <p>***ESPECIFICACIONES TÉCNICAS***<br><ol><li>Voltaje de Operación: 3V - 5V DC</li>Rango de medición de temperatura: 0 a 50 °C</li><li>Precisión de medición de temperatura: ±2.0 °C</li><li>Resolución Temperatura: 0.1°C</li><li>Rango de medición de humedad: 20% a 90% RH.</li>Precisión de medición de humedad: 5% RH.</li><li>Resolución Humedad: 1% RH</li><li>Tiempo de sensado: 1 seg.</li><li>Interface digital: Single-bus (bidireccional)</li>Modelo: DHT11</li>Dimensiones: 16*12*5 mm.</li><li>Peso: 1 gr.</li><li>Carcasa de plástico celeste</li></ol></p>| 3 o 4 |
|Sensores de humedad de suelo|![sensor-de-humedad](https://user-images.githubusercontent.com/90642664/171305162-4179dc54-f8ce-475d-9491-5815a5954015.jpg)| <p><ol><li>Alta Precisión y Detección de Datos en Tiempo Real El sensor de temperatura funciona con el Hub gateway 2 a través de la aplicación "Mi Home", no puede funcionar por separado. (El control de la aplicación Homekit requiere el uso de Hub) Puede detectar las condiciones de temperatura, humedad y presión atmosférica en tiempo real, también puede ver los datos históricos en la aplicación. Rango de detección de temperatura y precisión - 20 ° C - + 60 ° C, +0.3 ° C</li><li>Alarma Automática Cuando detecta que la temperatura, la humedad y la presión atmosférica son anormales, enviará una notificación a su teléfono y activará la alarma de sirena intermitente local en el Hub</li><li>Tamaño Pequeño y Larga Vida útil Diseño pequeño de 3.6 * 3.6 * 0.9 cm con una cinta adhesiva, puede colocarlo en cualquier lugar que desee. El sensor de termómetro inteligente también viene con una celda de botón CR2032, diseño de ahorro de energía que ofrece 2 años de vida útil</li><li>Vida Inteligente y Cuidado de la Salud】 En combinación con otros dispositivos inteligentes mi, puede conectar el sensor con una salida inteligente. Si la humedad detectada es demasiado baja, puede encender el tomacorriente y encender el humidificador. Con el sensor en la habitación del bebé / niño, puede conocer oportunamente el cambio de temperatura de la humedad, brindarle a su hijo el cuidado y la protección más íntimos</li><li>Instalación y Prueba de Alcance Efectiva Solo presione el botón de reinicio en el dispositivo en la posición deseada. Si el concentrador hace mensajes de voz, indica que el dispositivo puede comunicarse efectivamente con el concentrador</li></ol></p>  | entre 3 y 4 |
|ESP32| ![ESP32](https://user-images.githubusercontent.com/90642664/171304942-8e8571fb-f99a-47b0-833b-af3abb0ba370.jpg)| <p>Las características del ESP32 incluyen bastantes por lo cual se añadieron solamente 2 de cada uno:</p><p>***Procesador:***<br> CPU: microprocesador de 32-bit Xtensa LX6 de doble núcleo (o de un solo núcleo), operando a 160 o 240 MHz y rindiendo hasta 600 DMIPS.<br>Co-procesador de ultra baja energía (ULP)</p><p>***Memoria:***<br>520 KiB SRAM</p><p>***Conectividad inalámbrica:***<br>Wi-Fi: 802.11 b/g/n<br>Bluetooth:v4.2 BR/EDR y BLE<br></p><p>***Interfaces periféricas:***<br>12-bit SAR ADC de hasta 18 canales<br>Seguridad:Soporta todas las características de seguridad estándar de IEEE 802.11, incluyendo WFA, WPA/WPA2 y WAPI<br>Arranque seguro</p><p>***Administración de energía:***<br>Regulador interno de baja caída<br>Dominio de poder individual para RTC</p>| 1 |
|Mini bomba de agua|![Mini bomba de agua sumergible](https://user-images.githubusercontent.com/90642664/171305127-7652ea60-741a-4e3a-87dc-d2b574467ebd.jpg)| <p>***ESPECIFICACIONES TÉCNICAS.<br><ol><li>Voltaje de funcionamiento: 2,5-6v DC.</li><li>Altura bombeo máx.: 40-110cm.</li><li>Caudal bombeo máx.: 80-120 l/h.</li><li>Diámetro salida Exterior: 7,5 mm.</li><li>Diámetro salida Interior: 5 mm.</li><li>Longitud cable: 20cm.</li><li>Tiempo continuo de trabajo de 500 horas.</li></ol></p>| 2 |.

## Historia de usuario Epicas
 
Yo como Innovador deseo que este proyecto nos permita ayudar al medio ambiente mediante los riegos automatizados para así mantener las áreas verdes para personas en un futuro, también se pretende cuidar el agua mediante el riego solamente en cierto tiempo mediante un sensor de temperatura que nos idicará el momento justo para el riego aprovechandoa las bajas temperaturas para evitar la rapida evaporación del agua.

Yo como Vegana deseo un dispositivo que me permita colocar plantas dentro del poco espacio que dispongo y poder mantenerlas vivas para así poder incluso cultivar diferentes especies que yo considere necesarias para empezar un huerto a futuro.

Yo como agricultor me gustaría tener el sistema de riego automático para que remota mente tener mis plantas  con el cuidado debido de agua.

Yo como trabajador con un horario muy volátil deseo aprovechar lugares pequeños en mi casa para plantar todo tipo de plantas y con el sistema de riego automatico poder estar seguro que en el momento en que me sea imposible regarlas no se vean perjudicadas.

## Diagrama inicial   //Nestor
<p>Diagrama de Conexion  con ESP-32 ![Untitled Sketch_bb](https://user-images.githubusercontent.com/95454472/171703028-4751b226-4028-4f2c-bdff-d85b3c5eb86f.jpg)</p>


## Prototipo  // Alma

## Mapa de historia de usuario  //Fer
