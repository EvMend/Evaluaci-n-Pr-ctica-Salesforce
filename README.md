# Evaluaci-n-Pr-ctica-Salesforce

                                                       EJERCICIO 2.


          1.  ¿Qué es un servidor HTTP? 

Un servidor HTTP o servidor web es un software que forma parte del servidor y tiene como misión principal devolver información (páginas) cuando recibe peticiones realizadas a través de la World Wide Web por parte de los usuarios. Procesa una aplicación del lado del servidor, generando o cediendo una respuesta en cualquier lenguaje o aplicación del lado del cliente. En otras palabras, es el software que permite que los usuarios que quieren ver una página web en su navegador puedan hacerlo. El código recibido por el cliente es renderizado por un navegador web. Para la transmisión de todos estos datos suele utilizarse algún protocolo. Generalmente se usa el protocolo HTTP para estas comunicaciones, perteneciente a la capa de aplicación del modelo OSI.


           2.	¿Qué son los verbos HTTP? Mencionar los más conocidos.	

HTTP define un conjunto de métodos de petición para indicar la acción que se desea realizar para un recurso determinado. Aunque estos también pueden ser sustantivos, estos métodos de solicitud a veces son llamados HTTP verbs. Estos verbos indican qué acción queremos realizar sobre el servidor y son GET, POST, PUT, PATCH, DELETE, HEAD, CONNECT, OPTIONS y TRACE. Cada uno indica una acción diferente a la que el servidor debe responder.
-	El método GET solicita una representación de un recurso específico. Las peticiones que usan el método GET sólo deben recuperar datos. Una petición GET es de sólo lectura.
-	El método POST añade datos al servidor. Siempre es un método de creación. Se utiliza para enviar una entidad a un recurso en específico, causando a menudo un cambio en el estado o efectos secundarios en el servidor.
-	El método PUT reemplaza todas las representaciones actuales del recurso de destino con la carga útil de la petición. Es decir, se utiliza cuando se desea crear o actualizar el recurso identificado por la URL.
-	El método PATCH es utilizado para aplicar modificaciones parciales a un recurso.
-	DELETE significa que queremos eliminar un recurso. Realiza lo contrario de PUT.
-	El método HEAD pide una respuesta idéntica a la de una petición GET, indica que únicamente queremos que se responda con los encabezados de la respuesta, y se ignore el cuerpo de datos.
-	El método CONNECT establece un túnel TCP/IP hacia el servidor identificado por el recurso.
-	El método OPTIONS es utilizado para describir las opciones de comunicación para el recurso de destino.
-	El método TRACE realiza una prueba de bucle de retorno de mensaje a lo largo de la ruta al recurso de destino. Sirve para comprobar si la solicitud se ha visto modificada por servidores intermedios.


          3.	¿Qué es un request y un response en una comunicación HTTP? ¿Qué son los headers? 

En HTTP, la comunicación de datos empieza con una petición (request) enviada del cliente, y termina con la respuesta (response) del servidor web.
El comando HTTP Request permite enviar todo tipo de petición HTTP a un URL específico y procesar la respuesta del servidor HTTP. El navegador envía información al servidor cada vez que navegamos a una pagina, como el lenguaje utilizado por el navegador, el tipo de navegador que estas usando, etc.

Los HTTP headers son la parte central de los HTTP requests y responses, y transmiten información acerca del navegador del cliente, de la página solicitada, del servidor, etc.
Un HTTP request se compone de:

-Método: GET, POST, PUT, etc. Indica que tipo de request es.
-Path: la URL que se solicita, donde se encuentra el resource.
Protocolo: contiene HTTP y su versión.
-Headers. Son esquemas de key:value que contienen información sobre el HTTP request y el navegador. Aquí también se encuentran los datos de las cookies. La mayoría de los headers son opcionales.
-Body. Si se envía información al servidor a través de POST o PUT, ésta va en el body.

Una vez que el navegador envía el HTTP request, el servidor responde con un HTTP response, compuesto por:

