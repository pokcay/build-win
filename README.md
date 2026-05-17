# Build New

A blank-slate starter for full-stack apps with **Rails 8 + Inertia.js + React 19 + PostgreSQL** — by [Brian Casel](https://buildermethods.com) at Builder Methods.

📚 [**Full documentation**](https://buildermethods.com/rails-react-template)

## Quick start

```bash
bin/setup      # installs gems, creates and migrates the database
npm install    # installs JS dependencies
bin/dev        # starts Rails (:3000) + Vite (:3036)
```

Requires Ruby 3.3.6, Node 20.19+ (or 22.12+), and PostgreSQL 10+.

## Windows setup

Windows requires a few extra steps:

**1. Install Ruby 3.3.x with DevKit**

Download **Ruby+Devkit 3.3.x (x64)** from [rubyinstaller.org/downloads](https://rubyinstaller.org/downloads/).
During installation, check "Add Ruby executables to your PATH" and run `ridk install` → choose option **3** at the end.

**2. Set Ruby 3.3 as active (if multiple versions installed)**

```powershell
$env:PATH = "C:\Ruby33-x64\bin;" + $env:PATH
ruby --version  # should show 3.3.x
```

**3. Run setup**

```powershell
bundle lock --add-platform x64-mingw-ucrt
ruby bin/setup
npm install
```

**4. Start the dev server**

On Windows, `bin/dev` does not work directly. Start each process in a separate terminal:

```powershell
# Terminal 1 — Rails server
$env:PATH = "C:\Ruby33-x64\bin;" + $env:PATH
ruby bin/rails server

# Terminal 2 — Vite
$env:PATH = "C:\Ruby33-x64\bin;" + $env:PATH
ruby bin/vite dev
```

> **Note:** Solid Queue (background jobs) does not run on Windows due to an unsupported `SIGQUIT` signal. The app works normally without it for local development.

See the [docs](https://buildermethods.com/rails-react-template) for everything else — what's inside, how to add pages, the design system, SSR, deployment, and more.

## Links

- 💬 Direct support: [Builder Methods Pro](https://buildermethods.com/pro)
- 📬 Free weekly newsletter: [Builder Briefing](https://buildermethods.com)

## License

Open source. Free to use, fork, and adapt.
