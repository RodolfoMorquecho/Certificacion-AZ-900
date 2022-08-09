# AZ900-WebApp
"App Service" es un servicio que se utiliza para las aplicaciones de grado empresarial este servivcio es un servicio web.

Guía para crear una Web App dentro de Azure.

Lo primero que debemo hacer, es dirigirnos al portal de [Azure](https://portal.azure.com/#home).

## Paso 1
En en la vista de Home seleccionamos la opcion "Crear un recurso".

![1W](https://user-images.githubusercontent.com/99112892/183569398-13bf228a-7fb5-4bce-bd99-c2c4489d1b4e.png)

## Paso 2
Nos aparaceran distintos servicios, elegimos 'Aplicación Web'.

![2W](https://user-images.githubusercontent.com/99112892/183569528-4483f9f9-197f-47f8-9f27-4493dcc3e166.png)

## Paso 3
### Pestaña:Datos básicos
- Nos aseguramos de que la suscripción es de tipo 'student'.
- Creamos un nuevo grupo de recursos, el cual sería un folder donde vamos a guardar nuestra aplicación web dentro de la nube, lo nombramos como: lab02-dr.
- Le damos un nombre a nuestra aplicación web, en este caso la nombro: lab002-dr.
- En la sección publicar, marcamos la que dice 'Código' ya que utilizaremos el código desde un repositorio de GitHub el cual se obtuvo mediante un fork de la Sherpa Fer.
- La 'pila del entorno en tiempo de ejecución' es con el lenguaje/codigo con el que esta realizada nuestra aplicacion, en este caso pondre: Node 14 LTS.

![3W_Basics1](https://user-images.githubusercontent.com/99112892/183569677-aa5bafca-ad36-497c-a435-15d219eda27b.png)

- El sitema operativo en este ejemplo lo dejo en Linux.
- En Región seleccionamos Central US.
- Dentro del "Plan de App service" dejaremos el SKU y tamaño con la opción ´Básico B1'.

![3W_Basics2](https://user-images.githubusercontent.com/99112892/183569769-fc5542eb-84d5-4518-9979-67f5e078d6dd.png)

### Pestaña:Implementación(Deployment)
- En el apartado de "Configuración de Acciones de Github' elegimos "habilitar", de inmediato nos saldra una ventana emergente, donde nos pedira que autorizemos el acceso o conexión a nuestro perfil de GitHub.

![3W_Imple1](https://user-images.githubusercontent.com/99112892/183570095-6eb10500-976e-4e52-be9c-3ba1e196349e.png)

![3W_Imple1 1](https://user-images.githubusercontent.com/99112892/183570121-81cb4132-43b7-48b6-9931-27233e62069f.png)

- La organización ponemos el perfil de nuestro GitHub.
- En repositorio tendremos acceso a todos lo que tenemos en nuestro perfil, incluyendo a los forks, seleccionare 'lab1'.
- La rama/branch es 'master'.

![3W_Imple2](https://user-images.githubusercontent.com/99112892/183570238-f2d14c68-a6ee-47e1-bb8e-203850862e37.png)

- Nos da una vista previa del archivo y su configuracion de flujo de trabajo.

![3W_Imple3](https://user-images.githubusercontent.com/99112892/183570330-68686456-c839-4585-bab9-d90933da1df8.png)

### Pestaña:Redes(Networking)
- Se queda con la configuración predeterminada.

![3W_Redes](https://user-images.githubusercontent.com/99112892/183570442-e5b38984-3c15-4ff8-adc4-bfa3f593a0f8.png)

### Pestaña:Supervisión(Monitoring)
- Como no utilizaremos 'Insights' lo dejamos con la configuración predeterminada.

![3W_Supervision](https://user-images.githubusercontent.com/99112892/183570532-703027df-52db-4180-9c8b-e480df4c9a10.png)

### Pestaña:Tags(Etiquetas)
Las etiquetas nos sirven para cuando hay muchas personas trabajando dentro de una organización, es importante saber quien esta subiendo que cambios. -En el campo nombre es muy usual poner: CreatedBy y para el campo valor ponemos por quien fue creado.

- Podemos observar que hay 12 recursos que se crean de manera automatica.
- Agregamos otra etiqueta con Nombre:Area y Valor:Rivan.
- Finalizamos con una ultima Nombre:Ciclo y Valor:7maEd.

![3W_Etiquetas](https://user-images.githubusercontent.com/99112892/183570696-5af8fa7a-94f4-401d-908b-246a2bc73be7.png)

### Pestaña:Review+Create(Revisar y Crear)
Va a tomar el codigo de la aplicación hecha(GitHub) y se lo traera a Azure para empezar a trabajar sobre de él.
- Pulsamo en 'crear'.

![3W_RevisarCrear](https://user-images.githubusercontent.com/99112892/183570867-6530ad06-4354-48bd-b9bc-d6727beea85f.png)

- Podemos ver que se completo la implementación y nuestra aplicación esta lista.

![3W_Finalizada](https://user-images.githubusercontent.com/99112892/183570946-c104f440-5314-47c9-be40-51e615953172.png)

