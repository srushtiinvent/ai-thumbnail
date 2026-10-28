# ThumbCraft AI

An AI thumbnail studio for YouTube creators. Describe your video, and ThumbCraft optimises your prompt, generates thumbnail images, and saves everything to your history.

🔗 **Live demo:** TODO_ADD_NETLIFY_LINK

![ThumbCraft AI preview](docs/preview.png)
<!-- TODO: take a screenshot, save it as docs/preview.png -->

## Features

- **Prompt optimisation:** turns a rough idea into a detailed prompt built for thumbnail-style images
- **AI image generation:** creates thumbnails using Gemini and OpenAI models
- **History:** every generation is saved in MongoDB so you can revisit and reuse it
- **CDN delivery:** images are stored and served through Cloudinary
- TODO: add or remove features to match what the app really does (download, aspect ratio options, auth, etc.)

## Tech stack

| Layer | Tools |
|---|---|
| Frontend | React, Vite |
| Backend | Node.js, Express |
| Database | MongoDB |
| AI | Google Gemini, OpenAI |
| Media | Cloudinary |
| Deployment | Netlify (frontend) |

## How it works

1. You enter a video idea or title.
2. The backend rewrites it into an optimised image prompt.
3. The image model generates the thumbnail.
4. The image is uploaded to Cloudinary and its URL is saved to MongoDB.
5. The frontend shows the result and your past generations.

## Getting started

### Prerequisites

- Node.js 18+
- A MongoDB database (Atlas or local)
- API keys for Gemini, OpenAI and Cloudinary

### Install

```bash
git clone https://github.com/srushtiinvent/ai-thumbnail.git
cd ai-thumbnail
npm install
cd backend && npm install
```

### Environment variables

Create `backend/.env`. TODO: rename these to match the names in your code.

```env
PORT=5000
MONGODB_URI=your_mongodb_connection_string
GEMINI_API_KEY=your_gemini_key
OPENAI_API_KEY=your_openai_key
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_key
CLOUDINARY_API_SECRET=your_cloudinary_secret
```

### Run

```bash
# backend
cd backend
npm start        # TODO: confirm the script name

# frontend (from the repo root, in another terminal)
npm run dev
```

The app runs at http://localhost:5173.

## Project structure

```
ai-thumbnail/
├── backend/        # API server, AI and database logic
├── src/            # React frontend
├── index.html
├── vite.config.js
└── netlify.toml    # Netlify deployment config
```

## Deployment

The frontend is deployed on Netlify using `netlify.toml`. TODO: say where the backend is hosted (Render, etc.) and how the frontend finds it.

## Roadmap

- [ ] User accounts and per-user history
- [ ] Usage limits and cost tracking
- [ ] Style presets and templates
- [ ] Caching for repeated prompts

## Author

**Srushti Nerkar**: [GitHub](https://github.com/srushtiinvent) · [LinkedIn](https://www.linkedin.com/in/srushti-nerkar-58034827b/)
