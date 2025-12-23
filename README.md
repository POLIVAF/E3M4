# 📸 Galería Interactiva de Imágenes

Proyecto educativo que implementa una **galería de imágenes interactiva** usando **HTML, CSS y JavaScript puro**, siguiendo buenas prácticas de la industria.

---

## 🧩 Descripción del Proyecto

La galería permite:

* Mostrar una **imagen principal**.
* Cambiar la imagen principal al hacer clic en una **imagen thumbnail**.
* Mostrar dinámicamente un **pie de foto** basado en el atributo `alt` de la imagen seleccionada.
* Evitar duplicación de elementos usando **validación defensiva**.

---

## 🛠️ Tecnologías Utilizadas

* **HTML5** → Estructura del contenido
* **CSS3** → Estilos y layout
* **JavaScript (ES6)** → Lógica e interactividad

---

## 📁 Estructura del Proyecto

```
/E3M4
│
├── index.html
├── README.md
└── assets
    ├─ style.css
    │   ├─ style.css
    └── js
        └─ app.js
```

---

## 🧱 Estructura HTML (index.html)

* Imagen principal con `id="imagen-principal"`
* Contenedor principal con `id="imagen-principal-container"`
* Thumbnails con la clase `.thumbnail`

Estos identificadores permiten una **selección clara y precisa desde JavaScript**.

---

## 🎨 Estilos CSS (style.css)

* Layout centrado usando `flexbox`
* Thumbnails con efecto `hover`
* Estilos definidos para el pie de foto (`#pie-de-foto`)

El CSS está desacoplado del JavaScript, siguiendo buenas prácticas.

---

## ⚙️ Lógica JavaScript (app.js)

### 1️⃣ Selección de elementos del DOM

```js
const imagenPrincipal = document.querySelector('#imagen-principal');
const contenedorImagen = document.querySelector('#imagen-principal-container');
const thumbnails = document.querySelectorAll('.thumbnail');
```

---

### 2️⃣ Validación defensiva

```js
if (!imagenPrincipal || !contenedorImagen || thumbnails.length === 0) {
  console.error('Error: Elementos del DOM no encontrados.');
}
```

📌 **Objetivo**:

* Verificar que los elementos existen antes de usarlos
* Evitar errores de ejecución
* Facilitar debugging

---

### 3️⃣ Manejo de eventos

Se asigna un `click` a cada thumbnail usando `forEach`:

```js
thumbnails.forEach(thumbnail => {
  thumbnail.addEventListener('click', () => {
    // lógica del evento
  });
});
```

---

### 4️⃣ Lógica del evento `click`

Al hacer clic en un thumbnail:

* Se obtiene su `src` y `alt`
* Se actualiza la imagen principal
* Se elimina el pie de foto anterior (si existe)
* Se crea un nuevo `<p>` dinámicamente
* Se agrega al contenedor principal

```js
const pieDeFoto = document.createElement('p');
pieDeFoto.id = 'pie-de-foto';
pieDeFoto.textContent = altThumbnail;
contenedorImagen.appendChild(pieDeFoto);
```

---

## 🧠 Conceptos Clave Aplicados

* Selector de clase (`.thumbnail`)
* Selector por id (`#imagen-principal`)
* Selector descendente
* `querySelector` y `querySelectorAll`
* `addEventListener`
* Manipulación del DOM
* Validación defensiva

---

## ✅ Buenas Prácticas Implementadas

* Código legible y comentado
* Prevención de errores comunes
* No acumulación de nodos en el DOM
* Separación de responsabilidades
* Base escalable para futuras mejoras

---

## 🚀 Posibles Mejoras Futuras

* Marcar thumbnail activo
* Animaciones de transición
* Versión responsive avanzada
* Refactorización a funciones reutilizables
* Migración a componentes

---

## 👨‍💻 Autor

Proyecto desarrollado con enfoque **Full-Stack JavaScript**, aplicando criterios reales de la industria IT.

---

✨ *Este proyecto sirve como base sólida para aprender manipulación del DOM y eventos en JavaScript moderno.*


##repositorio y page GITHUB

[E34M] (https://github.com/POLIVAF/E3M4.git)
[E34M] (https://polivaf.github.io/E3M4/)

