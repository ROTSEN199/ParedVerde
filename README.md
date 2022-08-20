# ParedVerde

# Autores
- Sergio Abisay Cervantes Sánchez.
- Nestor Emmanuel Briones Ramírez.

## Justificación 

En la vida diaria se puede encontrar que los espacios verdes dentro de los diferentes establecimientos escasean por la falta de espacio, la dificultad que genera la humedad de las areas verdes por el riego y por que en la velocidad en la que se vive diariamente resulta dificil mantener las plantas vivas y sanas.
Una de las razones por las que las plantas suelen no sobrevivir es que no recordamos el riego, las mejores horas para regarse y el sobre riego. Por ende es necesario ser más meticulosos.

## Objetivo

El riego proporciona a la planta el agua necesaria para su crecimiento y desarrollo. Dada la escasez de agua, es conveniente para la planta pero también para la protección del medio ambiente, que el riego se aplique con la mayor eficiencia. Una de las alternativas para lograr este objetivo es la utilización de sistemas de riego con programación de autocontrol: se trata de sistemas que establecen la ejecución automática de riegos mediante la valoración continua de uno o varios parámetros de control.
Implementar un dispositivo que nos permita monitorear plantas dentro de un prototipo plano que se instale en la pared, aprovechando los espacios reducidos, el dispositivo nos permite estar calculando la humedad y la temperatura para automatizar el riego. Todo esto mediante la comunicación con la base de datos utilizada, al igual que también se usara la ESP32 para la conexión de internet.

## Descripción general
El proyecto monitoriza el cuidado de plantas en un entorno en el cual las plantas tendran tratos y cuidados en los que por medio de riego y la temperatura habiiente en la que se encuentran se tomaran datos en la aplicacion manejada por el telefono movil. 

- Identificar las variables ambientales a tener en cuenta para el riego adecuado de cultivos y la instrumentación requerida para el sistema de control de riego y monitoreo de variables ambientales. 
- Implementar un prototipo del sistema en las instalaciones de la Universidad.
- Diseñar el sistema de control, teniendo en cuenta los requerimientos del terreno y las necesidades de los usuarios y el sistema de monitoreo de variables desde una aplicación móvil.
El dispositivo contará con una aplicación, esta contará con:
1. Una página de inicio de sesión y registro de usuarios para que se logee el usuario y acceda a el demás contenido.
2. Contendra una pantalla la cual mediante tres opciones mostrará el estado de humedad y temperatura, y el registro de riego, así permitiendo un mejor control de riego.

## Material de uso  

