# Azure IoT Hub (Ionternet of Things)

Nos dirigimos al portal de [Azure](https://portal.azure.com/#home)

## Paso 1
- Desde la vista home/inicio de Azure vamos al menú y seleccionamos "Todos los servicios".

![1](https://user-images.githubusercontent.com/99112892/177709568-79261094-efba-4807-95dd-522dfae23f00.png)

- Nos situamos en "Internet de las cosas" y dentro de sus opciones, elegimos "Centro de IoT(Iot Hub)".

![2](https://user-images.githubusercontent.com/99112892/177709631-f46d66eb-2965-450a-8799-109e19969dbe.png)

- Creamos el "Centro de IoT(Iot Hub)".

![3](https://user-images.githubusercontent.com/99112892/177709683-b71ab01e-79fe-4dec-bed0-00bc0778a902.png)


### Pestaña:Aspectos básicos(Basics)
- Suscripción: Azure for Students.
- Grupo de recursos: lab07-dr.

*Detalles de instancia*
 
- Nombre de IoT Hub: iot-datarangers22.
- Región: East US.
- Le damos click al boton "Siguiente:Redes".

![4](https://user-images.githubusercontent.com/99112892/177709778-cccfb718-5819-4528-adc4-53a542d463c4.png)

### Pestaña:Redes(Networking)
- Configuración de conectividad: Acceso público.
- Le damos click al boton "Siguiente:Administración".

![5](https://user-images.githubusercontent.com/99112892/177709825-784f0db4-0f7c-4cef-8a9b-7efc68bc3ba5.png)

### Pestaña:Administración(Management)
- Dejamos la configuración que tiene por default, para esta practica.
- Le damos click al boton "Siguiente:Etiquetas".

![6](https://user-images.githubusercontent.com/99112892/177709879-e5e55436-98b4-4818-9462-62d9a5d6b1be.png)

![7](https://user-images.githubusercontent.com/99112892/177709903-2a3d044b-59a9-4239-a3e6-9ae9b9a0c50f.png)

### Pestaña:Etiquetas(Tags)
- Llenamos los campos con la información que no ayude a saber por quien fue creado, cuando, etc.
- Le damos click al boton "Siguiente:Revisar y crear".

![8](https://user-images.githubusercontent.com/99112892/177709972-f75b5e81-0d0c-40e2-88ad-1ceb25062cc7.png)

## Paso 2
Ya implementado nuestro recurso, haremos uso de la simulación de una placa "Raspberry Pi", para ello utilizaremos [Raspberry Pi Azure IoT Online Simulator](https://azure-samples.github.io/raspberry-pi-web-simulator/) en donde podremos verificar la información del circuito que se reflejara en Iot Hub mediante la conexión bidericcional.

![9](https://user-images.githubusercontent.com/99112892/177710186-37811ab7-24eb-445f-ab2f-972a3a16af6c.png)

## Paso 3
- En Azure damos click en "Ir al recurso".

![10](https://user-images.githubusercontent.com/99112892/177710246-5a64cfbb-16c1-41d2-b043-b57302f1b6ee.png)

- Seleccionamos la opción "Dispositivos".

![11](https://user-images.githubusercontent.com/99112892/177710307-3ef2a1a9-eece-48e2-b597-88435372bb99.png)

- Agregamos nuestro dispositivo.

![12](https://user-images.githubusercontent.com/99112892/177710372-f54cb5a2-e2aa-442e-8d4d-fc0194e577a9.png)

- En esta ventana, solo modificare el apartado "Id. de dispositivo" y las otras opciones las dejare por default.
- Le damos "Guardar".

![13](https://user-images.githubusercontent.com/99112892/177710525-e655314e-41be-499d-8c74-7fc0733d20f5.png)

- Ya tenemos un dispositivo, lo seleccionamos.

![14](https://user-images.githubusercontent.com/99112892/177710590-cf9fb800-1e6e-42c7-831f-fbad8e1692df.png)

## Paso 4
- Dentro de las opciones que tiene el dispositivo "miRaspi" vamos a buscar la "Primary Connection String(Cadena de conexión principal)" y lo copiaremos.
Nos servira para establecer una conexión bidireccional entre el dispositivo y el servicio de Iot Hub en la nube.

![15](https://user-images.githubusercontent.com/99112892/177710755-46d51d03-4bcc-48b1-a1a2-9be901d64b5b.png)

- Regresaremos a la pagina de simulación de "la Raspberry pi".

Observaremos dos secciones en la pantalla, la primera mitad contiene un circuito que esta conformado por la placa que esta conectada a un sensor que permite leer la humedad de la temperatura y un led indicador rojo. La segunda mitad esta conformada por codigo en python que en terminos generales incluye todo lo que requiere para tener una comunicación continua con los servicios de la nube y el algoritmo para las distintas temperaturas sensadas.

![16](https://user-images.githubusercontent.com/99112892/177710920-1cbd8c8a-6d4b-4816-bd81-4171873e3bb4.png)

- Dentro de el código buscaremos la linea "connectionString" y borraremos todo lo que esta despues del igual, dentro de las comillas.

![17](https://user-images.githubusercontent.com/99112892/177710999-5fa75473-e403-4e0f-a7ed-aab0371de3fc.png)

- Pegaremos la "Primary Connection String" que habiamos copiado y le damos "Run".

![18](https://user-images.githubusercontent.com/99112892/177711068-48ae5d97-070d-43c2-be46-059bbb19b3f2.png)

- Nos informa que esta enviando mensajes al IoT Hub, como el led indicador prende y apaga.

![19](https://user-images.githubusercontent.com/99112892/177711127-985484cb-000f-4490-8911-cbccc1ae5e72.png)

Verificamos que en realidad se nos esten enviando esos mensajes en la interfaz de Iot Hub.
- Para eso, nos vamos a la información general(overview) de nuestro recuro.
- Checamos la sección de "Uso" y veremos las graficas indicadoras.

![20](https://user-images.githubusercontent.com/99112892/177711218-acaeed88-72a0-48d1-b091-6e967a169920.png)

![21](https://user-images.githubusercontent.com/99112892/177711259-b0317e8c-dbe4-4533-9318-9baf685492f0.png)

- En la página podemos ver los mensajes, que nos detallan la temperatura, humedad, etc.

![22](https://user-images.githubusercontent.com/99112892/177711344-11ce6924-3c8e-4c4d-b5c1-96c681343bcf.png)

- Detendremos la ejecución y eleminaremos el grupo de recursos.

![23](https://user-images.githubusercontent.com/99112892/177711402-537d2b32-6ff0-4e16-a112-7653a3b93aec.png)
