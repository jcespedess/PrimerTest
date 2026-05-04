# CLAUDE.md

Este archivo proporciona orientación a Claude Code (claude.ai/code) para trabajar con el código de este repositorio.

## Descripción del Proyecto

Es un proyecto web estático mínimo usado como ejercicio de aprendizaje de Git y Vue.js básico. No tiene herramientas de construcción, gestores de paquetes ni frameworks de pruebas — se ejecuta directamente en el navegador.

## Estructura de Archivos

- `index.html` — Punto de entrada. Carga Vue.js 2.5.17 desde CDN y monta una instancia Vue en `#miApp`.
- `app.js` — Archivo JS independiente con un console.log; actualmente no está vinculado a `index.html`.
- `style.css` — Hoja de estilos vacía; tampoco está vinculada a `index.html`.

## Cómo Ejecutar el Proyecto

Abre `index.html` directamente en el navegador, o sírvelo con cualquier servidor de archivos estáticos:

```bash
python3 -m http.server 8080
# luego abre http://localhost:8080
```

## Notas de Arquitectura

- Vue 2 se carga desde CDN (`vue@2.5.17`), por lo que no hay paso de `npm install`.
- La instancia Vue está definida inline en `index.html` con `new Vue({ el: '#miApp', data: { mensaje: 'Hola Mundo' } })`.
- `app.js` y `style.css` no están referenciados en `index.html`; para activarlos habría que agregar `<script src="app.js">` y `<link rel="stylesheet" href="style.css">` al HTML.
