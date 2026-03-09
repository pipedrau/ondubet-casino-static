# Sistema de Diseño Hondubet - Documentación

> Investigación realizada el 9 de Marzo de 2026 desde Hondubet.com

## 1. Paleta de Colores

### Colores Primarios
| Nombre | Hex | Uso |
|--------|-----|-----|
| Primary Background | `#151c30` | Fondo principal de la app |
| Secondary Background | `#0d1220` | Fondos más oscuros, headers |
| Accent Cyan | `#28CDDF` | Acentos principales, CTAs, highlights |
| Accent Cyan Light | `#34C6E9` | Versión clara del accent |
| Accent Dark | `#003746` | Fondos de gradient |
| Gradient Start | `#8a2be2` (purple) | Gradientes decorativos |

### Colores Semánticos
| Nombre | Hex | Uso |
|--------|-----|-----|
| Success/Green | `#00ff88` | Saldo, ganancias, wins |
| Warning | `#ffab00` | Warnings, saldo bajo |
| Error | `#ff1744` | Errores, pérdidas |
| Text Primary | `#ffffff` | Texto principal |
| Text Muted | `#a0a4b8` | Texto secundario |
| Text Gray | `#71717a` | Texto disabled |

### Gradientes
```css
/* Gradient principal */
bg-gradient-to-tr from-hgradient-50 to-hgradient-100
/* radial gradient decorativo footer */
bg-[radial-gradient(71.39%_51.03%_at_50%_50%,rgba(138,43,226,0.3)_0%,rgba(138,43,226,0)_98%)]
```

---

## 2. Tipografía

### Familias de Fuente
| Fuente | Uso |
|--------|-----|
| DM Sans | Texto principal (font-text) |
| Poppins | Títulos secundarios |
| Montserrat | Texto UI |
| Bungee Shade | Logos/Títulos destacados |
| Pacifico | Decorative (poco uso) |

### Tamaños Típicos
- `text-xs`: 12px - Metadata, timestamps
- `text-sm`: 14px - Texto secundario, chips
- `text-base`: 16px - Cuerpo de texto
- `text-lg`: 18px - Subtítulos
- `text-xl` / `text-2xl`: 20-24px - Títulos de sección
- `text-3xl+`: 30px+ - Headlines principales

### Pesos
- `font-normal`: 400 - Texto regular
- `font-medium`: 500 - Texto enfatizado
- `font-semibold`: 600 - Buttons, labels
- `font-bold`: 700 - Títulos

---

## 3. Componentes UI

### Buttons

**Primary Button:**
```css
bg-gradient-to-tr from-hgradient-50 to-hgradient-100
text-transparent (para gradient text)
rounded-small / rounded-2xl
px-4 py-2
font-semibold
```

**Secondary/Outline:**
```css
bg-transparent
border border-hgradient-100
text-hgradient-100
```

**Nav Items:**
```css
rounded-full
transition-all ease-in-out duration-300
navbar-item-active / navbar-item-inactive
```

### Cards

**Game Cards:**
```css
bg-default-100 (o bg-card)
rounded-lg
hover:scale-105 transition
aspect-ratio 16/9 o similar
```

**Skeleton Loading:**
```css
bg-default-100 rounded
animate-[fade_1.5s_ease-in-out_infinite]
```

### Navigation
- Bottom nav móvil: `fixed bottom-0`, `backdrop-blur-md`
- Nav items: ícono + label, `rounded-full`
- Nav activo: `bg-white/15`

### Badges/Chips
```css
rounded-full
px-3 py-1
text-xs font-bold
bg-accent / bg-success
```

---

## 4. Layout & Espaciado

### Container
- `max-w-8xl` (para contenido principal)
- `px-4 sm:px-8` padding horizontal
- Centered con `mx-auto`

### Grid
- `grid-cols-1` mobile
- `lg:grid-cols-2` tablet
- `gap-4` o `gap-6`

### Mobile
- Bottom navigation fixed
- Full width cards
- Touch-friendly: min 44px tap targets

---

## 5. Proveedores (Casino)

Logos de proveedores visibles (con filter para hacerlos blancos):
- Evolution
- Pragmatic Play
- Ezugi
- GameArt
- NetEnt
- PlayTech
- Spribe
- Y muchos más (~70 proveedores)

### Estilo de Logos
```css
filter brightness-0 invert  /* Para mostrar en dark theme */
w-auto h-auto
object-contain
```

---

## 6. Imágenes & Assets

### tratamiento de Imágenes
- `object-contain` para logos
- `object-cover` para backgrounds
- `aspect-ratio` para mantener proporciones
- Lazy loading con `loading="lazy"`

### Efectos
- Glow effects con box-shadow y transparency
- Gradientes radiales en backgrounds
- Blur overlays para modals

---

## 7. Mobile UX

### Bottom Navigation
```css
fixed bottom-0
bg-black/50 backdrop-blur-md
border-t border-white/10
5 items: Inicio, Casino, Deportes, Misiones, Menu
```

### Touch Targets
- Minimum 44x44px
- Full-width en mobile
- Swipe gestures para carousels

---

## 8. Casino Específico

### Game Card Structure
```
┌────────────────────────┐
│   [Game Thumbnail]    │  ← 16:9 aspect ratio
│        🎰              │
├────────────────────────┤
│  Sweet Bonanza        │  ← title, truncated
│  Pragmatic Play       │  ← provider, muted
└────────────────────────┘
```

### Categorías
- Recomendados
- Tragamonas
- Casino Live
-jackpots
- Torneos

### Estados de Juego
- Disponible
- Jugando (modal/iframe)
- Error

---

## 9. Tokens CSS (Tailwind)

Basado en el análisis, los tokens key son:
- `hprimary-*` / `hsecondary-*` → colores brand
- `hgradient-*` → gradientes
- `hbackground` → fondo
- `default-100` → card backgrounds
- `sivarbet-*` → algunos componentes legacy

---

## 10. Referencias Visuales

### Fútbol Honduras (Sponsors visible)
- Liga Nacional de Fútbol Honduras
- Olimpia, Marathon, Motagua, Real España
- etc.

### Promociones Vistas
- Bono bienvenida 100% hasta L.1,500
- Bono primer depósito 300%
- Torneos (Casino Caribeño)
- Jackpots

---

## Próximos Pasos

1. Implementar tokens en el prototipo
2. Usar DM Sans como font principal
3. Aplicar gradientes cyan/purple
4. Matching de componentes con esta specs

---

*Documento generado automáticamente desde análisis de Hondubet.com*
