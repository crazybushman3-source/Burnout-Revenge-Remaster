# Burnout Revenge PC (Windows) - roadmap

**Status (9 Oct 2026): on hold.** This work was built as patches on top of
[Xerenge](https://github.com/shipa-2/Xerenge) by shipa-2. Xerenge has no licence, and I don't have permission to
publish work built on it, so the installer and the patches stay unreleased. No game files and no Xerenge code are
in this repository. Much of this work was done with AI assistance (Claude).

## What should happen next? Your input, please

These are the options I'm weighing. Tell me which you'd prefer, and why, in [Issues](../../issues)
("On hold: what should this project do next?"):

1. **Stop here.** The work stays private; this page stays up as a record.
2. **Offer it to Xerenge.** Describe or send the fixes (texture sampling, vertex unpacking) and the in-game
   graphics options to Xerenge, if its author wants them. They would become part of his project.
3. **An independent version, from scratch.** A new PC version built only on openly licensed code (no Xerenge
   code, nothing copied from unlicensed projects), with its own renderer. Realistically many months of work, and
   I would first check that nobody else is already building the same thing, so I don't step on anyone's toes.

## What was built (tested privately, not published)

- PC options in the game's own menus (front end and pause menu), saved between runs: render scale, anti-aliasing
  (SMAA / TAA) + TAA sharpness, ambient occlusion + radius, reflections, HD textures, texture filter, texture
  sharpness, mipmaps, bloom, extra bloom, sharpen, contrast, shadow lift, colour, dither, takedown music.
- Rendering fixes: texture sampling (mipmaps), vertex/index handling, HUD layering, explosion shaders.
- Frame-pacing work and a 60 fps hitch test that changes every setting and measures each frame.
- EU and US discs; a test bot that drives full races by itself from game memory.
- A Windows installer that builds the game from your own disc on your PC (portable tools, offline mode).

## Already done elsewhere (not planned here)

Earlier versions of this page listed ultrawide support and high frame rates as plans. Xerenge already has wide
screens, frame generation and an unlocked frame rate, and it had a render-resolution option before my in-game
render scale. Those are shipa-2's work and are credited to him.

## Credits

- **shipa-2** - [Xerenge](https://github.com/shipa-2/Xerenge), the recompilation this work is built on, including
  its render-resolution option and wide-screen support, which came before mine.
- **bikhe** - the Xerenge fork this work started from, and fixes that went into Xerenge.
- **hedge-dev** - [XenosRecomp](https://github.com/hedge-dev/XenosRecomp) (MIT); its original texture sampling is
  what my mipmap fix restores.
- **ReXGlue SDK** (rexglue-sdk) - BSD 3-Clause; by Tom Clay, based on Xenia by Ben Vanik and contributors.
  Its notice is kept; use of their names does not imply endorsement.
- **plume** (renderbag) - MIT.
- **SMAA** (Jimenez et al.), **stb_image**, **RenderDoc** API header - MIT.
- **CrownParkComputing** - Xbox360-Native-Ports, another recompiled Burnout Revenge.

Burnout and Burnout Revenge are trademarks of Electronic Arts. This project is not affiliated with or endorsed by
Electronic Arts or Criterion Games, and contains no game files.
