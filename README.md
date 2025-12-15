# MoviesXR

**Plataforma de streaming de películas con arquitectura de microservicios con Docker**

### Link del proyecto
(https://api-gateway-3bca.onrender.com)

## Sobre el Proyecto

**MoviesXR** es una aplicación web full-stack de streaming de películas construida con arquitectura de microservicios. El sistema integra catálogos de TMDB, autenticación de usuarios, watchlist persistente y trailers de YouTube, todo desplegado en la nube con Render.

## Tecnologías

### Backend
- **Node.js** - Entorno de ejecución JavaScript
- **Express** - Framework web para Node.js
- **MongoDB Atlas** - Base de datos NoSQL en la nube para usuarios y watchlist
- **Mongoose** - ODM para MongoDB
- **Firebase Authentication** - Autenticación de usuarios con Google
- **TMDB API** - Catálogo de películas y metadatos
- **YouTube Data API** - Integración de trailers
- **Axios** - Cliente HTTP para comunicación entre servicios

### Frontend
- **Vanilla JavaScript** - Sin frameworks, JavaScript puro
- **CSS3** - Animaciones y diseño responsivo
- **Firebase SDK** - Autenticación del lado del cliente

### Infraestructura
- **Render** - Plataforma de despliegue en la nube
- **Docker** - Contenedores para desarrollos de microservicios 
- **Git/GitHub** - Control de versiones y CI/CD

### Herramientas de Desarrollo
- **dotenv** - Variables de entorno
- **CORS** - Políticas de origen cruzado
- **Nodemon** - Auto-reload en desarrollo

---

## Características

### Arquitectura de Microservicios
- **API Gateway** - Punto de entrada único y enrutamiento
- **Users Service** - Gestión de usuarios y suscripciones
- **Movies Service** - Catálogo de películas con integración TMDB
- **Auth Service** - Autenticación centralizada con Firebase
- **Watchlist Service** - Lista de películas favoritas con MongoDB
- **Profiles Service**  - Gestión de perfiles (máx. 5 por cuenta, estilo Netflix)
- **Recommendations Service**  - Recomendaciones personalizadas basadas en gustos
- **Reviews Service**  - Calificaciones (⭐1-5) y reseñas de películas

### Funcionalidades
- **Catálogo de películas** - Trending, top rated, categorías por género
- **Trailers de YouTube** - Reproducción de trailers en modales
- **Mi Lista** - Guardar películas favoritas con persistencia en MongoDB
- **Búsqueda** - Buscar películas por título
- **Autenticación** - Login con Google mediante Firebase
- **Perfiles múltiples**  - Hasta 5 perfiles por cuenta, perfiles infantiles
- **Recomendaciones personalizadas**  - "Para ti", "Porque viste X", Top 10
- **Calificaciones y reseñas**  - Sistema de 👍👎, estrellas y reseñas escritas
- **Match personalizado**  - Porcentaje de compatibilidad por película
- **Diseño responsivo** - Funciona en desktop, tablet y móvil

### Seguridad y Autenticación
- **Firebase Authentication** - Login seguro con Google
- **JWT Tokens** - Autenticación mediante tokens
- **Sesiones persistentes** - Mantiene la sesión del usuario
- **Protección de rutas** - Endpoints protegidos por autenticación

### Flujo de Datos
1. Usuario accede a la aplicación - Frontend carga desde API Gateway
2. Usuario hace login con Google - Firebase autentica y retorna token
3. Usuario selecciona perfil - Profiles Service carga perfiles disponibles
4. Frontend solicita películas - API Gateway enruta a Movies Service
5. Movies Service consulta TMDB - Obtiene datos y trailers de YouTube
6. Sistema genera recomendaciones - Recommendations Service analiza gustos y watchlist
7. Usuario agrega a Mi Lista - Watchlist Service guarda en MongoDB
8. Usuario califica película - Reviews Service registra rating (👍👎 o ⭐1-5)
9. Usuario reproduce trailer - Modal con YouTube embed

## Contacto

**Yessetk Rodriguez**

- GitHub: [@yessetkr21](https://github.com/yessetkr21)
- Email: yessetkr2190@gmail.com

### Los contenedores no inician:
```bash
docker-compose down
docker-compose up --build
```

### Puerto ya en uso:
Cambia los puertos en `docker-compose.yml`:
```yaml
ports:
  - "3010:3000"  # Usa 3010 en lugar de 3000
```

### Ver errores detallados:
```bash
docker-compose logs
```

## 📚 Recursos Adicionales

- [Documentación de Docker](https://docs.docker.com/)
- [Express.js Guide](https://expressjs.com/)
- [Microservices Pattern](https://microservices.io/)

---



