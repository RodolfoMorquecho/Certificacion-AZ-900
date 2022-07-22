# Inteligencia Artificial (Computer Vision)

## Paso 1
- Vamos abrir nuestro editor de código, en este caso usare Visual Studio Code.
- Crearemos un folder dentro del editor, lo llame "DataRangersCode".
- Dentro del folder guardaremos un archivo con la extensión ".ipynb" para que nos genere un cuaderno interactivo(cuaderno de jupyter).

![1](https://user-images.githubusercontent.com/99112892/180354638-23dfa68d-13a9-4341-81a7-26d842d26e25.png)

## Paso 2
Comenzaremos a trabajar sobre nuestro cuaderno interactivo:
- Vamos a poner el titulo del servicio que utilizaremos, para ello haremos uso de Markdown.

![2](https://user-images.githubusercontent.com/99112892/180354709-769ac6bf-03d0-46b2-9c41-e9e6679089bc.png)

## Paso 3
Como vimos el título del cuaderno, trabajaremos con Computer Vision de la seccion de Inteligencia Artificial de Azure, por le que debemos de ir al portal de [Azure](https://portal.azure.com/#home).
- Ingresaremos al menú y despues seleccionaremos "todos los servicios".

![3](https://user-images.githubusercontent.com/99112892/180354779-7c85ad41-1da2-4c19-a49d-09df36b803c8.png)

- Despues elegimos la categoría "AI + aprendizaje automático(machine learning)" y podremos encontrar "Computer Vision".

![4](https://user-images.githubusercontent.com/99112892/180354840-dde86896-786f-4cea-8cc7-a3bc99f2c397.png)

- Lo creamos

![5](https://user-images.githubusercontent.com/99112892/180354901-98bdb889-6a9d-4b0e-a8bc-5c79d5d9bea8.png)

### Pestaña:Aspectos básicos
- Suscripción: Azure for Students
- Grupo de recursos: cv-dr
*Detalles de la instancia*
- Región: East US
- Nombre: cvdr22
- Plan de tarifa: Free(20 Calls per minute, 5k Calls per month).
- Se marca la casilla, despues de revisar los terminos.
- Le daremos "Siguiente" hasta la pestaña de "Etiquetas".

![6](https://user-images.githubusercontent.com/99112892/180354956-2504223d-d5e9-42a0-96fd-6c273fa31cff.png)

### Pestaña:Etiquetas
- Creamos las etiquetas necesarias para saber quien esta creando el recurso y para que area o departamento.
- Le damos en "Revisar y Crear".

![7](https://user-images.githubusercontent.com/99112892/180355019-5d47d0b0-047d-4951-a1bc-7c86f82393e1.png)

Resumiendo lo que se realizo anteriormente, acabamos de crear un puente que va a permitir conectarnos a la computadora central de Microsoft que tiene instalados estos algoritmos ya predefinidos de "Computer Vision".

![8](https://user-images.githubusercontent.com/99112892/180355126-8fcc246c-e060-48dc-b4cc-bc8868c4986e.png)

- Le damos "ir al recurso".
Ya generado el puente para acceder a esos algoritmos, lo unico que necesitamos son las llaves o claves.
- Seleccionaremos "Claves y punto de conexión".
- Copiaremos la Clave 1.

![9](https://user-images.githubusercontent.com/99112892/180355184-1d0f730b-8129-4743-8936-90334f6b28d7.png)

## Paso 4
- Ya que tenemos acceso y claves para usar "Computer Vision" regresaremos a Visual Studio y usaremos la clave/credencial.
- Establecemos nuestras credenciales.
*Esto quiere decir, que el sistema ya sabe que cuando yo use la palabra "key" o "endpoint" me voy a poder conectar*.

![10](https://user-images.githubusercontent.com/99112892/180355246-bc7d63b1-c08c-495c-8419-9e6e9e728624.png)

- Añadimos una celda en la que instalaremos la biblioteca de Azure:

![11](https://user-images.githubusercontent.com/99112892/180355308-8cc710dd-b01c-4354-9f37-b584284984e4.png)

- En otra celda "Conectamos con azure", Linea 2: vamos a solicitar desde azure.cognitiveservices que necesitamos el servicio llamado"vision" que es en relación a "ComputerVision". Y tambien nos vamos a traer/importar el ComputerVision del cliente, porque es con el que voy a autenticar o verificar que soy yo.
- Linea 3: Como nos vamos a verificar, necesitamos usar los servicios "rest" de microsoft y dentro de ellos utilizaremos el de "authentication", al igual que importaremos "CognitiveServicesCredentials".
- Linea 5: Conectaremos con azure atraves de "ComputerVisionClient" y le pasaremos como parametros para establecer la conexión el "endpoint" y la "key" pero la llave la debemos pasar como parametro dentro de un tipo de credencial.

![12](https://user-images.githubusercontent.com/99112892/180355426-034b8e7e-94c5-49b3-84da-87648e190f31.png)

## Paso 5
Necesitamos una imagen que nos ayude a probar el algoritmo o funcionamiento de el servicio d "ComputerVision".
- Guardaremos dicha imagen en un folder llamado "vision", el cual a su vez esta dentro de otro folder llamado "data".

![13](https://user-images.githubusercontent.com/99112892/180355526-4a4767b1-47b9-4d8c-8ab3-81b62f4c90af.png)

## Paso 6
Agregaremos un archivo llamado "vision.py" al folder data, su función es mostrar descripciones de una imagen y así saber que es lo que contiene esa imagen, por lo que no nos sirve para realizar un analisis. Basicamente pone texto sobre la imagen para que sea mas sencillo de interpretarse el ejemplo.

![14](https://user-images.githubusercontent.com/99112892/180355608-5db3ccee-a3c1-4d5c-8108-1d0af760cf48.png)

## Paso 7
Dentro de una nueva celda:
- Importaremos el archivo "vision.py" en el cuaderno "LabsAI".
- Importaremos "os" que permite trabajar con partes del sistema operativo.
- Importaremos la biblioteca "%matplotlib inline".

### Obtenenos la imagen 
- Creamos una variable(image_path) que almacena la ubicación de la imagen.
- Creamos una variable con la que abrimos la imagen junto con los derechos correspondientes "open(image_path, "rb")".
- Creamos una variable(description) para obtener la descripción de la imagen.

Podriamos hacer una prueba para ver la descripción con lo que tenemos hasta ahora, solo que esa descripción no apareceria en la imagen, solo la podriamos ver como mensaje de salida.
- Pero ya que tenemos nuetro archivo "vision.py" podemos usar el metodo "show_image_caption" para que la descripción este implicita en nuestra imagen.

![15](https://user-images.githubusercontent.com/99112892/180355855-2ad66b67-85d7-4ad4-b64d-dfac6a01cbd1.png)

*Salida de nuestro codigo:*

![16](https://user-images.githubusercontent.com/99112892/180355920-22f90261-1167-4452-9f69-17e413bc21c2.png)

## Paso 8
- Haremos la prueba con otra imagen.

![17](https://user-images.githubusercontent.com/99112892/180355959-6200cbc8-849e-4324-80ad-29d5b8d5e99d.png)

## Paso 9
Ahora en lugar de solo realizar una descripción sobre la imagen, tambien vamos a hacer un analisis. 
Por lo que haremos las siguientes modificaciones en el código:

![18](https://user-images.githubusercontent.com/99112892/180356017-eaa21c38-2c4e-491b-b81a-54d7dc94fa33.png)

# Face API
## Paso 10
Ya que creamos un recurso con "computervision" y vimos como funciona, haremos lo mismo con "Face API",crearemos un recurso de ese servicio en Azure y lo trabajaremos en nuestro editor de código, de modo que utilizaremos la "key" y el "endpoint".
- Tambien instalaremos la biblioteca de FAce API.

![19](https://user-images.githubusercontent.com/99112892/180356321-dd926484-ffea-4dca-bf3d-a419eae6aee1.png)

![20](https://user-images.githubusercontent.com/99112892/180356341-dc571590-8507-4fd5-9765-5cb1e0ce79eb.png)

- Podemos copiar el codigo en el que conectamos en el servicio de computervision a azure ya que se hace de la misma forma en "Face API", en nuestro código solo sustituiremos la palabra "Face" por la palabra "ComputerVision".

![21](https://user-images.githubusercontent.com/99112892/180356422-d8af12ae-eee6-4639-8294-1d13e45cb76e.png)

Nuestra intención al utilizar este servicio,es que a partir de una imagen podamos detectar rostros, si es que los hay.
- Así como hicimos uso de un archivo "vision", tambien importaremos uno llamado "faces" el cual tendra un metodo que nos servira para dibujar rectangulos alrededor de los rosotros, señalandolos.

![22](https://user-images.githubusercontent.com/99112892/180356520-cdbf3304-6d22-4a46-b5b3-5ccfe63381cf.png)

![23](https://user-images.githubusercontent.com/99112892/180356540-11508cc7-93b6-438f-a5ff-23ae47e436ff.png)

- Nos traermos la segunda imagen que utilizamos en los ejemplos de "computervision" ya que tiene mas rosotros, la abriremos con los permisos de escritura correctos.
- Lo replicaremos con dos ejemplos mas, el segundo a parte de que nos enmarcara los rostros nos mostrara el id que tienen.
- El tercero enmarca el rostro y muestra un listado de emociones y cuales detecta.

![24](https://user-images.githubusercontent.com/99112892/180356619-4a14e028-f76e-48ed-9056-c9ea94d741c9.png)

![25](https://user-images.githubusercontent.com/99112892/180356635-4450ef84-88a7-4d49-9e6a-011db17b7fb8.png)

![26](https://user-images.githubusercontent.com/99112892/180356655-bd12c447-f123-4039-9b47-4496fccbecd0.png)

![27](https://user-images.githubusercontent.com/99112892/180356668-efec2e8a-c0fc-4dd8-9754-ea4ddbd0a4cd.png)



