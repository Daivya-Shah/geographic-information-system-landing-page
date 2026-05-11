# Site Selection Dashboard

A dashboard landing page for a site selection and location strategy service. Users can browse service offerings and submit a report request for a client.

## What it does

The page showcases six service categories: Labor Analytics, Market Trends, GIS Data Analysis, Risk Mitigation, Transportation & Emergency Planning, and Competitive Analysis. A request form lets users fill in client details and submit directly via email.

No backend required. Form submission opens a pre-filled draft in the user's default mail client.

## Tech stack

- **React 18 + TypeScript** via Vite
- **Tailwind CSS** with a custom HSL design token system
- **shadcn/ui** for the base component library (Radix UI primitives)
- **React Router v6** and **TanStack Query**
- **lucide-react** plus custom SVGs for icons

## Getting started

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

- **Left sidebar** - collapsed icon navigation
- **Main content** - page title, a full-width hero image, and a grid of service cards that overlap the bottom of the hero
- **Right sidebar** - a sticky request form (visible on screens 1600px and wider)

On tablet (900px to 1599px) and mobile (under 900px), the right sidebar is hidden and a "Request report" button opens a modal with the same form.

## Design system

All colors are defined as HSL CSS custom properties in `src/index.css`. Card titles use Libre Baskerville (serif) and everything else uses Inter.
