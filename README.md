# Tómbola de Repaso

Juegos de preguntas por equipos para la sala de clases. Escribes tus preguntas, armas los equipos con la lista del curso y proyectas el juego: la tómbola elige quién responde, hay rebote, comodines y preguntas de oro.

Es una página web estática, gratuita y sin registro. Funciona en cualquier navegador.

## Cómo se usa

1. **Crea un juego.** En la biblioteca, «+ Nuevo juego» abre el editor. Escribe cada pregunta, sus alternativas y marca la correcta. Si quieres, agrega una explicación, una pista y por qué cada incorrecta no lo es.
2. **O pega tus preguntas desde Word o Docs** con este formato (la correcta lleva un asterisco):

   ```
   1. ¿Quién propuso la separación de los poderes del Estado?
   A) Rousseau
   *B) Montesquieu
   C) Voltaire
   D) Olympe de Gouges
   Explicación: Montesquieu la propuso en El espíritu de las leyes (1748).
   Pista: Revisa la sección I.c de la guía.
   Tema: La Ilustración
   ```

   Explicación, Pista y Tema son opcionales. Deja una línea en blanco entre preguntas. Para verdadero o falso, usa solo A y B.
3. **Revisa.** El editor avisa si falta algo y si la alternativa correcta es bastante más larga que las demás, para que no se adivine sin leer.
4. **Juega.** En «Equipos y ajustes» pega la lista del curso y reparte los equipos al azar (de 1 a 6 equipos).

## Reglas del juego

- Los equipos se turnan las preguntas. La tómbola elige a un integrante del equipo en turno y solo esa persona responde.
- Respuesta correcta: 100 puntos. Si falla, hay rebote: la ruleta elige otro equipo y, si acierta, gana 50.
- Tres aciertos seguidos suman 50 puntos de racha (hasta dos veces por equipo).
- Comodines por equipo: 50/50, Susurro (30 segundos para consultar con el equipo) y Pista.
- Cada equipo tiene una pregunta de oro escondida que vale el doble.
- Faltas de conducta (gritar o pararse del asiento): la primera es advertencia y después cada una descuenta 50 puntos.

Teclado: `S` sortear · `A`–`D` responder · `R` rebote · `Enter` siguiente · `←` `→` moverse entre preguntas.

## Dónde se guardan los datos

Todo queda en el navegador donde usas la página: tus juegos, las listas de curso y las partidas en curso. No se envía nada a ningún servidor. Para llevar un juego a otro computador, usa «Descargar respaldo» y luego «Cargar respaldo» en el otro equipo.

## Juegos incluidos

Los juegos de la carpeta [`juegos/`](juegos/) aparecen para cualquier persona que abra la página, en la sección «Juegos incluidos». Para agregar uno:

1. En la página, abre el juego y usa «Descargar respaldo». Se descarga un archivo `.json`.
2. Sube ese archivo a la carpeta `juegos/` de este repositorio.
3. Agrega el nombre del archivo a [`juegos/index.json`](juegos/index.json), por ejemplo:

   ```json
   ["razon-y-revolucion.json", "mi-nuevo-juego.json"]
   ```

Quien abra un juego incluido puede jugarlo o copiarlo a sus juegos para modificarlo.

## Para la casa: modo individual

Cada juego incluido tiene una versión para responder solo, desde el celular y en familia, sin equipos ni tómbola:

```
https://<usuario>.github.io/<repositorio>/individual.html?juego=dados-y-datos
```

Cambia `dados-y-datos` por el nombre del archivo del juego (sin `.json`). En la plataforma, el botón «Para la casa» de cada juego incluido abre este link. `individual.html` sin `?juego=` muestra la lista de juegos disponibles.

- El estudiante escribe su nombre y curso, y responde una pregunta por pantalla, con un solo intento.
- Puede pedir una pista y, después de responder, ve la respuesta correcta con su explicación.
- Si cierra el navegador, continúa donde quedó.
- Al final aparece una tarjeta con su puntaje, las preguntas acertadas, la fecha, las pistas usadas y el número de intento. La idea es que le tome una captura de pantalla y se la envíe al profesor.
- Nada se envía a un servidor: el nombre y las respuestas quedan solo en ese celular.

## Publicar con GitHub Pages

En el repositorio: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, rama `main`, carpeta `/ (root)`. La página queda en `https://<usuario>.github.io/<repositorio>/`.

## Archivos

- `index.html`: la plataforma completa (HTML, CSS y JavaScript en un solo archivo).
- `individual.html`: el modo individual para el celular.
- `juegos/index.json`: lista de juegos incluidos.
- `juegos/*.json`: cada juego incluido, en el mismo formato que «Descargar respaldo».
