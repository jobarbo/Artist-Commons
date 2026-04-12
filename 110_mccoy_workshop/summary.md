# Crystal Images: Process Workshop with Jen and Kevin McCoy

**Speakers:** Kevin McCoy, Jenn McCoy  
**Host:** Haiver  
**Context:** Second Artist Commons session with the McCoys—a craft/process workshop following their first-session presentation of their body of work. The workshop makes space for the "messy side of creativity," material process, and conceptual thinking.

---

## Overview

This workshop walks through the McCoys' current project **Crystal Images**—work that is still in progress—from conceptual sources (theory and film) through design, fabrication, and display. The goal is to show how a half-baked idea moves into physical reality: the "horse and cart" problems between sculpture and image, the meeting of handmade and technology processes, and the open questions that remain. The project involves **glass casting**, **video**, and **live software**, with conceptual roots in Gilles Deleuze's writing on the crystal image and Orson Welles's *The Lady from Shanghai*.

---

## Conceptual Sources

### Deleuze, *Cinema 2: The Time-Image* — "The Crystals of Time"

The McCoys draw on the French philosopher **Gilles Deleuze**'s chapter "The Crystals of Time" in *Cinema 2* (1985). Deleuze introduces the **crystal image**: an image that has two sides, **actual** and **virtual**, in constant exchange. The virtual is not (here) the digital but the mental—memory, flashbacks, mirror images, superimpositions—and the real is the present. He describes a **circuit** between actual and virtual: "the real object is reflected in a mirror image, as in the virtual object, which from its side simultaneously envelops or reflects the real. There is a coalescence between the two." In one passage he writes that it is "as if in a mirror, an image in a mirror, a photo or a postcard came to life, assumed independence and passed into the actual, even if this meant that the actual image returned to the mirror and resumed the place of the postcard or the photo following the double movement of liberation and capture." For the McCoys this suggests a **dynamic, unstable** conception of the image—incessant transition between actual and virtual within a single image—that remains productive today precisely because it is not locked to one technology.

**Jenn** emphasizes that Deleuze's "virtuality" is a **mental construction** (memory, association), not a prefiguring of the digital; the text is one of the few that asks what we are doing when we make an image—what synapses and associative mechanisms make images intelligible and express what writing cannot. **Artists using theory:** The McCoys are not trying to correct Deleuze or answer him academically. They use the text as **inspiration** and **speed it up**—grabbing an idea and testing it in practice rather than illustrating theory. Their work functions as **responses** to the text: "Let's actually try that idea."

### Orson Welles, *The Lady from Shanghai*

Deleuze discusses **Orson Welles**'s *The Lady from Shanghai* (1947/48) in the same chapter. The film offers **funhouse mirrors**, fractured images, and sequences shot through **glass**; in Deleuze's reading, "this is the moment where the virtuality comes crashing down. And in order to have access to the real, the image has to be shattered." The McCoys take from the film a visual **recipe**: a frame that is at once **glass** and **image** (a person, an action). That combination—glass + image—becomes the guiding script for the project: make glass pieces and integrate images into them, bringing the formation of the image and the formation of the glass together as a single piece. The film also exemplifies a bridge between **high and pop culture** that resonates with digital and lens-based practice.

### No origin

When asked where the project "actually started," **Kevin** pushes back: maybe there is **no origin**. He returns to Deleuze: the image is an "incessant oscillation between the actual and the virtual"—so which came first? There is no starting point; the image is this unstable thing. **Jenn** adds that the spark was the **marriage** of several concerns: the moving image as object, screens as glass, handmade + high-tech convergence, and a desire to **capture and freeze** the image rather than let it sit in endless churn—a kind of memorial to film. Ideas "drift in"; the practice is to **pay attention** when something strikes you as weird and to consider it rather than scrolling on.

---

## Project Idea: Crystal Images

- **Core formula:** Cast glass forms (abstract, lens-like topographies) in front of **screens** that play process-based video. The screen is usually treated as neutral; the McCoys want to **complicate viewership sculpturally**—to give the act of looking through/at the screen nuance it doesn't have when it's "just" glass you look through.
- **Integration:** The question of how the **image** is formed and how the **glass** is formed is brought together in one work. The same algorithmic logic that shapes the glass can appear in the video processing (e.g. lens formulas, caustics).
- **First iteration:** Using images/clips from *The Lady from Shanghai*. **Next iteration:** Starting from images they shoot (e.g. concert lights, light through glass or water), then developing glass forms that best exploit those images—a **dialogic** process between idea, media, and object.
- **Metaphor (grant language):** "Preserve in amber"—small looping images as "memory nuggets" or circuits (Deleuze). The computer allows **algorithmic** assembly and variation rather than fixed playback.

