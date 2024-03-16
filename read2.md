# NODE JS

💻Node.js es un entorno de ejecución de JavaScript basado en el motor V8 de Google Chrome. Permite a los desarrolladores ejecutar código JavaScript fuera del navegador web, lo que lo convierte en una herramienta fundamental para crear aplicaciones de servidor escalables y de alto rendimiento

⌨️Este curso no solo te enseñará Node.js sino que también abarca Express, MongoDB, PostgreSQL, Docker, Mongoose, Prisma, Railway, Github, entre otros.

🔶 Secciones del curso
00:00:00 Introducción cinemática
00:00:19 Saludo Inicial
00:00:19 Bienvenida
00:01:42 Instalaciones necesarias
00:20:23 ¿Qué es Node.js?
00:26:51 Consola de Node.js
00:34:18 Ejecutando archivos JavaScript
00:37:56 File System (Manipular archivos)
00:45:25 npm init & package.json
00:55:07 nodemon
01:00:37 importanciones y exportaciones
01:09:13 variables de entorno
01:21:25 Herramientas para las prácticas

🔷 PRÁCTICA 1
01:28:05 PRACTICA 1: json-server
01:36:57 Postman
01:46:30 Subir Repositorio a Github
01:51:07 Códigos HTTP

🔷 PRÁCTICA 2
01:55:14 PRACTICA 2: Web Server
02:09:20 Express js
02:28:02 Migrar Web Server a ES6
02:24:47 Editar README.md con stackedit

🔷 PRÁCTICA 3
02:34:59 PRACTICA 3: API REST (CRUD) con Mongo
02:42:02 Mongoose
02:53:42 Middleware propio
02:59:20 Body Parser
03:04:25 MongoDB
03:08:35 Docker
03:10:15 Mongo Compass
03:12:32 Probando la API REST
03:34:53 Despliegue de backend y base de datos en Railway

🔷 PRÁCTICA 4
03:45:00 PRACTICA 4: API REST(CRUD) con PostgreSQL
03:49:18 Node.js con TypeScript
04:06:27 Prisma
04:12:13 Bcrypt (encriptar contraseñas)
04:16:57 JWT (autenticación token)
04:23:10 PostgreSQL
04:34:51 TablePlus
04:37:28 Manejo de errores
05:15:09 Probando la API
05:23:25 Scripts despliegue y build
05:26:24 Subir repositorio externo
05:28:22 Despliegue
05:38:30 Despedida

## npm init & package.json

- Crear una carpeta para el proyecto
- Ir a la Terminal de la carpeta y colocar: npm init
- Esto crea el archivo "package.joson"

  {
  "name": "node_project",
  "version": "0.0.1",
  "description": "Node Project for Learning",
  "main": "index.js",
  "scripts": {
  "dev": "node src/index.js",
  "console": "echo 'Hi World from Scripts' && npm run dev"
  },
  "author": "Miguel Alvarado",
  "license": "ISC"
  }

## nodemon

    https://nodemon.io/

    https://www.npmjs.com/package/nodemon

- Se instala solo para que funcione solo como dependencia de desarrollo: npm i nodemon --save-dev

## Importaciones y Exportaciones

- En los ejemplos contenidos en function.js, index.js y objects.js se define como se ejecutan las importaciones y exportaciones de dos formas de codificación.

## Variables de Entorno

### Variable de Entorno "dotenv"

- se crea el file "env" y el ".gitignore" para que la información no se suba al repositorio
- dentro de .gitignore se pone ".env"
- Para configurar el puerto(port) y se capture su información, colocamos: "npm i dotenv" y se instala como dependencia.
-

### Variable de Entorno "env-var"

- Para configurar el puerto(port) y se capture su información, colocamos: "npm install env-var" .

- En el archivo index.js se colocan:

  - import env from "env-var";

  y const PORT = env.get("PORT").default("5432").asPortNumber();

## HERRAMIENTAS Y BIBLIOTECAS

1. Express
2. MongoDB
3. Mongoose
4. Railway
5. Docker
6. Body-Parcer

## **PRÁCTICA 1**

### PRACTICA 1: json-server

- Crear una carpeta para el proyecto: "proyecto-json-server"
- Ir a la Terminal de la carpeta y colocar: npm init
- Esto crea el archivo "package.joson"
- Instalar json-server: colocar "npm install json-server" en la Terminal, y crea una dependencia.
- Crear un "db.json" or "db.json5" file

  {
  "posts": [
  { "id": "1", "title": "a title", "views": 100 },
  { "id": "2", "title": "another title", "views": 200 }
  ],
  "comments": [
  { "id": "1", "text": "a comment about post 1", "postId": "1" },
  { "id": "2", "text": "another comment about post 1", "postId": "1" }
  ],
  "profile": {
  "name": "typicode"
  }
  }

## **POSTMAN**

    https://blog.postman.com/

### ¿Qué son los métodos HTTP?

    https://blog.postman.com/what-are-http-methods/

Los métodos HTTP se utilizan para indicar la acción que un cliente API desea realizar en un recurso determinado. Cada método HTTP se asigna a una operación específica, como crear, leer, actualizar o eliminar un recurso, y se debe incluir un método HTTP con cada solicitud a una API REST.

