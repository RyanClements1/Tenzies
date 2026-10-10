# Tenzies Dice Game 🎲

Tenzies is an interactive dice game built with **React** and **JavaScript**. Roll ten dice, hold the values you want to keep, and continue rolling until all ten dice show the same number. When you win, the game displays confetti and lets you start a new round.

## Features

- Roll ten six-sided dice.
- Click a die to hold or release it between rolls.
- Automatically detect a win when every die is held and all ten values match.
- Celebrate a win with a confetti animation.
- Start a fresh game with the **New Game** button.
- Use accessible button labels and a screen-reader win announcement.

## Technologies and dependencies

The project's dependencies are listed in [`package.json`](./package.json). Click a package name to visit its documentation or npm page.

| Package | Version in project | Purpose | Link |
| --- | --- | --- | --- |
| React | 18.3.1 | Builds the game's user interface and manages state | [React documentation](https://react.dev/) |
| React DOM | 18.3.1 | Renders React components in the browser | [react-dom on npm](https://www.npmjs.com/package/react-dom) |
| Nano ID | 5.0.7 | Generates unique IDs for each die | [nanoid on npm](https://www.npmjs.com/package/nanoid) |
| React Confetti | 6.1.0 | Displays confetti when the player wins | [react-confetti on npm](https://www.npmjs.com/package/react-confetti) |
| Vite | latest (per `package.json`) | Runs the development server and builds the app | [Vite documentation](https://vite.dev/) |
| Vite React plugin | `*` (development dependency) | Enables React support in Vite | [@vitejs/plugin-react on npm](https://www.npmjs.com/package/@vitejs/plugin-react) |

## Prerequisites

Install **Node.js** and **npm** before running the project:

- [Download Node.js (LTS)](https://nodejs.org/en/download)
- [npm documentation](https://docs.npmjs.com/)
- [Git downloads](https://git-scm.com/downloads) (optional, for cloning a repository)

To check that Node.js and npm are installed, open a terminal and run:

```bash
node --version
npm --version
```

## Installation and setup

1. **Get the project files.** Download the project ZIP and extract it, or clone your GitHub repository if you've uploaded it there.
2. **Open a terminal in the project folder**, where `package.json` is located.
3. **Install all dependencies:**

   ```bash
   npm install
   ```

   This reads `package.json` and installs React, React DOM, Nano ID, React Confetti, Vite, and the Vite React plugin. You do **not** need to install those packages one by one.

4. **Start the development server:**

   ```bash
   npm start
   ```

   You can also run `npm run dev`, which starts the same Vite development server.

5. **Open the local URL** printed in your terminal (typically `http://localhost:5173/`) in your browser.

### Optional: install dependencies individually

If you are rebuilding the project from an empty npm setup rather than using the included `package.json`, install the runtime dependencies with:

```bash
npm install react@18.3.1 react-dom@18.3.1 nanoid@5.0.7 react-confetti@6.1.0 vite@latest
```

Then install the Vite React plugin as a development dependency:

```bash
npm install --save-dev @vitejs/plugin-react
```

**Note:** These individual installation commands are *not* necessary after running `npm install` in this project. The commands above mirror the package versions in this repository, except for dependencies whose versions are already set to `latest` or `*`.

## Available commands

| Command | Description |
| --- | --- |
| `npm install` | Install dependencies from `package.json`. |
| `npm start` | Start the Vite development server. |
| `npm run dev` | Start the same development server. |
| `npm run build` | Create a production build in `dist/`. |
| `npm run preview` | Preview the production build locally. |

## How to play

1. Click **Roll** to change the values of all dice that are not held.
2. Click any die to **hold** its current number. Click it again to release it.
3. Keep rolling until **all ten dice have matching numbers and are held**.
4. When the confetti appears, click **New Game** to play again.

## Project structure

```text
.
├── App.jsx          # Game state, rolling, hold logic, and win detection
├── Die.jsx          # Individual clickable die component
├── index.jsx        # React entry point
├── index.css        # Styles for the game
├── index.html       # HTML document
├── package.json     # Scripts and dependency declarations
├── vite.config.js   # Vite and React plugin configuration
└── README.md        # Project documentation
```

## Learning resource

This project is based on a React learning exercise from [Scrimba's Learn React course](https://scrimba.com/learn-react-c0e/~04ao).
