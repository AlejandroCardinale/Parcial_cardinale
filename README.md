# 🎮 GameHub — Gestión de Videojuegos

Aplicación web desarrollada con **Angular 21** para la gestión y visualización de un catálogo de videojuegos. Proyecto académico que implementa los conceptos fundamentales del framework Angular: componentes standalone, enrutamiento SPA, servicios, inyección de dependencias, directivas de control de flujo y pipes.

---

## 📋 Descripción del Proyecto

GameHub es una aplicación de una sola página (SPA) que permite:

- 🏠 Visualizar una **página principal** con bienvenida y descripción del sistema.
- 🎮 Explorar un **catálogo de videojuegos** presentado mediante cards de Bootstrap 5.
- 💰 Ver el **precio en pesos argentinos** (ARS) formateado con `CurrencyPipe`.
- 🟢🔴 Identificar si cada juego está **disponible o agotado** con indicadores visuales.
- 🔤 Ver los géneros con formato correcto usando `TitleCasePipe`.

---

## 🛠️ Tecnologías Utilizadas

| Tecnología | Versión | Uso |
|---|---|---|
| **Angular** | 21.x | Framework principal (componentes standalone) |
| **TypeScript** | 5.x | Lenguaje de programación |
| **Bootstrap** | 5.x | Framework CSS para diseño responsive |
| **Bootstrap Icons** | 1.x | Librería de íconos SVG |
| **Node.js** | 24.x | Entorno de ejecución |
| **Angular CLI** | 21.x | Herramienta de scaffolding y build |

---

## 🏗️ Estructura del Proyecto

```
GameHub/
├── src/
│   ├── index.html                        # HTML principal con meta SEO
│   ├── main.ts                           # Bootstrap de la aplicación
│   ├── styles.css                        # Estilos globales + imports Bootstrap
│   │
│   └── app/
│       ├── app.ts                        # Componente raíz (layout)
│       ├── app.html                      # Template raíz (navbar + router-outlet)
│       ├── app.routes.ts                 # Configuración de rutas SPA
│       ├── app.config.ts                 # Config global (locale es-AR, router)
│       │
│       ├── models/
│       │   └── videojuego.model.ts       # Interface Videojuego (entidad)
│       │
│       ├── services/
│       │   └── videojuegos.ts            # VideojuegosService (datos + lógica)
│       │
│       ├── components/
│       │   └── navbar/
│       │       ├── navbar.ts             # NavbarComponent (standalone)
│       │       ├── navbar.html           # Template con routerLink
│       │       └── navbar.css            # Estilos del navbar
│       │
│       └── pages/
│           ├── home/
│           │   ├── home.ts               # HomeComponent (standalone)
│           │   ├── home.html             # Hero + info cards
│           │   └── home.css              # Estilos animados de la home
│           │
│           └── videojuegos/
│               ├── videojuegos.ts        # VideojuegosComponent (standalone)
│               ├── videojuegos.html      # Grid de cards con @for, @if, pipes
│               └── videojuegos.css       # Estilos de las game cards
│
├── package.json
├── angular.json
└── tsconfig.json
```

---

## ✅ Requisitos Académicos Implementados

| Requisito | Implementación | Archivo |
|---|---|---|
| Página principal con bienvenida | Hero section + descripción | `home.html` |
| Página de listado funcional | Grid de cards con datos reales | `videojuegos.html` |
| Interfaz de entidad | `interface Videojuego` con 6 atributos | `videojuego.model.ts` |
| Servicio con datos precargados | `VideojuegosService` con 10 juegos + `obtenerVideojuegos()` | `videojuegos.ts (service)` |
| Ruteo configurado | 4 rutas: `/`, `/home`, `/videojuegos`, `**` | `app.routes.ts` |
| Navbar con routerLink | Links a Inicio y Videojuegos con estado activo | `navbar.html` |
| Inyección de dependencias | `inject(VideojuegosService)` en el componente | `videojuegos.ts (page)` |
| Interpolación `{{ }}` | Título, género, plataforma, precio, ID | `videojuegos.html` |
| `@for` con `track` | Itera la lista completa de juegos | `videojuegos.html` |
| `@if / @else` | Badge "Disponible" / "Agotado" | `videojuegos.html` |
| `@if` lista vacía | Mensaje alternativo si no hay juegos | `videojuegos.html` |
| `CurrencyPipe` | Precio en pesos ARS: `$ 59,99` | `videojuegos.html` |
| `TitleCasePipe` | Género con formato título: `Aventura` | `videojuegos.html` |
| Bootstrap 5 | Cards, grid, badges, navbar responsive | Global |
| Diseño visual profesional | Dark theme, gradientes, animaciones | CSS files |
| Comentarios en el código | JSDoc en todos los archivos `.ts` | Todos los `.ts` |

---

## 👨‍💻 Autor

Desarrollado como proyecto académico para la materia de Desarrollo Web con Angular.

---

## 📄 Licencia

Este proyecto es de uso académico.
