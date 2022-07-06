
## Paso 1
- Desde el la vista home/inicio de Azure vamos a "Crear un recurso".

![1](https://user-images.githubusercontent.com/99112892/177494980-85a862c7-c452-46b7-87d0-599451f285ca.png)

- Seleccionamos dentro de categorias: "Integración" y despues en "Aplicación lógica" le damos crear.

![2](https://user-images.githubusercontent.com/99112892/177495084-bc3aa7ab-7bcd-4668-977f-84fdba43a957.png)

### Pestaña:Datos basicos
- Nos aseguramos de que la suscripción es de tipo 'student'.
- Grupo de recursos: lab02.
*Detalles de instancia*
- Nombre de la aplicación lógica: lab06dr.
- Publicar: Flujo de trabajo.
- Región: East US.

![3](https://user-images.githubusercontent.com/99112892/177495403-bbc5c2c6-9bc1-48a8-ad34-f8740a918a86.png)

- Plan: Consumo(Recomendado para el nivel de entrada. Pague solo lo que el flujo de trabajo ejecute).
- Redundancia de zona: Deshabilitado.
- Le damos en "Revisar y crear".

![4](https://user-images.githubusercontent.com/99112892/177495528-4bcc828f-4288-49e9-a5c4-6a3ec5e04b13.png)

- Seleccionamos "Ir al recurso".

![5](https://user-images.githubusercontent.com/99112892/177495608-576c9014-47e0-43c6-82f8-3f94f99c12ab.png)

- Accederemos a la siguiente interfaz.

![6](https://user-images.githubusercontent.com/99112892/177495662-cae448b4-568d-4c0b-87db-2cdd9f365767.png)

## Paso 2
Para poner en funcionamiento un desencadenador, probaremos con la siguiente que nos alertara cuando se publica un tweet nuevo.
- Seleccionamos la logicApp de la interfaz.

![7](https://user-images.githubusercontent.com/99112892/177495768-a6df4317-a631-4a21-8b3a-9fbb34fe4bc7.png)

### Diseño de la LogicApp
- Cada que alguien publica un tweet, le doy en iniciar sesión.

![8](https://user-images.githubusercontent.com/99112892/177495854-11f3d150-5db3-4d04-9a2a-7a569371f0ab.png)

- Nombre de la conexión: tweets , e iniciamos sesión.

![9](https://user-images.githubusercontent.com/99112892/177495925-825bbd1a-357a-4f8d-97ec-dfd700228972.png)

- Nos pedira los datos de nuestra cuenta de twitter para poder vincularse.

![10](https://user-images.githubusercontent.com/99112892/177495989-fe515e43-bb65-4883-bbc7-575ceaf8eec9.png)

Queda vinculada, ahora solo necesitamos detallar mas el tipo de tweet.
- Le damos en "Continuar".

![11](https://user-images.githubusercontent.com/99112892/177496077-2f60bae3-412b-4fdf-ad28-3b36d2b7e31f.png)

- Recopilara los tweets con #Metallica y lo hara cada 2 min.
- Añadiremos un nuevo paso.

![12](https://user-images.githubusercontent.com/99112892/177496145-d60adf41-46a0-423f-a320-a774c84bbda7.png)

- Agregaremos una nueva acción, en este caso veremos una hoja de (sheets) que actualice un renglon.

![13](https://user-images.githubusercontent.com/99112892/177496347-84189cdf-a3df-44df-a610-f7bf05feefb7.png)

## Paso 3
- En el navegador iremos a googlesheets para usar una hoja de calculo que se vincule con mi logicApp.
- Creare una nueva hoja de calculo y la nombrare TweetsRaw.

![14](https://user-images.githubusercontent.com/99112892/177496422-f70988c5-d4e3-414e-8ef6-d5d086d5488d.png)

- Le pondremos campos a la hoja, para tener una mejor abstracción de los tweets que recopilara la logicApp.

![15](https://user-images.githubusercontent.com/99112892/177496532-8aedfb23-c1cc-4dc4-94be-f5861fc97d17.png)

## Paso 4
Regresaremos a terminar de configurar la logicApp en el portal de Azure.
- Elegiremos la oppción "Google Sheets" tambien puede aparecer como "Hojas de calculo".

![16](https://user-images.githubusercontent.com/99112892/177496637-e9dd6b90-8987-430f-b690-f6ed985037c4.png)

- Despues elegiremos "Insertar fila" e "Iniciar sesión".
- Me pedira que permita logearme con mi cuenta personal de Google, le daremos el permiso.

![17](https://user-images.githubusercontent.com/99112892/177496724-4a95b586-b9fa-4bc8-aab9-4959bcd6a93b.png)

Ahora nos pedira el nombre del archivo, nombre de la hoja de calculo y los parametros con los que clasificaremos a nuestros tweets, como los anteriores que definimos en la hoja.
- Archivo: /TweetsRaw
- Hoja de cálculo: Raw
- Añadiremos todos los parametros que nos aparecen.

![18](https://user-images.githubusercontent.com/99112892/177496835-af360942-2f16-4859-bfb9-24ebd267e566.png)

- Asignaremos el contenido dinamico al flujo de las filas de la hoja que le corresponden.
- Ya que se termino de diseñar la LogicApp le damos en "guardar".

![19](https://user-images.githubusercontent.com/99112892/177496900-a5968385-4f78-4be0-8724-1bc467daffa4.png)

## Paso 5
Tenemos el diseño finalizado, conectado y guardado. Esta listo para ser ejecutado.
- Presionamos "Ejecutar desencadenador".

![20](https://user-images.githubusercontent.com/99112892/177496992-c58a144c-d693-43f4-ab4e-8a0cca92d4b4.png)

![21](https://user-images.githubusercontent.com/99112892/177497019-ef7129d2-844f-4aa4-bb68-1b4815a92b5c.png)

## Paso 6
Ahora solo nos toca verificar en nuestra hoja de calculo las actualizaciones, en caso de no verlas reflejadas podemos actualizar la página.

![22](https://user-images.githubusercontent.com/99112892/177497108-948fa468-7424-4421-b2f0-6d9673039673.png)

- Si actualizamos(ejecutar de nuevo) veremos mas tweets recopilados, ya que le pusimos el tiempo de cada 2 minutos.

![23](https://user-images.githubusercontent.com/99112892/177497205-52899907-dc37-44ae-a220-79839e6f0822.png)

## Paso 7
- Eliminamos el grupo de recursos, a su vez eliminara las conexiones con twitter, googleShets, etc.

![24](https://user-images.githubusercontent.com/99112892/177497281-1b19a86b-a19b-43f3-9477-497702bd3620.png)


