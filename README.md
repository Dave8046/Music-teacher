# 🎹 Music Teacher Management System

![Piano Logo](https://img.shields.io/badge/Music-Teacher-gold?style=flat&logo=musical-note)
![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue?logo=typescript)
![React](https://img.shields.io/badge/React-18-61dafb?logo=react)
![Express](https://img.shields.io/badge/Express-4.18-green?logo=express)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15-blue?logo=postgresql)

Sistema de gestión musical elegante con diseño inspirado en teclas de piano para profesores de música que enseñan violín y piano.

## ✨ Características Principales

### 🎓 Para Profesores
- **Dashboard Completo**: Vista general con estadísticas en tiempo real
- **Gestión de Estudiantes**: Agregar, editar y organizar información de estudiantes
- **Programación de Clases**: Calendario integrado con seguimiento de asistencia
- **Sistema de Tareas**: Asignación y evaluación de ejercicios musicales
- **Seguimiento de Progreso**: Monitoreo del desarrollo musical de cada estudiante
- **Notas Personalizadas**: Sistema de anotaciones para cada estudiante

### 🎵 Para Estudiantes  
- **Dashboard Personal**: Vista de su progreso y próximas clases
- **Calendario de Clases**: Horarios y confirmación de asistencia
- **Tareas Asignadas**: Lista de ejercicios y piezas por practicar
- **Progreso Musical**: Visualización de su evolución y logros
- **Comunicación**: Mensajes y feedback del profesor

### 🎨 Diseño Único
- **Tema Piano**: Colores inspirados en teclas de piano (negro/blanco/dorado)
- **Logo Minimalista**: Representación elegante de teclas de piano
- **Interfaz Intuitiva**: Diseño limpio y profesional
- **Responsive**: Funciona perfectamente en dispositivos móviles y desktop

## 🚀 Tecnologías

### Frontend
- **React 18** con TypeScript
- **Vite** para desarrollo y build
- **Wouter** para routing
- **TanStack Query** para manejo de estado del servidor
- **Shadcn/ui** componentes de UI con Radix UI
- **Tailwind CSS** para estilos
- **React Hook Form** + Zod para formularios

### Backend
- **Node.js** con Express y TypeScript
- **Sesiones** con express-session
- **bcrypt** para seguridad de contraseñas
- **Zod** para validación de datos

### Base de Datos
- **PostgreSQL** con Neon serverless
- **Drizzle ORM** para queries type-safe
- **Drizzle Kit** para migraciones

## 📋 Requisitos Previos

- Node.js 18 o superior
- PostgreSQL (o cuenta en Neon)
- npm o yarn

## 🛠️ Instalación

1. **Clonar el repositorio**
```bash
git clone <repository-url>
cd music-teacher
```

2. **Instalar dependencias**
```bash
npm install
```

3. **Configurar variables de entorno**
```bash
# Crear archivo .env
DATABASE_URL=postgresql://username:password@localhost:5432/music_teacher
SESSION_SECRET=tu-clave-secreta-super-segura
```

4. **Configurar base de datos**
```bash
# Aplicar esquema a la base de datos
npm run db:push
```

5. **Iniciar el servidor de desarrollo**
```bash
npm run dev
```

La aplicación estará disponible en `http://localhost:5000`

## 🎯 Uso

### Primer Acceso

El sistema incluye usuarios de prueba predefinidos:

**Profesor:**
- Usuario: `profesor1`
- Contraseña: `123456`

**Estudiante:**
- Usuario: `estudiante1` 
- Contraseña: `123456`

### Dashboard del Profesor

1. **Estadísticas**: Vista rápida de estudiantes totales, clases del día, tareas pendientes
2. **Estudiantes**: Lista completa con información de contacto y progreso
3. **Clases de Hoy**: Agenda del día con estudiantes programados
4. **Gestión**: Agregar nuevos estudiantes, programar clases, asignar tareas

### Dashboard del Estudiante

1. **Mi Progreso**: Visualización de logros y áreas de mejora
2. **Próximas Clases**: Calendario personal con horarios confirmados
3. **Mis Tareas**: Lista de ejercicios y piezas asignadas por el profesor
4. **Comunicación**: Mensajes y feedback recibido

## 🏗️ Arquitectura del Proyecto

```
music-teacher/
├── client/                 # Frontend React
│   ├── src/
│   │   ├── components/     # Componentes reutilizables
│   │   ├── pages/         # Páginas principales
│   │   ├── lib/           # Utilidades y configuración
│   │   └── hooks/         # Custom hooks
├── server/                # Backend Express
│   ├── index.ts          # Servidor principal
│   ├── routes.ts         # Endpoints API
│   ├── storage.ts        # Capa de datos
│   └── db.ts            # Configuración BD
├── shared/               # Código compartido
│   └── schema.ts        # Esquemas y tipos
└── package.json         # Dependencias
```

## 🔧 Scripts Disponibles

```bash
# Desarrollo
npm run dev              # Inicia servidor de desarrollo

# Base de datos  
npm run db:push          # Aplica cambios de esquema
npm run db:studio        # Abre Drizzle Studio

# Build
npm run build           # Build de producción
npm start              # Inicia servidor de producción
```

## 🎼 Características Técnicas

### Autenticación
- Sesiones seguras con express-session
- Hash de contraseñas con bcrypt
- Rutas protegidas por rol (profesor/estudiante)

### Base de Datos
- Modelos relacionales: Users, Students, Lessons, Assignments, Progress
- Queries optimizadas con Drizzle ORM
- Migrations automáticas

### UI/UX
- Tema customizado con colores piano
- Componentes accesibles con Radix UI
- Diseño responsive para móviles
- Loading states y error handling

## 🚀 Despliegue

### Replit (Recomendado)
1. Importar proyecto a Replit
2. Configurar secrets para DATABASE_URL
3. Ejecutar `npm run db:push`
4. Usar el botón Deploy de Replit

### Manual
1. Build del proyecto: `npm run build`
2. Configurar variables de entorno en producción
3. Configurar base de datos PostgreSQL
4. Ejecutar migraciones: `npm run db:push`
5. Iniciar: `npm start`

## 📝 Contribución

1. Fork el proyecto
2. Crear rama feature: `git checkout -b feature/nueva-funcionalidad`
3. Commit cambios: `git commit -am 'Agregar nueva funcionalidad'`
4. Push a la rama: `git push origin feature/nueva-funcionalidad`
5. Crear Pull Request

## 📄 Licencia

Este proyecto está bajo la Licencia MIT. Ver el archivo `LICENSE` para más detalles.

## 🎵 Sobre el Proyecto

Music Teacher nació de la necesidad de tener una herramienta elegante y funcional para la gestión de clases de música. Con un diseño inspirado en las teclas del piano, combina funcionalidad profesional con una estética que refleja la belleza de la música.

---

**Desarrollado con ❤️ para la comunidad musical**