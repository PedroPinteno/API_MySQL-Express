# API_MySQL_Express
Desarrollo de una API con Express y base de datos MySQL.

## Estructura del Proyecto

### Archivo Principal (app.js)
- Configura una aplicación Express
- Implementa middleware básico (logger, parser de JSON y cookies)
- Define las rutas principales: '/', '/users' y '/api'

### Configuración de Base de Datos (dbConfig.js)
- Configura una conexión a MySQL
- Se conecta a una base de datos llamada 'Blog'
- Utiliza el puerto 3306 (puerto estándar de MySQL)

### Sistema de Rutas
- Estructura modular de rutas
- Ruta principal para API ('/api')
- Subruta específica para autores ('/api/autores')
- Rutas adicionales para usuarios y página principal

### Estructura de Directorios
- `/models`: Contiene los modelos de datos
- `/routes`: Contiene las definiciones de rutas
- `/public`: Para archivos estáticos
- `/bin`: Script de inicio de la aplicación

## Funcionalidad

### Gestión de Autores
- **Crear autores**: Nombre, Email, Imagen
- **Listar autores**: Obtener todos los autores
- **Actualizar autores**: Modificar información existente
- **Eliminar autores**: Por ID

### Endpoints API
- `POST /api/autores`: Crear nuevo autor
- `GET /api/autores`: Obtener todos los autores
- `PUT /api/autores/:autorId`: Actualizar autor específico
- `DELETE /api/autores/:autorId`: Eliminar autor

### Base de Datos
Tabla `autores` con los campos:
- id (automático)
- nombre
- email
- imagen

## Características Técnicas
- API RESTful
- Manejo de errores básico
- Respuestas en formato JSON
- Estructura modular y organizada
- Arquitectura MVC (Modelo-Vista-Controlador)

## Tecnologías Utilizadas
- Node.js como runtime
- Express como framework web
- MySQL como base de datos
- Middleware:
  - morgan (logging)
  - cookie-parser
  - express.json
  - express.urlencoded

## Caso de Uso
Este proyecto sirve como backend para un sistema de blog donde:
1. Los administradores pueden gestionar los autores del blog
2. Se mantiene un registro de quién escribe qué contenido
3. Se pueden asociar imágenes y correos electrónicos a los autores
4. Se puede obtener información de todos los autores del blog

## Buenas Prácticas Implementadas
- Separación de responsabilidades
- Modularización de rutas
- Uso de middleware para funcionalidades comunes
- Configuración centralizada de la base de datos