Aquí, brindaremos una descripción general de alto nivel de HTTP y explicaremos cómo se relaciona con las API REST . También revisaremos los métodos HTTP más comunes y explicaremos cuáles son seguros e idempotentes.

### ¿Qué es HTTP y cómo se relaciona con REST?

HTTP , que significa Protocolo de transferencia de hipertexto, es el protocolo dominante para transmitir datos (como páginas HTML, imágenes y vídeos) entre clientes y servidores en Internet. Opera según un modelo de solicitud-respuesta, en el que el cliente envía una solicitud al servidor y el servidor responde con los datos solicitados o un mensaje de error. HTTP no tiene estado, lo que significa que el servidor maneja cada solicitud de forma independiente, sin ningún conocimiento de solicitudes anteriores.

REST (Transferencia de estado representacional) es el estilo arquitectónico más utilizado para crear servicios web y API, y enfatiza las interacciones estandarizadas y sin estado entre clientes y servidores. Las API REST están diseñadas en torno a recursos a los que se puede acceder a través de puntos finales de API únicos. Estas características hacen de HTTP la opción ideal para implementar principios RESTful. Los métodos HTTP son componentes críticos de las solicitudes a las API REST, ya que permiten a los clientes especificar la acción que desean realizar en un recurso determinado. De hecho, no es posible enviar una solicitud a una API REST sin un método HTTP.

### ¿Cuáles son los métodos HTTP más comunes?

Los métodos HTTP permiten a los clientes API realizar acciones CRUD (Crear, Leer, Actualizar y Eliminar) en los recursos de una API de una manera estandarizada y predecible. Los métodos HTTP más utilizados son:

### CONSEGUIR (GET)

El método GET se utiliza para recuperar datos en un servidor. Los clientes pueden usar el método GET para acceder a todos los recursos de un tipo determinado, o pueden usarlo para acceder a un recurso específico. Por ejemplo, una solicitud GET al /productspunto final de una API de comercio electrónico devolvería todos los productos de la base de datos, mientras que una solicitud GET al /products/123punto final devolvería el producto específico con una IDextensión de 123. Las solicitudes GET normalmente no incluyen un cuerpo de solicitud, ya que el cliente no intenta crear ni actualizar datos.

### CORREO (POST)

El método POST se utiliza para crear nuevos recursos. Por ejemplo, si el administrador de una tienda de comercio electrónico quisiera agregar un nuevo producto a la base de datos, enviaría una solicitud POST al /productspunto final. A diferencia de las solicitudes GET, las solicitudes POST suelen incluir un cuerpo de solicitud, que es donde el cliente especifica los atributos del recurso que se creará. Por ejemplo, una solicitud POST al /productspunto final podría tener un cuerpo de solicitud similar a este:

    {
      "nombre": "Zapatillas",
      "color azul",
      "precio": 59,95,
      "Moneda: USD"
    }

### PONER

El método PUT se utiliza para reemplazar un recurso existente con una versión actualizada. Este método funciona reemplazando todo el recurso (es decir, el producto específico ubicado en el /products/123punto final) con los datos incluidos en el cuerpo de la solicitud. Esto significa que todos los campos o propiedades no incluidos en el cuerpo de la solicitud se eliminan y se agregan todos los campos o propiedades nuevos.

### PARCHE (PATCH)

El método PATCH se utiliza para actualizar un recurso existente. Es similar a PUT, excepto que PATCH permite a los clientes actualizar propiedades específicas en un recurso, sin sobrescribir las demás. Por ejemplo, si tiene un recurso de producto con campos para name, brandy price, pero solo desea actualizar price, puede usar el método PATCH para enviar una solicitud que solo incluya el nuevo valor para el pricecampo. El resto del recurso se mantendría sin cambios. Este comportamiento hace que el método PATCH sea más flexible y eficiente que PUT.

### BORRAR (DELETE)

El método DELETE se utiliza para eliminar datos de una base de datos. Cuando un cliente envía una solicitud DELETE, solicita que se elimine el recurso en la URL especificada. Por ejemplo, una solicitud DELETE al /products/123punto final eliminará permanentemente el producto con un IDde 123de la base de datos. Algunas API pueden aprovechar mecanismos de autorización para garantizar que solo los clientes con los permisos adecuados puedan eliminar recursos.

### ¿Qué métodos HTTP son seguros?

Los métodos HTTP seguros facilitan operaciones de solo lectura, lo que significa que no crean ni alteran los recursos de la API. GET es el método seguro más utilizado, pero el método HEAD, que se utiliza para recuperar sólo los encabezados de un recurso, también es seguro.

### ¿Qué métodos HTTP son idempotentes?

Un método HTTP se considera idempotente si dará el mismo resultado sin importar cuántas veces se ejecute. Todos los métodos seguros también son idempotentes, al igual que PUT y DELETE. Sin embargo, POST y PATCH no son idempotentes. POST no es idempotente porque llamarlo varias veces dará como resultado la creación de múltiples recursos. PATCH puede ser idempotente, pero no necesariamente lo es. Por ejemplo, una solicitud PATCH puede incrementar un campo específico cada vez que se llama, lo que modificaría el recurso cada vez.

## **SUBIR REPOSITORIO A GITHUB**

## **Códigos HTTP**
