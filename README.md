# MovieHub (Project 4)

A simple front-end movie discovery app that lets you:
- Browse **Trending** and **Popular** movies
- **Search** for movies by title keywords
- **Save favourites** (liked movies) using `localStorage`
- Add **personal notes** to your favourite movies

---

## Features

### Home page (`index.html`)
- Shows:
  - **Trending Movies** (weekly trending)
  - **Popular Movies**
- Provides a **search bar** to filter movies by title keywords.
- Click the **heart (♥)** icon to like/unlike a movie:
  - Liked movies are stored in `localStorage` under `likedMovies`.

### Favourites page (`journal.html`)
- Displays movies saved in `likedMovies`.
- Shows the total number of selected movies.
- Supports:
  - Removing individual favourites (by unliking)
  - **Remove all movies** button
  - Adding/editing a **note** for each favourite movie (stored inside the saved movie object in `localStorage`)

---

## Built With

- **HTML**
- **JavaScript (Vanilla)**
- **Tailwind CSS (CDN)** via `@tailwindcss/browser`
- **TMDB API** (The Movie Database) for movie data

---

## Getting Started (Run Locally)

### Option 1: Open directly
1. Download / clone the repo
2. Open `index.html` in your browser

### Option 2: Use a local server (recommended)
Some browsers restrict certain features when opening files directly. Using a local server is best.

If you have VS Code:
1. Install **Live Server**
2. Right-click `index.html` → **Open with Live Server**

Or using Node:
```bash
npx serve
```

---

## Configuration (TMDB API)

This project currently uses a TMDB API key directly in `main.js`.

- Trending endpoint is called from:
  - `https://api.themoviedb.org/3/trending/movie/week`
- Popular/discover endpoint is called from:
  - `https://api.themoviedb.org/3/discover/movie`

If you plan to publish or share this project, you should move the API key out of the client code (for example, load it from a backend or environment variable during a build step).

---

## Project Structure

- `index.html` — Home page (Trending/Popular/Search)
- `main.js` — Fetch + render movies, search logic, like/unlike logic
- `journal.html` — Favourites page
- `journal.js` — Render favourites, notes, remove actions
- `assets/` — Images, fonts, etc.

---

## Local Storage Keys Used

- `likedMovies` — array of liked movie objects (includes optional `note`)
- `Movies` — cached popular/discover results (as saved by the app)
- `TrendingMovies` — cached trending result objects (as saved by the app)

---

## Credits

- Movie data provided by [TMDB](https://www.themoviedb.org/)
- UI styling with Tailwind CSS

---

## License

No license specified yet. If you want, add a `LICENSE` file (MIT is common for student projects).
