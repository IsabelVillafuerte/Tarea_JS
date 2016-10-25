# Conceptos clave del video 

https://www.youtube.com/watch?v=8aGhZQkoFbQ

------


A continuación se presentan los conceptos clave mencionados y explicados durante el video.

**JavaScript** es un lenguaje concurrente de un solo subproceso. Algunos de los puntos clave es que cuanta con pila de llamadas, un bucle de eventos, una devolución de llamada, cola y algunas otras API, entre otras cosas.

**V8**, tiempo de ejecucion usado por Chrome, con v8 hay una pila de llamadas y un heap. El heap, hace referencia a donde la asignación de memoria que ocurre, y luego está la llamada de vuelta. No contiene cosas asinconas como se cree.

Es importante comprender que JS es un lenguaje de programacion de un solo hilo, de un solo tiempo de ejecución, y tiene una sola pia de llamadas.

La **pila de llamadas** (call stack)
Es una estructura dinámica que almacena la información sobre las subrutinas de un programa. El programa que llama a la subrutina empuja la dirección de regreso en la pila , y la subrutina llamada, cuando finaliza, retira la dirección de retorno de la pila de llamadas y transfiere el control a esa dirección. Si el empujar se consume todo el espacio asignado para la pila de llamadas, ocurre un error de desbordamiento.

El **blocking** (bloqueo) es un problema generado por código que es lento. Algunos ejemplos son los siguientes: console.log no es lento, per las solicitudes de red y las solicitudes de imagenes, sí lo son, por mencionar algunas. El problema esta en que se corre el codigo en el navegador. Se tiene una petición sincrona, y el navegador no puede hacer nada más, está atascado.

Cuando se habla de una solución a devolucines de llamada asíncrona se integra la concurrencia y el blucle de eventos.

JavaScript puede hacer solo una cosa a la vez. La razón por la que se pueden hacer cosas concurrentets es porque el navegador es más que solo el tiempo de ejecución.

El trabajo de los **eventos de bucles** es mirar a la pila y mirar en la cola de tareas. Si la pila está vacía, toma la primera cosa en la cola y lo empuja en la pila.

Las **Callbacks** pueden ser una función que llama a otra función o pueden ser una callback asíncrona.