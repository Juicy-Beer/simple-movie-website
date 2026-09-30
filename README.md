# Watch

Small Next.js app to browse movies and TV from TMDB and play embeds

## Stack

- Next.js (App Router)
- TMDB API (posters, search, details)
- CineSrc embed player (sandboxed iframe)

## Setup

1. Clone the repo
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
  movie/[id]/page.js
  tv/[id]/page.js
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
