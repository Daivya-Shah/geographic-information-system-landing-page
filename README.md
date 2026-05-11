# Site Selection Dashboard

An internal tool for Newmark brokers to browse site selection and location strategy services, then request custom reports for their clients.

## What it does

Brokers land on a dashboard that showcases six service offerings (Labor Analytics, Market Trends, GIS Data Analysis, Risk Mitigation, Transportation & Emergency Planning, and Competitive Analysis). From there, they fill out a short form with client details and hit "Request client report," which drafts a pre-filled email in their default mail client.

No backend, no auth, no database. Just a clean UI that gets out of the way.

## Tech stack

- **React 18 + TypeScript** via Vite
- **Tailwind CSS** with a custom HSL design token system
- **shadcn/ui** for the base component library (Radix UI primitives)
- **React Router v6** and **TanStack Query** wired up and ready for future use
- **lucide-react** plus custom SVGs for icons

## Getting started

Install dependencies and start the dev server:

```bash
npm install
npm run dev
```

Other scripts:

```bash
npm run build       # production build
npm run build:dev   # development build
npm run preview     # preview the production build locally
npm run lint        # run ESLint
```

## Project structure

```
src/
├── components/
│   ├── SiteSelectionDashboard.tsx   # main UI component
│   ├── Icons/                       # SVG icon assets
│   ├── Images/                      # hero image
│   └── ui/                          # shadcn/ui components
├── pages/
│   ├── Index.tsx                    # home route
│   └── NotFound.tsx                 # 404 route
├── hooks/                           # custom React hooks
├── lib/                             # utility functions
├── index.css                        # design tokens and global styles
└── App.tsx                          # router and provider setup
```

## Layout

The dashboard has three panels:

- **Left sidebar** - collapsed icon navigation with the Newmark logo and nav items
- **Main content** - page title, a full-width hero image, and a 3x2 grid of service cards that overlap the bottom of the hero
- **Right sidebar** - a sticky request form (visible on screens 1600px and wider)

On tablet (900px to 1599px) and mobile (under 900px), the right sidebar is hidden and a "Request report" button opens a modal with the same form.

## Design system

All colors are defined as HSL CSS custom properties in `src/index.css`. The primary brand color is Newmark blue (`hsl(204 100% 36%)`). Card titles use Libre Baskerville (serif) and everything else uses Inter.
