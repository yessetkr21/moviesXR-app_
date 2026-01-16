# MoviesXR

**Movie Streaming Platform with Microservices Architecture using Docker**

### Project Link
(https://api-gateway-3bca.onrender.com)

## About the Project

**MoviesXR** is a full-stack web application for streaming movies built with a microservices architecture. The system integrates TMDB catalogs, user authentication, a persistent watchlist, and YouTube trailers, all deployed in the cloud with Render.

## Captures
<table>
  <tr>
    <td>
      <img src="https://github.com/user-attachments/assets/bf724906-8d24-4f84-9701-82ef8936ae98" width="520" />
    </td>
    <td>
      <img src="https://github.com/user-attachments/assets/5e1e79d6-789e-4a0a-a5a1-0e36419b85e7" width="250" />
      <br />
      <img src="https://github.com/user-attachments/assets/54f09f69-d444-4841-bee1-e3e3127d309c" width="250" />
    </td>
  </tr>
</table>

## Technologies

### Backend
- **Node.js** - JavaScript runtime environment
- **Express** - Web framework for Node.js
- **MongoDB Atlas** - Cloud-based NoSQL database for users and watchlists
- **Mongoose** - ODM for MongoDB
- **Firebase Authentication** - User authentication with Google
- ** API** - Movie catalog and metadata
- **YouTube Data API** - Trailer integration
- **Axios** - HTTP client for communication between services

### Frontend
- **Vanilla JavaScript** - No frameworks, pure JavaScript
- **CSS3** - Animations and responsive design
- **Firebase SDK** - Client-side authentication

### Infrastructure
- **Render** - Cloud deployment platform
- **Docker** - Containers for microservices development
- **Git/GitHub** - Version control and CI/CD

### Development Tools
- **dotenv** - Environment variables
- **CORS** - Cross-origin policies
- **Nodemon** - Auto-reload in development

---

## Features

### Microservices Architecture
- **API Gateway** - Single point of entry and routing
- **Users Service** - User and subscription management
- **Movies Service** - Movie catalog with TMDB integration
- **Auth Service** - Centralized authentication with Firebase
- **Watchlist Service** - Watchlist with MongoDB
- **Profiles Service** - Profile management (max. 5 per account, Netflix style)
- **Recommendations Service** - Personalized recommendations based on preferences
- **Reviews Service** - Movie ratings (⭐1-5) and reviews

### Functionalities
- **Profiles** - Create profiles for different people at home and save everything in the cloud. Continue Watching, reviews, my list, user profiles and Auth
- **Movie Catalog** - Trending, top-rated, categories By Genre
- **YouTube Trailers** - Play trailers in modals
- **My List** - Save favorite movies persistently in MongoDB
- **Search** - Search for movies by title
- **Authentication** - Log in with Google and GitHub using Firebase
- **Multiple Profiles** - Up to 5 profiles per account, child profiles
- **Personalized Recommendations** - "For You", "Because You Watched X", Top 10
- **Ratings and Reviews** - 👍👎 system, stars, and written reviews
- **Custom Match** - Compatibility percentage per movie
- **Responsive Design** - Works on desktop, tablet, and mobile

### Security and Authentication
- **Firebase Authentication** - Secure login with Google
- **JWT Tokens** - Authentication using tokens
- **Persistent Sessions** - Maintains user session
- **Route Protection** - Endpoints protected by Authentication

### Data Flow
1. User accesses the application - Frontend loads from API Gateway
2. User logs in with Google - Firebase authenticates and returns token
3. User selects profile - Profiles Service loads available profiles
4. Frontend requests movies - API Gateway routes to Movies Service
5. Movies Service queries TMDB - Retrieves data and trailers from YouTube
6. System generates recommendations - Recommendations Service analyzes preferences and watchlist
7. User adds to My List - Watchlist Service saves to MongoDB
8. User rates movie - Reviews Service records rating (👍👎 or ⭐1-5)
9. User plays trailer - Modal with YouTube embed

## Contact

**Yessetk Rodriguez**

- GitHub: [@yessetkr21](https://github.com/yessetkr21)
- Email: yessetkr2190@gmail.com



