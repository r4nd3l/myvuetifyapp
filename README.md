# MyVuetifyApp

A Vue 3 + TypeScript + TailwindCSS + Vuetify project, containerized with Docker.
Supports **live-reload development** and **production build with Nginx**.

---

## 🚀 Tech Stack

- [Vue 3](https://vuejs.org/) + [Vite](https://vitejs.dev/) (with hot reload)
- [TypeScript](https://www.typescriptlang.org/)
- [TailwindCSS](https://tailwindcss.com/)
- [Vuetify](https://vuetifyjs.com/)
- [Docker](https://www.docker.com/) for containerization
- [Nginx](https://www.nginx.com/) for production serving

---

## 📦 Setup

### 1. Clone repository

```bash
git clone https://github.com/r4nd3l/myvuetifyapp.git
cd myvuetifyapp
```

### 2. Development (with hot reload)

Run inside Docker with **Vite dev server**:

```bash
docker compose up --build app-dev
```

Then open [http://localhost:5173](http://localhost:5173).

> 💡 Changes to your code are reflected immediately thanks to hot reload.
> If you are on Windows or WSL2 and hot reload doesn’t trigger, enable polling:
> add in `docker-compose.yml` → `environment: - CHOKIDAR_USEPOLLING=true`.

---

### 3. Production (optimized build + Nginx)

Build and run the production container:

```bash
docker build -t myvuetifyapp-prod -f Dockerfile .
docker run -p 8080:80 myvuetifyapp-prod
```

Now open [http://localhost:8080](http://localhost:8080).

---

### 4. Useful Commands

- Install dependencies locally:

  ```bash
  npm install
  ```

- Run locally without Docker:

  ```bash
  npm run dev
  ```

- Build for production:

  ```bash
  npm run build
  ```

- Preview production build locally:

  ```bash
  npm run preview
  ```

---

## ⚡ Project Structure

```
myvuetifyapp/
├─ src/               # Vue components, pages
├─ public/            # Static assets
├─ Dockerfile         # Multi-stage build (prod)
├─ Dockerfile.dev     # Dev build (hot reload)
├─ docker-compose.yml # Compose config
├─ tailwind.config.js # Tailwind setup
├─ vite.config.ts     # Vite configuration
└─ package.json
```

---

## 🔑 Notes

- Dev mode runs on port **5173** (Vite).
- Prod mode runs on port **8080** (Nginx).
- Always rebuild after editing `Dockerfile` or dependencies:

  ```bash
  docker compose build --no-cache
  ```
