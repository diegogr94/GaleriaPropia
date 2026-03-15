# 🎨 Galería de Arte Propia

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Vite](https://img.shields.io/badge/Vite-B73BFE?style=for-the-badge&logo=vite&logoColor=FFD62E)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-181818?style=for-the-badge&logo=supabase&logoColor=3ECF8E)
![Stripe](https://img.shields.io/badge/Stripe-626CD9?style=for-the-badge&logo=stripe&logoColor=white)

**Galería de Arte Propia** es una plataforma de comercio electrónico de lujo (High-Ticket E-commerce) diseñada para que artistas independientes gestionen la venta directa de sus obras originales sin intermediarios. La aplicación combina una experiencia visual inmersiva basada en el concepto de "Cubo Blanco" con una zona exclusiva para coleccionistas VIP, garantizando transacciones seguras y una gestión de inventario automatizada.

## ✨ Características Principales
* **🖼️ Exposición Inmersiva:** Galería asimétrica (Masonry) con carga optimizada de imágenes en alta resolución y efectos visuales minimalistas.
* **💎 Comunidad VIP:** Área restringida para coleccionistas registrados con acceso a noticias exclusivas, preventas y contenido curatorial.
* **💳 Pagos Seguros con Stripe:** Integración completa con la pasarela financiera para el procesamiento de cobros internacionales y gestión de envíos.
* **🛡️ Control de Inventario Estricto:** Gestión de piezas únicas (Stock = 1) mediante bloqueos de concurrencia para evitar ventas duplicadas de originales.
* **📱 Diseño Responsivo y Accesible:** Interfaz adaptada a dispositivos móviles y cumplimiento de normativas de accesibilidad WCAG 2.1 para una navegación sin barreras.

## 🛠️ Tecnologías
**Frontend:**
* **Core:** React (v18+) + Vite + JavaScript (ES6+).
* **Enrutamiento:** React Router DOM para una navegación SPA fluida.
* **Estilos:** Tailwind CSS (Enfoque Utility-First).
* **Estado Global:** React Context API (Auth y Carrito).
* **Iconografía:** Lucide React.

**Backend & Infraestructura (Serverless):**
* **Base de Datos:** PostgreSQL (Gestionado en Supabase).
* **Autenticación:** Supabase Auth (JWT).
* **Almacenamiento:** Supabase Storage para fotografías en alta resolución.
* **Pasarela de Pagos:** Stripe API & Webhooks.
* **Despliegue:** Vercel (CI/CD) con red CDN global.

## 🗄️ Modelo de Datos
La arquitectura relacional en PostgreSQL garantiza la integridad referencial y la trazabilidad de cada venta:

1. `usuarios`: Perfiles de coleccionistas y credenciales de administrador.
2. `colecciones`: Agrupaciones temáticas de obras de arte.
3. `obras`: Catálogo detallado con metadatos técnicos, precios y URLs de imágenes.
4. `pedidos`: Cabeceras transaccionales vinculadas a las sesiones de Stripe.
5. `noticias`: Contenido exclusivo para el feed de la comunidad VIP.

### Seguridad y Aislamiento (RLS):
* **Público:** Lectura de obras disponibles y acceso a la landing page.
* **Coleccionistas VIP:** Acceso de lectura a noticias restringidas y a su propio historial de pedidos.
* **Artista (Admin):** Control total (CRUD) sobre el catálogo, precios y gestión de noticias mediante políticas de seguridad a nivel de fila (Row Level Security).

## 👤 Roles de Usuario
| Rol | Permisos |
| :--- | :--- |
| **Visitante Anónimo** | Navegación por la galería pública y compra de obras mediante "Guest Checkout". |
| **Coleccionista VIP** | Acceso a noticias exclusivas, preventas y panel personal de seguimiento de compras. |
| **Artista (Admin)** | Gestión de inventario, edición de precios, publicación de noticias y visualización de ventas globales. |

## 🖥️ Vistas Principales

| Vista | Descripción |
| :--- | :--- |
| **🏠 Landing Page** | Presentación de la artista y propuesta de valor estética. |
| **🖼️ Galería Pública** | Catálogo interactivo con filtros por colección y buscador de obras. |
| **💎 Dashboard VIP** | Feed de noticias y contenido exclusivo para coleccionistas registrados. |
| **🛒 Checkout** | Pasarela de pago segura integrada con Stripe Elements. |
| **⚙️ Backoffice** | Panel administrativo privado para subir obras y gestionar el stock. |

## 🚀 Instalación y Configuración Local

Sigue estos pasos para levantar el proyecto en tu máquina de desarrollo. Necesitarás Node.js (v18+).

### 1. Clonar el repositorio
```bash
git clone [https://github.com/tu-usuario/galeria-arte-propia.git](https://github.com/tu-usuario/galeria-arte-propia.git)

## 📅 Evolución del Proyecto (Cronología Completa)
Documentación detallada del avance semanal del proyecto.

| Fecha | Hito / Fase Realizada |
| :--- | :--- |
| **12-sep-2025** | Presentación de Asignatura y Proyecto. |
| **19-sep-2025** | Creación de Imagen Corporativa y concepto visual. |
| **26-sep-2025** | Elaboración de Contrato y Recogida de Necesidades. |
| **03-oct-2025** | Definición de Requisitos Funcionales y No Funcionales. |
| **10-oct-2025** | Desarrollo de Interfaces Gráficas y Prototipado UI/UX. |
| **17-oct-2025** | Desarrollo de la Estructura de la Base de Datos. |
| **24-oct-2025** | Definición del Modelo Relacional y Normalización. |
| **31-oct-2025** | Presentación de Interfaces y Base de Datos al cliente. |
| **07-nov-2025** | Elección y Justificación de Tecnologías (Stack). |
| **14-nov-2025** | Estructuración Inicial de Documentación y Arquitectura Base. |
| **21-nov-2025** | Definición de Puntos de los Manuales de Usuario y Técnico. |
| **05-dic-2025** | Desarrollo Inicial de Manuales (Fase de Abstracción). |
| **12-dic-2025** | Análisis Arquitectónico y Opciones de Despliegue. |
| **19-dic-2025** | Pruebas de Despliegue en Entorno Local. |
| **09-ene-2026** | Pruebas de Despliegue en Vercel (Producción). |
| **16-ene-2026** | Fase de Pruebas Extensivas (QA) y Corrección de Errores. |
| **23-ene-2026** | Revisión Final y Auditoría de Documentación. |
| **30-ene-2026** | Preparación para la Presentación y Defensa. |
| **06-feb-2026** | Implementación de Feedback y Accesibilidad Web (WCAG). |
| **13-feb-2026** | Optimización de Base de Datos y Revisión de Ciberseguridad. |
| **20-feb-2026** | Generación de Datos Simulados y Pruebas de Estrés. |
| **27-feb-2026** | Cierre de Documentación y Manual de Despliegue. |
| **05-mar-2026** | Congelación de Código (Code Freeze) y Versionado Semántico. |
| **12-mar-2026** | Preparación de la Defensa y Creación de Material Audiovisual. |
| **19-mar-2026** | Entrega Definitiva y Defensa del Proyecto. |
