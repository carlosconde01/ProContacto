# Evaluación Práctica 

![Logo Procontacto](/img/logo.png)

## Ejercicio 1

1. Instalar el IDE Visual Studio Code
2. Instalar GIT y GIT Bash


![Logo Visual Studio](/img/vs.png)
![Logo Git](/img/git.png)


## Ejercicio 2

1. **¿Qué es un servidor HTTP?** 

Un servidor HTTP es un componente de software capaz de comprender direcciones web (URLs) y el protocolo HTTP (hypertext transfer protocol). Cuando un navegador requiere un archivo, el servidor HTTP es el encargado de aceptar la solicitud, encontrar el documento requerido y enviarlo.

2. **¿Qué son los verbos HTTP? Mencionar los más conocidos.**  

Los verbos HTTP con un conjunto de métodos de petición para indicar la acción que se desea realizar para un recurso específico. Los más utilizados se enlistan a continuación.

- GET: Solicita una representación de un recurso específico, recupera datos.
- HEAD: Pide una respuesta idéntica al GET, pero omite el cuerpo de la respuesta.
- POST: Crea una nueva entidad de forma no idempotente, es decir, si se ejecuta varias veces, creará múltiples elementos. 
- PUT: Actualiza una entidad existente con la carga de la petición, produce el mismo resultado si se ejecuta en diversas ocasiones por lo que es idempotente. Si la entidad no existe, la crea.
- DELETE: Borra un recurso específico.


3. **¿Qué es un request y un response en una comunicación HTTP? ¿Qué son los headers?**

Un request se trata de una petición que se le hace al servidor.  
Un response se refiere a la respuesta que envía el servidor al recibir un request como estímulo.  
Los headers HTTP están presentes tanto en requests como en responses y permiten el envío de información adicional entre el cliente y el servidor.

4. **¿Qué es un queryString? (En el contexto de una url)**  

Un queryString o por su nombre en español, cadena de consultas, hace referencia a una interacción con la base de datos y es la parte de una URL que contiene los datos que deben pasar a las aplicaciones web en una petición para obtener una respuesta personalizada. 

5. **¿Qué es el responseCode? ¿Qué significado tiene los posibles valores devueltos?** 

Es un código de 3 dígitos emitido por un servidor en respuesta a la petición de un cliente. Estos códigos son de utilidad para identificar de forma concisa el estado de respuesta de la solicitud. Sus valores suelen encontrarse en un rango del 100 al 599 y están divididos en 5 categorías que se enlistan a continuación.

- Respuestas informativas (100-199)
- Respuestas exitosas (200-299)
- Mensajes de redirección (300-399)
- Error por parte del cliente (400-499)
- Error por parte del servidor (500-599)

6. **¿Cómo se envía la data en un GET y cómo en un POST?**   

Tanto GET como POST son métodos válidos de envío de información de formularios. Sin embargo, su diferencia radica en que con el método GET es posible ver los parámetros enviados pues están dentro de la URL, mientras que con el método POST los datos viajan ocultos. 

- GET: `www.procontacto.com/newuser.php?nombre=Carlos&apellido=Conde`
- POST: `<form action="http://www.procontacto.com/newuser" method ="post">`

7. **¿Qué verbo http utiliza el navegador cuando accedemos a una página?**  

Cuando accedemos a una página web, el navegador utiliza el verbo `GET /index.html` para obtener el índice o en su defecto la página que deseamos visualizar.

8. **Explicar brevemente qué son las estructuras de datos JSON y XML dando ejemplos de estructuras posibles.** 
  
JSON por sus siglas en inglés Javascript Object Notation es un formato o estándar basado en texto plano de intercambio de datos. Es ampliamente utilizado pues es fácil de leer y escribir para los desarrolladores y sencillo de interpretar para los equipos de cómputo. A continuación se muestra un ejemplo que guarda los datos de un usuario.

```
{
  "firstName": "Carlos",
  "lastName": "Conde",
  "address": {
    "street": "Coyoacán #11",
    "city": "CDMX",
    "country": "México",
  },
  "phoneNumbers": [
    "212-732-1234",
    "646-123-4567"
  ]
}
```

XML que significa Extensive Markup Language, es un lenguaje de marcado de propósito general que no está predefinido, esto quiere decir que el usuario debe definir las etiquetas que desea utilizar. En la actualidad su principal uso de XML se encuentra en el intercambio de información entre sitios web, bases de datos y aplicaciones. Un ejemplo que guarda información de empleados se muestra a continuación.

```
<?xml version="1.0" encoding="utf-8"?>
<person>
    <firstName>Carlos</firstName>
    <lastName>Conde</lastName>
    <company>Procontacto</company>
    <birthday>1999-03-03</birthday>
    <gender>male</gender>
  </person>
```

9. **Explicar brevemente el estándar SOAP.** 

Respuesta

10. **Explicar brevemente el estándar REST Full.**

Respuesta

11. **¿Qué son los headers en un request? ¿Para qué se utiliza el ket Content-type en un header?**  

Respuesta
