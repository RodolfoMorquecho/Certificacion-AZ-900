# AZ900-VirtualMachine

Guía para crear un recurso y configurarlo para utilizar una Máquina virtual dentro de Azure.

Lo primero que debemos hacer, es dirigirnos al portal de [Azure](https://portal.azure.com/#home)

## Paso 1
En el menu seleccionamos la opcion "todos los servicios".

![1](https://user-images.githubusercontent.com/99112892/183571667-1e5cfcdc-841b-4135-8c57-a25977a536fa.png)

## Paso 2
En la sección categorias elegimos 'compute' y dentro de sus servivios encontramos las 'Máquinas virtuales'.

![2](https://user-images.githubusercontent.com/99112892/183571785-eadfc8de-85a1-455f-b14f-b3dc6c4b49fe.png)

## Paso 3
Nos dirigimos a la pestaña 'crear' y dentro de su desplegado de opciones elegimos 'Máquina virtual de Azure'.

![3](https://user-images.githubusercontent.com/99112892/183571834-98232ee3-200b-4355-a132-58f470465c4a.png)

## Paso 4
### Pestaña:Datos básicos
- Nos aseguramos de que la suscripción es de tipo 'student'.
- Creamos un nuevo grupo de recursos, el cual sería un folder donde vamos a guardar nuestra máquina virtual dentro de la nube, lo nombramos como: lab01_dr.
- Le damos un nombre a nuestra máquina virtual, en este caso la nombro: mv01-dr.
- En Región seleccionamos (US) Central US
- Las opciones de disponibilidad son para tener respaldada nuestra información en otro centro de datos en caso de que el primero falle,pero debido a que solo es una prueba no los requerimos.
- La seguridad se queda en 'Estándar'.
- Para la Imagen escogemos: Windows Server 2019 Datacenter - Gen2. El cual sera nuestro sistema operativo con el que trabajara la VM.

![4 ](https://user-images.githubusercontent.com/99112892/183571983-bea9b192-fbab-4fbc-94dd-be72360cb949.png)

- Seleccionamos un tamaño al que tengamos acceso considerando nuestro credito y requerimientos, para eso podemos ir a la pestaña ´ver todos los tamaños' y decidir el que nos convenga, para esta situación me decidí por el 'DS2' que esta dentro de 'Tamaños de generaciones anteriores'.

![4-5 _tamanio](https://user-images.githubusercontent.com/99112892/183572239-8dad80c7-83fb-4d60-883f-5eac1868556b.png)

- Ponemos un nombre de usuario:Rivan y una contraseña mayor o igual a 12 digitos y al menos una letra mayuscula.

![4 1](https://user-images.githubusercontent.com/99112892/183572366-ae697232-1534-4770-a2e0-d412b62b8b85.png)

- Aceptamos para usar una licencia de Windows Server existente.

![4 1_2](https://user-images.githubusercontent.com/99112892/183572430-a7f74d84-3015-4a35-98d7-0670667624af.png)

### Pestaña:Disks(Discos)
- El tipo de disco duro lo dejamos con la opción predeterminada junto a los demas campos de la parte inferior.

![4 2](https://user-images.githubusercontent.com/99112892/183572579-a8588840-b3b1-4c9f-99c5-4f9579993a3b.png)

### Pestaña:Networking(Redes)
- Observamos que ya nos crea una red virtual, una mascara de subred y los puertos permitidos.

![4 3](https://user-images.githubusercontent.com/99112892/183572824-ddda531b-6bcd-4a49-a72b-bd9165cba05e.png)

### Pestaña:Management(Administración)
- Usamos las opciones predeterminadas por Azure.

![4 4](https://user-images.githubusercontent.com/99112892/183572924-c7269611-572d-4c4e-b31c-0426a19fa798.png)

### Pestaña:Advanced(Opciones avanzadas)
- Usamos las opciones predeterminadas por Azure.

![4 5](https://user-images.githubusercontent.com/99112892/183573014-39cc9015-215c-45d6-a8d5-001beac6d511.png)

### Pestaña:Tags(Etiquetas)
Las etiquetas nos sirven para cuando hay muchas personas trabajando dentro de una organización, es importante saber quien esta subiendo que cambios.

- En el campo nombre es muy usual poner: CreatedBy y para el campo valor ponemos por quien fue creado.
Podemos observar que hay 12 recursos que se crean de manera automatica

- Agregamos otra etiqueta con Nombre:Area y Valor:Skilling
- Finalizamos con una ultima, Nombre:Ciclo y Valor:7maEd

![4 6](https://user-images.githubusercontent.com/99112892/183573199-2e8c23c8-b010-4b1b-be69-04d9098c6599.png)

### Pestaña:Review+Create(Revisar y Crear)
Como su nombre lo dice ya que configuramos las caracteristicas y requerimientos necesarios para nuestra máquina virtual, Azure revisara toda la información y nos creara lo solicitado cuando nos indique 'Validación superada'.

![4 7](https://user-images.githubusercontent.com/99112892/183573302-2ef5d54e-2720-4b9c-bac9-4d477f5e6c45.png)

- Le damos en crear.

![4 7_1](https://user-images.githubusercontent.com/99112892/183573377-d8307878-7e03-466d-b92d-4e93f7ecd4ba.png)

- Nos muestra que se completó la implementación y tambien podemos ver los detalles de la implementación, como los recursos, que tipo de recurso es y su estado.

![4 8](https://user-images.githubusercontent.com/99112892/183573475-ebc473c4-d818-4219-8ea6-975d615a74ce.png)

- Para verificar nuestra máquina virtual, seleccionamos 'ir al recurso'.

![4 8_1](https://user-images.githubusercontent.com/99112892/183573555-dd79d1c1-442b-4bba-88b3-342c612b48b5.png)

- Exploramos nuestra máquina virtual, para eso presionamos en 'conectar' y despues elegimos 'RDP'.

![4 9](https://user-images.githubusercontent.com/99112892/183573632-35e413ca-2a51-4511-a26b-066b53580cdb.png)

## Paso 5
- Descargamos el archivo 'RDP' y lo abrimos.

![5](https://user-images.githubusercontent.com/99112892/183573754-dd231981-f2e9-4984-9312-26c25469e513.png)

## Paso 6
- Nos saldra una ventana emergente, en la cual nos preguntara si nos queremos conectar, por lo que elegiremos 'conectar'.

![6](https://user-images.githubusercontent.com/99112892/183573869-fc681136-909a-4bf7-97db-f8adc7392c12.png)

## Paso 7
- Nos pedira los datos con los que creamos nuestra máquina virtual y le damos en aceptar.

![7](https://user-images.githubusercontent.com/99112892/183573981-0398d179-09f5-40bb-9ad8-fef51b376711.png)

## Paso 8
-Volvera a salir una ventana emergente donde preguntara si nos queremos conectar, ya que es la primera vez que lo hacemos, le diremos que 'si'.

![8](https://user-images.githubusercontent.com/99112892/183574107-78ad637d-c43b-48c6-84b4-892936a30741.png)

## Paso 9
- Obtendremos acceso a nuestra máquina virtual en la que podremos realizar cualquier cosa que necesitemos, ya que es una computadora a nuestras especificaciones requeridas, incluso vemos que tenemos conexión a internet.

![9](https://user-images.githubusercontent.com/99112892/183574875-4ce07332-74b6-4467-9c3e-7590939b8cb2.png)

![9 1](https://user-images.githubusercontent.com/99112892/183574968-d33fea35-f53f-4c2b-8e95-d08d5ab06a73.png)

![9 2](https://user-images.githubusercontent.com/99112892/183574983-0c252717-8b52-4178-abea-76422bfdda58.png)

### Nota:
Cuando creamos una máquina virtual vamos a tener un disco duro, que aunque apaguemos nuestra máquina virtual el disco va a seguir ocupado por lo que nos van a continuar cobrando ese servicio.

## Paso 10
- Ya comprobado que la guía concluyo satisfactoriamente, ahora nos desconectaremos de la máquina virtual y la apagaremos.

![10](https://user-images.githubusercontent.com/99112892/183575142-c07f309a-9d73-4f90-86cc-1ccf50717edc.png)

## Paso 11
Eliminaremos la VM:

- Primero iremos a Home en el portal de Azure y seleccionamos 'grupo de recursos'.

![11](https://user-images.githubusercontent.com/99112892/183575208-4e8e8fed-edf7-4868-9195-2d4dbea1f02d.png)

- Seleccionamos 'lab01_dr' y presionamos 'eliminar grupo de recursos'.

![11 1](https://user-images.githubusercontent.com/99112892/183575261-8d518096-cc66-4bad-b571-f4ffaec6d192.png)

- Escribimos el nombre de nuestra máquina virtual y presionamos 'eliminar', repetiremos el proceso ya que algunas veces no se eliminan a la primera.

![11 2](https://user-images.githubusercontent.com/99112892/183575345-dd34da7f-bf34-43c5-848a-a26e75a3501d.png)

- Por ultimo tambien eliminaremos 'NetworkWatcherRG' el cual se encarga de vigilar la red del grupo de recursos.

![11 3](https://user-images.githubusercontent.com/99112892/183575431-858af789-2265-4a17-8d71-4d086695231f.png)

### Nota:
Siempre es recomendable tener limpia nuestra area de grupos de recursos.

![11 4](https://user-images.githubusercontent.com/99112892/183575527-4e7c4655-a051-4240-bf53-8c6248b25a03.png)
