
# Schedulion OFF — Your private desktop calendar 🗓️✨

![Hero image](https://img.freepik.com/free-vector/laptop-with-program-code-isometric-icon-software-development-programming-applications-dark-neon_39422-971.jpg)

[![version](https://img.shields.io/badge/version-0.1.5-blue.svg)](./package.json) [![license](https://img.shields.io/badge/license-MIT-green.svg)](./LICENSE)

Welcome to Schedulion OFF — a fast, offline-first desktop calendar built for people who want privacy, speed, and a delightful UI. This repo bundles a modern React renderer (Vite + TypeScript) and an Electron shell so you get a native-feeling desktop app with web dev ergonomics.

## 🚀 Highlights

- 🔒 Offline-first & local-first data — your events stay on your machine.
- ⚡ Snappy UI built with React + Vite + Tailwind + Framer Motion.
- 📅 Multiple calendar views: Day, Week, Month, Year, Widgets.
- 🔁 Import / export and optional encryption utilities for backups.
- 🖥️ Packaged with Electron + electron-builder for Windows/macOS/Linux.

## 🧩 Technology

- Renderer: React + TypeScript + Vite
- Styling: Tailwind CSS
- Desktop: Electron + electron-builder
- Developer tools: concurrently, cross-env, TypeScript

## 📁 Repo layout

- `client/` — Vite + React app (UI)
- `electron/` — Electron main & preload code
- `release/` — generated build artifacts and installers
- `DOCS.md` — design & docs

## ⚡ Quick start (PowerShell)

Install dependencies and run the dev environment (renderer + Electron):

```powershell
# From repository root
npm install
cd client; npm install; cd ..

# Start renderer + electron in dev mode
npm run electron:dev
```

Only editing the web UI? Run the renderer alone:

```powershell
cd client
npm run dev
```

Build production artifacts and package the app:

```powershell
# Build renderer and package the Electron app
npm run electron:build

# Or build renderer only
cd client; npm run build
```

Preview the renderer production build:

```powershell
cd client
npm run preview
```

Notes:
- `renderer:dev` and `renderer:build` are root helper scripts that call the `client/` scripts with the right environment variables.
- `electron:dev` runs the renderer dev server and Electron concurrently for fast iteration.

```markdown
![My app — calendar view](docs/assets/screenshot-1.png)
![My app — event modal](docs/assets/screenshot-2.png)
```

Tips:
- Prefer PNG or JPG. For animated demos, use GIF or a short MP4 (hosted or in `docs/assets/`).
- Recommended width: 1000–1600px for good display on GitHub. Optimize images before committing (tinyPNG, ImageOptim, or a CLI tool).

If you want, I can:
- Add a small script that generates a markdown gallery from anything inside `docs/assets/`.
- Resize and optimize images I add for you.
## 🛠️ Development tips

- Run `npm run electron:dev` to iterate quickly (UI updates + Electron reload).
- Use `cd client && npm run typecheck` to run TypeScript project references (`tsc -b`).
- When packaging, electron-builder uses the `build` block in `package.json` to create release artifacts in `release/`.

## 🧾 Data & privacy

Schedulion OFF keeps user data locally by default. The repo includes helpers for import/export and optional encryption. Always backup before migrations.

## 🤝 Contributing

Contributions are welcome. A simple flow:

1. Open an issue to discuss bigger changes.
2. Fork, create a branch (`feat/your-feature` or `fix/issue-123`).
3. Keep PRs focused and add a short description of the change.
4. Ensure `tsc -b` passes in `client/` and the app runs in dev.

## 🧰 Tests & typecheck

Typecheck the client:

```powershell
cd client
npm run typecheck
```

Add unit/integration tests as needed — I can scaffold a minimal test setup (Vitest + React Testing Library) if you want.

## ⚠️ Troubleshooting

- Electron fails to launch: ensure the renderer is running and no port conflicts exist.
- Build issues on Windows: verify Node version and any native build tools are installed.
- Packaging problems: check `release/` and `electron-builder` logs for details.

## 📜 License

MIT — see `LICENSE`.


## 🙏 Credits & assets

- Hero & primary screenshot: "Laptop with program code isometric icon — software development" (Freepik). Source page:

	https://www.freepik.com/free-vector/laptop-with-program-code-isometric-icon-software-development-programming-applications-dark-neon_4102879.htm

- License: this image is provided under Freepik's licensing terms. See Freepik license details:

	https://support.freepik.com/s/topic/0TO3V000000Cla4WAC/licenses?language=en_US

- Please ensure you comply with Freepik's license (attribution requirements or a valid commercial/premium license). If you don't have redistribution rights, replace the image with your own screenshots or purchase the appropriate Freepik license before publishing.

- Other placeholder screenshots are hotlinked from Unsplash via `https://source.unsplash.com`.

- Badges by shields.io.

---

If you want, I can now:

- Replace placeholder Unsplash images with real screenshots (you can paste images here or I can add instructions to capture them). 
- Add polished badges (CI, downloads, platform support) and a GIF demo.
- Create a `docs/` folder with high-resolution local images and a `CONTRIBUTING.md`.

Which of the above would you like next?
