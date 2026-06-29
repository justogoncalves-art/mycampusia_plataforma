# My Campus.IA — Simulación de plataforma web

> **Unlimited made real.** — Buscador y guía universitaria con IA.
> Simulación funcional construida para presentar a dirección/CTO.

Esta es una **simulación navegable de un solo archivo** de la plataforma web de
**My Campus.IA**, parte del ecosistema **MY PATH.IA**. Reúne en una sola aplicación el
buscador de universidades, el buscador de carreras, el perfil vocacional RIASEC, el
comparador y el test Mento.IA, todo siguiendo el design system oficial de la marca
(paleta Forest / Cream / Sand, tipografías Space Grotesk · Quicksand · DM Mono).

---

## Cómo abrirlo

- **`My Campus.IA — standalone.html`** — versión **autónoma de un solo archivo**. Ábrela
  directamente en cualquier navegador (doble clic). No necesita servidor; incluye estilos,
  componentes e imágenes embebidas (las tipografías se cargan desde Google Fonts, requiere
  conexión la primera vez).
- **`My Campus.IA.dc.html`** — archivo fuente editable. Requiere la carpeta `_ds/`
  (design system), `assets/` (imágenes) y `support.js` junto a él.

---

## Estructura del proyecto

```
My Campus.IA.dc.html      Aplicación (fuente): plantilla + lógica
My Campus.IA — standalone.html   Versión autónoma para distribuir
support.js                Runtime de los componentes (no editar)
README.md                 Este archivo
_ds/                      Design system My Campus.IA (tokens, estilos, bundle)
assets/campus/            Fotos de campus y recursos visuales
```

---

## Pantallas y funciones

**Banner superior (en todas las pantallas)**
- Logo My Campus.IA (vuelve al inicio).
- Centro: **Ver resultados de Mento.IA**, **Estadísticas del mundo**, **Hacer test vocacional**.
- Derecha: selector de **idioma ES/EN**, usuario (Martina) y **ajustes**.

**1. Landing** — saludo personalizado, 4 accesos (Afinidad RIASEC, buscar por universidad,
buscar por programa, comparador) y un bloque de frase filosófica.

**2. Tu Afinidad RIASEC** — perfil del alumno (código Holland + 6 ejes) y **10 carreras
ordenadas por % de afinidad** (97 %→57 %) calculadas a partir de Mento.IA. Cada carrera
lleva al listado de universidades filtrado por su área.

**3. Universidades** — vistas **Listado / Mosaico / Mapa**, filtros (país, tipo, idioma,
área, ranking QS, coste, becas) y tarjetas con foto, ranking y favorito (corazón). Cada
universidad abre su **ficha**: rankings QS/THE/ARWU, programas con coste/empleabilidad/
salario, **coste de vida** estimado (alquiler, Airbnb, Booking, comida, transporte) y botón
**Contactar con la universidad**.

**4. Carreras** — buscador + 10 programas relevantes. Cada carrera abre una ficha con
**¿Qué es?**, **¿Qué hace un alumno?**, **salidas profesionales**, competencias y datos de
empleo, con acceso directo a las universidades que la imparten.

**5. Comparador** — enfrenta **hasta 4 universidades o carreras** dato a dato, agrupados por
categoría (identidad, rankings, académico, costes, resultados), resaltando el mejor valor
de cada fila.

**Test vocacional Mento.IA** — popup de bienvenida ("Focused on your future."), detalle del
programa (7 capítulos · 50 min · 15 u$s) y flujo de **Pagar y continuar** → confirmación.

**Asistente IA (Mento)** — burbuja flotante de chat con preguntas sugeridas y respuestas
orientativas sobre perfil, universidades, costes, becas y comparativas.

---

## Datos

Todos los datos son **simulados con fines de demostración**: 10 universidades reales de 9
países con la estructura de campos de la BBDD (rankings, acreditaciones, programas, costes,
empleabilidad, salarios y coste de vida). Las cifras de rankings, precios, alojamiento y
salarios son aproximaciones inventadas, no oficiales.

## Notas técnicas

- Los **favoritos** se guardan en el navegador (localStorage).
- El **idioma** (ES/EN) cambia la navegación y los textos principales.
- El **chatbot** usa respuestas predefinidas por palabra clave (no IA en vivo): listo para
  conectar a un modelo real en una fase posterior.
- El **mapa** es una vista estilizada, no un mapa interactivo con coordenadas.

---

*My Campus.IA · MY PATH.IA — @mypath.ia*