-Protocolo. Contiene HTTP y su versión.
-Status code. El código de respuesta, por ejemplo: 200 OK, que significa que el GET request ha sido satisfactorio y el servidor devolverá los contenidos del documento solicitado. Otro ejemplo es 404 Not Found, el servidor no ha encontrado el resource solicitado.
-Headers. Contienen información sobre el software del servidor, cuando se modificó por última vez el resource solicitado, el mime type, etc. De nuevo la mayoría son opcionales.
-Body. Si el servidor devuelve información que no sean headers ésta va en el body.


          4.	¿Qué es un queryString? (En el contexto de una url)

Las Query String o cadenas de consultas es un término que se utiliza para hacer referencia a una interacción con una base de datos. Además, es la parte de una URL que contiene los datos que deben pasar a las aplicaciones web.
En resumen, las Query String permiten acceder a páginas web dinámicas con distintas variables consiguiendo así que las páginas web no estén compuestas de decenas de directorios y permitiendo que su estructura esté basada en URLs amigables para el posicionamiento web SEO.


          5.	¿Qué es el responseCode? ¿Qué significado tiene los posibles valores devueltos?

El response Code o los códigos de estado de respuesta HTTP indican si se ha completado satisfactoriamente una solicitud HTTP específica. Los Códigos están organizados por categorías:
1xx : Los que empiezan por 100 , son los códigos de mensaje referentes a mensajes informativos a nivel de protocolo HTTP no es típico encontrárselos.
2xx: Los que empiezan por 200 son los más habituales ya que indican el cliente ha tenido éxito a la hora de procesar su petición
3xx: Son los relativos a redirecciones e indican que el cliente debe realizar alguna acción adicional a la hora de completar de forma correcta la petición.
4xx: Esta categoría es la más odiada y hace referencia a un error que se ha producido desde el cliente al realizar la petición
5xx: Estos errores son algo menos habituales y hacen referencia a fallos que se han producido en el lado servidor.


           6.	¿Cómo se envía data en un Get y cómo en un POST?	

Con el método GET, los datos que se envían al servidor se escriben en la misma dirección URL. Cuando escribes la dirección URL www.ejemplo.com en tu navegador, este se conecta con el servidor web y le envía una petición GET: 
GET /index.php
El archivo index.php de esta muestra de código de petición es la página de inicio de un sitio web, que el servidor enviará como respuesta al navegador.

La petición de la dirección www.ejemplo.com/test.html se formularía de forma análoga:
GET /test.html
El servidor enviaría el archivo test.html como respuesta.

A la petición GET puede añadirse más información, con la intención de que el servidor web también la procese. Estos llamados parámetros de URL se adjuntan a la dirección URL. La sintaxis es bastante simple:

-La secuencia de petición (query string) se inicia con un signo de interrogación “?”.
-Todos los parámetros se componen de un nombre y un valor: “Nombre=Valor”.
-Si se han de adjuntar varios parámetros, se unen con un signo “&”.

Por ejemplo: www.ejemplo.com/registrarse.php?nombre=pedro&amp;apellido=perez&amp;edad=55&amp;genero=hombre

Toda la información introducida por el usuario (los llamados “parámetros URL”) se transmiten tan abiertamente como el URL en sí mismo. Además, los parámetros URL se guardan sin cifrar junto al URL, y admite solo caracteres ASCII (limitados al máximo del URL: 2048 caracteres). El método GET es adecuado para la personalización de páginas web: el usuario puede guardar búsquedas, configuraciones de filtros y ordenaciones de listas junto al URL como marcadores, de manera que en su próxima visita la página web se mostrará según sus preferencias.

