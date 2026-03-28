# Finance Tracker — Project Instructions

## Overview

A personal finance tracker built with React and Vite. Users can add income/expense transactions, view summary totals, and filter the transaction list by type and category.

## Tech Stack

- **Framework**: React 19 (functional components, hooks)
- **Build Tool**: Vite 7
- **Language**: JavaScript (JSX)
- **Styling**: Plain CSS (no CSS-in-JS, no Tailwind)

## Project Structure

```
src/
  main.jsx        # Entry point, renders <App /> into #root
  App.jsx         # Single-component app with all state and UI
  App.css         # App-specific styles
  index.css       # Global/reset styles
  assets/         # Static assets
public/           # Public static files
index.html        # HTML shell
```

## Architecture

- Currently a single-component app (`App.jsx`) — all state lives in `App` via `useState`
- No routing, no state management library, no backend
- Transactions are stored in local component state (not persisted)
- Categories are hardcoded: food, housing, utilities, transport, entertainment, salary, other

## Code Conventions

- Use functional components with hooks (`useState`, etc.)
- Use plain CSS with class names — no CSS modules, no utility frameworks
- Keep JSX in `.jsx` files
- Use `Date.now()` for generating unique IDs
- Amounts are stored as strings from input; summary calculations use addition directly

## Build & Run

```bash
npm install       # Install dependencies
npm run dev       # Start Vite dev server (http://localhost:5173)
npm run build     # Production build
npm run preview   # Preview production build
npm run lint      # Run ESLint
```

## Known Issues / Bugs

- Transaction amounts are stored as strings, causing summary totals to concatenate instead of sum numerically
- "Freelance Work" is marked as `type: "expense"` but should likely be `type: "income"`
- No input validation beyond empty checks
- No delete or edit functionality for transactions
- Data is not persisted (resets on page refresh)
