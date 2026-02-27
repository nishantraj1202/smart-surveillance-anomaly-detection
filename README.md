# Sentinel: AI Video Threat Analysis

Sentinel is a multimodal AI-powered web application that performs frame-by-frame analysis of surveillance videos to detect threats such as violence, accidents, fire, theft, and other anomalies in real-time.

## Features

- **Upload & Analyze**: Upload surveillance footage and automatically analyze it using advanced AI models.
- **Threat Detection**: Automatically identifies violence, accidents, fire, theft, and other anomalies.
- **Frame Extraction**: Extracts key frames from the video for a detailed pinpointed analysis.
- **Detailed Threat Reporting**: Provides an analysis summary, confidence score, and timestamp of detected anomalies.

## Project Architecture

The codebase has a feature-based structure for better scalability:

```text
src/
├── core/
│   ├── api/             # Supabase and other external API integrations
│   ├── components/      # Shared components (e.g., UI elements, NavigationLink)
│   ├── hooks/           # Core hooks (e.g., use-toast)
│   └── lib/             # Shared utilities
├── features/
│   └── video-analysis/
│       ├── components/  # Feature-specific components (e.g., VideoUploader, AnalysisProgress)
│       └── utils/       # Feature-specific utilities (e.g., frameExtractor)
└── pages/
    ├── Home.tsx         # The main entrypoint mapping video analysis features
    └── Error404.tsx     # Catch-all 404 page
```

## Tech Stack

- **Framework**: [React](https://react.dev/) + [Vite](https://vitejs.dev/)
- **Styling**: [Tailwind CSS](https://tailwindcss.com/)
- **UI Components**: [Shadcn UI](https://ui.shadcn.com/) (Radix Primitives)
- **Animations**: [Framer Motion](https://www.framer.com/motion/)
- **State & Data Fetching**: [TanStack Query](https://tanstack.com/query)
- **Backend/AI Trigger**: [Supabase Edge Functions](https://supabase.com/) integrating Gemini Multimodal Analysis

## Setup & Run Local Development

1. **Install dependencies**
   ```bash
   npm install
   ```

2. **Start the development server**
   ```bash
   npm run dev
   ```

3. **Build for production**
   ```bash
   npm run build
   ```

## Environment Variables

Make sure to create a `.env` file at the root of your project based on `.env.example` (or configure your Supabase instance to match your backend endpoints).

```env
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
```