|Componente|Imagen|Descripción|Cantidad|
|---|---|---|---|
|Raspberry pi| ![raspberry-pi-](https://user-images.githubusercontent.com/90642664/171302620-60e77d6f-04f1-4e92-abd3-60c3bd514649.jpg)| <p>***Especificaciones de la Raspberry Pi 4***<br><ol><li>Sistema en un chip: Broadcom BCM2711</li><li>CPU: Procesador de cuatro núcleos a 1,5 GHz con brazo Cortex-A72</li><li>GPU: VideoCore VI</li><li>Memoria: 1/2/4GB LPDDR4 RAM</li><li>Conectividad: 802.11ac Wi-Fi/Bluetooth 5.0, Gigabit Ethernet</li><li>Vídeo y sonido: 2 x puertos micro-HDMI que admiten pantallas de 4K@60Hz a través de HDMI 2.0, puerto de pantalla MIPI DSI, puerto de cámara MIPI CSI, salida estéreo de 4 polos y puerto de vídeo compuesto.</li><li>Puertos: 2 x USB 3.0, 2 x USB 2.0</li><li>Alimentación: 5V/3A vía USB-C, 5V vía cabezal GPIO</li><li>Expansión: Cabezal GPIO de 40 pines</li></ol></p> | 1 |
| Relay |![image](https://user-images.githubusercontent.com/90642664/184465280-6b5e043e-bead-453d-be36-2a0012164dbc.png)| <p><br><p><ol><li>El relé (en francés, relais 'relevo') es un dispositivo electromagnético. Funciona como un interruptor controlado por un circuito eléctrico en el que, por medio de una bobina y un electroimán, se acciona un juego de uno o varios contactos que permiten abrir o cerrar otros circuitos eléctricos independientes.</li></ol></p> | 1 |
|Bateria de 9V | ![image](https://user-images.githubusercontent.com/90642664/183945599-03857c21-9d43-4b82-8a62-0e7513a0f37c.png)| <p><ol><li>Las baterías consiguen convertir la energía química en eléctrica para poder poner en funcionamiento los aparatos que requieren de ellas para ser utilizados. El caso de las pilas de 9 voltios es el mismo.</li></ol></p> | 1 |
|Sensor de temperatura y humedad | ![sensor de temperatura](https://user-images.githubusercontent.com/90642664/171311674-c51042c7-e5e5-43f9-862f-56726043b1ab.jpg) | <p>***ESPECIFICACIONES TÉCNICAS***<br><ol><li>Voltaje de Operación: 3V - 5V DC</li>Rango de medición de temperatura: 0 a 50 °C</li><li>Precisión de medición de temperatura: ±2.0 °C</li><li>Resolución Temperatura: 0.1°C</li><li>Rango de medición de humedad: 20% a 90% RH.</li>Precisión de medición de humedad: 5% RH.</li><li>Resolución Humedad: 1% RH</li><li>Tiempo de sensado: 1 seg.</li><li>Interface digital: Single-bus (bidireccional)</li>Modelo: DHT11</li>Dimensiones: 16*12*5 mm.</li><li>Peso: 1 gr.</li><li>Carcasa de plástico celeste</li></ol></p>| 3 o 4 |
|Sensores de humedad de suelo|![sensor-de-humedad](https://user-images.githubusercontent.com/90642664/171305162-4179dc54-f8ce-475d-9491-5815a5954015.jpg)| <p><ol><li>Alta Precisión y Detección de Datos en Tiempo Real El sensor de temperatura funciona con el Hub gateway 2 a través de la aplicación "Mi Home", no puede funcionar por separado. (El control de la aplicación Homekit requiere el uso de Hub) Puede detectar las condiciones de temperatura, humedad y presión atmosférica en tiempo real, también puede ver los datos históricos en la aplicación. Rango de detección de temperatura y precisión - 20 ° C - + 60 ° C, +0.3 ° C</li><li>Alarma Automática Cuando detecta que la temperatura, la humedad y la presión atmosférica son anormales, enviará una notificación a su teléfono y activará la alarma de sirena intermitente local en el Hub</li><li>Tamaño Pequeño y Larga Vida útil Diseño pequeño de 3.6 * 3.6 * 0.9 cm con una cinta adhesiva, puede colocarlo en cualquier lugar que desee. El sensor de termómetro inteligente también viene con una celda de botón CR2032, diseño de ahorro de energía que ofrece 2 años de vida útil</li><li>Vida Inteligente y Cuidado de la Salud】 En combinación con otros dispositivos inteligentes mi, puede conectar el sensor con una salida inteligente. Si la humedad detectada es demasiado baja, puede encender el tomacorriente y encender el humidificador. Con el sensor en la habitación del bebé / niño, puede conocer oportunamente el cambio de temperatura de la humedad, brindarle a su hijo el cuidado y la protección más íntimos</li><li>Instalación y Prueba de Alcance Efectiva Solo presione el botón de reinicio en el dispositivo en la posición deseada. Si el concentrador hace mensajes de voz, indica que el dispositivo puede comunicarse efectivamente con el concentrador</li></ol></p>  | entre 3 y 4 |
|ESP32| ![ESP32](https://user-images.githubusercontent.com/90642664/171304942-8e8571fb-f99a-47b0-833b-af3abb0ba370.jpg)| <p>Las características del ESP32 incluyen bastantes por lo cual se añadieron solamente 2 de cada uno:</p><p>***Procesador:***<br> CPU: microprocesador de 32-bit Xtensa LX6 de doble núcleo (o de un solo núcleo), operando a 160 o 240 MHz y rindiendo hasta 600 DMIPS.<br>Co-procesador de ultra baja energía (ULP)</p><p>***Memoria:***<br>520 KiB SRAM</p><p>***Conectividad inalámbrica:***<br>Wi-Fi: 802.11 b/g/n<br>Bluetooth:v4.2 BR/EDR y BLE<br></p><p>***Interfaces periféricas:***<br>12-bit SAR ADC de hasta 18 canales<br>Seguridad:Soporta todas las características de seguridad estándar de IEEE 802.11, incluyendo WFA, WPA/WPA2 y WAPI<br>Arranque seguro</p><p>***Administración de energía:***<br>Regulador interno de baja caída<br>Dominio de poder individual para RTC</p>| 1 |
|Mini bomba de agua|![Mini bomba de agua sumergible](https://user-images.githubusercontent.com/90642664/171305127-7652ea60-741a-4e3a-87dc-d2b574467ebd.jpg)| <p>***ESPECIFICACIONES TÉCNICAS.<br><ol><li>Voltaje de funcionamiento: 2,5-6v DC.</li><li>Altura bombeo máx.: 40-110cm.</li><li>Caudal bombeo máx.: 80-120 l/h.</li><li>Diámetro salida Exterior: 7,5 mm.</li><li>Diámetro salida Interior: 5 mm.</li><li>Longitud cable: 20cm.</li><li>Tiempo continuo de trabajo de 500 horas.</li></ol></p>| 1 |.

## Diagrama inicial   
![Untitled Sketch_bb](https://user-images.githubusercontent.com/95454472/172226808-e73c491d-ef6f-4e07-a26a-0efc44457029.jpg)

#### Requerimientos.
| No.|Requerimientos funcionales|
|--|--------------------------|
|RF01|Tendra una maquetación accesible, con el fin de que si gusta mover su pared lo pueda hacer sin tanto problema|
|RF02|Para empezar a usar la app el usuario debera registrarse con su Nombre de usuario y Contraseña.|
|RF03|Una vez registrado, el usuario podra iniciar sesión para ver os datos de los sensores.|
|RF04|La aplicación debe permitir acceder a la plataforma utilizando Usuario y contraseña.|
|RF05|La aplicación debe permitir la actualización de los datos de los Usuarios. Así como el nombre de usuario y contraseña. |
|RF06|Nuestra aplicación guardara los datos en la base de datos de firebase.|
|RF07|La aplicación debe mostrar los datos del sensor de húmedad y sensor de temperatura.|
|RF08|La aplicación debe estar activa 24/7 todo el tiempo, además de contar con rapidez en sus procesos.|

|  No. |Requerimientos no funcionales|
|------|-----------------------------|
|RNF 01| Una vez el sensor de humedad detecte muy seca la tierra, la bomba se activara mediante 30 segundos para el riego.|
|RNF 02| Para la comunicación de los datos usaremos mosquitto v2.0.14 conectado con un broker donde estara conectado los dispositivos que enviaran la señal|
|RNF 03| Para las ordenes de las acciones de la bomba y el ventilador se haran mediante node-red, al igual que la comunicación con mosquitto. La versión usada en node-red es la v14.19.3|
|RNF 04| Usaremos la ESP32-WROOM-32 para subir el código de arduino |
|RNF 05|Las macetas en la parte de abajo tendran tubos de pvc para que reutilize la misma agua que caiga de las plantas.|
|RNF 06| La aplicación sera creada mediante app inventor.|
|RNF 07|La aplicación debera visualizarse y funcionar correctamente en tablets y celulares. |
|RNF 08|La aplicación se hara mediante un webview con el fin de que cualquier usuario le sea más fácil visualizar sus datos. |
|RNF 09|El sensor de temperatura se encargara de la temperatura ambiental. Para que así cuando este detecte muy caliente el clima active un mini ventilador para mantener frescas las plantas|
|RNF 10|El sensor de temperatura se encargara de la temperatura ambiental. Para que así cuando este detecte muy caliente el clima mande datos con sugerencias a la ESP32|
|RNF 11|Mediante el sensor de humedad monitoriara la humedad que contenga la tierra en la que estan las plantas con un gráfico en la aplicación. El cual estara conectado mediante node-red V|


## Diagrama de Clase de Uso
![image](https://user-images.githubusercontent.com/90642664/184923970-9f426d70-8692-4aa6-9502-ac21a753b430.png)

![image](https://user-images.githubusercontent.com/90642664/184926687-b54212ef-bc34-4277-9c7b-7f2b73f1dc9a.png)

![image](https://user-images.githubusercontent.com/90642664/184923162-7dc6d79e-9080-45f5-8e5d-756ef08159b4.png)

![image](https://user-images.githubusercontent.com/90642664/184923553-814cd74c-bab1-495b-8af2-9ccd83c49dbb.png)

## Planificación de Proyecto

https://trello.com/b/RLmiaqJo/primer-sprint

## Entidad_Relación

![image](https://user-images.githubusercontent.com/90642664/182158911-f4e9137d-9583-4117-a30f-fc0e70cd3d64.png)

## Prototipo de la maquetacion.
![Portotipo](https://user-images.githubusercontent.com/95454472/174725938-e7d3c37f-4162-4b8c-a555-7849abf5cd66.jpg)

## Conclusiones 

Las investigaciones revisadas a lo largo de este proyecto, evidencian una de las grandes problemáticas que se presenta a nivel Nacional y mundial. Como lo es el mal uso de la funtes hídricas y el desgate de mano de obra en pequeños productores agricultores, que no cuentan con un apoyo tegonologico para mantener la mano de obra y ahorrar agua. Se logró encender/apagar algún dispositivo por medio de teléfonos celulares, que a su vez posibilita la automatización del riego, en tiempo real, a partir de variables de suelo, clima y cultivo, con el fin de de alcanzar una mayor eficiencia en la aplicación del limitado recurso agua.

Se logró con éxito el monitoreo de la humedad de suelo, donde se puede visualizar en tiempo real los datos de la cantidad de humedad de suelo, así como será capaz de almacenar un registro de datos, además de esto también la temperatura en la que se encuentra el cultivo, esto también en tiempo real. Por último, se debe tener en cuenta que las tecnologías por si solas no resuelven todos los problemas, pero si se logra una implementación sistemática y coordinada de estas, pueden
ayudar a enfocarse por el camino correcto. Lo importante no es contar con la tecnología, sino aplicarla y utilizarla de la mejor manera, enfocándola a un problema real y concreto como por ejemplo, nuestra población Campesina que es la mas afectada
