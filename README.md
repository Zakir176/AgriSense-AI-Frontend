# AgriSense AI — Frontend

Vue 3 + Vite frontend for **AgriSense AI** — an intelligent poultry farm management platform.

Features an offline-first PWA with Capacitor mobile support, real-time visual monitoring, audio telemetry, and comprehensive farm analytics.

## Related Repository

- **Backend API**: [AgriSense-AI-Backend](https://github.com/Zakir176/AgriSense-AI-Backend)

## Tech Stack

- **Framework**: Vue 3 (Composition API)
- **Build Tool**: Vite
- **Styling**: Tailwind CSS
- **Charts**: Chart.js + chartjs-plugin-zoom
- **i18n**: vue-i18n (English + Chichewa)
- **Offline**: IndexedDB (idb) + Service Worker (vite-plugin-pwa)
- **Mobile**: Capacitor (Android + iOS)
- **Testing**: Vitest + Vue Test Utils

## Quick Start

### Prerequisites

- Node.js 18+
- The [AgriSense-AI-Backend](https://github.com/Zakir176/AgriSense-AI-Backend) running locally or deployed

### Setup

```bash
# 1. Install dependencies
npm install

# 2. Configure environment
cp .env.example .env.local
# Edit .env.local — set VITE_API_URL to your backend

# 3. Start dev server
npm run dev
```

The app will be available at `http://localhost:5173`.

### Build for Production

```bash
npm run build
npm run preview  # preview the production build
```

### Mobile (Capacitor)

```bash
npm run cap:sync    # build + sync to native projects
npx cap open android  # open in Android Studio
npx cap open ios      # open in Xcode
```

## Environment Variables

| Variable | Description | Default |
|---|---|---|
| `VITE_API_URL` | Backend API base URL | `http://127.0.0.1:8000/api/v1` |

## Project Structure

```
src/
├── App.vue              # Root component with navigation
├── main.js              # App entry point
├── style.css            # Global styles
├── i18n.js              # Internationalization setup
├── assets/              # Images, CSS animations
├── components/          # Reusable components
│   ├── ui/              # Design system (AgriButton, AgriCard, etc.)
│   └── __tests__/       # Component tests
├── composables/         # Vue composables (hooks)
├── locales/             # Translation files (en, ny)
├── router/              # Vue Router config
├── services/
│   ├── api.js           # API client (offline-first)
│   ├── db.js            # IndexedDB cache
│   └── store.js         # Reactive state
├── utils/               # Utility functions
└── views/               # Page-level components
```

## Testing

```bash
npm run test
```

## License

See [CONTRIBUTING.md](CONTRIBUTING.md) for contribution guidelines.
