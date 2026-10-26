# Exposición: Objetos predefinidos de JavaScript

## 1. ¿Qué es JavaScript?

JavaScript es un lenguaje de programación que se usa principalmente para agregar interactividad a las páginas web. Por ejemplo, permite mostrar mensajes, realizar cálculos, consultar la fecha y modificar el contenido de una página.

En esta exposición veremos 11 herramientas: `Number`, `Math`, `Boolean`, `Date`, intervalos de tiempo, `String`, `Location`, `Navigator`, `Document`, `Window` y `Frame`.

## 2. JavaScript puro y HTML

**JavaScript puro**, también llamado *Vanilla JavaScript*, significa usar JavaScript sin instalar librerías o frameworks adicionales.

- **HTML** organiza el contenido de la página.
- **JavaScript** realiza operaciones y puede cambiar el contenido.
- Algunas herramientas, como `Location`, `Navigator`, `Document`, `Window` y los `Frame`, pertenecen al entorno del navegador, no al núcleo del lenguaje ECMAScript.

## 3. Ejemplos de cada tema

### 1. Number

Sirve para convertir valores a números y trabajar con cantidades.

```javascript
let numero = Number("10");
console.log(numero + 5); // Muestra 15
```

### 2. Math

Incluye funciones matemáticas, como calcular una raíz cuadrada.

```javascript
let raiz = Math.sqrt(25);
console.log(raiz); // Muestra 5
```

### 3. Boolean

Representa un valor verdadero (`true`) o falso (`false`).

```javascript
let esMayor = Boolean(10 > 5);
console.log(esMayor); // Muestra true
```

### 4. Date

Permite consultar la fecha y la hora.

```javascript
let fecha = new Date();
console.log(fecha); // Muestra la fecha y hora actuales
```

### 5. Intervalos de tiempo

`setInterval()` repite una función cada cierto tiempo. El tiempo se indica en milisegundos; 2000 milisegundos equivalen a 2 segundos.

```javascript
let intervalo = setInterval(function() {
    console.log("Han pasado 2 segundos");
}, 2000);

// Para detenerlo cuando sea necesario:
// clearInterval(intervalo);
```

### 6. String

Sirve para guardar y manipular texto.

```javascript
let nombre = String("Carlos");
console.log(nombre.toUpperCase()); // Muestra CARLOS
```

### 7. Location

Permite consultar la dirección web actual.

```javascript
console.log(location.href); // Muestra la URL actual
```

### 8. Navigator

Permite consultar información del navegador, como el idioma configurado.

```javascript
console.log(navigator.language); // Por ejemplo, es-CO
```

### 9. Document

Representa el documento HTML y permite modificar su contenido.

```javascript
document.getElementById("resultado").textContent = "Hola, mundo";
```

Este ejemplo necesita que exista en el HTML un elemento con `id="resultado"`.

### 10. Window

Representa la ventana o pestaña del navegador. Por ejemplo, permite mostrar una alerta.

```javascript
window.alert("Bienvenidos a mi ejemplo");
```

### 11. Frame (iframe)

Un `iframe` permite mostrar otra página o documento dentro de la página actual. Cada marco tiene su propio contexto de ventana.

```html
<iframe id="marco" src="about:blank"></iframe>

<script>
    let marco = document.getElementById("marco");
    console.log(marco.contentWindow);
</script>
```

En este ejemplo se consulta la ventana del marco interno. El acceso a su contenido puede estar limitado por las reglas de seguridad del navegador.

## 4. Ejemplo completo para ejecutar

Guarda el siguiente código en un archivo llamado `index.html`. Incluye HTML para mostrar los resultados y JavaScript puro para trabajar con los temas de la exposición.


<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Objetos predefinidos de JavaScript</title>
</head>
<body>
    <h1>Objetos predefinidos de JavaScript</h1>
    <p id="resultado"></p>

    <iframe id="marco" src="about:blank" title="Marco de ejemplo"></iframe>

    <script>
        // 1. Number: convierte texto a número
        let numero = Number("10");

        // 2. Math: calcula la raíz cuadrada
        let raiz = Math.sqrt(25);

        // 3. Boolean: guarda un valor verdadero o fal