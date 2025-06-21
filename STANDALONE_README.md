# Mood Tracker - Standalone Version

A beautiful, interactive mood tracking calendar app built with React, TypeScript, and Vite. Track your daily emotions with emojis and visualize your mood patterns over time.

## Features

- 📅 Interactive calendar interface with emoji mood tracking
- 🎨 Dark-themed responsive design with neon accents
- 📊 Statistics page showing mood breakdown and streaks
- ⚙️ Settings with theme toggle and data management
- 💾 Local storage for persistent data
- 📤 Export/Import functionality for data backup
- 🎭 5 mood options: 😊 😢 💔 😡 ✅

## Installation & Setup

### Prerequisites
- Node.js (version 16 or higher)
- npm or yarn

### Getting Started

1. **Clone or download this project**

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the development server**
   ```bash
   npm run dev
   ```

4. **Open your browser**
   Navigate to `http://localhost:5173` (or the port shown in terminal)

## Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint

## Project Structure

```
├── client/src/
│   ├── components/          # Reusable UI components
│   │   ├── ui/             # Shadcn/ui components
│   │   ├── calendar.tsx    # Main calendar component
│   │   ├── emoji-picker.tsx # Emoji selection modal
│   │   ├── bottom-navigation.tsx # Navigation bar
│   │   └── theme-provider.tsx # Theme context
│   ├── hooks/              # Custom React hooks
│   │   ├── use-mood-data.ts # Mood data management
│   │   └── use-toast.ts    # Toast notifications
│   ├── lib/                # Utility functions
│   │   ├── mood-storage.ts # LocalStorage wrapper
│   │   └── utils.ts        # Helper utilities
│   ├── pages/              # Page components
│   │   ├── home.tsx        # Calendar page
│   │   ├── stats.tsx       # Statistics page
│   │   └── settings.tsx    # Settings page
│   ├── App.tsx             # Main app component
│   └── index.css           # Global styles
├── shared/
│   └── schema.ts           # TypeScript types
└── server/                 # Simple Express server (optional)
```

## Data Storage

The app uses browser localStorage to persist your mood data. Your data includes:
- Daily mood entries (date → emoji mapping)
- Theme preferences
- All data stays on your device

## Export/Import Data

- **Export**: Go to Settings → Export Data to download your mood data as JSON
- **Import**: Go to Settings → Import Data to restore from a JSON file

## Customization

### Adding New Moods
Edit `client/src/components/emoji-picker.tsx`:
```typescript
const emojis = ['😊', '😢', '💔', '😡', '✅', '🎉']; // Add new emoji
```

### Changing Colors
Edit `client/src/index.css` to modify the color scheme:
```css
:root {
  --neon-purple: hsl(262, 83%, 58%);
  --neon-pink: hsl(326, 78%, 69%);
  --neon-cyan: hsl(189, 94%, 43%);
}
```

## Building for Production

1. **Build the app**
   ```bash
   npm run build
   ```

2. **Serve the built files**
   The `dist` folder contains all static files that can be served by any web server.

## Technologies Used

- **React 18** - UI framework
- **TypeScript** - Type safety
- **Vite** - Build tool and dev server
- **Tailwind CSS** - Styling
- **Shadcn/ui** - UI components
- **Lucide React** - Icons
- **TanStack Query** - Data fetching (simplified for standalone)

## Browser Support

- Chrome/Edge 88+
- Firefox 78+
- Safari 14+

## License

This project is open source and available under the MIT License.