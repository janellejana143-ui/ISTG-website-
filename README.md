# iSTG Website – Settings Page

This is a React + Vite + TailwindCSS project containing a **Settings UI** for iSTG.  
It includes Privacy, Notifications, Appearance, and Account Security settings using **lucide-react** icons and Tailwind styling.

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/YOUR-USERNAME/iSTG-website.git
cd iSTG-website
istg-website/
│
├── index.html
├── package.json
├── postcss.config.js
├── tailwind.config.js
├── vite.config.js
│
└── src/
    ├── App.jsx
    ├── index.css
    └── components/
        └── Settings.jsx
{
  "name": "istg-website",
  "version": "1.0.0",
  "private": true,
  "scripts": {
    "dev": "vite",
    "build": "vite build",
    "preview": "vite preview"
  },
  "dependencies": {
    "lucide-react": "^0.445.0",
    "react": "^18.3.1",
    "react-dom": "^18.3.1"
  },
  "devDependencies": {
    "@vitejs/plugin-react": "^4.2.0",
    "autoprefixer": "^10.4.20",
    "postcss": "^8.4.38",
    "tailwindcss": "^3.4.13",
    "vite": "^5.3.1"
  }
}
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>iSTG Website</title>
  </head>
  <body class="bg-gray-900">
    <div id="root"></div>
    <script type="module" src="/src/main.jsx"></script>
  </body>
</html>
import { defineConfig } from 'vite';
import react from '@vitejs/plugin-react';

// https://vitejs.dev/config/
export default defineConfig({
  plugins: [react()],
});
export default {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  },
};
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}"
  ],
  theme: {
    extend: {},
  },
  plugins: [],
};
@tailwind base;
@tailwind components;
@tailwind utilities;

body {
  font-family: system-ui, sans-serif;
}
import React from 'react';
import ReactDOM from 'react-dom/client';
import App from './App.jsx';
import './index.css';

ReactDOM.createRoot(document.getElementById('root')).render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);
import Settings from "./components/Settings";

function App() {
  return (
    <div className="min-h-screen bg-gray-900">
      <Settings />
    </div>
  );
}

export default App;
npm install
npm run dev
