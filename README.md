# ⚙️ WackyFlip-Engine

**Core Game Engine & Physics Logic powering all Wacky Flip games**

`WackyFlip-Engine` is the heart of the Wacky Flip universe, providing the **physics simulation**, **gameplay loop**, and **core systems** that bring all flips, jumps, crashes, and ragdoll antics to life. This engine powers both web and mobile versions of [wackyflip.com](https://wackyflip.com) games.

---

## 🎯 Features

* 🌀 **Physics Engine** – Realistic ragdoll dynamics, momentum, gravity flips, and collision handling
* 🎮 **Game Loop System** – Frame-based updates optimized for 2D/3D gameplay
* 🎨 **Rendering Pipeline** – Abstraction for WebGL / Canvas / Unity-style rendering backends
* 🏗 **Entity Component System (ECS)** – Modular architecture for characters, props, and obstacles
* ⚡ **Cross-Platform** – Runs consistently on desktop browsers, mobile devices, and embedded game clients
* 🔧 **Extensible Modules** – Input handling, animation blending, AI behaviors, and camera control
* 🎯 **Deterministic Mode** – Replay-safe logic for tournaments, replays, and leaderboards

---

## 🛠 Tech Stack

* **Language:** TypeScript / C# (depending on platform target)
* **Physics:** Custom 2D/3D physics (inspired by Box2D, Bullet Physics)
* **Rendering:** WebGL / Three.js for browser builds, Unity/C# for mobile ports
* **Integration:** Connects with `WackyFlip-Assets`, `WackyFlip-Audio`, and `WackyFlip-Stats`

---

## 📁 Repository Structure

```
WackyFlip-Engine/
├── core/
│   ├── gameLoop.ts
│   ├── entitySystem.ts
│   ├── inputManager.ts
│   └── time.ts
├── physics/
│   ├── rigidBody.ts
│   ├── collisions.ts
│   ├── joints.ts
│   └── gravity.ts
├── rendering/
│   ├── renderer.ts
│   ├── shaders/
│   └── camera.ts
├── examples/
│   ├── bottleFlipDemo.ts
│   ├── ragdollDemo.ts
│   └── obstacleCourse.ts
└── README.md
```

---

## 🚀 Getting Started

1. Clone the repository:

```bash
git clone https://github.com/wackyflipgame/WackyFlip-Engine.git
cd WackyFlip-Engine
npm install
```

2. Run a demo scene:

```bash
npm run demo:bottleflip
```

3. Example usage (spawn an entity with physics):

```ts
import { Engine, RigidBody, Gravity } from 'wackyflip-engine';

const engine = new Engine();
const player = engine.entities.create('player');

player.addComponent(new RigidBody({ mass: 5 }));
player.addComponent(new Gravity());

engine.start();
```

---

## 📬 Contribution Guidelines

* Keep **physics deterministic** for consistent replays
* Write **unit tests** for all core math and physics functions
* Optimize for **low-latency mobile performance**
* Use **ECS patterns** for new gameplay features

---

## 🔗 Related Repositories

* [`WackyFlip-Assets`](https://github.com/wackyflipgame/WackyFlip-Assets) – Characters, animations, and environments
* [`WackyFlip-Audio`](https://github.com/wackyflipgame/WackyFlip-Audio) – Sound effects and music integration
* [`WackyFlip-Replays`](https://github.com/wackyflipgame/WackyFlip-Replays) – Replay-safe recording of engine states
* [`WackyFlip-Stats`](https://github.com/wackyflipgame/WackyFlip-Stats) – Player stats and leaderboard tracking

---

## 📜 License

MIT © 2025 Wacky Flip Studios
