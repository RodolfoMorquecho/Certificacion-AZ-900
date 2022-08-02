# AZ900-Functions

Es una fracción de codigo que permite ejecutar acciones, cumplir con peticiones para traer cosas de internet, etc. Se denominan como serverless.

Lo primero que debemo hacer, es dirigirnos al portal de [Azure](https://portal.azure.com/#home)

## Paso 1
En en la vista de Home nos posicionamos en el menú y seleccionamos "Aplicación de funciones".

![1](https://user-images.githubusercontent.com/99112892/182480332-2e490976-9ae9-4103-b4cb-8ecfab260293.png)

## Paso 2
Creamos una Function.

![2](https://user-images.githubusercontent.com/99112892/182480407-125a1eb2-f8bb-4550-8c0f-31cf9c3e44a1.png)

## Paso 3
Pestaña:Datos básicos
- Nos aseguramos de que la suscripción es de tipo 'student'.
- Creamos un nuevo grupo de recursos, el cual sería un folder donde vamos a guardar nuestra 
aplicación web dentro de la nube, lo nombramos como: lab04-dr.
- Para este ejemplo, nombramos a la aplicación de funciones como "hello-dr".
- Publicar mediante código.
- La "pila del entorno en tiempo de ejecución" es con el lenguaje/codigo con el que esta realizada
nuestra aplicacion de funciones, en este caso uaremos: Node.js.
- La versión con la que trabajadar de Node.js es "16 LTS".
- En la Región para esta ocasion utilizamos Central US.
- El sistema operativo que usaremos sera Windows.
- Y el plan que utilizaremos sera "Consumo (Sin servidor)".
El plan elegido dicta cómo se escala la aplicación, qué características están habilitadas
y cómo se establece el precio.
- Nos vamos a la pestaña etiquetas.

![3](https://user-images.githubusercontent.com/99112892/182480512-1e7708f7-3524-45a9-b2f2-07b6b823c68c.png)

Pestaña:Tags(Etiquetas)
Las etiquetas nos sirven para cuando hay muchas personas trabajando dentro de una organización, es importante saber quien esta subiendo que cambios.

![4](https://user-images.githubusercontent.com/99112892/182480555-4e9fcf74-6f43-48be-b30a-7cd6fa526bd2.png)

Pestaña:Review+Create(Revisar y Crear)
- Analiza todo lo requerido anteriormente para proceder a aprovisionarlo. 
- Pulsamo en 'crear'.

![5](https://user-images.githubusercontent.com/99112892/182480648-211168cb-92df-49a6-9cc5-5e0a8cc6f97e.png)

- Esperaremos unos segundos hasta que se complete la implementación.
- Cuando este lista, presionamos en "ir al recurso".

![6](https://user-images.githubusercontent.com/99112892/182480695-a0d745f5-633f-4f50-864d-0c09023b7c4b.png)

## Paso 4
Nos ubicara automaticamente en la sección "introducción" donde obtendremos toda la informaciíón de nuestra function creada.
- Para ver que nuestra Function esta corriendo entramos al link que nos aparece posicionado a lado de "URL".

![7](https://user-images.githubusercontent.com/99112892/182480805-32cf6c9d-74d2-45c0-8f4a-9b1acd3f8f77.png)

- Verificamos que esta funcionando y corriendo a la prefección nuestra aplicación.

![8](https://user-images.githubusercontent.com/99112892/182480847-7de34a59-d2dc-48c2-959a-ed3349edc604.png)


## Paso 5
- Regresamos a la interfaz previa donde esta la información esencial y en el menú lateral izquierdo presionaremos "Funciones".

![9](https://user-images.githubusercontent.com/99112892/182480928-8027f0f2-1d32-4a1e-ae91-5e25924bfc0a.png)


- Agregaremos una function.

![10](https://user-images.githubusercontent.com/99112892/182480978-5e560528-59d6-493a-b15f-fc981b29361d.png)

- Buscaremos una function "HTTP" y le daremos en Crear , es una función a la que le pasaremos argumentos y esta se ejecutara.

![11](https://user-images.githubusercontent.com/99112892/182481128-8192d4de-f431-4782-9b9a-b44553e83d97.png)

## Paso 6
- Ya creada nuestra función HTTP, tendremos está interfaz, donde iremos a la opción "Código y prueba".

![12](https://user-images.githubusercontent.com/99112892/182481178-fc6a74a6-ab21-4a5a-aadb-c1802652f111.png)

Nos aparacera el codigo de la function.
- Primero obtendremos la URL y la copiamos.

![13](https://user-images.githubusercontent.com/99112892/182481245-9a453ed1-3f5f-49bc-a264-32a726a627a0.png)

- Lo pegamos en una pestaña nueva y nos aparecera el siguiente mensaje.

![14](https://user-images.githubusercontent.com/99112892/182481286-b63ef353-cb2f-4a54-84c4-eaa7a35fca5d.png)

## Paso 7
Tenemos nuestra funtion implementada y corriendo pero necesitamos ver que se ejeccute ante una petición.

- Como se pide en el mensaje, necesitamos agregar un nombre en la URL para obtener una respuesta personalizada, por lo que nos dirigimos a esa sección y procedemos a agregar: "&&name=Rodolfo".

![15](https://user-images.githubusercontent.com/99112892/182481440-dfbc6747-05d0-4f90-9aea-07a8ff1aa4e9.png)

- Obtendremos nuestra respuesta personalizada. 

![16](https://user-images.githubusercontent.com/99112892/182481513-d5265296-1820-4557-b5ae-843ddba8a02b.png)
