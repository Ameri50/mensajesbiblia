# Mensajes — web de estudio

Aplicación React para explorar el catálogo en español de mensajes de William Branham y hacer preguntas en un chat con respuestas fundamentadas en pasajes del catálogo.

## Requisitos

- Node.js 20 o posterior
- Una clave de Google Gemini para habilitar el chat con IA

## Desarrollo local

1. Instala las dependencias: `npm install`
2. Copia `.env.example` a `.env` y coloca tu clave de Gemini en `GEMINI_API_KEY`. El servidor carga `.env` localmente; no guardes la clave en el código ni en el navegador.
3. Inicia la aplicación: `npm run dev`
4. Abre la URL que muestra el servidor (por defecto `http://localhost:5173`).

Sin la variable `GEMINI_API_KEY`, puedes navegar y leer el catálogo, pero el chat mostrará que falta configurar el servicio.

## Producción

Ejecuta `npm run build` y luego inicia el servidor con `GEMINI_API_KEY` configurada usando `npm start`. El servidor sirve la aplicación compilada y mantiene las solicitudes de Gemini en el backend.

El catálogo se sirve de forma paginada y los textos completos se cargan por mensaje para no descargar los 105 MB del archivo al abrir la web.

## Estudio

En cada mensaje puedes compartir, marcar favoritos, resaltar (4 colores) y añadir notas por párrafo o por mensaje. Las secciones **Favoritos**, **Notas** y **Resaltados** del menú lo reúnen todo. Se guarda en el navegador (`localStorage`, clave `branham-study`).

## Biblia

Sección "Biblia" (debajo de Mensajes): los 66 libros en Reina-Valera 1960 (`Resources/biblia_rv1960.json`), con navegación por libro/capítulo, búsqueda por palabra o referencia (`Juan 3:16`) y compartir versículos. La **IA de la Biblia** solo muestra versículos reales del archivo; el modelo únicamente elige y explica brevemente.

Variable opcional en `.env`: `GEMINI_BIBLE_API_KEY` (si falta, usa `GEMINI_API_KEY`).

También incluye Nota múltiple y edición/eliminación de mensajes en el chat.
# biblia-mensaje
# biblia-mensaje
# biblia-mensaje
# mensaje-biblia
# mensaje-biblia
# mensajesbiblia
