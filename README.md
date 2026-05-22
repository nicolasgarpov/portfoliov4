# 🚀 Portfolio v4 — Ecosistema Profesional

¡Bienvenido a tu nuevo espacio de trabajo de desarrollo! Este proyecto es una plantilla de portafolio moderna, ultra-rápida y altamente escalable. Está construida usando las últimas versiones de **Astro**, **Tailwind CSS v4** y cuenta con integración lista para **Firebase**.

---

## 🛠️ Tecnologías Utilizadas

*   **[Astro v5](https://astro.build/)**: Framework web moderno diseñado para la velocidad. Utiliza la arquitectura de islas para entregar el menor JavaScript posible al cliente.
*   **[Tailwind CSS v4](https://tailwindcss.com/)**: Motor de estilos de última generación, integrado de forma nativa a través de Vite. Ofrece procesamiento ultra veloz y un sistema de configuración simplificado desde hojas de estilo CSS.
*   **[Firebase SDK v10+](https://firebase.google.com/)**: Configurado y listo para expandir tu aplicación con base de datos en tiempo real (Firestore), autenticación de usuarios y almacenamiento en la nube.
*   **TypeScript**: Tipado estático para garantizar un código robusto y libre de errores en tiempo de desarrollo.

---

## 📂 Estructura del Proyecto

El ecosistema cuenta con una arquitectura limpia organizada de la siguiente manera:

```text
portfoliov4/
├── .vscode/                 # Configuraciones optimizadas para VS Code
│   ├── extensions.json      # Extensiones sugeridas (Astro, Tailwind CSS)
│   └── settings.json        # Autocompletado experimental y auto-formateo
├── src/
│   ├── components/          # Componentes de UI reutilizables
│   ├── layouts/
│   │   └── Layout.astro     # Estructura HTML base con soporte SEO y fondo animado
│   ├── lib/
│   │   └── firebase.ts      # Inicialización y exportación de servicios Firebase
│   ├── pages/
│   │   └── index.astro      # Página principal interactiva y responsiva
│   └── styles/
│       └── global.css       # Hoja de estilos global e importación de Tailwind v4
├── .env                     # Variables de entorno locales (Ignorado en Git)
├── .env.template            # Plantilla guía para credenciales de Firebase
├── astro.config.mjs         # Configuración del compilador Astro y Vite
└── tsconfig.json            # Configuración de compilación TypeScript
```

---

## ✨ Características de Diseño y UI

Este espacio de trabajo incluye un diseño premium inicial con:
*   **Estética Glassmorphism**: Barra de navegación y componentes flotantes con efectos de desenfoque traslúcidos (`backdrop-blur`).
*   **Modo Oscuro Inmersivo**: Fondo enriquecido HSL oscuro con orbes luminosos ambientales difuminados en segundo plano para una apariencia premium.
*   **Micro-interacciones**: Transiciones fluidas de escala y gradiente en botones y tarjetas de proyectos.
*   **Formulario de Contacto Interactivo**: Script cliente integrado en Astro para simular estados de carga y notificaciones de éxito dinámicas.

---

## 🔑 Configuración de Firebase

Para activar las funcionalidades del backend en el futuro, renombra el archivo `.env.template` a `.env` y rellena tus credenciales del panel de Firebase:

```env
PUBLIC_FIREBASE_API_KEY="tu-api-key"
PUBLIC_FIREBASE_AUTH_DOMAIN="tu-auth-domain"
PUBLIC_FIREBASE_PROJECT_ID="tu-project-id"
PUBLIC_FIREBASE_STORAGE_BUCKET="tu-storage-bucket"
PUBLIC_FIREBASE_MESSAGING_SENDER_ID="tu-sender-id"
PUBLIC_FIREBASE_APP_ID="tu-app-id"
PUBLIC_FIREBASE_MEASUREMENT_ID="tu-measurement-id"
```

El archivo [src/lib/firebase.ts](file:///c:/Users/nicol/OneDrive/Escritorio/portfoliov4/src/lib/firebase.ts) importará y expondrá automáticamente las instancias de `db` (Firestore), `auth` (Autenticación) y `storage` (Almacenamiento) listas para usar.

---

## 🚀 Comandos de Desarrollo

Ejecuta estos comandos en la raíz del proyecto para gestionarlo:

| Comando | Acción |
| :--- | :--- |
| `npm run dev` | Inicia el servidor de desarrollo local en `http://localhost:4321` |
| `npm run build` | Compila el sitio estático optimizado para producción en `./dist/` |
| `npm run preview` | Previsualiza localmente la compilación de producción |
| `npm run astro check` | Realiza un diagnóstico de tipos y estructura del código |

---

## 🔮 Futuras Ampliaciones Sugeridas

1.  **Conexión Real de Contacto**: Reemplaza el temporizador en la sección de contacto de `index.astro` con un llamado real `addDoc(collection(db, "messages"), { ... })` para recibir los mensajes en tu Firestore Database.
2.  **Panel de Administración**: Protege una ruta `/admin` usando Firebase Auth para editar tus proyectos directamente desde la web.
3.  **Despliegue Continuo**: Vincula este repositorio con plataformas como **Vercel**, **Netlify** o **Firebase Hosting** para despliegues automáticos al hacer push a la rama `main`.