El método POST no escribe el parámetro del URL en la dirección URL, sino que introduce los parámetros en la solicitud HTTP para el servidor. Por ello, no quedan visibles para el usuario. Las peticiones POST suelen emplearse con formularios digitales. Además, admite caracteres ASCII y datos binarios, y la capacidad del método POST es ilimitada. El método POST es aconsejable para la transferencia de información y datos. Por ejemplo, cuando el usuario debe enviar datos o archivos al servidor, cuando se rellenan formularios o se suben fotos.


          7.	¿Qué verbo http utiliza el navegador cuando accedemos a una página?

El verbo GET es el que utilizar el navegador cuando accedemos a una página. Es el tipo más simple de método de solicitud HTTP: la que usan los navegadores cada vez que hace clic en un enlace o escribe una URL en la barra de direcciones.


           8.	Explicar brevemente qué son las estructuras de datos JSON y XML dando ejemplo de estructuras posibles.	

JavaScript Object Notation (JSON) es un formato basado en texto estándar para representar datos estructurados en la sintaxis de objetos de JavaScript. Es comúnmente utilizado para transmitir datos en aplicaciones web.
Los JSON son cadenas - útiles cuando se quiere transmitir datos a través de una red. Debe ser convertido a un objeto nativo de JavaScript cuando se requiera acceder a sus datos. Es posible incluir los mismos tipos de datos básicos dentro de un JSON que en un objeto estándar de JavaScript - cadenas, números, arreglos, booleanos, y otros literales de objeto. Esto permite construir una jerarquía de datos, como ésta:

   ![image](https://user-images.githubusercontent.com/86135193/123558855-e6979400-d76e-11eb-8282-5cddecea7718.png)


XML es el acrónimo de Extensible Markup Language, es decir, es un lenguaje de marcado que define un conjunto de reglas para la codificación de documentos.
El lenguaje de marcado es un conjunto de códigos que se pueden aplicar en el análisis de datos o la lectura de textos creados por computadoras o personas. El lenguaje XML proporciona una plataforma para definir elementos para crear un formato y generar un lenguaje personalizado. XML utiliza etiquetas para definir el contenido y el signficado de la información. 
Estructura XML:

![image](https://user-images.githubusercontent.com/86135193/123558874-19da2300-d76f-11eb-8bd5-462c26cde46e.png)



          9.	Explicar brevemente el estándar SOAP.	

SOAP (Simple Object Access Protocol) es un estándar basado en XML para la transmisión de mensajes en HTTP y otros protocolos de Internet. Se creó originalmente para permitir la comunicación entre las aplicaciones que se diseñaban con diferentes lenguajes y en diferentes plataformas. Es un protocolo ligero para el intercambio de información en un entorno descentralizado y distribuido. Proporciona un mecanismo estándar de empaquetar mensajes. Un mensaje SOAP se compone de un sobre que contiene el cuerpo del mensaje y cualquier información de cabecera que se utiliza para describir le mensaje. Como es un protocolo, impone reglas integradas que aumentan la complejidad y la sobrecarga, lo cual puede retrasar el tiempo que tardan las páginas en cargarse. Sin embargo, estos estándares también ofrecen normas integradas que pueden ser ideales para el sector empresarial. Los estándares de cumplimiento integrados incluyen la seguridad, la atomicidad, la uniformidad, el aislamiento y la durabilidad (ACID), que forman un conjunto de propiedades que garantizan operaciones confiables de las bases de datos.


          10.	Explicar brevemente el estándar REST Full.	
          
Rest (Representational State Transfer), es un modelo de arquitectura web basado en el protocolo HTTP para mejorar las comunicaciones cliente-servidor, mientras que Restful Web Service o Restful API son programas basados en REST. Una API RESTful es un servicio que funciona como un estándar para compartir información, en un sistema de doble vía: Consulta y Respuesta (Request => Response). La arquitectura REST al trabajar sobre el protocolo HTTP, los procedimientos o métodos de comunicación son los mismos que HTTP, siendo los principales: GET, POST, PUT, DELETE. Otros métodos que se utilizan en RESTful API son OPTIONS y HEAD. 
Otro componente de un RESTful API es el “HTTP Status Code”, que le informa al cliente o consumidor del API que debe hacer con la respuesta recibida.

          
          11.	¿Qué son los headers en un request? ¿Para qué se utiliza el key Content-type en un header?

Headers en request: son esquemas de key: value que contienen información sobre el HTTP request y el navegador. Aquí también se encuentran los datos de las cookies. La mayoría de los headers son opcionales. 
La key content-Type es la propiedad de cabecera (header) usada para indicar el tipo del recurso. Content-Type dice al cliente que tipo de contenido será retornado.




                                                       EJERCICIO 3.

1)	
 ![image](https://user-images.githubusercontent.com/86135193/123531542-c36fd480-d6db-11eb-816a-0155a5efe7bf.png)

2)	
  ![image](https://user-images.githubusercontent.com/86135193/123531554-dbdfef00-d6db-11eb-8791-883368996184.png)


3)	
  ![image](https://user-images.githubusercontent.com/86135193/123531558-ec906500-d6db-11eb-9e4e-f3c3a7d5840a.png)


-	La diferencia entre las llamadas 1 y 3 es que utilizando el método POST de la llamada 2 se agregó lo solicitado al body, y haciendo una nueva request GET en 3 podemos ver el resultado del request POST en 2.




                                                       EJERCICIO 5.
1.	Lead: es un potencial cliente interesado en comprar un producto o contratar un servicio. Datos que almacena: Address, Company, Description, Email, LastActivityDate, entre otros.
2.	Account: compañías o personas individuales con las que se hace negocio. Pueden ser clientes, competidores y socios. Datos que almacena: BillingAddress, LastActivityDate, NumberOfEmployees, etc.
3.	Contact: se usa para almacenar información acerca de personas que trabajan para dichas compañías. Es decir, personas asociadas a una cuenta. Datos que almacena: Name, Phone, Description, etc.
4.	Opportunity: negociaciones o acuerdos en curso. Almecenan información detallada sobre las cuentas y personas implicadas, y las cantidades de las ventas potenciales. Datos que almacena: Probability, Stage, Main Competitor(s), etc.
5.	Product: elementos y servicios que se ofrecen a los clientes o compradores. Datos que almacena: Description, Discount, ProductName, etc.
6.	PriceBook: es la lista maestra de todos los productos y sus precios. Datos que almacena: Name, Description, ValidFrom, ValidTo, etc.
7.	Quote: muestra los precios propuestos de los productos y servicios de la empresa. Datos que almacena: ContactId, ExpirationDate, Status, entre otros.
8.	Asset: representa un artículo de valor comercial, como un producto vendido por su empresa o un competidor, que un cliente ha comprado e instalado. Datos que almacena: AssetLevel, AssetProvidedById, AssetServicedById, Availability, ContactId, Description, LastReferencedDate, entre otros.
9.	Case: representa un caso, que es un problema o inconveniente que tiene un cliente. Datos que almacena: CaseNumber, OwnerId, Priority, etc.
10.	Article: este objeto se puede utilizar para asociar un artículo con categorías de datos de un grupo de categorías de datos o para consultar las selecciones de categorías para un artículo. Datos que almacena: DataCategoryName, ParentId, etc.
            
            
            https://github.com/EvMend/Evaluaci-n-Pr-ctica-Salesforce/blob/main/RelacionesObjetos.png
          
          


                                                       EJERCICIO 7.

          
          Soluciones de Salesforce

          
          A.	¿Qué es Salesforce?
Salesforce es una plataforma que integra todos los departamentos de una organización, otras empresas y clientes. Está basada en la nube y es CRM (administrador de relaciones con clientes). 

          B.	¿Qué es Sales Cloud?
Sales Cloud es un paquete de Salesforce situado en la nube. Su función es gestionar todos los procesos llevados a cabo con Salesforce, como ventas, relaciones con clientes y con socios. Mejora la productividad y la eficiencia.

          C.	¿Qué es Service Cloud?
Service Cloud es un software diseñado para la atención al cliente. Gestiona casos y optimiza la comunicación con el cliente.

          D.	¿Qué es Health Cloud?
Health Cloud es una plataforma que permite gestionar y llevar a cabo conversaciones entre pacientes y médicos, entidades sanitarias asociadas o prestadores de servicios de salud.

          E.	¿Qué es Marketing Cloud?
Marketing Cloud es una herramienta orientada al departamento de Marketing de una organización. Permite mejorar la relación entre la compañía y sus clientes, y atraer nuevos clientes, para generar un aumento en ventas.


          Funcionalidades de Salesforce

          
          A.	¿Qué es un RecordType?
RecordType o tipo de registro es utilizado cuando se crea o modifica un registro. Permite seleccionar un diseño de página, procesos y valores para cada registro y diferenciarlo del resto, en un mismo objeto.

          B.	¿Qué es un ReportType?
Un ReportType o tipo de reporte selecciona los registros y campos que están disponibles en un reporte para su acceso.

          C.	¿Qué es un Page Layout?
Page Layout es el formato o diseño de página que se puede configurar para páginas de registros de objetos. El usuario puede elegir el contenido que ve en la página, como tipos de botones, campos y su orden, acciones rápidas disponibles, entre otros.

          D.	¿Qué es un Compact Layout?
Compact Layout o formato compacto permite la adición de campos importantes en la parte superior de un registro, es decir, en su encabezado.

          E.	¿Qué es un Perfil?
Un Perfil define los permisos que tiene un usuario para acceder a objetos y datos, y las funciones habilitadas en su aplicación.

          F.	¿Qué es un Rol?
Un Rol controla lo que un usuario puede hacer sobre los datos de su organización, como ver o editar.

          G.	¿Qué es un Validation Rule?
Validation Rule o regla de validación de datos verifica que un dato ingresado por un usuario cumple con las especificaciones obligatorias para poder guardarlo.

          H.	¿Qué diferencia hay entre una relación Master Detail y Lookup?
Una relación Lookup entre dos objetos posiciona a uno de los objetos entre los elementos relacionados del otro, y de esa forma se lo puede buscar y encontrar más fácilmente.
Una relación Master-Detail posiciona a uno de los objetos como el principal, y al otro como un detalle. El objeto principal controla al objeto detalle.

          I.	¿Qué es un Sandbox?
Sandbox es un entorno en donde se pueden realizar distintas acciones, como cambios en configuración o testeos, sin que los usuarios lo noten ya que es una copia exacta de la organización, con todos sus objetos y datos.

          J.	¿Que es un ChangeSet?
ChangeSet es un conjunto de cambios enviado de organización a organización que lleva información sobre personalizaciones y nuevas configuraciones en objetos, aplicaciones, clases, etc.

          K.	¿Para qué sirve el import Wizard de Salesforce?
Import Wizard sirve para importar datos externos en objetos estándar, como por ejemplo cuentas y contactos.

          L.	¿Para qué sirve la funcionalidad Web to Lead?
Web to Lead sirve para generar un formulario que se puede agregar en la web de la compañía, en el que se incluyen preguntas y campos sobre cierto negocio o producto y datos de contacto para que sea completado por potenciales usuarios y leads.

          M.	¿Para qué sirve la funcionalidad Web to Case?
Web to Case sirve para generar un formulario en el que los usuarios pueden pedir solicitudes de atención al cliente. Es decir, genera casos. Y puede insertarse en la web de la compañía.

          N.	¿Para qué sirve la funcionalidad Omnichannel?
Omnichannel sirve para enrutar el trabajo o elemento de trabajo al agente de asistencia adecuado y disponible. Es decir, conecta a los clientes con el agente que está disponible para ayudarlo.

          O.	¿Para qué sirve la funcionalidad Chatter?
Chatter sirve para optimizar la colaboración de los usuarios en tiempo real, compartir información y conectar equipos, entre otras funciones. Funciona como una red social.



          Conceptos generales

          
          A.	¿Qué significa SaaS? ¿Salesforce es Saas?
SaaS significa Software as a Service. Funciona como un servicio orientado a empresas, que brinda soluciones de software, como aplicaciones en la nube, de modo que las empresas tienen todas estas funcionalidades integradas en una misma plataforma en Internet sin necesidad de instalar y mantener varios softwares y hardwares distintos. Sí, Salesforce es SaaS.

          B.	¿Que significa que una solución sea Cloud?
Que una solución sea Cloud significa que se puede acceder a ella por medio de Internet y de la nube. Estas soluciones, como aplicaciones y software, están almacenadas en servidores remotos.

          C.	¿Que significa que una solución sea On-Premise?
Que una solución sea On-Premise significa que este software está instalado dentro del servidor y dispositivos locales de la empresa. Es decir, dentro de su infraestructura. Se tiene acceso físico a los datos y no se necesita Internet.

          D.	¿Que es un pipeline de ventas?
Un pipeline de ventas es una herramienta de gestión que ilustra el conjunto de acciones que lleva a cabo un vendedor desde el primer contacto con un cliente, hasta el cierre de la venta, pasando por todas las etapas de negociación. El pipeline se concentra en el proceso.

          E.	¿Que es un funnel de ventas?
Un funnel de ventas (o embudo de ventas) es una herramienta que ilustra las etapas por las que pasa el cliente desde que se realiza el primer contacto, hasta el cierre de la venta. El funnel se concentra más en los números.

          F.	¿Qué significa Customer Experience?
Customer Experience significa la experiencia que atraviesa un cliente al comprar un producto o contratar un servicio, desde el primer contacto y atención brindada, hasta la experiencia final de uso con el producto o servicio. Es decir, la experiencia de interacción con tu compañía.

          G.	¿Qué significa omnicanalidad?
Omnicanalidad significa que todos los canales de comunicación de la compañía están sincronizados e integrados para mejorar la experiencia de los clientes.

          H.	¿Qué significa que un negocio sea B2B?
El marketing B2B significa “business to business”. Funciona dentro del mercado corporativo, es decir, empresas que ofrecen productos y servicios a otras empresas u organizaciones.

          I.	¿Qué significa que un negocio sea B2C?
El marketing B2C significa “business to consumer”. Funciona en el mercado de consumo masivo, es decir, empresas que ofrecen productos y servicios al público en general.

          J.	¿Qué es un KPI?
KPI (Key Performance Indicator) o Medidor de Desempeño es un indicador que mide la eficacia y productividad de las acciones y estrategias que lleva a cabo una empresa. Sirve para analizar los resultados y tomar decisiones en base a ellos.

          K.	¿Qué es una API y en qué se diferencia de una Rest API?
API (Application Programming Interfaces) es un conjunto de definiciones y protocolos que funcionan como una interfaz entre dos aplicaciones para el intercambio de información. Es decir, permite la comunicación entre estos dos softwares. Las API pueden utilizar cualquier tipo de protocolo.
Una REST API es un servicio web, es decir, es una API que se comunica sólo mediante protocolo REST. Una REST API presenta esa limitación frente a una API.

          L.	¿Qué es un Proceso Batch?
Un Proceso Batch o proceso por lotes es un modo en el un programa ejecuta un lote o un gran conjunto de información sin la supervisión del usuario y de manera secuencial.

          M.	¿Qué es Kanban?
Kanban es una metodología ágil y visual de producción que gestiona las tareas. Con un solo vistazo permite reconocer el estado de los proyectos y tareas, su seguimiento y supervisión.

          N.	¿Qué es un ERP? ¿Salesforce es un ERP?
ERP (Enterprise Resource Planning), o Planificación de Recursos Empresariales, es un sistema integrado de aplicaciones de software de una empresa. Sirve para centralizar la información de todas las áreas o departamentos que componen a una organización. De esta forma, automatiza y facilita los procesos. Sí, Salesforce es un ERP.

          
          
          

            
            

