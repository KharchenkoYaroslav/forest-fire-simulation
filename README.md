# 🔥 Forest Fire Simulation

An interactive forest fire simulation built to explore probabilistic cellular automata. Uses Server-Sent Events to stream real-time generation updates via Next.js.

## 📦 Technologies

- `TypeScript`
- `Nx`
- `Next.js`
- `React`
- `Server-Sent Events`
- `SCSS`

## 🚀 Features

- **Probabilistic Simulation**: Visualizes complex fire spread dynamics based on cellular automata principles
- **Real-time Streaming**: Uses Server-Sent Events for seamless, unidirectional state updates via Next.js
- **Interactive Grid**: Ability to toggle cell states and define custom simulation scenarios
- **Configurable Parameters**: Dynamic control over field size, burn probability, fire duration, and update intervals
- **Simulation Control**: Ability to start, stop, and resume the simulation at any moment, preserving the current grid state
- **Viewport Navigation**: Intuitive pan and zoom controls to freely explore and inspect specific areas of the simulation grid

## 📍 The Process

This is a small educational project for researching cellular algorithms. It provided me with experience working with Next.js as a fully self-sufficient application, utilizing Server-Sent Events, and experience working with an interactive canvas. 

## 🏗️ System Architecture

The system is built as a unified **Next.js** application managed within an **Nx** mosnorepo:

- **Backend API** (`Next.js API Routes`): Handles simulation initialization and manages session state. It calculates the next generation of the fire spread using cellular automata algorithms on the server.
- **Real-time Stream** (`Server-Sent Events`): A dedicated unidirectional channel that pushes simulation updates from the server to the client.
- **Client** (`React`): Consumes the SSE stream and visualizes the grid using an optimized HTML5 Canvas component. 

## 📂 Project Structure

This monorepo project is organized into the following key areas:

- `apps/forest-fire-simulation` - Main Next.js application containing both frontend and backend logic.
  - `src/app/algorithm` - Core logic implementation of the probabilistic cellular automaton model.
  - `src/app/api` - API routes handling session creation and real-time event streaming.
  - `src/app/page.tsx` - Main UI page orchestrating the simulation state, canvas rendering, and control menu.
  - `src/app/components` - UI components including the interactive `Canvas` and `ControlMenu`.
  - `src/types` - Shared TypeScript definitions for simulation state, cell structures, and API types.

## 🚦 Running the Project

1. Clone the repository
2. Install dependencies: `npm install`
3. Start the applications:
```
npx nx run forest-fire-simulation:start 
```
4. Open `http://localhost:3000` in your browser
> [!TIP]
> Highly recommend installing the Nx Console extension for VS Code.

## 🎞️ Preview

https://github.com/user-attachments/assets/c508a33a-9e2d-4820-8788-f69505217090
