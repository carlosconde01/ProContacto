# Evaluación Práctica 

![Logo Procontacto](/img/logo.png)

Carlos Andrés Conde Besil  

[Perfil de Trailhead](https://trailblazer.me/id/carlosconde)

## Tabla de Contenidos

- [Ejercicio 1](#ejercicio-1)
- [Ejercicio 2](#ejercicio-2)
- [Ejercicio 3](#ejercicio-3)
- [Ejercicio 4](#ejercicio-4)
- [Ejercicio 5](#ejercicio-5)
- [Ejercicio 6](#ejercicio-6)
- [Ejercicio 7](#ejercicio-7)



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

6. **Price Book:** Se trata de una lista de productos y sus respectivos precios. Existen dos tipos, el estándar que se conforma con la creación de los elementos de productos y el personalizado que se utiliza para ofrecer el mismo producto a distintos precios en diferentes mercados.

    - Active
    - Created By
    - Description
    - Is Standard Price Book
    - Last Modified By
    - Price Book Name

7. **Quote:** Representa un presupuesto, es decir, los precios propuestos de los productos y servicios de la compañía. Un presupuesto se puede crear desde una oportunidad.

    - Account Name
    - Additional To & Additional To Name
    - Bill To & Bill To Name
    - Contact Name
    - Contract
    - Created By
    - Description
    - Discount
    - Email 
    - Expiration Date
    - Fax 
    - Grand Total
    - Last Modified By
    - Line Items
    - Opportunity Name
    - Owner Name
    - Phone
    - Quote Name, Number, PDF, To, To Name
    - Shipping and Handling
    - Shipping, To, To Name
    - Status
    - Subtotal
    - Syncing
    - Tax
    - Total Price

8. **Asset:** Mientras que el objeto de Product representa los productos que la compañía vende, los assets representan los productos específicos que los clientes han comprado. Es decir, los Assets se utilizan para guardar información de las adquisiciones de los clientes.

    - Account
    - Address
    - Asset Level, Name, Owner
    - Asset Provided By, Serviced By
    - Competitor Asset
    - Consequence of Failure
    - Contact
    - Created By & Last Modified By
    - Current Amount, Lifecycle End Date, Monthly Recurring Revenue, Quantity
    - Description
    - Digital Asset Status
    - External Id
    - Has Lifecycle Management
    - Install Date
    - Internal Asset
    - Lifecycle End Date

9. **Case:** Un case se refiere a alguna pregunta, retroalimentación o inconveniente que proviene de un cliente. Tiene especialidad utilidad para identificar acciones que se pueden tomar para tener una mejor atención y conformidad del cliente. 

    - Account Name
    - Asset
    - Business Hours
    - Case Number, Origin, Owner, Reason
    - Closed When Created
    - Contact Email, Fax, Mobile, Name, Phone
    - Created By
    - Date/Time Closed & Opened
    - Description
    - Engineering Req Num
    - Entitlement Name, Process End Time, Process Start Time
    - Escalated
    - Internal Comments
    - Milestone Status & Status Icon
    - Parent Case
    - Potential Liability
    - Priority
    - Product
    - Service Contract
    - SLA Violation
    - Status
    - Stopped & Stopped Since
    - Subject 
    - Type
    - Web Company, Email, Name, Phone


10. **Article:** Los artículos capturan información acerca de los productos y servicios que se desean hacer disponible en la base de conocimiento. Pueden ser clasificados en categorías para facilitar el proceso de búsqueda y añadir funcionalidades de control de acceso. 


    - Archived By & Date                                                   
    - Article Number & Type ID
    - Case Association Account
    - Created By & Date
    - Custom Fields
    - First Published Date
    - Knowledge Article Version
    - Last Modified By, Date, Published Date
    - Primary Language
    - Article Type
    - Is Latest Version
    - Summary
    - Title
    - Validation Status
    - Total Views
    - Owner
    

**Diagrama de relaciones**

![UML relaciones](/img/uml.png)


## Ejercicio 6

### Soluciones de Salesforce

1. **¿Qué es Salesforce?**

Es una plataforma CRM en la nube que facilita la gestión de relaciones con clientes. Es capaz de ofrecerle a una compañía una vista única y compartida de sus clientes, facilita la toma de decisiones, gestión de procesos y cierre de tratos. 

2. **¿Qué es Sales Cloud?**

Sales Cloud es una parte del CRM que ofrece Salesforce, está creado específicamente para la fuerza de venta de una empresa. Es el producto más popular por lo que mucha gente menciona Salesforce refiriéndose en realidad a Sales Cloud. Esta nube es capaz de agrupar toda la información de los clientes en el mismo lugar, evitar la pérdida de información crítica, generar reportes para monitoreo de ventas, es escalable y accesible desde teléfonos móviles. En términos generales tiene el propósito de ayudar a las compañías a vender más rápido y de forma más inteligente para tener un mayor crecimiento.

3. **¿Qué es Service Cloud?**

Es una plataforma de asistencia al cliente que permite a los agentes entregar un servicio de atención a cliente efectivo e integrado. Los clientes tienen la posibilidad de solicitar soporte por el medio de su preferencia, cada canal está abierto a los agentes para monitorear las necesidades del cliente y responder.

4. **¿Qué es Health Cloud?**

Se trata de la plataforma en la nube que está dirigido para el sector de ciencias de la salud. Tiene capacidad de proveer una vista completa del perfil de los pacientes, acceder a una red colaborativa de cuidado, integrar datos de dispositivos de monitoreo de signos vitales (wearables) y finalmente llevar un registro integral de salud.


5. **¿Qué es Marketing Cloud?**

Es el módulo de Salesforce con las herramientas necesarias para mejorar la interacción de las marcas con sus clientes utilizando diversos canales. Contiene inteligencia artificial para proporcionar una experiencia de comunicación personalizada, logra un mayor engagement cuidando y mejorando las relaciones con los prospectos y finalmente emite una serie de estadísticas con base en las mediciones realizadas.

### Funcionalidades de Salesforce

1. **¿Qué es un RecordType?**

Define distintos Busines Process, Pages Layouts y Picklist Values en un determinado objeto. Se utiliza cuando un objeto cumple múltiples propósitos y muestra diferente información en su Page Layout. Un RecordType puede ser creado para todos los objetos, sin embargo, en algunos se requiere crear un Business Process y posteriormente su Record Type. 

2. **¿Qué es un ReportType?**

Un ReportType funciona como una plantilla y define los objetos que se muestran en el reporte, las relaciones de estos objetos, campos incluidos en resultados, campos que aparecen por defecto y sus respectivos nombres. En otras palabras, un ReportType determina los registros y campos que aparecen en el reporte. Por ejemplo, el reporte de Opportunities permite acceder a resistros de Opportunity y campos como Amount, Stage y Type.

3. **¿Qué es un Page Layout?**

Los Page Layouts controlan el diseño y organización visual de botones, campos. Definen también cuáles campos son visibles, de sólo lectura y requeridos. Se utilizan comúnmente para personalizar el contenido de páginas de registro de los usuarios.

4. **¿Qué es un Compact Layout?**

El Compact Layout despliega los campos más importantes en la aplicación móvil, Lightning Experience así como en integraciones de correo electrónico. Se recomienda el uso de Compact Layouts con el objetivo de facilitar al usuario encontrar la información que requiere, al estar anclada al header del registro.

5. **¿Qué es un Perfil?**

Cada vez que se crea un usuario, es necesario asignarle un Perfil para definir cómo este usuario accede a los objetos y datos, así como otorgar permisos para las acciones que podrá realizar.

6. **¿Qué es un Rol?**

Los roles controlan el nivel de visibilidad que tiene un usuario sobre los datos de su organización. Cada usuario podrá ver, editar e informar todos los datos por debajo de ellos en una estructura jerárquica. A los usuarios que requieran visualización de todos los datos se les deberá asignar el rol más alto. 

7. **¿Qué es un Validation Rule?**

Las reglas de validación verifican que los datos que ingresó el usuario cumplen con los estándares y especificaciones predefinidas antes de guardar el registro. Suelen estar conformados por una fórmula o expresión que regresa ya sea un valor de verdadero o de falso. 

8. **¿Qué diferencia hay entre una relación Master Detail y Lookup?**

La relación de Lookup vincula dos objetos para poder buscar uno en los elementos del otro. Pueden tratarse de relaciones uno a uno, o de uno a muchos. Se utilizan cuando los objetos están relacionados sólo en ciertos casos y funcionan como objetos independientes que tienen sus propias fichas en la interfaz de usuario. 

La relación Master Detail añade complejidad al tener un objeto principal que controla los comportamientos de otro objeto detalle. El detalle no funciona como objeto independiente por lo que si se elimina un registro del objeto principal, se eliminarán automáticamente los del objeto detalle. 

9. **¿Qué es un Sandbox?**

Un entorno Sandbox se trata de una copia de los metadatos de una organización de producción. Este tipo de entornos están aislados, lo que significa que cualquier operación realizada no afectará a la organización de producción. 


10. **¿Qué es un ChangeSet?**

Los ChangeSets son una herramienta que se utiliza para enviar personalizaciones de una organización de Salesforce a otra. Un uso muy común es enviar cambios que ya fueron probados en Sandbox al ambiente de producción. Cabe mencionar que está limitado al envío de información de la organización, no contienen registros.

11. **¿Para qué sirve el Import Wizard de Salesforce?**

El Data Import Wizard se utiliza para importar datos de objetos de Salesforce. Permite importar tanto objetos estándar como personalizados, sin embargo es importante saber que permite hasta 50,000 registros a la vez.

12. **¿Para qué sirve la funcionalidad Web to Lead?**

Se le llama así al proceso de utilizar un formulario en un sitio web para capturar la información de los visitantes y almacenarla como un nuevo Lead en Salesforce. Se trata de una manera efectiva de obtener nuevos Leads y el hecho de tener un formulario bien diseñado permite capturar información demográfica así como intereses en productos y servicios.  

13. **¿Para qué sirve la funcionalidad Web to Case?**

Se le conoce como Web to Case al proceso de recolectar solicitudes de servicio de un sitio web para automáticamente generar Cases en Salesforce. Para utilizarlo debe habilitarse esta función, personalizar el formulario y añadirlo al sitio.

14. **¿Para qué sirve la funcionalidad Omnichannel?**

El concepto de Omnichannel se refiere a brindar servicios y soporte al cliente en múltiples canales. Se encuentra presente en la Service Cloud de Salesforce y permite a los agentes proporcionar un servicio ágil y oportuno. Su implementación en Salesforce es declarativa.


15. **¿Para qué sirve la funcionalidad Chatter?**

Es una red social empresarial de Salesforce que se utiliza para que los miembros del equipo comercial puedan interactuar. Permite en términos generales conectarse, motivarse, trabajar con eficiencia, fomentar la colaboración y reconocer el trabajo bien hecho. 


### Conceptos generales

1. **¿Qué significa SaaS?**

Software as a Service son aplicaciones ejecutadas en los servidores de los proveedores y que se ponen a disposición de los clientes por medio de internet, como un servicio. Con este modelo, no se requiere instalar, mantener ni actualizar los componentes de software y hardware.

2. **¿Salesforce es SaaS?**

Salesforce es un SaaS ya que ofrece sus servicios en la nube bajo un modelo de suscripción donde se hace cargo de gestionar el acceso, mantener la estructura de datos, la conectividad y los servidores necesarios para el funcionamiento del servicio.

3. **¿Qué significa que una solución sea Cloud?**

Se trata de una alternativa a la ejecución clásica de aplicaciones en equipos de cómputo o servidores locales. Una solución Cloud permite el acceso remoto a aplicaciones, almacenamiento de archivos, procesamiento de datos, sin necesidad de instalar programas.

4. **¿Qué significa que una solución sea on-Premise?**

Se refiere a la adquisición de una licencia de uso de software para instalarlo en el entorno propio de la organización que lo requiere. Con este modelo pueden evitar posibles fallos de seguridad y accesos no autorizados al sistema. Sin embargo, al adquirir el control total de los datos asumen tanto el riesgo en materia de seguridad pues no existen garantías, como los costos de mantenimiento.

5. **¿Qué es un pipeline de ventas?**

Un pipeline hace referencia a los procesos que se llevan a cabo para conseguir un objetivo en concreto. Específicamente, un pipeline de ventas es una herramienta del equipo comercial en el que figuran todos los pasos que se dan durante el proceso de venta. 

6. **¿Qué es un funnel de ventas?**

Un funnel de ventas es un sistema diseñado para atraer a desconocidos, convertirlos en leads, transformarlos en clientes y aumentar su frecuencia de compra. Su implementación implica tener estudiado el modelo de negocio, definir el perfil de los compradores, contar con una oferta atractiva y proveer valor. 

7. **¿Qué significa Customer Experience?**

La experiencia del cliente es lo que se genera en la mente del consumidor como consecuencia de su relación con la marca. Buscar tener una buena relación implica la interación antes, durante y después de la compra. Más aún debe estar estandarizado y ofrecerse en todos los niveles de la compañía. Por lo tanto, es una disciplina que genera valor en las empresas, eleva datos de ventas y consumidores.


8. **¿Qué significa omnicanalidad?**

El concepto de Omnichannel se refiere a brindar servicios y soporte al cliente en múltiples canales. Se encuentra presente en la Service Cloud de Salesforce y permite a los agentes proporcionar un servicio ágil y oportuno. Su implementación en Salesforce es declarativa.

9. **¿Qué significa que un negocio sea B2B? ¿Qué significa que un negocio sea B2C? ¿Qué es un KPI?**

Business to business es un modelo de negocio comercial entre empresas, es decir una compañía entrega servicios y productos a otra con el objetivo de mejorar los bienes que ofrece. Permite a las empresas involucradas un ahorro económico, tener agilidad digital, reconocimiento de marca y como consecuencia, mayores ganancias.

Business to customer es un modelo de negocio donde las transacciones y prestación de servicios se producen entre una empresa y su consumidor final. Es ampliamente utilizado pues el número de clientes potenciales es mayor, los productos adquieren mejor distribución y los canales de comunicación pueden ser más eficientes.

Key Performance Indicators son una serie de indicadores que permiten medir si una estrategia está atendiendo los objetivos de la organización. A pesar de que se suelen utilizar en el área de marketing, no están limitadas a esto pues se aplican de igual forma en empresas financieras, comerciales, entre otras.

10. **¿Qué es una API y en que se diferencia de una Rest API?**

Una API es una serie de funciones y procedimientos que permiten que una aplicación acceda a características de otra. 

REST es un estilo arquitectónico para aplicaciones conectadas en la red que utilizan el modelo cliente servidor. REST implica una serie de reglas para construir una API. Al ser una forma estandarizada, su uso implica facilidad en su implementación y comprensión. Una comparación entre APIs suele ser SOAP vs REST siendo la primera menos flexible pues cuenta con más estándares. 

En resumen, REST es un tipo de API, no todas las APIs son REST, pero todos los servicios REST son APIs.

11. **¿Qué es un proceso batch?**

El procesamiento batch o también llamado por lotes, es un procedimiento mediante el cual un equipo de cómputo procesa lotes de trabajo usualmente de forma simultánea, en orden secuencial y sin pausa. Esto implica que los grandes trabajos se calculen en partes más pequeñas, por lo que se aumenta la eficiencia. 

12. **¿Qué es Kanban?**

El origen de la palabra proviene de Japón donde significa tablero visual. Se trata de un método gráfico de gestión del flujo de trabajo que ayuda a las organizaciones a gestionar y mejorar sus desarrollos. Se basa principalmente en la identificación de tareas de una lista de acciones pendientes y se organiza en columnas representando la etapa correspondiente.

13. **¿Qué es un ERP?**

Por sus siglas en inglés Enterprise Resource Planning es un software que se utiliza para gestionar contabilidad, aprovisionamiento, gestión de proyectos, gestión de riesgos, entre otros. Ayudan a proporcionar transparencia en el proceso de negocio al supervisar aspectos de producción, logística y finanzas. 


14. **¿Salesforce es un ERP?**

Salesforce no es un ERP, es un CRM. Si bien ambos son utilizados para mejorar la productividad en las organizaciones, cumplen propósitos distintos. Sin embargo, a pesar de que Salesforce no ofrece ERP, sí cuenta con Revenue Cloud así como con una serie de herramientas que se complementan y facilitan la integración.


## Ejercicio 7

Importar al Playground el archivo CSV compartido por Laura Lejarza, utilizando Dataloader.

**Mostrar cómo fue realizado paso a paso.**

1. Tras el análisis inicial del archivo de importación, se añadieron los campos correspondientes en el objeto Account. 
2. Se realizó una limpieza del documento en Excel para eliminar las columnas sin valores y se exportó el CSV. 
3. Se inició sesión en el Dataloader (cabe mencionar que se utilizó el Playground llamado "EjercicioInmobiliaria" que se puede encontrar en mi [perfil de Trailhead](https://trailblazer.me/id/carlosconde), y se seleccionó insert.
4. Se seleccionó el objeto Account y el archivo de importación.

![Selección CSV](/img/seleccion.png)

5. Se seleccionó la opción de create or edit map, se utilizó la opción de auto-match fields to columns, se verificó que el mapeo propuesto fuera correcto.

![Mapeo](/img/mapeo.png)

6. Se indicó la ubicación del directorio para crear los archivos de errores y éxitos para finalizar con la importación.

![Directorio](/img/directorio.png)

7. Se crearon los documentos correspondientes que confirman una importación exitosa.

![Confirmación](/img/confirma.png)

**Un listado que muestre sólo las cuentas importadas, que la lista muestre una columna por cada columna del CSV.**

Se agregó un campo llamado Importada_procontacto con un valor de "Sí" con el objetivo de colocar en la lista un filtro que muestre efectivamente sólo las cuentas importadas.

![Filtro](/img/filtro.png)

A continuación se muestra la lista con las columnas solicitadas. Cabe mencionar que no se puede configurar para visualizarlas todas ya que el límite es de 15.

![Lista](/img/lista.png)



Una vez realizada la importación de Accounts, se procede a realizar la importación de Opportunities. Cabe mencionar que cada Opportunity está asociada a una Account, por lo que para realizarlo en Dataloader se requiere exportar las cuentas y sus respectivos ids para poder mapearlos.

1. Se selecciona export en Dataloader, se escoge Account y se establece la ubicación del CSV a exportar.


![Export](/img/export1.png)

2. Se selecciona el nombre y el ID para su exportación, también se añade el filtro para exportar únicamente los datos que fueron importados en el ejercicio anterior.

![Export2](/img/export2.png)

3. Se abre el archivo para asignarle el ID utilizando la función VLOOKUP de Excel. 

![vlookup](/img/vlookup.png)

Cabe mencionar que por la naturaleza de las relaciones de Salesforce, importar una oportunidad tiene como prerequisito tener registrada la cuenta relacionada. Esto quiere decir que para fines de este ejercicio no se realizó la importación completa de oportunidades, únicamente aquellas cuya cuenta ya era existente. En ambiente de producción, se tendría que solicitar al cliente el registro completo de cuentas para posteriormente importar las oportunidades.

4. Una vez asignados los IDs del sistema, se procede a realizar la importación siguiendo el procedimiento anterior.

