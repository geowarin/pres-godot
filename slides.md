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
  <a href="https://github.com/geowarin/pres-godot" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---

<Toc text-sm minDepth="1" maxDepth="2" />

---

# What Godot is

- A fully featured, free, open‑source 2D/3D game engine with an all‑in‑one lightweight editor.
- Broad platform support for development and deployment: Windows, macOS, Linux, Android, iOS, Web, XR (Quest/Horizon OS), and consoles (Switch, Xbox, PS5).
- Architecture: user‑facing “scenes and nodes” on top of high‑performance “servers” (data‑oriented systems for rendering, physics, etc.).
- Scripting: GDScript (tight integration), C# (high performance but historically less tightly integrated), and GDExtension bindings for many languages (C++, Rust, Go, Python, JavaScript).
- Notable tech: Jolt Physics integrated in 4.4; flexible modern rendering (forward+ hybrid, real‑time GI, scalable low‑end renderer); strong i18n including full RTL support.

---

# What is Godot?

Godot is a free and open‑source 2D and 3D game engine focused on developer ergonomics, a clean scene/node architecture,
and a permissive MIT license.

- Cross‑platform editor and export: Windows, macOS, Linux, Web, Mobile, Console (via partners)
- Languages: GDScript (Python‑like), C#, C++ via GDExtension, and more
- Batteries included: physics, animation, tilemaps, UI, audio, navigation, shaders, and more
- No royalties, no mandatory accounts, no online check‑ins

<div class="flex justify-center">
  <img src="https://godotengine.org/assets/showcase/until-then-2.webp" alt="Godot editor screenshot" class="h-48 w-96 object-cover rounded" />
</div>

---

# Godot unfair advantages

- Very light: 120Mb
    - Unreal: 35Gb
    - Unity: 10Gb + Launcher + mandatory account
- Free forever
- Open source
- Modular & well architected
- Intuitive scene system

---

# Free & Open Source

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
layout: iframe-right
url: https://docs.godotengine.org/en/stable/contributing/development/best_practices_for_engine_contributors.html
---

# Modular & Well Architected

