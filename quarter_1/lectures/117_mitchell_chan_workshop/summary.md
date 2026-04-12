# Craft Workshop: Making a Video Game in Unity

**Speaker:** Mitchell F. Chan — conceptual artist  
**Host:** Haiver — Artist Commons director  
**Context:** Third Artist Commons session with Mitchell Chan, following his body-of-work presentation (114) and students' close-looking with his games. A live demonstration of his full workflow — Blender → Unity → custom shaders → game logic — building a pinball game from scratch in real time. The session is explicitly framed not as a Unity tutorial but as **demystification**: showing that digital tools are less scary than they appear, and that making distinctive-looking digital art is achievable through deliberate aesthetic decisions.

---

## Overview

Mitchell builds a working (and eventually chaotic) pinball game live, narrating every step — why he chose these tools, how he approaches aesthetics before mechanics, how he codes interactivity, and what it means for a video game to be generative art. The philosophical throughline is the same as his broader practice: **take care of the low-hanging fruit first, develop a distinctive style, and understand your medium well enough to interrogate it**. The game gradually escapes his control — balls multiply, physics go haywire — and the workshop ends in deliberate mayhem that feels more like a Rafiq Bhatia particle simulation than a game.

---

## 1. Demystification as Method

The session opens with a single declared goal: **not to make you good at Unity, but to make you unafraid of it**.

Mitchell traces this back to his own learning at Interaccess (Toronto): short workshops that didn't produce mastery, just removed the fear. Once something is no longer scary, you can start learning it properly.

**His learning stack:**
- **Blender:** YouTube tutorials — specifically Blender Guru's donut series, worked through on family vacation, one hour per day
- **Unity:** The official Unity Learn site — sequential, cumulative, lesson-by-lesson. He prefers structured curriculum over a patchwork of YouTube videos because in digital art there are too many contradictory techniques for any one goal

**On tool selection:** He deliberately chose tools that are professionally supported and widely used — not out of corporate loyalty but because "I hate jank." When a tool is janky, diagnosing problems becomes impossible. Reliability is a prerequisite for focus.

---

## 2. Tool Philosophy: Why Unity (and Not Unreal)

Mitchell chose Unity for a specific, pragmatic reason: **Unity exports to WebGL**, which means games can run in a browser, which means they can be NFTs. For Digital Zones (his blockchain conceptual art series), setting a game as its own standalone website and pointing the NFT metadata's animation URI to it was the entire distribution model.

The aesthetic argument is more pointed:
> "I find that Unreal Engine projects all kind of look the same, and it kind of annoys me."

He names Jeremy Couillard and Gabriel Masson as artists he respects whose work converges visually because both use Unreal without enough deviation from defaults. His principle: **if you're going to fight an uphill battle to present a game engine as an artistic medium, handle the low-hanging fruit first — make it look like art, not like a tech demo**.

---

## 3. Blender 3D Modeling Workflow

The session begins in Blender, building the physical elements of a pinball machine:
- Rectangular boundary walls (scaled cubes)
- A flipper paddle (cylinder stretched in edit mode)
- Pop bumpers (cylinders)

Key discipline: **naming every object clearly** before importing into Unity. When you have a complex scene with dozens of game objects, unintuitive names become a debugging problem.

Mitchell acknowledges he's not expert-level in Blender and moves quickly — the point is seeing the pipeline, not mastering 3D modeling. Blender's file format imports directly into Unity, preserving the object hierarchy.

---

## 4. The MFC Grail Shade: Developing a Distinctive Visual Identity

Before adding any game logic, Mitchell applies his custom shader library — the **"MFC Grail Shade"** — which he calls his "Nike Air Max technology" with self-deprecating sincerity.

**The problem it solves:** Out-of-the-box Unity visuals look like Unity. He spent years developing a personal shader library that produces **stippling, hatching, and cross-hatching effects**, giving his games a consistent hand-drawn quality.

