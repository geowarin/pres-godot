---
# You can also start simply with 'default'
theme: seriph
background: https://cover.sli.dev
# some information about your slides (markdown enabled)
title: Godot — the friendly open‑source game engine
info: |
  A practical overview of Godot for newcomers and hobbyist developers:
  - What is Godot?
  - Why it’s becoming so popular
  - Why it’s great for hobbyists
  - Advantages of an open‑source engine
  References included.
# apply unocss classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
---

# Godot

Presentation slides for developers

<div @click="$slidev.nav.next" class="mt-12 py-1" hover:bg="white op-10">
  Press Space for next page <carbon:arrow-right />
</div>

<div class="abs-br m-6 text-xl">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="slidev-icon-btn">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---

<Toc text-sm minDepth="1" maxDepth="2" />

---

# Code

Use code snippets and get the highlighting directly, and even types hover!

```gdscript [example.gd] {all|1|2}
extends Node
class_name Example

func _ready() -> void:
    pass
```

<!--
Notes can also sync with clicks

[click] This will be highlighted after the first click

[click] Highlighted with `count = ref(0)`

[click:3] Last click (skip two clicks)
-->

---

# What is Godot?

Godot is a free and open‑source 2D and 3D game engine focused on developer ergonomics, a clean scene/node architecture, and a permissive MIT license.

- Cross‑platform editor and export: Windows, macOS, Linux, Web, Mobile, Console (via partners)
- Languages: GDScript (Python‑like), C#, C++ via GDExtension, and visual scripting
- Batteries included: physics, animation, tilemaps, UI, audio, navigation, shaders, and more
- No royalties, no mandatory accounts, no online check‑ins

<div class="mt-6 flex items-center justify-center gap-6">
  <img src="https://godotengine.org/assets/press/icon_color.png" alt="Godot logo" class="h-28" />
  <img src="https://godotengine.org/assets/press/screenshot1.webp" alt="Godot editor screenshot" class="h-28 rounded shadow" />
</div>

<v-click>

Docs: https://docs.godotengine.org

</v-click>

<!--
Notes:
- Emphasize “scene as a tree of nodes” mental model.
- Mention clean project structure and lightweight installs.
-->

---

# Why is Godot becoming so popular?

- Open‑source momentum: transparent roadmap, community trust, rapid iteration
- Great 2D performance + improving 3D with Vulkan renderer (Godot 4.x)
- Friendly scripting (GDScript) and quick iteration times
- Strong ergonomics: scene instancing, signals, built‑in tools
- Vibrant ecosystem: Asset Library, plugins, exporters, templates
- Predictable licensing (MIT): zero royalties, clear redistribution rights

<v-clicks>

- Industry interest and ports via partners for consoles
- Increasing showcase and commercial releases as social proof

</v-clicks>

References:
- Engine overview: https://godotengine.org
- Roadmap: https://godotengine.org/roadmap
- Showcase: https://godotengine.org/showcase

---

# Why is Godot a good choice for hobbyists?

- Low friction: small download, fast startup, easy project setup
- Gentle learning curve with great docs and tutorials
- Productive loop: save → run → tweak → repeat
- Flexible scale: from game jams to complete indie titles
- No lock‑in or paywalls; keep your projects forever
- Cross‑platform exports without extra fees

Resources:
- Getting started: https://docs.godotengine.org/en/stable/getting_started/index.html
- Tutorials: https://docs.godotengine.org/en/stable/tutorials/index.html
- Asset Library: https://godotengine.org/asset-library

---

# Advantages of an open‑source engine

- Transparency: inspect source, understand internals, learn from it
- Control: fix bugs, fork, or extend without waiting
- Community: contributions, add‑ons, and peer support
- Longevity: projects aren’t tied to a vendor’s business model
- Licensing clarity: permissive MIT license, no royalties

Learn more:
- License: https://godotengine.org/license
- Source code: https://github.com/godotengine/godot
- Contributing: https://docs.godotengine.org/en/stable/contributing/index.html

---

# Where Godot shines

- 2D games: platformers, tactics, puzzle, roguelikes, narrative
- Tools and editors: custom in‑editor tools with EditorPlugins
- Rapid prototypes and game jams
- Educational projects and teaching fundamentals

Also capable:
- Modern 3D with Vulkan, GI, NavigationServer, AnimationTree
- Scripting choices: GDScript for speed, C# for ecosystem, GDExtension for native

Docs:
- 2D intro: https://docs.godotengine.org/en/stable/tutorials/2d
- 3D intro: https://docs.godotengine.org/en/stable/tutorials/3d

---

# Ecosystem at a glance

- Asset Library: free assets, shaders, tools
- Export templates: desktop, mobile, web; consoles via partners
- GDExtension: write high‑performance C++ modules without engine forks
- Community hubs: Q&A, forums, Discords, and regional groups

Links:
- Asset Library: https://godotengine.org/asset-library
- GDExtension: https://docs.godotengine.org/en/stable/tutorials/scripting/gdextension/index.html
- Q&A: https://godotengine.org/qa

---

# References and further reading

- Website: https://godotengine.org
- Documentation: https://docs.godotengine.org
- Roadmap: https://godotengine.org/roadmap
- Showcase: https://godotengine.org/showcase
- Source: https://github.com/godotengine/godot
- License (MIT): https://godotengine.org/license
- Asset Library: https://godotengine.org/asset-library
- Learn (Tutorials): https://docs.godotengine.org/en/stable/getting_started/step_by_step/index.html

<PoweredBySlidev mt-10 />
