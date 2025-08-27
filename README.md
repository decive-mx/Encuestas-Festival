# App de Encuestas — Festival Cívico 2025

Aplicación web **estática** (un solo archivo `index.html`) para capturar respuestas de los instrumentos:

- **Anexo 6**: Encuesta de satisfacción (personas asistentes).
- **Anexo 7**: Cuestionario para personal de instituciones participantes (con bloque de voluntariado).

> Las respuestas se guardan localmente (LocalStorage). Se puede **exportar a CSV** por cada formulario o todo consolidado.

---

## Uso rápido (local)
1. Abra `index.html` en su navegador (desde la carpeta o arrastrándolo).
2. Elija el formulario con los botones superiores.
3. Complete y **Guardar respuesta**.
4. En la tarjeta inferior, use **Exportar CSV** o **Exportar todo (CSV)**.

> **Nota:** Si desea crear **dos QR**, utilice estas rutas:
- `?form=anexo6` — asistentes (Anexo 6)
- `?form=anexo7` — personal (Anexo 7)

Ejemplo: si publica en GitHub Pages en `https://usuario.github.io/festival/`, los QR serían:
- `https://usuario.github.io/festival/?form=anexo6`
- `https://usuario.github.io/festival/?form=anexo7`

---

## Publicar en GitHub Pages
1. Cree un repositorio nuevo (p. ej. `festival-encuestas`).
2. Suba **solo** `index.html` (y opcionalmente este `README.md`).
3. Active **Pages** (en *Settings → Pages → Deploy from a branch*).
4. Espere a que quede disponible la URL pública.

## Incrustar en Genially
- En su Genially, inserte un **elemento externo (iframe)** y pegue la URL pública de su `index.html` (con el parámetro `?form=anexo6` o `?form=anexo7`).
- Ajuste alto/alto automático y permita el *scroll* interno.

---

## Exportar y compartir
- **CSV**: el archivo incluye columnas para edad, género, texto abierto y cada reactivo con valor numérico (1–5) y etiqueta.
- **Compartir**: si su navegador móvil permite *Web Share*, puede compartir el CSV directamente; de lo contrario, copie el contenido.

## Privacidad
- No hay backend: nada se envía a servidores externos.
- Si necesita centralizar datos, puede montar un endpoint propio y adaptar `exportAll()` para hacer un `fetch` `POST` (JSON o CSV).

---

Hecho con ❤️ en 2025-08-26.
