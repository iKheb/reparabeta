# Reparo · Gestión para servicio técnico de celulares

App profesional para tu taller: **clientes y equipos** (con fotos de evidencia y patrón de desbloqueo),
**recibos por WhatsApp**, **gastos de repuestos**, **inventario** con lista "Por pedir",
**ganancias semanales y mensuales**, **registro de actividad** con fecha y hora, y **notificaciones**.

- Funciona en **celular, tablet y computadora**.
- Se **instala como app** (PWA) y **funciona sin internet**: tus datos se guardan en el dispositivo.

## Ponerla en línea con GitHub Pages (una sola vez)

1. Entra a **https://github.com/iKheb/reparabeta** → pestaña **Settings** (Configuración).
2. En el menú izquierdo, abre **Pages**.
3. En **Build and deployment → Source** elige **Deploy from a branch**.
4. En **Branch** elige **main** y la carpeta **/docs**. Pulsa **Save**.
5. Espera 1–2 minutos y recarga esa página: aparecerá
   **"Your site is live at https://ikheb.github.io/reparabeta/"**. Ese es el enlace de tu app.

> El repositorio debe ser **público** para usar GitHub Pages gratis (o tener un plan que lo permita en privados).

## Instalarla como app

- **Android (Chrome):** abre el enlace → menú ⋮ → **Instalar app** (o "Agregar a pantalla principal").
- **iPhone / iPad (Safari):** abre el enlace → botón **Compartir** → **Agregar a inicio**.
- **Computadora (Chrome / Edge):** abre el enlace → ícono de instalar en la barra de direcciones.

Después de abrirla una vez con internet, funciona **sin conexión**.

## Importante sobre tus datos

- Los datos viven **en cada dispositivo** (no en la nube). Si usas la app en el celular y en la PC,
  cada uno tiene sus propios datos, salvo que actives la sincronización con el servidor opcional (ver `server/README.md`).
- Haz **respaldos** desde **Ajustes → Datos y respaldo → Descargar respaldo** de forma periódica.
  Si borras los datos del navegador o desinstalas la app sin respaldo, los datos se pierden.

## Para desarrolladores

```bash
npm install
npm run dev        # desarrollo en http://localhost:5173
npm test           # pruebas
npm run build      # compila la app en docs/ (lo que publica GitHub Pages)
npm run server     # servidor opcional: sincronización entre dispositivos + notificaciones push
```

Código: React + TypeScript + Vite, Three.js (3D), Dexie (IndexedDB), service worker propio.
Arquitectura en `ARCHITECTURE.md`.