**How it was built:**
- He first exhausted every built-in Shader Graph node to understand what Unity could already do
- Then wrote custom HLSL code for the one thing it couldn't: **isolating scene lighting into separate channels** — just shadow, just colored light — so he could apply stylized rendering on top
- The shader graph is a node-based visual coding interface (similar to Blender's material editor, or Grasshopper in Rhino)
- He's "not very good at HLSL" by his own account; the code is cobbled and poorly maintained. But it does the one thing he needs

**The aesthetic framework:** When designing shaders, he thinks like a painter — analyzing how light and shadow describe form. When reducing to final aesthetics, he thinks like a cartoonist — editing ruthlessly:

> "A really good cartoonist — cartooning is just a process of editing. I have six lines and four colors. What is the information that I need to convey?"

**An important admission:** Having limited technical skill creates useful constraints. With infinite possibilities, you waste time on wrong directions. With constrained skill, you're forced to commit:

> "If I had more skill in this, I'd probably waste a lot of time. Given that I'm not that good at this, I've got to choose very specifically what direction I'm pointing, then go there."

---

## 5. Unity's Object-Component System

The session's most transferable concept for non-Unity artists is the **game object + components** model:

- **Everything** in Unity is a game object
- Game objects have **components** attached to them — scripts, physics properties, rendering data
- Components communicate with each other through the game object's shared namespace

The basic component stack for any physical object:
- **Transform** — position in space
- **Mesh Filter** — 3D geometry data
- **Mesh Renderer** — tells the graphics engine to draw it
- **Collider** (Box, Sphere, etc.) — tells the physics engine this object has boundaries
- **Rigid Body** — gives the object mass, gravity, and collision response

Mitchell demonstrates by adding a Rigid Body to a sphere, pressing play, and watching it fall — then removing the collider from the ground and watching the ball fall through it. The component model makes this legible: **every behavior is a module you add or remove**.

---

## 6. Writing Game Logic in C#

Unity scripting is in **C#**, which Mitchell found immediately accessible coming from Processing:

> "If you know Processing, do not be afraid of any programming language. It's 95% the same."

The structure maps directly:
- `Setup()` in Processing → `Start()` in C#
- `Draw()` → `Update()`
- Variables marked `[SerializedField]` appear as editable sliders in the Unity GUI — no recompile needed to tweak values

**The flipper script:** Uses a Hinge Joint component (a physics constraint that allows rotation around a single axis) with a motor. When the spacebar input is detected, the motor applies torque in the opposite direction.

**On live debugging:** When the flipper doesn't work, he writes a debug message: "Tell me this if it's doing this." Checking one assumption at a time — not rewriting everything. The approach is identical whether in Processing or Unity.

**On autocomplete and "vibe coding":** He uses AI-assisted coding occasionally but dislikes autocomplete in the flow of writing game logic:

> "I hate this autocomplete stuff... It really takes me out of my flow."

For games with hundreds of interacting scripts, he needs to know where everything is. Autocomplete guesses wrong about intent in complex systems.

---

## 7. The Pop Bumper Script and Emergent Chaos

The pop bumper script applies a force in the direction **opposite to the collision** — when a ball hits, it bounces away. A second modification: each collision spawns a new ball at a random position.

The result: the game rapidly exceeds Mitchell's intention. Balls multiply exponentially. Physics becomes chaotic. The scene eventually looks like a particle simulation — evocative of Rafiq Bhatia's generative work, which was the half-formed inspiration behind the tutorial concept.

The lesson he draws:

> "Every video game is a collection of generative art scripts all interacting with each other."

This is how he conceptualizes his own practice — not as designing finished images, but as designing rules whose interactions produce emergent behavior.

---

## 8. Cinematography and Viewer Placement

The Q&A opens into a discussion of camera work — the other half of game art direction.

Mitchell's approach: **halfway between artist and filmmaker**. He studies cinematography specifically for how to situate viewers in space. He cites Paul Thomas Anderson and Steven Spielberg (the West Side Story remake) as influences for camera placement and movement.

In his game *Boys of Summer*, cameras follow spline tracks — curved paths through the scene — with the specific track assigned by the NFT token's random hash. The viewer's spatial position is part of the generative logic.

The question of where to place the camera is, for Mitchell, a compositional question identical to canvas composition — what is in frame, what is out, what the viewer is oriented toward. Relinquishing that control (as in an open-world game) is why he considers most "artist-made game art" to fail:

> "You've just created a bunch of conditions that the viewer can fuck up."

---

## 9. Sound Systems (Brief Demo)

Sound in Unity follows the same component model:
- Each game object has a sound file reference and a script that says when to play it
- For his game *Boys of Summer*, all sounds were synchronized to a beat grid, triggered by in-game events

He had built an elaborate system for synchronizing ambient sound — more complex than needed in retrospect. The lesson: custom systems become hard to maintain. Unity's existing audio libraries (and third-party packages) handle most sound needs without custom code.

---

## 10. Archive and Longevity

A practical note on digital art preservation: Mitchell's games are archived through Rhizome. This requires preserving specific Unity editor versions alongside the project files, since new Unity builds can introduce incompatibilities. He flags this as not actually scary — editor version management is straightforward — but worth planning from the beginning of a project.

---

## Key Takeaways

- **Demystification is the first and most important step.** You don't need to become expert; you need to stop being afraid. Fear is the real barrier to entry in digital tools
- **Develop a distinctive visual identity before worrying about mechanics.** If the work looks generic, you've made the uphill battle harder. Handle aesthetic low-hanging fruit first
- **Limited technical skill can be an asset.** Constraints force commitment to specific directions. Infinite technical possibility often leads to wasted exploration
- **Think like a painter, edit like a cartoonist.** For Mitchell: analyze light and shadow as a painter would; then distill to the minimum information a cartoonist would use
- **Every game is a collection of generative art scripts.** The interesting thing isn't the finished image — it's the rules whose interactions produce emergent behavior
- **User agency is the medium, not the tool.** The question of what the player can and cannot affect is the artwork. Everything else is scaffolding
- **Camera work is compositional work.** Viewer placement in space is as deliberate as placing elements on a canvas
- **Use the presets.** Start with built-in components before writing custom logic. Learn what already exists before building from scratch

---

## Reflection Questions

1. **Demystification:** What tool or medium in your practice still feels frightening? What would the equivalent of a 90-minute demystification session look like — not to become expert, but to stop being afraid?

2. **Distinctive aesthetics:** If you work in a digital medium (game engine, 3D software, generative code), what makes your work visually distinct from the tool's defaults? What is your equivalent of the MFC Grail Shade?

3. **Constraints as advantage:** Where in your practice do limited technical skills force useful specificity? What do you make because you *can't* do the fancier thing?

4. **Generative framing:** If your work involves multiple interacting rules or systems — even offline — what happens when those rules interact in unexpected ways? Is that emergent behavior part of the work, or do you fight it?

5. **The component model:** In your practice (whatever medium), what are the "components" — discrete, modular behaviors — that you attach to elements of a work? What would it mean to be more explicit about designing those modules separately?

---

*Summary based on the Artist Commons craft workshop transcript (117_mitchell_chan_workshop/transcript.txt), third session with Mitchell F. Chan.*
