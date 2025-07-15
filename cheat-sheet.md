# Tailwind CSS Cheat Sheet

---

## ✅ Tailwind Utility Class Pattern Sheet — **Memorize by Heart**

### 🧠 General Pattern

```
<property-abbreviation>-<value>
<responsive>:<property>-<value>
<state>:<property>-<value>
```

---

### 1. 🌈 **Colors**

```
text-{color}-{shade}        → text-red-500
bg-{color}-{shade}          → bg-blue-100
border-{color}-{shade}      → border-gray-300
placeholder-{color}-{shade} → placeholder-green-400

Common Colors: red, green, blue, yellow, purple, pink, indigo, gray, slate, emerald, amber
Shades: 50 → 900 (lighter to darker)
```

---

### 2. 📦 **Container & Spacing**

#### 🧱 Padding & Margin

```
p-{n}    → padding: e.g. p-4
pt-{n}   → padding-top
px-{n}   → padding-left & right

m-{n}    → margin
mx-auto  → margin-left & right: auto
```

#### 🧭 Container

```
container     → Centers the content and adds padding
mx-auto       → Horizontally center
```

---

### 3. 🔠 **Typography**

```
text-{size}          → text-sm | text-lg | text-2xl
font-{weight}        → font-bold | font-light | font-medium
leading-{value}      → line-height
tracking-{value}     → letter-spacing
italic / not-italic  → font-style
underline / no-underline
text-{color}-{shade} → text-red-600
```

---

### 4. 📏 **Sizing**

```
w-{n}         → width: e.g. w-10
w-full        → 100% width
h-{n}         → height
min-w-{n}     → min-width
max-w-{n}     → max-width
```

---

### 5. 📐 **Layout & Position**

```
block, inline-block, inline
absolute, relative, fixed, sticky
top-{n}, bottom-{n}, left-{n}, right-{n}
z-{index}      → z-10, z-50, z-0
```

---

### 6. 🌄 **Backgrounds & Shadows**

```
bg-{color}-{shade}
bg-gradient-to-{direction} → bg-gradient-to-r
from-{color}, to-{color}

shadow          → default box-shadow
shadow-md/lg/xl → intensity
```

---

### 7. 🎯 **Borders**

```
border              → border: 1px solid
border-2 / border-4 → thickness
border-{side}       → border-t, border-l
rounded             → border-radius
rounded-{side}-{size} → rounded-tl-lg
```

---

### 8. 🧪 **Filters**

```
filter, backdrop-filter
blur, brightness, contrast, grayscale
e.g., blur-sm, grayscale, brightness-75
```

---

### 9. 🧩 **Interactivity**

```
cursor-pointer
pointer-events-none
select-none
hover:, focus:, active:
e.g. hover:bg-blue-500, focus:outline-none
```

---

### 10. 📱 **Breakpoints (Responsive)**

```
sm:   ≥640px
md:   ≥768px
lg:   ≥1024px
xl:   ≥1280px
2xl:  ≥1536px

Usage:
md:bg-red-500 → applies only on md and above
```

---

### 11. 🧱 **Columns**

```
columns-{n} → columns-2 (for multi-column layout)
```

---

### 12. 📦 **Flexbox**

```
flex             → display: flex
flex-row, flex-col
items-center     → align-items: center
justify-between  → justify-content
gap-{n}          → gap between children
```

---

### 13. 🧮 **Grid**

```
grid
grid-cols-{n}       → grid-cols-3
col-span-{n}
gap-{n}
```

---

### 14. 🎛️ **Transform & Transition**

```
transform             → Enables transform
scale-{n}, rotate-{n}, translate-x-{n}
transition            → transition-all
duration-{ms}         → duration-300
ease-in, ease-out
```

---

### 15. 🌀 **Animation**

```
animate-spin
animate-bounce
animate-ping
```

---

### 16. 🧭 **Transitions**

```
transition             → transition-all
transition-colors      → only color-related transitions
ease-{type}            → ease-in, ease-out
duration-{ms}          → duration-500
```

---

### 17. 🧾 **Tables**

```
table, table-auto, table-fixed
border-collapse, border-separate
```

---

### 18. ✨ **Effects**

```
shadow, opacity, mix-blend-mode, backdrop-blur
e.g. opacity-50, backdrop-blur-md
```

---

### 19. 🛠️ **Customization**

```js
// tailwind.config.js
theme: {
  extend: {
    colors: {
      brand: '#123456',
    },
    spacing: {
      '72': '18rem',
    }
  }
}
```

---

### 20. 🌙 **Dark Mode**

```
dark: prefix for dark mode
e.g. dark:bg-black, dark:text-white

// tailwind.config.js
darkMode: 'class' | 'media'
```

---

## 📌 Memorization Tips

| Abbreviation   | Meaning         | Example                     |
| -------------- | --------------- | --------------------------- |
| `p`, `m`       | padding, margin | `p-4`, `mx-auto`            |
| `w`, `h`       | width, height   | `w-full`, `h-12`            |
| `bg`           | background      | `bg-red-500`                |
| `text`         | text styling    | `text-xl`, `text-green-700` |
| `flex`, `grid` | layout          | `flex-row`, `grid-cols-2`   |
| `rounded`      | border-radius   | `rounded-lg`                |
| `shadow`       | box shadow      | `shadow-md`                 |
| `hover:`       | hover state     | `hover:bg-blue-500`         |
| `sm:`–`2xl:`   | breakpoints     | `md:text-lg`                |

--- 
