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

Simple Object Access Protocol o SOAP es un protocolo para el intercambio de información en entornos descentralizados y distribuidos. Este protocolo está basado en XML y cada proceso de comunicación cuenta con 3 secciones. El sobre define la infraestructura para describir qué hay en un mensaje y su forma de procesrlo, las reglas de codificación expresan instancias de tipos de datos definidos para la aplicación y el estilo de comunicación indica si se sigue el formato llamada a procedimiento remoto o en su defecto, el orientado a mensajes.  

Comparado con REST, los servicios web de SOAP generalmente ofrecen mayor seguridad, por lo que son más adecuados para soluciones empresariales. Una desventaja que vale la pena mencionar es que al tratarse de un protocolo, establece reglas estrictas que aumentan la complejidad y la sobrecarga, lo cual suele retrasar el tiempo de respuesta. 

10. **Explicar brevemente el estándar REST Full.**

Una API RESTful es una intefaz de intercambio de información que se creó inicialmente como una guía para administrar la comunicación en redes complejas. Comúnmente las solicitudes se envían en protocolo HTTP y la respuesta recibida puede ser en distintos formatos como HTML, XML, texto sin formato, y JSON.   
Ofrece una implementación más flexible que SOAP pues como surgió más tarde, se considera una alternativa más rápida. Los servicios RESTful son más ligeros por lo que han cobrado mucha presencia tanto en internet de las cosas como en el desarrollo de aplicaciones móviles.



11. **¿Qué son los headers en un request? ¿Para qué se utiliza el key Content-type en un header?**  

Los headers son la parte medular de los requests y responses pues transmiten información acerca del navegador del cliente, de la página solicitada, del servidor, entre otros. Cada vez que se envía una petición la primera línea contiene el método y la URL, mientras que la parte inferior contiene los headers. De forma análoga, al recibir la respuesta la primera línea representa el código de respuesta seguido de los headers. Cabe mencionar que al inspeccionar el código fuente de un sitio, los headers no aparecen pues para visualizarlos se requieren otras herramientas.

El content-type indica el tipo de archivo utilizado en la comunicación con el objetivo de ayudar a comprender el formato en la que se está enviando la información y mejorar el procesamiento y visualización de contenido. 


## Ejercicio 3

1. **Realizar un request GET a la URL: https://procontacto-reclutamiento-default-rtdb.firebaseio.com/contacts.json**

![Primer get](/img/get.png)

2. **Realizar un request POST a la URL anterior con body:**
```
{
"name": "Carlos Andrés Conde Besil",  
"email": "carlos.conde@procontacto.com.mx"
}
```
![Post](/img/post.png)

3. **Realizar nuevamente un GET a la URL. ¿Qué diferencias se observan entre las llamadas del punto 1 y 3?**

La diferencia radica en que la segunda llamada incluye la información que se agregó en el POST del punto 2, como se muestra a continuación.

![Segundo get](/img/get2.png)


## Ejercicio 4

Realizar los siguientes módulos de Trailhead: https://trailhead.salesforce.com/users/norozco3/trailmixes/introduccion

La resolución de los módulos puede ser consultada en mi [perfil de Trailhead](https://trailblazer.me/id/carlosconde).


## Ejercicio 5

Explicar qué son conceptualmente, qué datos almacenan en forma estándar y cómo se relacionan al resto cada uno de los siguientes objetos de Salesforce.

1. **Lead:** Representan a personas que están interesadas en el producto o servicio. Provienen de internet, tarjetas de contacto que el equipo almacena, asistentes de conferencias, entre otros. 

    - Address
    - Annual Revenue
    - Campaign
    - Clean Status
    - Company
    - Company D-U-N-S Number
    - Created By
    - Current Generator(s)
    - D&B Company
    - Data.com Key
    - Description
    - Do Not Call
    - Email & Email Opt Out
    - Fax & Fax Opt Out
    - Individual
    - Industry
    - Last Modified By
    - Last Transfer Date
    - Lead Owner
    - Lead Source
    - Lead Status
    - Mobile
    - Name
    - No. of Employees
    - Number of Locations
    - Phone
    - Primary
    - Product Interest
    - Rating
    - SIC Code
    - Title
    - Website

2. **Account:** Representan compañías con las que se hace negocio o relacionadas con el mismo (clientes, socios, competencia).

    - Account Name, Number, Owner, Site Source
    - Active
    - Annual Revenue
    - Billing Address
    - Clean Status
    - Created By
    - Customer Priority
    - D&B Company
    - Data.com Key
    - Description
    - D-U-N-S Number
    - Einstein Account Tier
    - Employees
    - Fax
    - Industry
    - Last Modified By
    - NAICS Code & Description
    - Number of Locations
    - Ownership
    - Parent Account
    - Phone
    - Rating 
    - Shipping Address
    - SIC Code & Description
    - SLA, Expiration Date, Serial Number
    - Ticker Symbol
    - Tradestyle
    - Type
    - Upsell Opportunity
    - Website
    - Year Started

3. **Contact:** Son personas asociadas con una cuenta, con las que se requiere comunicación y relaciones de negocio. Provienen de Leads u otras fuentes y tienen especial utilidad en permitir darle seguimiento a la información que provoca relaciones efectivas. 

    - Account Name
    - Assistant & Asst. Phone
    - Birthdate
    - Clean Status
    - Contact Owner
    - Created By
    - Data.com Key
    - Department
    - Description
    - Do Not Call
    - Email & Email Opt out
    - Fax & Fax Opt Out
    - Home Phone
    - Individual
    - Languages
    - Lasy Modified By
    - Last Stay-in-Touch Request Date & Last Stay-in-Touch Save Date
    - Lead Source
    - Level
    - Mailing Address
    - Mobile
    - Name
    - Reports To
    - Stage
    - Title

4. **Opportunity:** Son tratos cualificados con los que el equipo de ventas está trabajando. Ayudan a monitorear la etapa en la que se encuentra el proceso de venta. Una oportunidad se suele crear cuando un Lead es convertido.

    - Account Name
    - Amount
    - Close Date
    - Contract
    - Created By
    - Current Generator(s)
    - Delivery/Installation Status
    - Description
    - Expected Revenue
    - Forecast Category
    - Lasy Modified By
    - Lead Source
    - Main Competitor(s)
    - Next Step
    - Opportunity Name, Owner, Score
    - Order Number
    - Price Book
    - Primary Campaign Source
    - Private
    - Probability (%)
    - Quantity
    - Stage
    - Tracking Number
    - Type

5. **Product:** Son artículos o servicios que se ofrecen a los clientes. Cada producto puede existir en múltiples Price Books con diferentes precios.
 
    - Active
    - Created By
    - Display URL
    - External Data Source
    - External ID
    - Last Modified By
    - Product Code, Description, Family, Name, SKU
    - Quantity Unit of Measure

6. **Price Book** 
    
