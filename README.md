# Terminal Code Editor (Rust)

Editor de código en terminal para Windows, escrito en **Rust**, inspirado en el paradigma modal de **NeoVim**, pero diseñado desde cero con un enfoque **minimalista, modular y seguro**.

Este proyecto busca construir un **motor de edición de texto robusto**, priorizando rendimiento, claridad arquitectónica y extensibilidad futura.

---

## 🎯 Objetivo del proyecto

Desarrollar un editor de código en terminal que:

- Funcione correctamente en **Windows**
- Sea **rápido y liviano**
- Use un **modelo de edición eficiente**
- Separe claramente **core, UI e input**
- Sirva como base para extensiones futuras (plugins, LSP, scripting)

No pretende reemplazar NeoVim, sino explorar un diseño moderno de editores TUI utilizando Rust.

---

## 🧱 Principios de diseño

- Separación estricta de responsabilidades
- Core agnóstico de la interfaz de usuario
- Entrada de teclado desacoplada
- Seguridad de memoria por diseño
- Escalabilidad progresiva

---

## 🛠️ Stack tecnológico

- **Rust (stable)**
- **crossterm** — Control del terminal y eventos de teclado
- **ratatui** — Interfaz TUI (layout y renderizado)
- **ropey** — Manejo eficiente de texto mediante Rope

---

## 🚀 Estado actual

- ☑️ Inicialización del proyecto
- ☑️ Terminal en modo raw
- ☑️ Captura de eventos de teclado
- ⏹️ Estructura modular base
- ⏹️ Inserción de texto en buffer
- ⏹️ Renderizado del contenido
- ⏹️ Cursor visual
- ⏹️ Modo Insert / Normal
- ⏹️ Abrir y guardar archivos
- ⏹️ Barra de estado (status bar)

---

## ✅ Funcionalidades planificadas

* Edición básica de texto (insertar / borrar)
* Soporte de archivos (open / save)
* Modos estilo Vim (Normal / Insert / Command)
* Barra de estado (archivo, modo, posición del cursor)
* Keybindings configurables
* Syntax highlighting
* Undo / Redo
* Múltiples buffers y splits (futuro)
* Integración LSP (futuro)

---

## ▶️ Ejecución Requisitos

Rust (stable)

Windows Terminal o PowerShell

Compilar

``` bash
cargo build
```

Ejecutar
``` bash
cargo run
```
Presiona **q** para salir.

---

## 🗺️ Roadmap

Fase 1 — MVP
* Edición básica de texto
* Guardado de archivos
* Cursor funcional
* Barra de estado

Fase 2 — Edición modal
* Modo Insert / Normal
* Comandos básicos (:w, :q)
* Undo / Redo

Fase 3 — Productividad
* Syntax highlighting
* Configuración por archivo
* Keybindings personalizados

Fase 4 — Avanzado
* Sistema de plugins (Lua o WASM)
* Integración LSP
* Múltiples buffers y split

---

## 🧪 Enfoque de aprendizaje

Este proyecto prioriza:

* Diseño de software
* Arquitectura de sistemas
* Construcción de tooling
* Buenas prácticas en Rust
Es un proyecto formativo y experimental, orientado a crecimiento técnico.

---

## 📌 Convenciones del proyecto Commits

Se recomienda usar mensajes estilo Conventional Commits:
* ```feat:``` nuevas funcionalidades
* ```fix:``` correcciones
* ```refactor:``` refactor sin cambios de comportamiento
* ```chore:``` tareas de mantenimiento
* ```docs:``` documentación

``` bash
cargo fmt
cargo clippy
```

🤝 Contribuciones

Las contribuciones son bienvenidas una vez definido el MVP.
* Haz un fork del repositorio
* Crea una rama:
``` bash
git checkout -b feat/mi-cambio
```
* Realiza cambios y valida
``` bash
cargo fmt
cargo clippy
cargo test
```
* Haz cambios y publica
``` bash
git commit -m "feat: descripcion del cambio"
git push origin feat/mi-cambio
```
* Abre un Pull Request con una descripción clara del cambio.
Antes de proponer cambios mayores, abre un Issue para discutir el enfoque.

---

## 🔐 Seguridad

* El editor corre localmente en terminal.
* En fases futuras (plugins / scripting) se priorizará un enfoque secure-by-design, evitando ejecución arbitraria sin permisos o configuración explícita.

---

## 🧾 Licencia

Este proyecto se distribuye bajo la licencia MIT.
Consulta el archivo LICENSE para más detalles.