- Addons extend the engine with new features (gdscript, C#)
- Engine is modular (can be compiled without 3D for example)
- [GDExtension](https://docs.godotengine.org/en/stable/tutorials/scripting/gdextension/what_is_gdextension.html) allows
  writing C/C++ modules without engine forks
    - Terrain support
    - Language
      bindings ([D](https://github.com/godot-dlang/godot-dlang), [Go](https://github.com/grow-graphics/gd), [Nim](https://github.com/godot-nim/gdext-nim), [Rust](https://github.com/godot-rust/gdext), [Swift](https://github.com/migueldeicaza/SwiftGodot), [Odin](https://github.com/dresswithpockets/odin-godot),
      etc.)
- Godot is written "in godot"

---

# The Scene Tree

<div class="float-right">
  <img src="https://docs.godotengine.org/en/stable/_images/nodes_and_scene_instances_player_scene_example.webp" class="h-72 rounded shadow" />
</div>

- Games are built from scenes composed of nodes arranged in a tree.
- Each node provides a focused responsibility (e.g., Sprite2D, Area3D, AnimationPlayer).
- Inheritance by composition: reuse via instancing scenes as children of others.
- Signals enable decoupled communication between nodes (event-driven).
- Editing workflow: drag-and-drop nodes, set properties, connect signals, and instance scenes.
- Benefits:
    - Modular, maintainable architecture
    - Easy reuse and composition
    - Clear separation of concerns

---
layout: image-right
image: /img/PRs.png
---

# Godot popularity — by the numbers

- 100,000+ GitHub stars milestone reached [[1]](https://godotengine.org/article/beyond-100000-you-re-breathtaking/)
- 2,800+ code contributors over the project’s lifetime [[2]](https://github.com/godotengine/godot/issues/100000)
- Approx. 600 new pull requests and 600 new issues per month (sustained
  pace) [[1]](https://godotengine.org/article/beyond-100000-you-re-breathtaking/)

<div class="mt-6 inline-flex flex-col gap-4 grow-0">
  <img src="https://img.shields.io/github/stars/godotengine/godot?style=social" alt="GitHub stars badge" class="h-8" />
  <img src="https://img.shields.io/github/contributors/godotengine/godot" alt="Contributors badge" class="h-8" />
  <img src="https://img.shields.io/github/issues-pr-closed/godotengine/godot?label=PRs%20closed" alt="Closed PRs badge" class="h-8" />
</div>

<!--
Notes:
- Stars indicate community traction; badges auto-update.
- The ~600 PRs/month figure shows sustained contributor activity.
-->

---

# Adoption and momentum

- Rapid growth over the last few years (e.g., strong increase in Steam releases; high community traction among indie and young developers).
- Now appearing in industry surveys; projected significant growth this decade.
- Revenue traction: rising number of Godot games exceeding $1M; cumulative revenues moving toward the nine‑figure range with strong year‑over‑year growth.
- Signals of industry trust: established studios migrating projects and catalogs to Godot.

References:

- Engine overview: https://godotengine.org
- Roadmap: https://godotengine.org/roadmap
- Showcase: https://godotengine.org/showcase

---
layout: image
image: /growth.png
---

---

# Unity debacle

- Unity's controversial pricing changes in 2023
- Godot's accessibility and zero-cost model
- Growing community of developers migrating from Unity
- Comparable feature set for most game development needs
- No "runtime fee" or revenue sharing

---

# Godot adoption: Game jams

<div class="mt-6 flex gap-4">
  <img src="/gmtk/2025.png" class="w-50%" />
</div>

---

# Godot adoption: Influencers

- Brackeys
- Passivestar
- Acerola

---

# Godot adoption: Commercial successes

- "Brotato" - top-selling roguelike
- "Cassette Beasts" - monster-collecting RPG
- "Cruelty Squad" - cult hit FPS

https://godotengine.org/article/godot-showcase-dogwalk/

---

# Why developers prefer Godot

- Usability and rapid iteration: integrated debugger, hot‑editing via remote scene tree, very fast run/test cycles.
- Freedom and ownership: open license, no vendor lock‑in, modify the engine as needed; ability to upstream changes to reduce long‑term maintenance.
- Cost control: no licensing fees; pay only for optional services (support, ports, tooling) from multiple competing providers.

Resources:

- Getting started: https://docs.godotengine.org/en/stable/getting_started/index.html
- Tutorials: https://docs.godotengine.org/en/stable/tutorials/index.html
- Asset Library: https://godotengine.org/asset-library

---

# The Godot Foundation

- Independent non‑profit stewarding the Godot Engine and its ecosystem
- Facilitates governance and roadmap; maintains infrastructure and releases
- Manages the Godot Development Fund and sponsorships to finance core development
- Supports maintainers, grants/bounties, community initiatives, and events
- Handles trademarks and legal matters; promotes openness and transparency

Links:

- About/Governance: https://godotengine.org/about
- Development Fund: https://fund.godotengine.org

--- 

# The 4.0 revolution

https://godotengine.org/article/godot-4-0-sets-sail/

https://godotengine.org/article/godot-4-1-is-here/

https://godotengine.org/article/godot-4-2-arrives-in-style/

https://godotengine.org/releases/4.3/

https://godotengine.org/releases/4.4/

---

# Jolt Physics

- Modern, multi‑core rigid‑body physics engine (MIT‑licensed)
- Proven in AAA titles such as Horizon Forbidden West and others
- Benefits for devs: high performance, robust constraints, CCD, stable character controllers
- In Godot: built-in since 4.4, previously as a plugin

Refs: Horizon Forbidden West and Jolt
overview [[1]](https://www.guerrilla-games.com/read/architecting-jolt-physics-for-horizon-forbidden-west),
Projects using Jolt [[2]](https://jrouwe.github.io/JoltPhysics/md__docs_2_projects_using_jolt.html)

<div class="mt-6 flex items-center justify-center">
  <img src="https://upload.wikimedia.org/wikipedia/en/6/69/Horizon_Forbidden_West_cover_art.jpg" alt="Horizon Forbidden West cover art" class="h-72 rounded shadow" />
</div>

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

# GDScript at a glance

- Purpose‑built, Python‑like language designed for Godot’s node/scene model
- Optional static typing for better tooling and performance
- Tight engine integration: signals, coroutines (await), resources, editor hints
- Fast iteration: hot‑reload, live inspector, autocompletion
- When to pick others: C# for ecosystem/libraries; GDExtension (C/C++) for hotspots

Quick taste:

```gdscript example.gd
extends Node

var speed: float = 200.0

func _process(delta: float) -> void:
    position.x += speed * delta
```

Learn more:

- GDScript basics: https://docs.godotengine.org/en/stable/tutorials/scripting/gdscript/index.html
- Static typing: https://docs.godotengine.org/en/stable/tutorials/scripting/gdscript/static_typing.html
- Signals: https://docs.godotengine.org/en/stable/tutorials/scripting/signals.html
- Coroutines (await): https://docs.godotengine.org/en/stable/tutorials/scripting/coroutines.html

---

# Demo: Creating a bouncing ball 

![ball scene](/demo/ball_scene.png)

- Root is a [RigidBody3D](https://docs.godotengine.org/en/stable/classes/class_rigidbody3d.html)
  - Contains a [MeshInstance3D](https://docs.godotengine.org/en/stable/classes/class_meshinstance3d.html)
  - Contains a [CollisionShape3D](https://docs.godotengine.org/en/stable/classes/class_collisionshape3d.html)

- Make it a scene
- Add a lot of balls!

---

# Demo: customize the ball color

```gdscript
extends RigidBody3D

@export var color: Color = Color(1, 0, 0)

func _ready() -> void:
    var material = StandardMaterial3D.new()
    material.albedo_color = color
    $Mesh.material_override = material

```

---

# Demo: edit color in the editor

- add `@tool` to the script
- create a setter

```gdscript
@tool
extends RigidBody3D

@export var color: Color = Color(1, 0, 0):
	set(value):
		color = value
		var material = StandardMaterial3D.new()
		material.albedo_color = color
		$Mesh.material_override = material
```

---

# Demo: add a button to create balls

```gdscript
@tool
extends Node3D

@export_tool_button("Add Ball", "Add") var add_ball_button = add_ball

func add_ball():
	var ball_scene = load("res://ball.tscn")
	var ball_instance = ball_scene.instantiate()
	ball_instance.color = Color.from_ok_hsl(randf(), 1, 0.5)
	ball_instance.position = Vector3(randf_range(-4, 4), randf_range(1, 5), randf_range(-4, 4))
	add_child(ball_instance, true)
	ball_instance.owner = get_tree().edited_scene_root
```

---

# Demo: Inspect the godot editor with godot!

<kbd>Debug</kbd> > <kbd>Customize run instances</kbd>

Main run args:
```
--path ../demo --editor
```

![Editor debugging editor](/demo/editor_debug.png)

---

# Future

- 4.5 release
  - shader baker
  - SDL 3 gamepad support
  - 

--- 

# Roadmap

https://godotengine.org/priorities/

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
