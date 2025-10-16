# 🌌 **Asterium: proyecto fullstack sobre astronomía**

Asterium es una **plataforma fullstack** dedicada a la astronomía, el cosmos y la ciencia del universo.  
Combina **un blog interactivo** (frontend) y **una API REST profesional** (backend) para gestionar artículos, descubrimientos astronómicos, usuarios y contenido visual.

El objetivo del proyecto es **hacer que la astronomía sea accesible, inspiradora y visualmente atractiva**, integrando diseño, tecnología y comunidad.

## 🧭 **Índice**
1. [Visión general](#-visión-general)
2. [Frontend — Blog Interactivo](#-frontend--blog-interactivo)
3. [Backend — API REST Asterium Server](#-backend--api-rest-asterium-server)
4. [Equipo de desarrollo](#-equipo-de-desarrollo)
5. [Notas finales](#-notas-finales)

## 🚀 **Visión general**

**Frontend:** React + Vite + TailwindCSS  
**Backend:** Node.js + Express + TypeScript + Sequelize + MySQL  
**Infraestructura:** Cloudinary · JWT · Helmet · CORS  
**Testing:** Jest · Supertest  
**Validación:** Zod  

## 🌠 **Frontend — Blog interactivo**

<img width="1920" height="1713" alt="homepage" src="https://github.com/user-attachments/assets/32747c7f-c291-4779-9936-2e3ef2d7c815" />

El frontend de **Asterium** permite a los usuarios:

- 🪐 Leer artículos sobre planetas, galaxias y descubrimientos  
- ✍️ Crear y publicar sus propias entradas
- 👤 Gestionar su perfil y actividad  

El diseño está inspirado en el cielo nocturno: tonos oscuros, detalles estelares, transiciones suaves y tipografía moderna.

### 🧭 **User Journey**

1. **Página principal:** flujo de artículos y secciones temáticas  
2. **Registro / Inicio de sesión:** autenticación mediante formulario  
3. **Perfil del usuario:** gestión del perfil y publicaciones propias  
4. **Crear artículo:** editor con soporte Markdown  
5. **Ver artículo:** página limpia con contenido y comentarios

### 🎨 **Prototipo en Figma**

[🎨 Ver diseño en Figma](https://www.figma.com/design/kofeymVilSP9jyQ7k8P2Wx/Asterium?node-id=17-2&t=BqSRzoE0jWOoDuy3-1)

### ⚙️ **Tecnologías (Frontend)**

| Categoría | Tecnologías |
|------------|--------------|
| Framework | React + Vite |
| Estilos | TailwindCSS |
| Navegación | React Router |
| API | Axios |
| Renderizado | Markdown |
| Estado global | Context API / Store |
| Validación | Custom Validators |

### 📁 **Estructura del proyecto (Frontend)**

```bash
/client  
  ├── src/  
  │   ├── assets/           # imágenes e íconos  
  │   ├── components/       # componentes UI  
  │   ├── pages/            # vistas (Home, Article, Profile)  
  │   ├── router/           # enrutamiento  
  │   ├── services/         # conexión con API  
  │   ├── store/            # estado global  
  │   ├── validators/       # validaciones  
  │   └── main.tsx
```
### **⚡ Instalación y ejecución (Frontend)
```bash
# 1. Clonar el repositorio
git clone https://github.com/Asterium360/Aster-Client.git
cd client

# 2. Instalar dependencias
npm install

# 3. Ejecutar el proyecto
npm run dev
```
**🛰️ Frontend disponible en → http://localhost:5173**

## **🌌 Backend — API REST Asterium Server**

Node.js · Express · TypeScript · Sequelize · MySQL · Cloudinary · JWT

**Asterium Server** es una API REST moderna y escalable para gestionar descubrimientos astronómicos con autenticación, roles y carga de imágenes.

### **🧱 Características principales**

* 🔐 Registro y autenticación de usuarios (roles: admin y user)

* 🧩 CRUD completo de descubrimientos astronómicos

* ☁️ Carga flexible de imágenes (archivo o URL) con Cloudinary

* 🧠 Validación robusta con Zod

* 🧱 ORM Sequelize conectado a MySQL

* 🛡️ Middlewares personalizados para autenticación, validación y seguridad

* 🧪 Pruebas unitarias con Jest y Supertest

### **🧭 Roles y permisos**

| Rol | Listar | Ver detalle | Crear | Editar | Eliminar |
| ----- | ----- | ----- | ----- | ----- | ----- |
| 🧍‍♀️ Usuario | ✅ | ✅ | ✅ | ✅ (solo sus descubrimientos) | ✅ (solo sus descubrimientos) |
| 🛡️ Admin | ✅ | ✅ | ✅ | ✅ (todos) | ✅ (todos) |

🔒 Solo los usuarios autenticados pueden crear, editar o eliminar.  
👑 Los administradores tienen control total sobre todos los registros.

### **⚙️ Tecnologías utilizadas (Backend)**

| Categoría | Tecnologías |
| ----- | ----- |
| Lenguaje | TypeScript |
| Framework | Express.js |
| ORM / DB | Sequelize \+ MySQL |
| Validación | Zod |
| Seguridad | Helmet · CORS · JWT |
| Imágenes | Cloudinary \+ Multer |
| Testing | Jest · Supertest |
| Documentación | Postman |

### **📂 Estructura del proyecto (Backend)**

`src/`  
 `├── config/               # Configuración de Cloudinary`  
 `├── controllers/          # Lógica de negocio (Asterium, Auth, Users)`  
 `├── middlewares/          # Auth, roles, validaciones`  
 `├── models/               # Modelos Sequelize`  
 `├── routes/               # Definición de endpoints`  
 `├── schemas/              # Validaciones Zod`  
 `├── seeders/              # Datos iniciales`  
 `├── tests/                # Pruebas unitarias`  
 `├── db.ts                 # Conexión MySQL`  
 `├── app.ts                # Configuración Express`  
 `└── index.ts              # Punto de entrada`

### **⚡ Instalación y ejecución (Backend)**
```bash
# 1. Clonar el repositorio  
git clone https://github.com/Asterium360/Aster-Server.git  
cd Aster-Server`

# 2. Instalar dependencias  
npm install`

# 3. Configurar variables de entorno  
# Crea el archivo .env:  
DB_NAME=asterium  
DB_USER=root  
DB_PASSWORD=tu_contraseña  
DB_HOST=localhost  
DB_PORT=3306  
JWT_SECRET=tu_token_secreto  
PORT=4000

# 4. Ejecutar en modo desarrollo  
npm run dev
```

🌍 Servidor disponible en → [http://localhost:4000](http://localhost:4000)

### **☁️ Cloudinary integration**

* Imágenes gestionadas con **Multer \+ CloudinaryStorage**

* Carpeta automática: `Asterium_Discoveries`

* Se aceptan archivos locales o URLs externas

`const image_url = req.file?.path || body.image_url || null;`

### **🔐 Endpoints principales**

#### **🪐 Autenticación `/auth`**

| Método | Endpoint | Descripción | Auth |
| ----- | ----- | ----- | ----- |
| POST | /auth/register | Registrar usuario | ❌ |
| POST | /auth/login | Iniciar sesión (JWT) | ❌ |
| PUT | /auth/promote/:id | Promover usuario a admin | ✅ Solo admin |

#### **🌠 Descubrimientos `/asterium`**

| Método | Endpoint | Descripción | Auth |
| ----- | ----- | ----- | ----- |
| GET | /asterium | Listar descubrimientos | ✅ Logueados |
| GET | /asterium/:id | Ver detalle | ✅ Logueados |
| POST | /asterium | Crear nuevo descubrimiento | ✅ user/admin |
| PUT | /asterium/:id | Editar propio o admin | ✅ user/admin |
| DELETE | /asterium/:id | Eliminar propio o admin | ✅ user/admin |

### **🧪 Testing**

| Archivo | Propósito |
| ----- | ----- |
| `auth.test.ts` | Registro, login y JWT |
| `asterium.test.ts` | CRUD de descubrimientos |
| `auth.ts` | Middleware de autenticación |
| `checkRole.ts` | Middleware de permisos |

Ejecutar pruebas:

`npm test`

### **📘 Documentación Postman**

[📗 Ver colección completa en Postman](https://maryori-5224626.postman.co/workspace/Maryori%27s-Workspace~b4629cfb-3575-450f-84c7-237828081b35/collection/46421564-d0aae761-6651-474b-85ff-af970d5c081d)

Incluye todos los endpoints, ejemplos funcionales y tokens de prueba.

## **👩‍💻 Equipo de desarrollo**

| Nombre | Rol | GitHub | LinkedIn |
| ----- | ----- | ----- | ----- |
| **Anngie** | Project Lead, Fullstack Developer | [link](https://github.com/angiepereir) | [link](https://www.linkedin.com/in/anngy-pereira-094aa026a/) |
| **Larysa** | Scrum Master, UI designer, Frontend Developer   | [link](https://github.com/ambalari) | [link](https://www.linkedin.com/in/larysa-ambartsumian/) |
| **Michelle**  | Frontend Developer | [link](https://github.com/MichelleGel) | [link](https://www.linkedin.com/in/michelle-gelves/) |
| **Maryori** | Backend Developer | [link](https://github.com/MaryoriCruz) | [link](https://www.linkedin.com/in/maryori-cruz-6b440116b/)  |
| **Sofia**  | Backend Developer | [link](https://github.com/Sofiareyes12) | [link](https://www.linkedin.com/in/sofiareyes12/) |

Proyecto desarrollado en **Factoría F5 – Bootcamp FullStack & DevOps**.  
Diseñado aplicando **buenas prácticas de arquitectura, seguridad y documentación profesional**.

