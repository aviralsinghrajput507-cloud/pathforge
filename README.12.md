# PathForge: Reverse-Engineered Career Roadmapper

Hackathon problem statement: **1**

Type a hyper-specific dream job. PathForge asks a generative AI (Gemini) to work backwards from that goal and draws an interactive skill tree: goal on the right, prerequisites on the left. Click any node to see details and mark it done.

## How it works
- `index.html`: the whole front end (plain HTML, CSS, JS, SVG graph).
- `netlify/functions/roadmap.mjs`: calls the Gemini API. The API key stays on the server.
- If the AI is unreachable, the app shows a clearly labelled sample roadmap.

## Privacy
Only the dream job, current skills and level are sent to the AI. The page tells the user when AI is used. No name or other personal data is collected.

## Run / deploy
1. Import this repo in Netlify (no build command, publish directory `.`).
2. Add `GEMINI_API_KEY` as an environment variable (see `.env.example`).
3. Deploy.
