# 🧭 TaskPilot API

API REST moderna para gestionar tareas, proyectos y equipos.
Construida con **Node.js**, **Express**, **TypeScript** y **TypeORM**.

---

## 🚀 Características

- ✅ CRUD completo para tareas, usuarios y proyectos.
- 🔐 Autenticación JWT y roles (admin, user).
- 📦 Paginación, filtros y búsqueda avanzada.
- 🧩 Arquitectura limpia (controller → service → repository).
- 🧪 Pruebas unitarias con Jest.
- 📘 Documentación Swagger integrada.

---

## 🧠 Stack tecnológico

| Capa | Tecnología |
|------|-------------|
| Servidor | Node.js + Express |
| Lenguaje | TypeScript |
| ORM | TypeORM |
| Base de datos | PostgreSQL |
| Validación | class-validator |
| Auth | JWT + bcrypt |
| Tests | Jest + Supertest |

---

## ⚙️ Instalación y configuración

```bash
git clone https://github.com/tuusuario/taskpilot-api.git
cd taskpilot-api
npm install

Crea el archivo `.env` con las variables necesarias:

```
PORT=4000
DATABASE_URL=postgres://user:pass@localhost:5432/taskpilot
JWT_SECRET=supersecreto

```

Ejecuta migraciones y corre el servidor:

```bash
npm run migration:run
npm run dev

```

---

## 🧩 Endpoints principales

| Método | Ruta | Descripción |
| --- | --- | --- |
| `POST` | `/api/auth/register` | Registro de usuario |
| `POST` | `/api/auth/login` | Inicio de sesión |
| `GET` | `/api/tasks` | Listar tareas |
| `POST` | `/api/tasks` | Crear tarea |
| `PATCH` | `/api/tasks/:id` | Actualizar tarea |
| `DELETE` | `/api/tasks/:id` | Eliminar tarea |

---

## 🧱 Estructura del proyecto

```
src/
├── controllers/
├── services/
├── repositories/
├── entities/
├── middlewares/
├── routes/
└── index.ts

```

---

## 🧪 Pruebas

Ejecuta las pruebas unitarias y de integración:

```bash
npm run test

```

Ejemplo:

```tsx
describe("TaskController", () => {
  it("crea una tarea correctamente", async () => {
    const res = await request(app)
      .post("/api/tasks")
      .send({ title: "Nueva tarea" })
    expect(res.status).toBe(201)
  })
})

```

---

## 🧭 Roadmap

- [x]  CRUD básico
- [x]  JWT y roles
- [ ]  WebSockets para actualizaciones en tiempo real
- [ ]  Integración con Notion / Slack

---

## 🧾 Licencia

Licencia MIT — libre para usar, aprender y mejorar.

> “Gestionar tareas debería ser tan simple como cumplirlas.”
> 

```

---

## 🎮 2️⃣ README — **StarJump!** (videojuego retro tipo arcade)

```markdown
# 🌠 StarJump!

Un videojuego arcade retro donde saltas entre estrellas evitando agujeros negros.
Hecho con **Phaser.js**, **TypeScript** y mucho ☕.

---

## 🕹️ Gameplay

¡Eres una pequeña nave estelar que debe saltar entre plataformas cósmicas!
Cada salto correcto suma puntos. Si caes... el universo te devora 👀

---

## 🚀 Características

- ⭐ Movimiento con física realista.
- 🌌 Power-ups y niveles infinitos.
- 🎵 Música chiptune original.
- 📱 Soporte móvil (touch controls).
- 🏆 Tabla global de puntajes.

---

## 💻 Stack técnico

| Elemento | Tecnología |
|-----------|-------------|
| Motor de juego | Phaser.js |
| Lenguaje | TypeScript |
| Build | Vite |
| Assets | Aseprite + Bfxr |
| Backend (ranking) | Express + SQLite |
| Despliegue | GitHub Pages / Vercel |

---

## ⚙️ Instalación

```bash
git clone https://github.com/tuusuario/starjump.git
cd starjump
npm install
npm run dev

```

Abre tu navegador en 👉 [http://localhost:5173](http://localhost:5173/)

---

## 📂 Estructura

```
starjump/
├── src/
│   ├── scenes/
│   │   ├── GameScene.ts
│   │   ├── MenuScene.ts
│   │   └── GameOverScene.ts
│   ├── assets/
│   ├── utils/
│   └── main.ts
└── public/

```

---

## ✨ Controles

| Acción | Tecla / Input |
| --- | --- |
| Saltar | Espacio / Tap |
| Pausa | Esc |
| Reiniciar | R |

---

## 🧩 Ejemplo de escena

```tsx
// src/scenes/GameScene.ts
import Phaser from "phaser"

export class GameScene extends Phaser.Scene {
  private player!: Phaser.Physics.Arcade.Sprite

  create() {
    this.player = this.physics.add.sprite(100, 300, "ship")
    this.player.setCollideWorldBounds(true)
  }

  update() {
    if (this.input.keyboard?.addKey("SPACE").isDown) {
      this.player.setVelocityY(-300)
    }
  }
}

```

---

## 🏆 Próximas mejoras

- [x]  Ranking global (backend express)
- [ ]  Personalización de naves
- [ ]  Sistema de logros
- [ ]  Multiplayer cooperativo

---

## 🎨 Créditos

- Código y arte: **@tuusuario**
- Música chiptune: **@RetroVibes**
- Sonidos: **Bfxr**
- Inspirado en clásicos como *Doodle Jump* y *Celeste*

---

## 📜 Licencia

MIT — Puedes jugar, modificar y compartir libremente.

> “No saltes para escapar del vacío, salta para alcanzar la luz.”
>
