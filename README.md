```
 ████████╗ █████╗ ██╗     ██╗     ███████╗██████╗     ██████╗
    ██╔══╝██╔══██╗██║     ██║     ██╔════╝██╔══██╗   ╚════██╗
    ██║   ███████║██║     ██║     █████╗  ██████╔╝    █████╔╝
    ██║   ██╔══██║██║     ██║     ██╔══╝  ██╔══██╗    ╚═══██╗
    ██║   ██║  ██║███████╗███████╗███████╗██║  ██║   ██████╔╝
    ╚═╝   ╚═╝  ╚═╝╚══════╝╚══════╝╚══════╝╚═╝  ╚═╝   ╚═════╝
```

### Agencia de Diseño & Desarrollo Web

Sitio web moderno, accesible y responsive construido con HTML5 y Bootstrap 5

---

## 📋 Tabla de contenidos

- [Descripción](#-descripción)
- [Páginas](#-páginas)
- [Tecnologías](#-tecnologías)
- [Estructura del proyecto](#-estructura-del-proyecto)
- [Instalación](#-instalación)
- [Guía Git & GitHub](#-guía-git--github)
- [Características de accesibilidad](#-características-de-accesibilidad)
- [Autor](#-autor)

---

## 📖 Descripción

**Taller 3** es un proyecto web académico desarrollado como parte de un taller de formación. Simula el sitio público y el panel interno de una agencia colombiana de diseño digital, desarrollo web y estrategia.

El proyecto está diseñado con énfasis en:

- **Accesibilidad** — cumple prácticas ARIA, navegación por teclado y saltos de contenido
- **Responsive** — adaptable a dispositivos móviles, tablets y escritorios con la grilla de Bootstrap
- **Rendimiento** — carga diferida de imágenes, preload de assets críticos y CSS/JS minificados
- **Semántica** — uso correcto de etiquetas HTML5 (`nav`, `main`, `section`, `article`, `footer`, `address`)

---

## 📄 Páginas

### 🌐 Sitio público — `index.html`

Página de aterrizaje completa con las siguientes secciones:

| Sección | Descripción |
|---|---|
| **Inicio** | Carrusel a pantalla completa con imágenes de Chicago, Los Ángeles y Nueva York |
| **Servicios** | 6 tarjetas: Desarrollo Web, UI/UX, Analítica, Seguridad, Cloud & DevOps, Soporte 24/7 |
| **Equipo** | Perfiles del equipo: Lead Dev, UX Designer, Backend Dev y Data Analyst |
| **Precios** | 3 planes: Starter ($1.200/mes), Pro ($3.500/mes) y Enterprise (Custom) |
| **FAQ** | 5 preguntas frecuentes con acordeón interactivo |
| **Contacto** | Formulario de contacto + datos de la agencia (Medellín, Colombia) |

### 🏠 Panel interno — `app/index.html`

Dashboard privado que centraliza el acceso a las herramientas internas del proyecto. Contiene tres accesos directos en tarjetas:

- **Tabla** — Directorio de empleados
- **Formularios** — Registro e inicio de sesión
- **GitHub** — Guía de control de versiones

### 📊 Directorio de empleados — `app/tables.html`

Tabla responsive con **20 empleados** y los siguientes campos:

> ID · Nombre · Apellido · Edad · Ciudad · Correo · Teléfono · Cargo · Estado · Fecha de ingreso

### 📝 Formularios — `app/forms.html`

Dos formularios en diseño de dos columnas:

- **Crear cuenta** — Nombre, correo, contraseña, confirmación y opción "Recordar sesión"
- **Iniciar sesión** — Correo, contraseña con enlace "¿Olvidaste tu contraseña?" y opción "Recordar sesión"

### 🐙 Guía Git & GitHub — `app/github.html`

Tutorial paso a paso para conectar un repositorio local con GitHub desde la terminal de VSCode:

```
Paso 1 → Abrir la terminal en VSCode
Paso 2 → Inicializar el repositorio (git init)
Paso 3 → Configurar identidad en Git
Paso 4 → Crear el repositorio en GitHub
Paso 5 → Conectar el repositorio remoto (git remote add origin ...)
Paso 6 → Primer commit y push (git push -u origin main)
```

---

## 🛠 Tecnologías

| Tecnología | Versión | Uso |
|---|---|---|
| **HTML5** | — | Estructura semántica de todas las páginas |
| **Bootstrap CSS** | 5.x | Grid, componentes y utilidades de estilo |
| **Bootstrap JS Bundle** | 5.x | Carrusel, navbar colapsable y acordeón |
| **Bootstrap Icons** | 1.13.1 | Iconografía en toda la interfaz |

> Todos los assets de Bootstrap se sirven de forma **local** (sin CDN externo), excepto Bootstrap Icons que se carga desde `cdn.jsdelivr.net` con técnica de carga no bloqueante.

---

## 📁 Estructura del proyecto

```
taller_3/
│
├── index.html                  # Landing page pública (sitio de la agencia)
│
├── app/
│   ├── index.html              # Panel interno — menú de aplicaciones
│   ├── tables.html             # Directorio de empleados
│   ├── forms.html              # Formularios de registro e inicio de sesión
│   └── github.html             # Guía paso a paso de Git & GitHub
│
└── assets/
    ├── css/
    │   ├── bootstrap.min.css           # Bootstrap completo (minificado)
    │   ├── bootstrap-grid.min.css      # Solo el sistema de grilla
    │   ├── bootstrap-reboot.min.css    # CSS reset de Bootstrap
    │   ├── bootstrap-utilities.min.css # Clases utilitarias
    │   └── *.rtl.min.css              # Variantes RTL (árabe, hebreo, etc.)
    │
    ├── js/
    │   ├── bootstrap.bundle.min.js     # Bootstrap + Popper (minificado)
    │   └── bootstrap.esm.min.js       # Versión ES Modules
    │
    └── img/
        ├── chicago.jpg                 # Imagen carrusel — Chicago
        ├── la.jpg                      # Imagen carrusel — Los Ángeles
        ├── ny.jpg                      # Imagen carrusel — Nueva York
        └── logo_sena.webp              # Logo institucional
```

---

## 🚀 Instalación

No requiere instalación de dependencias ni servidor de build. Solo necesitas un navegador moderno.

**Opción 1 — Abrir directamente:**

```bash
# Clona el repositorio
git clone https://github.com/joanstvn/taller_3.git

# Entra al directorio
cd taller_3

# Abre el archivo principal en tu navegador
open index.html          # macOS
start index.html         # Windows
xdg-open index.html      # Linux
```

**Opción 2 — Con Live Server (recomendado para desarrollo):**

1. Instala la extensión **Live Server** en VSCode
2. Haz clic derecho sobre `index.html`
3. Selecciona **"Open with Live Server"**
4. El proyecto se abre en `http://127.0.0.1:5500`

---

## 🐙 Guía Git & GitHub

El proyecto incluye una guía completa en `app/github.html`. En resumen:

```bash
# 1. Inicializar el repositorio
git init

# 2. Configurar identidad
git config --global user.name "Tu Nombre"
git config --global user.email "tu@correo.com"

# 3. Conectar con GitHub
git remote add origin https://github.com/tu-usuario/taller_3.git

# 4. Subir el proyecto
git add .
git commit -m "feat: primer commit del proyecto"
git branch -M main
git push -u origin main

# 5. Mantener actualizado
git pull
```

---

## ♿ Características de accesibilidad

Este proyecto implementa buenas prácticas de accesibilidad web:

- **Skip link** — enlace "Saltar al contenido principal" visible al navegar con teclado
- **ARIA labels** — atributos `aria-label`, `aria-current`, `aria-expanded` en todos los controles interactivos
- **Roles semánticos** — uso de `role="navigation"`, `role="contentinfo"`, `role="menubar"`
- **Texto alternativo** — todas las imágenes tienen `alt` descriptivo
- **Tabindex** — el elemento `<main>` tiene `tabindex="-1"` para recibir foco programático
- **Captions ocultos** — la tabla tiene `<caption class="visually-hidden">` con descripción completa
- **Contraste** — paleta blanco/negro/gris cumple ratios de contraste WCAG AA
- **Carga no bloqueante** — Bootstrap Icons se carga con `preload` + `onload` para no bloquear el render

---

## 👤 Autor

**Joan Stiven Rios Valderrama**

---

&copy; 2026 Joan Stiven Rios Valderrama · Todos los derechos reservados