---

## Making Pipeline

The process is described below in **logical order** (design → object → display → software), not strict chronology.

### Design: 2D patterns to 3D relief

- **Aim:** Generate "lens-like" topographies—grayscale images that can act as **depth maps** (pixel intensity → z-height).
- **Tool chain:**  
  - **JavaScript** tool (developed with Claude / vibe coding) to generate grayscale patterns at different dimensions; **Photoshop** to combine multiple patterns.  
  - **Blender**, **Geometry Nodes (GeoNodes):** Import image, use dimensions for X/Y, sample grayscale for Z; export relief as **STL** for 3D printing.  
- **Iteration:** First tests were "10× too much"; they are moving toward **subtler**, more lens-like patterns (e.g. proper lens simulation algorithms, simple frequency changes). Glass distorts so intensely that one texture at different depths can be enough; sometimes two combined, but less dense than early collages.

### 3D print → mold

- **Printing:** STL files sent to a **friend** with a 3D printer (the McCoys don't own one). Prints are used as **positives** for mold-making.
- **Vapor smoothing:** Optional step to reduce layer lines; they **pulled back** from heavy smoothing because glass picks up such fine detail that retaining some print artifacts is optically interesting and makes the "digital birth" of the project visible in the final object.
- **Mold:** 3D prints are prepared (e.g. spray release, Vaseline) and used in **open-face plaster** casting. **Plaster/silica mix** (e.g. **Ransom & Ransom**, bought as pre-mixed dust)—poured, left to set (~20–30 min), then cracked out to get a **negative**. Process learned and carried out at **Urban Glass** (New York).

### Kiln casting and cold working

- **Kiln casting:** Glass **billets** (slabs) are cut to volume, placed in the mold, and fired in a kiln. Cycle includes specific heating (glass melts, flows into mold), hold, and controlled cool-down. **Annealing** (extended cool period) is critical for stability; poor annealing can lead to failure (e.g. cracking).
- **Cold working:** Sanding/polishing with **water** (wet sanding). **Challenge:** They want **selectively** clear vs foggy surfaces—edges optically clear so the image beneath reads fully, fading into more opaque texture. Standard belt sanders suit flat surfaces; for their textured relief they use **hand tools**, **Dremel**, and different grits. Either/or (fully clear or fully matte) is common in glass; blending the two is something they are "pioneering."
- **Edges:** They tried trimming edges (e.g. table saw with water) for a clean look but preferred keeping **jagged/organic** edges—more like "lightning striking sand" than a fabricated block.

### Mounting and display

- **Problem:** How to hold glass + screen on the wall with irregular glass profiles and minimal visible hardware. **Solution:** Collaboration with **Eric**, head mount maker at **MoMA**—design and fabrication of brackets in his studio (basement of MoMA). Mounts hold both screen and glass, with fabric or soft material so metal doesn't touch the sculpture. Pieces are designed to **pop off the wall** (current iteration); other options (e.g. embedded in wall) are still under consideration.
- **Electronics:** Separate the "brain" (mini PC) from the display and sculpture; run **one cable** (power + video signal) to a small enclosure. This simplifies install and future-proofs for exhibitions.

### Video and software

- **Platform:** **Mini PCs** (~$300), **Linux**, **Python** app using **OpenGL** for image processing. No GUI—**terminal-based**; behavior is set via **config files** (text) that specify source files, fragment shaders, video playback options, and many parameters (frequency, scale, color, etc.). Configs allow saving and reverting ("save it before you break it") and combat **parameter creep** from iterative vibe coding.
- **Content:** Mix of (e.g.) clips from *Lady from Shanghai*, the **same algorithmic shape** as the glass used as a video processing layer, and **caustic**/lens-style effects. First version uses *Lady from Shanghai*; next uses their own footage (e.g. concert lights)—**light** as subject (suns, moonlight, light through glass/water, virtual images).
- **Live vs fixed:** They could export to fixed MP4 for simple playback; they choose **live software** so the piece is a running process. **Jenn:** "Not quite looping"—something that moves through time but doesn't clearly progress; you can't easily find beginning, middle, end. **Kevin:** "Move through time, but not progress."
- **Coding approach:** Incremental—get the simplest thing working (e.g. video on screen, then overlay, then effects), then add. Built over time with **Claude/ChatGPT** (vibe coding). Risk: too many parameters; they try to keep a lid on it and use configs to make the "instrument" playable.

---

## Process and Practice Takeaways

- **Learning new mediums:** Step outside your comfort zone with a **concrete project**. You can "short-circuit" the "right" way and make expressive mistakes; a master craftsperson might question why you want certain effects, but that can be productive. **Hands-on** learning (e.g. classes at Urban Glass, project-specific consultations) is valuable; teaching someone with a specific project in mind is often more satisfying for the teacher than "I just want to get into this." You don't need ten years of craft before starting—but understanding the process helps when you later work with fabricators.
- **Doing it themselves vs "army":** Default is **mom-and-pop**—try to do it themselves. They bring in experts at key points (e.g. Eric for mounts) but prefer to understand the pipeline. **Jenn:** When they've used fabricators without that understanding, she’s later wished she’d known enough to ask better questions; you can "shut yourself off" to solutions if you don’t go down the road yourself first. Production can **scale to budget** (e.g. low-budget films that still reach Cannes).
- **Scaling and iteration:** First physical tests were far too busy; they dialed back to subtler, more lens-accurate patterns. Glass is "as geeky and weird as technology"—clarity, resolution, caustics are debated in both 3D graphics and glass.
- **Vibe coding / AI:** In this workshop they **foreground** it for transparency; in general they wouldn’t credit or foreground it (analogy: crediting the pencil company). AI has been a **strong accelerant** for their self-taught coding; parameter creep is a downside. Transition period for how we talk about it; they expect it will normalize like "analog vs digital" did.

---

## Key Takeaways

- **Conceptual sources:** Deleuze's crystal image (actual/virtual circuit, no single origin) and *The Lady from Shanghai* (glass + image, shattering virtuality) provide the conceptual and visual script; artists use theory to test ideas in practice, not to illustrate or correct it.
- **Project:** Crystal Images = cast glass forms + screens + live video; complicate the neutral screen; unite the formation of image and glass.
- **Pipeline:** 2D grayscale/depth maps → Blender GeoNodes → STL → 3D print → plaster/silica mold → kiln cast → cold work → mount (custom, e.g. MoMA fabricator) → mini PC + config-driven Python/OpenGL live video.
- **Practice:** Learn by doing; project-driven learning; do it yourself when possible, bring in experts when it makes sense; pay attention when an idea drifts in; "pay attention to the world, have an idea, frame it"; do the work even when it's a pain—often nobody does the "obvious" idea because it seems like too much work.
- **Mindset:** No single origin; image as oscillation; "move through time but not progress"; lean into being a doer; the weird, labor-intensive work is what people respond to.

---

## Q&A Highlights

**Orson Welles: "A filmmaker needs an army." How do you build a practice without one?**  
Default to trying it themselves ("mom and pop"); bring in key people when it helps. Knowing the process improves later collaboration with fabricators. Production can scale to budget; there are no fixed rules.

**Learning new mediums (e.g. glass)?**  
Project-driven learning; classes and consultations (e.g. Urban Glass); you don’t need to master the craft for years before starting—but hands-on understanding matters.

**Attributing credit to AI / vibe coding?**  
Useful to mention in this workshop context; generally wouldn’t credit it (like the pencil company or the delivery person). AI as accelerant; we’re in a transition in how we talk about it.

**Where did the project actually start?**  
Marriage of ideas: moving image as object, screens as glass, handmade + tech, desire to capture/freeze rather than churn. No single origin—Deleuze’s oscillation; paying attention when something "drifts in" and taking it seriously.

**Hitchcock and over-planning:**  
Contrast with wanting to **discover along the way**; fully conceptualizing then just executing feels "unexciting and kind of grueling." The project came from open questions approached from two directions at once.

---

## Studio Reflections

1. **Theory and practice:** Is there a text or concept you’ve been carrying that you could "speed up" by testing it in material or process rather than in argument?
2. **New mediums:** What would it take to get hands-on with a material or process you don’t yet know—classes, consultations, a single project—without waiting for full mastery?
3. **Origin and oscillation:** Where do you locate the "start" of a current project? What if you treated it as having no single origin but as an ongoing exchange between actual and virtual, idea and making?

---

*Summary based on the Artist Commons workshop transcript (110_mccoy_workshop/transcript.txt), second session with Jen and Kevin McCoy.*
