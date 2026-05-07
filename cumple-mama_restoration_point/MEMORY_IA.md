# 🎂 Proyecto: Cumpleaños Mamá — Página Web de Regalo

**Dueño:** Facundo Menna (mennafacundoagustin@gmail.com)  
**Fecha de inicio:** 2026-05-05  
**Entrega:** Jueves (cumpleaños de la mamá de Facundo)  
**Estado:** ✅ Página base completa — pendiente agregar fotos reales

---

## 🎯 Objetivo del proyecto

Crear una página web de regalo de cumpleaños para la mamá de Facundo.
- Expresar amor con texto: razones, poema, carta
- Collage de fotos al final (Facundo las agrega después)
- Estética premium, oscura, romántica con corazones animados
- Debe ser espectacular visualmente

---

## ✅ Lo que ya está hecho (index.html)

La página tiene estas secciones en orden:

1. **Hero** — Emoji ❤️ gigante + título "Mamá, te amo" con gradiente + subtítulo
2. **Carta** — Párrafo introductorio en itálica con glassmorphism
3. **8 Razones** — Cards con glassmorphism, hover 3D, íconos flotantes:
   - 01 Tu amor sin condiciones
   - 02 El hogar que construiste
   - 03 Tu fuerza silenciosa
   - 04 Esos sabores que son hogar
   - 05 Que siempre creíste en mí
   - 06 Tu risa
   - 07 Lo que me enseñaste a ser
   - 08 Simplemente vos
4. **Poema** — "Desde que tengo memoria" (3 estrofas)
5. **Collage** — 7 slots placeholder (1 grande + 6 chicos) listos para fotos
6. **Final** — "Feliz cumpleaños, Mamá" + mensaje + firma "Con todo mi amor, Facu ❤️"

### Animaciones implementadas
- Canvas con 45 corazones flotantes de fondo (toda la página)
- Burst de corazones al hacer click (10 corazones por click)
- Fade-in con slide-up al hacer scroll (IntersectionObserver)
- Delays escalonados en cards y slots
- Heartbeat en el emoji del hero
- Float animation en los íconos de las cards

### Stack
- HTML + CSS + JavaScript vanilla (sin frameworks, sin build)
- Google Fonts: Playfair Display (serif elegante) + Lato
- **Para abrir:** doble click en `index.html` → se abre en el navegador

---

## 🔄 Pendiente (lo que falta)

### ⭐ PRIORITARIO: Agregar fotos al collage

Facundo tiene que:
1. Copiar las fotos a la carpeta `fotos/`
2. En `index.html`, buscar los `<div class="slot ...">` del collage
3. Reemplazar el contenido placeholder de cada slot con una `<img>`:

**Antes (placeholder):**
```html
<div class="slot slot-featured reveal">
  <span class="slot-icon">📷</span>
  <span class="slot-label">foto principal</span>
</div>
```

**Después (con foto real):**
```html
<div class="slot slot-featured reveal">
  <img src="fotos/foto1.jpg" alt="Foto con mamá">
</div>
```

Los slots en orden son:
- `.slot-featured` → foto grande (ocupa 2 columnas × 2 filas) — poner la mejor foto
- Slots 2 al 7 → fotos regulares (1×1)

### Opcional: personalizar textos
- La firma dice **"Facu"** — cambiar si el usuario se llama diferente o quiere firmar distinto
- Los textos de las razones son genéricos y lindos — Facundo puede editarlos con anécdotas reales
- El poema puede editarse libremente

### Opcional: agregar música
Agregar antes de `</body>` para que suene al abrir:
```html
<audio autoplay loop style="display:none">
  <source src="fotos/cancion.mp3" type="audio/mpeg">
</audio>
```
(poner el MP3 en la carpeta `fotos/`)

### Opcional: Deploy para acceder desde cualquier dispositivo
La página es estática (solo archivos), se puede subir a Vercel gratis:
1. Crear cuenta en vercel.com
2. Arrastrar la carpeta `cumple-mama/` al dashboard
3. Vercel da una URL pública para compartir por WhatsApp

---

## 📁 Estructura actual

```
cumple-mama/
├── index.html       ← La página (abrir con doble click)
├── fotos/           ← Carpeta vacía: poner fotos acá
│   └── (vacío)
└── MEMORY_IA.md     ← Este archivo
```

---

## 🎨 Diseño / paleta / estilo

| Elemento | Valor |
|---|---|
| Fondo | `#0a0008` (negro burgúndy muy oscuro) |
| Acento | `#c9184a` (rosa intenso) |
| Rosa claro | `#ff6b8a` / `#ffb3c6` |
| Crema | `#fff0f3` |
| Fuente titulares | Playfair Display (serif, italiano) |
| Fuente body | Lato (sans-serif, limpio) |

---

## 🤖 Instrucciones para la IA que continúe

Si Facundo dice "continuá el proyecto cumple-mama" o similar:

1. **Leer este archivo primero** antes de cualquier acción.
2. La página base **ya está terminada** en `index.html`. No reescribirla.
3. Lo más probable que pida:
   - **A)** Integrar fotos: leer los `<div class="slot">` en el collage y reemplazar por `<img src="fotos/NOMBRE">`.
   - **B)** Cambiar algún texto (razones, poema, firma).
   - **C)** Agregar música de fondo.
   - **D)** Deploy en Vercel.
4. Para editar el HTML usar la herramienta **Edit** con el string exacto a reemplazar.
5. El archivo está en: `C:\Users\menna\OneDrive\Desktop\Proyectos de Velion\cumple-mama\index.html`
6. Las fotos irán en:  `C:\Users\menna\OneDrive\Desktop\Proyectos de Velion\cumple-mama\fotos\`

---

## 💡 Notas extras

- Facundo usa React + TypeScript normalmente, pero esta página es HTML vanilla para que la mamá la abra sin instalar nada.
- Todas las animaciones usan Canvas API nativo + CSS, sin dependencias externas.
- La página es responsive (funciona en móvil y desktop).
