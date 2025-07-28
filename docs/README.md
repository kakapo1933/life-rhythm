# Personal Task Tracker

A desktop application for managing personal tasks and tracking recurring events, built with Tauri, React, and TypeScript.

## Project Overview

This application provides a native desktop experience for task management and event tracking with local data persistence through SQLite. The application follows a modern architecture with React 19+ frontend, Tauri backend, and Tailwind CSS for styling.

## Technology Stack

- **Frontend**: React 19+ with TypeScript
- **Desktop Framework**: Tauri 2.x
- **Styling**: Tailwind CSS
- **Build Tool**: Vite
- **Package Manager**: pnpm
- **Database**: SQLite (local storage)

## Project Structure

```
├── src/                    # React frontend source
│   ├── components/         # React components
│   │   ├── common/         # Reusable UI components
│   │   ├── layout/         # Layout components
│   │   └── features/       # Feature-specific components
│   ├── hooks/              # Custom React hooks
│   ├── types/              # TypeScript type definitions
│   ├── utils/              # Utility functions
│   └── services/           # API and service layer
├── src-tauri/              # Tauri backend
│   ├── src/                # Rust source code
│   └── tauri.conf.json     # Tauri configuration
├── docs/                   # Project documentation
└── dist/                   # Build output
```

## Setup Instructions

1. **Prerequisites**:
   - Node.js (v18+)
   - Rust (latest stable)
   - pnpm package manager

2. **Installation**:
   ```bash
   # Install dependencies
   pnpm install
   
   # Start development server
   pnpm tauri dev
   
   # Build for production
   pnpm tauri build
   ```

3. **Development**:
   - Frontend runs on `http://localhost:5173`
   - Tauri handles the desktop application wrapper
   - Hot reload is enabled for both frontend and backend changes

## Architecture

The application follows a layered architecture:

- **Presentation Layer**: React components with TypeScript
- **Service Layer**: API abstraction and state management
- **Backend Layer**: Tauri commands and Rust handlers
- **Data Layer**: SQLite database with local persistence

## Next Steps

This initial setup provides the foundation for:
- Task management functionality
- Event tracking features
- Local data persistence
- Cross-platform desktop distribution

See the implementation tasks in `.kiro/specs/personal-task-tracker/tasks.md` for detailed development roadmap.