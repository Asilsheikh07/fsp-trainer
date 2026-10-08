# FSP Trainer

**Practice the German FSP (Fachsprachprüfung) with an AI patient.**
A free exam-prep platform for dentists moving to Germany: talk to a virtual patient in German by text or voice, take the history, make a diagnosis, and level up as you go.

**[Live demo → fsp-trainer-six.vercel.app](https://fsp-trainer-six.vercel.app)**

## Features

- **AI patient conversations** in German, powered by Gemini
- **Voice mode** with speech transcription and natural text-to-speech (ElevenLabs)
- **Diagnosis practice** with real radiograph findings from Wikimedia Commons (open licenses)
- **Learning tools:** lessons, daily practice, mistake review, a coach and a game mode
- **Career system and certificates** to track progress
- **Accounts** with Supabase Auth, protected by Cloudflare Turnstile

## Tech stack

| Layer | Technology |
|:--|:--|
| Frontend & backend | Next.js (App Router), React |
| Database & auth | Supabase (Postgres + Auth) |
| AI conversation & transcription | Gemini API |
| Text-to-speech | ElevenLabs |
| Hosting | Vercel |
| Testing | Vitest, ESLint |

## Run locally

```bash
git clone https://github.com/Asilsheikh07/fsp-trainer.git
cd fsp-trainer
npm install
cp .env.example .env.local   # then fill in your keys
npm run dev
```

Open http://localhost:3000.

### Environment variables

| Variable | Where it's used |
|:--|:--|
| `NEXT_PUBLIC_SUPABASE_URL`, `NEXT_PUBLIC_SUPABASE_ANON_KEY` | Supabase client |
| `SUPABASE_SERVICE_ROLE_KEY` | Server only, never expose to the browser |
| `GEMINI_API_KEY` | AI patient and transcription |
| `ELEVENLABS_API_KEY` | Voice output |
| `NEXT_PUBLIC_TURNSTILE_SITE_KEY` | Bot protection on sign-up |

See [SECURITY_SETUP.md](SECURITY_SETUP.md) for key handling.

## Scripts

| Command | What it does |
|:--|:--|
| `npm run dev` | Start the dev server |
| `npm run test` | Run tests (Vitest) |
| `npm run lint` | Lint the code |
| `npm run check` | Lint, test and build |

## Author

Built by **Asil**, web developer and AI engineer.
[Instagram](https://instagram.com/asilsheikh) · [Telegram](https://t.me/asilsheikh) · [infoaurasil@gmail.com](mailto:infoaurasil@gmail.com)
