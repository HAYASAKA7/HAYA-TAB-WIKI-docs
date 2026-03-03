# Installation

  ## Pre-built Binaries (Recommended)

  Download the latest release for your platform:

  👉 **[Download from Releases](https://github.com/HAYASAKA7/HAYA-TAB/releases)**

  | Platform | File |
  |----------|------|
  | Windows | `HAYA-TAB-windows-amd64.exe` |
  | macOS (Intel) | `HAYA-TAB-darwin-amd64` |
  | macOS (Apple Silicon) | `HAYA-TAB-darwin-arm64` |
  | Linux | `HAYA-TAB-linux-amd64` |

  ### Windows
  1. Download the `.exe` file
  2. Double-click to run (no installation required)
  3. Windows may show a SmartScreen warning - click "More info" → "Run anyway"

  ### macOS
  1. Download the appropriate file for your Mac
  2. Open Terminal and run: `chmod +x HAYA-TAB-darwin-*`
  3. Right-click the file → Open (to bypass Gatekeeper on first run)

  ### Linux
  1. Download the Linux binary
  2. Make it executable: `chmod +x HAYA-TAB-linux-amd64`
  3. Run: `./HAYA-TAB-linux-amd64`

  ---

  ## Build from Source

  ### Prerequisites

  - [Go 1.21+](https://go.dev/dl/)
  - [Node.js 18+](https://nodejs.org/) (with npm)
  - [Wails v2](https://wails.io/docs/gettingstarted/installation)

  ### Steps

  ```bash
  # 1. Clone the repository
  git clone https://github.com/HAYASAKA7/HAYA-TAB.git
  cd HAYA-TAB

  # 2. Install frontend dependencies
  cd frontend
  npm install
  cd ..

  # 3. Run in development mode
  wails dev

  # 4. Build for production
  wails build

  # Cross-Platform Builds

  # Windows
  wails build -platform windows/amd64

  # macOS Intel
  wails build -platform darwin/amd64

  # macOS Apple Silicon
  wails build -platform darwin/arm64

  # Linux
  wails build -platform linux/amd64
  ```

  Build output will be in the `build/bin/` directory.

  ---