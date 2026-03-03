# Development Setup

  Set up your environment to contribute to HAYA-TAB.

  ## Prerequisites

  | Tool | Version | Installation |
  |------|---------|--------------|
  | Go | 1.21+ | [go.dev/dl](https://go.dev/dl/) |
  | Node.js | 18+ | [nodejs.org](https://nodejs.org/) |
  | Wails | v2 | `go install github.com/wailsapp/wails/v2/cmd/wails@latest` |
  | Git | Any | [git-scm.com](https://git-scm.com/) |

  ### Verify Installation
  ```bash
  go version      # go version go1.21+
  node --version  # v18+
  wails version   # v2.x.x
  ```

  ---

  ## Clone & Setup

  ```bash
  # Clone repository
  git clone https://github.com/HAYASAKA7/HAYA-TAB.git
  cd HAYA-TAB

  # Install frontend dependencies
  cd frontend
  npm install
  cd ..

  # Verify Wails setup
  wails doctor
  ```

  ---

  ## Development Mode

  ```bash
  wails dev
  ```

  This starts:
  - Go backend with hot reload
  - Vite dev server for frontend
  - Opens app window automatically

  **Frontend changes:** Auto-reload via Vite HMR
  **Backend changes:** Requires restart (Ctrl+C, then `wails dev` again)

  ---

  ## Project Structure

  ```
  HAYA-TAB/
  ├── internal/app/       # Backend API
  ├── main.go             # Entry point, file server
  ├── frontend/           # Vue 3 + TypeScript
  │   ├── src/
  │   │   ├── components/ # Vue components
  │   │   ├── stores/     # Pinia state
  │   │   ├── composables/# Reusable logic
  │   │   ├── i18n/       # Translations
  │   │   └── views/      # Page views
  │   └── vite.config.ts
  ├── pkg/                # Go packages
  │   ├── store/          # SQLite + FTS5 (database_tabs.go, database_categories.go, database_settings.go)
  │   ├── sync/           # File sync engine
  │   ├── metadata/       # Parsing logic (MusicBrainz integration, initial calculation)
  │   ├── watcher/        # File watcher
  │   └── coverpool/      # Cover download pool
  ├── storage/            # Uploaded tabs
  ├── covers/             # Cover art cache
  └── data/               # SQLite database
  ```

  ---

  ## Building

  ```bash
  # Development build
  wails build

  # Production build (optimized)
  wails build -production

  # Cross-platform
  wails build -platform windows/amd64
  wails build -platform darwin/arm64
  wails build -platform linux/amd64
  ```

  Output: `build/bin/HAYA-TAB[.exe]`

  ---

  ## Testing

  ```bash
  # Backend tests
  go test ./...

  # Frontend type check
  cd frontend && npm run build
  ```

  ---

  ## Common Tasks

  ### Add a New Backend API

  1. Add method to `internal/app/app.go`
  2. Run `wails generate module`
  3. Import in frontend from `@/wailsjs/go/app/App`

  ### Add a New Translation

  1. Copy `frontend/src/i18n/locales/en.json`
  2. Translate strings
  3. Register in `frontend/src/i18n/index.ts`

  ### Add a New Component

  1. Create `.vue` file in `frontend/src/components/`
  2. Import and use in parent component

  ---