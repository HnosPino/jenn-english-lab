# Jenn English Lab 📲

Curso **libre y gratuito** de inglés A1 → B2: vocabulario, gramática, lectura, escucha y escritura, con seguimiento del progreso y simulacros tipo Cambridge (A2 Key, B1 Preliminary, B2 First).

- Es una **app web instalable (PWA)**: se instala en Android, iPhone, Windows y Mac desde el navegador, con su ícono propio.
- **Funciona sin conexión** después de abrirla la primera vez.
- No tiene anuncios, no pide cuenta y no envía datos: el progreso queda guardado en el dispositivo.
- Licencias: el código es **MIT** y el contenido **CC BY-SA 4.0** (ver `LICENSE`).

## Contenido de la carpeta

| Archivo | Para qué sirve |
|---|---|
| `index.html` | La app completa: diseño, contenido y lógica en un solo archivo |
| `manifest.webmanifest` | Nombre, colores e íconos para instalarla como app |
| `sw.js` | Permite que funcione sin internet |
| `icons/` | Íconos de la app |
| `LICENSE` | Licencias libres |

> ⚠️ Para que se pueda instalar y funcione sin conexión, la carpeta tiene que estar publicada en una dirección **https**. Si abres `index.html` directamente desde tu computador, la app funciona, pero no se puede instalar.

---

## Opción 1 · Netlify Drop (la más fácil, unos 2 minutos, sin escribir código)

1. Entra a **https://app.netlify.com/drop**.
2. Arrastra la **carpeta completa** `jenn-english-lab` a la página.
3. Netlify te da una dirección como `https://nombre-al-azar.netlify.app`. Si creas una cuenta gratuita, puedes cambiarle el nombre (por ejemplo `jenn-english-lab.netlify.app`).
4. Comparte ese enlace. Cualquier persona lo abre y la instala.

## Opción 2 · GitHub Pages (gratis y con el código abierto al público)

1. Crea una cuenta en **https://github.com**.
2. Pulsa **New repository**, ponle de nombre `jenn-english-lab`, márcalo como **Public** y créalo.
3. Pulsa **Add file → Upload files** y arrastra **todo lo que hay dentro** de la carpeta (no la carpeta en sí). Luego pulsa **Commit changes**.
4. Ve a **Settings → Pages**. En *Source* elige **Deploy from a branch**, rama `main`, carpeta `/ (root)`, y guarda.
5. En 1 o 2 minutos la app queda publicada en `https://TU-USUARIO.github.io/jenn-english-lab/`.

Otros servicios gratuitos que también sirven: Cloudflare Pages y Vercel.

## Instalarla en el dispositivo

- **Android (Chrome):** abre el enlace y pulsa el botón **📲 Instalar app** de la pantalla de inicio, o ve al menú ⋮ → *Instalar app*.
- **iPhone / iPad (Safari):** pulsa Compartir ⬆️ → *Agregar a inicio*.
- **Computador (Chrome / Edge):** pulsa el ícono de instalar que aparece a la derecha de la barra de direcciones.

## ¿Y en Google Play o App Store?

Con la app ya publicada en https:

1. Entra a **https://www.pwabuilder.com** (es gratis y de Microsoft) y pega el enlace de tu app.
2. Pulsa **Package for stores** → **Android**. Obtendrás el paquete listo para subir a Google Play (y también uno para la Microsoft Store).
3. Para publicarla en Google Play necesitas una cuenta de desarrollador; Google cobra una inscripción única. Apple pide una membresía anual y un Mac.

Para que sea **gratuita y libre** no hace falta ninguna tienda: el enlace instalable ya funciona como una app en cualquier dispositivo.

## Cómo editar o ampliar el curso

Abre `index.html` con cualquier editor de texto (VS Code, Bloc de notas…). Todo el contenido está dentro del objeto `CONTENT`:

- `CONTENT.levels`: niveles → unidades (`vocab`, `grammar`, `reading`, `listening`, `writing`).
- `CONTENT.exams`: simulacros. Los tipos de pregunta disponibles son `mc`, `text`, `cloze`, `open`, `wf`, `kwt`, `listen` y `write`.
- `CONTENT.decks`: mazos de vocabulario con el formato `[inglés, español, categoría, ejemplo]`.

En los ejercicios de opción múltiple, la **primera opción es la correcta** (la app las mezcla al mostrarlas): `["She ___ a teacher.", "is", "are", "am"]`.
Para preguntas de escribir la respuesta se usa: `{q: "I ___ 44 years old.", a: ["am"]}`.

Cada vez que publiques cambios, sube también el número de `VERSION` en `sw.js` (por ejemplo `jel-v2`), para que los dispositivos donde ya está instalada reciban la actualización.

## Progreso entre dispositivos

Ve a **Ajustes → Respaldo**, copia el código y pégalo en *Restaurar* en el otro dispositivo.
