<div align="center">
  <br />
  <br />
  
  # <code>TINYSHOW_ALPHA</code>
  
  **MINIMAL PORTFOLIO PLATFORM / JSON-DRIVEN**
  
  <br />

  <img src="https://img.shields.io/badge/ASTRO-FF5D01?style=for-the-badge&logo=astro&logoColor=white" alt="Astro" />
  <img src="https://img.shields.io/badge/REACT-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React" />
  <img src="https://img.shields.io/badge/TYPESCRIPT-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />


  <br />
  <br />
</div>

---

### 00. PREVIEW

![Portfolio Preview](portada.webp)

> **ABSTRACT:** Sistema de portafolio minimalista impulsado por un solo archivo JSON. Arquitectura estática con Astro + React para mostrar proyectos sin base de datos ni backend. Actualización mediante edición directa de `projects.json`.
>
> <br />
>
> **DEMO LIVE:** [tinyshow-alpha.vercel.app](https://tinyshow-alpha.vercel.app/)

---

### 01. ARCHITECTURE & DECISIONS

| COMPONENT | TECH | NOTE |
| :--- | :--- | :--- |
| **Core** | `Astro` | Static site generation, zero JS by default. |
| **UI** | `React (TSX)` | Island architecture for interactive components. |
| **Components** | `Shadcn/ui` | Radix UI primitives with Tailwind. |
| **Styles** | `Tailwind CSS` | Utility-first styling approach. |
| **Type Safety** | `TypeScript` | Strict mode enabled. |
| **Data Source** | `projects.json` | Single source of truth for portfolio content. |

<br>

### 02. INSTALLATION



*Run local environment:*

```bash
# 1. Clone or use template
git clone https://github.com/samuhlo/tinyshow-alpha.git
# OR
pnpm create astro@latest -- --template samuhlo/tinyshow-alpha

# 2. Navigate & install dependencies (pnpm enforced)
cd tinyshow-alpha
pnpm install

# 3. Ignite dev server
pnpm dev
```

*Access at [http://localhost:4321](http://localhost:4321)*

---

### 03. USAGE & CONFIGURATION

#### A. PROJECTS DATA STRUCTURE



Edit `projects.json` to manage portfolio content:

```json
[
  {
    "title": "Project Name",
    "description": "Technical description of what it does",
    "languages": ["typescript", "css", "html"],
    "image": "/project_images/screenshot.webp",
    "url": "https://project-demo.com",
    "github": "https://github.com/user/repo"
  }
]
```

**SCHEMA:**
- `title`: Project display name
- `description`: Brief technical summary
- `languages`: Array of tech tags (affects badge colors)
- `image`: Path to preview image (recommended: 1200×600px)
- `url`: Live demo URL (optional)
- `github`: Repository URL (optional)

<br>

#### B. LANGUAGE COLOR CUSTOMIZATION

Modify badge colors in component logic:

```typescript
// Example: src/components/ui/badge.tsx or similar
const languageColors = {
  typescript: "#3178c6",
  javascript: "#f1e05a",
  python: "#3572A5",
  // Add more as needed
}
```

---

### 04. COMMANDS



| COMMAND | ACTION |
| :--- | :--- |
| `pnpm dev` | Start dev server at `localhost:4321` |
| `pnpm build` | Generate static build in `./dist/` |
| `pnpm preview` | Preview production build locally |

<br>

### 05. DEPLOYMENT

**Vercel (Recommended):**
1. Push repo to GitHub/GitLab
2. Import project in Vercel dashboard
3. Auto-detected as Astro project
4. Deploy

**Alternative platforms:** Netlify, Cloudflare Pages, GitHub Pages (any static host).

---

<div align="center">


<code>DESIGNED & CODED BY @samuhlo</code>


<small>Lugo, Galicia</small>

</div>
