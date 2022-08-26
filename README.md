# flow2-NodeRed
Segundo ejercicio usando NodeRed

# Introducción

El flow 2 representa el segundo ejercicio a realizar con NodeRed. Este ejercicio consiste en conectar un nodo Inject con un nodo Debug y automatizarlo para que genere un TimeStamp cada 1 segundo. Además agregar un nodo funcion que convierta el timestamp en fecha legible.

# Material Necesario
Para realizar este flow necesitas lo siguiente:

1. Ubuntu 20.04
2. NodeJS
* NPM
* NodeRed
* Nodos Dashboard

# Material de referencia
En los siguientes enlaces puedes encontrar cursos en la plataforma de edu.codigoiot.com que te permitirán realiar las configuraciones necesarias

* [Instalación de Virtual Box y Ubuntu 20.04](https://edu.codigoiot.com/course/view.php?id=812)
* [Instalación de NodeRed](https://edu.codigoiot.com/enrol/index.php?id=817)
* [Introducción a NodeRed](https://edu.codigoiot.com/enrol/index.php?id=278)

# Instrucciones
## Requisitos previos
Para que este flow funcione, debes cumplir con los siguientes requisitos previos

1. Instalación de NodeJS. Se recomienda tener instalado NodeJS en alguna versión LTS. Al momento de creación de este documento, se usó la versión 16.17LTS. Esta instalación debe incluir las Build-Tools para hacer uso de NPM

2. Instalación de NodeRed. La instalación se realiza por NPM. Al momento de la creación de este contenido, se usó la versión 3.0.2


# Instrucciones de preparación del entorno
Para ejecutar este flow, es necesario lo siguiente

1. Arrancar NodeRed con el comando node-red
2. Exportar el flow 1 creado en la actividad anterior e importarlo, una vez importado cambiar el nombre dando doble clic en el flow 1
3. Modificar el nodo Inyect con un intervalo de 1 segundo para mandar timestamp
4. Agregar un nodo funcion que convierta el timestamp en fecha legible copiando el siguiente codigo en la pestalla "On Message": 

* // Lo que está después de “//” son comentarios
// Crea un objeto Date a partir del payload enviado por timestamp
var date = new Date(msg.payload);
// Cambia el payload para que sea una fecha con formato
msg.payload = date.toString();
// Regresa el mensaje para que se envíe al sigueinte nodo
return msg;

5. Hacer clic en el boton Deploy

# Instrucciones de operación
Para observar el resutlado de este flow, sólo es necesario abrir la pestaña Debug.

# Resultados
A continuación puede verse una vista previa del resultado de este flow.
Resultados

![Cargando](https://github.com/DanielRochez/flow2-NodeRed/blob/main/evidencia.mp4)


# Evidencias
Se mostraron en el apartado resultados

# Créditos
Desarrollado por Daniel Rochez

* [GitHub](https://github.com/DanielRochez)