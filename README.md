# Simple Movie Website
 
![Next.js](https://img.shields.io/badge/Next.js-black?style=for-the-badge&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-grey?style=for-the-badge&logo=react&logoColor=blue)
![TMDB](https://img.shields.io/badge/TMDB-blue?style=for-the-badge&logo=themoviedatabase&logoColor=white)
![Axios](https://img.shields.io/badge/Axios-purple?style=for-the-badge&logo=axios&logoColor=white)

Small Next.js app to browse movies and TV from TMDB and play embeds

## Stack

- Next.js (App Router)
- TMDB API (posters, search, details)
- CineSrc embed player (sandboxed iframe)

## Setup

1. Clone the repo

```bash 
git clone https://github.com/Juicy-Beer/simple-movie-website.git
```

2. Install dependencies:

```bash
npm install
npm install axios
```

3. Create `.env.local` in the project root:

```env
NEXT_PUBLIC_TMDB_API_KEY=your_tmdb_v3_key
```

Get an API key at https://www.themoviedb.org/settings/api

4. Run the dev server:

```bash
npm run dev
```

Open http://localhost:3000

## Routes

- `/` – popular movies/TV and search
- `/movie/[id]` – movie player
- `/tv/[id]?s=1&e=1` – TV player (season and episode)

## Project structure

```text
src/app/
  layout.js
  page.js
  movie/
      [id]/
          page.js
  tv/
    [id]/
        page.js
```

## Notes

- Embeds use CineSrc. If it breaks, change the embed URL in the movie/TV pages
- The iframe is sandboxed to stop the ads
- Don't commit `.env.local`

## Scripts

```bash
npm run dev      # local
npm run build    # production build
npm start        # run build
```
