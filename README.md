    .\start.ps1
  Option B - Separate Windows:
    Terminal 1 (Backend):
      .\run_backend.ps1
      (Service runs at http://localhost:8000 | Docs at http://localhost:8000/docs)
    Terminal 2 (Frontend):
      .\run_frontend.ps1
      (Service runs at http://localhost:5173)
--------------------------------------------------------------------------------
5. RUNNING THE AUTOMATED TEST SUITE
--------------------------------------------------------------------------------
To run the complete full-stack automated test suite:
  .\run_tests.ps1
  Backend Tests:  9 passed (Pytest + HTTPX)
  Frontend Tests: 3 passed (Vitest)
  Status:         SUCCESS (100% pass rate)
--------------------------------------------------------------------------------
6. REPOSITORY STRUCTURE
--------------------------------------------------------------------------------
payrakshak-ai/
  |-- backend/
  |     |-- app/
  |     |     |-- api/             # REST endpoints (transactions, messages, analytics)
  |     |     |-- core/            # Config and database session
  |     |     |-- models/          # DB models & Pydantic schemas
  |     |     |-- services/        # Rule engine, ML engine, NLP engine, seeder
  |     |     |-- ml/              # Trained model joblib artifacts
  |     |     `-- main.py          # FastAPI application entrypoint
  |     |-- tests/                 # Backend automated test suite
  |     `-- requirements.txt       # Python dependencies
  |-- frontend/
  |     |-- src/
  |     |     |-- components/      # UI components (Navbar, Sidebar, Badges, Modals)
  |     |     |-- pages/           # 6 core dashboards and simulators
  |     |     |-- services/        # API client
  |     |     |-- types/           # TypeScript interfaces
  |     |     `-- tests/           # Vitest component tests
  |     |-- package.json
  |     `-- tailwind.config.js
  |-- payrakshak.db                # SQLite database pre-seeded with live data
  |-- run_backend.ps1              # Backend runner script
  |-- run_frontend.ps1             # Frontend runner script
  |-- run_tests.ps1                # Automated full-stack test runner
  |-- start.ps1                    # One-click launcher script
  |-- README.md                    # Detailed Markdown documentation
  `-- README.txt                   # Plain text project guide
================================================================================
