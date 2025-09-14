Chuenlay Belajar — Complete package (ready-to-build APK)
=======================================================

This package includes a full frontend React PWA, backend Express API (file-based sample), Capacitor config,
adaptive icons, docker-compose for running backend in development, and sample data.

Quick start (dev):
1. Install Node.js (>=16) and npm.
2. In project root, run:
   cd backend && npm install
   node src/index.js
   # backend runs on http://localhost:4000
3. In a separate terminal, run frontend dev:
   cd frontend && npm install && npm run dev -- --host
   # frontend runs on http://localhost:5173

To build APK (Capacitor):
1. cd frontend && npm install && npm run build
2. npm install @capacitor/core @capacitor/cli
3. npx cap init "Chuenlay Belajar" id.chuenlay.belajar --web-dir=frontend/dist
4. npx cap add android
5. npx cap sync android
6. npx cap open android (open Android Studio and build APK) or build via CLI.

Notes:
- The backend in this package uses JSON files (sample_data) for simplicity. You can switch to PostgreSQL by using the migrations in /backend/migrations and adjusting docker-compose.
- Keystore creation and signing are not included. See capacitor/APK_README.md for signing steps.
