# Burnout Revenge PC (Windows) - roadmap

A native Windows build of Burnout Revenge (Xbox 360), built on [Xerenge](https://github.com/shipa-2/Xerenge) by
shipa-2: the game recompiled ahead of time to a native executable, with a Vulkan renderer. This project adds
Windows support, a PC graphics options menu, rendering fixes and a one-click installer. Much of this work was done
with AI assistance (Claude); if you would rather not use AI-assisted projects, that is completely fair.

**No game files are or will be in this repository, and no Xerenge code either.** It holds only this project's own
changes (as patch files), scripts, tools and docs. The installer downloads Xerenge and its libraries at a pinned
version, applies the patches, and builds everything from your own disc on your own PC. You need your own copy of
the game (retail EU or US Xbox 360 disc image).

**Status (8 Oct 2026):** not released yet. The installer is built and passed two full install tests on the
developer's PC; a clean-machine test (a fresh Windows install in a virtual machine) is running. This repository
only holds the plan for now; the installer and code follow once that test passes. No dates - it is done when it
is done.

## How installing will work (planned)

1. Download `Burnout_Revenge_Setup.exe` from Releases and run it.
2. Pick an install folder and your disc image (.iso). The image is checked against the known EU and US hashes.
3. Click Install. It installs Microsoft's free C++ Build Tools (one Windows permission prompt), downloads the
   other tools into the install folder (nothing else is added to your system), downloads Xerenge at the pinned
   version, applies this project's patches, extracts your disc, builds the game and adds Start menu and desktop
   shortcuts. Progress bar, full log, and it resumes where it stopped if anything fails.
4. Play. An uninstaller removes the install folder (and, if you want, the Build Tools).

Expect roughly 20 GB of disk space and a long first install (the game is compiled on your PC). Measured so far
on the developer's PC (Intel i9-10900KF, Build Tools already installed): the build took about 13 minutes and the
install folder was 11 GB, plus the space of Microsoft's Build Tools. Clean-machine numbers follow before release.

## Done (in testing, not published yet)

- Native Windows build (Visual Studio + LLVM), US and EU discs accepted.
- PC options in the game's own menus (front end and pause menu), saved between runs: render scale,
  anti-aliasing (SMAA / TAA) + TAA sharpness, ambient occlusion + radius, reflections, HD textures, texture
  filter, texture sharpness, mipmaps, bloom, extra bloom, sharpen, contrast, shadow lift, colour, dither,
  takedown music.
- Many rendering fixes (vertex/index handling, texture sampling, HUD layering, explosion shaders).
- Frame pacing and stutter work: texture swaps spread over frames, pooled uploads, a 60 fps hitch test that
  changes every setting and measures each frame.
- A test bot that drives full races by itself from game memory (used to test builds before anyone plays them).
- **One-click Windows installer**: built; two full install tests passed on the developer's PC (Build Tools,
  portable tools, Xerenge at the pinned version, the patches, disc extraction and the build).
- **Pre-release code review** of the renderer changes, scripts and installer patch; its fixes are in and tested.

## Next, in order

1. **Clean-machine install test** of the installer (running now).
2. **First public release**: licence notices, README + install guide.
3. **Automated tester, finished**: the bot records every run and checks each frame for problems
   (black/corrupt frames, missing textures, flicker, stutter).
4. **Render scale changes without a hitch** (prepare the new resolution in the background).

## Later (planned, no dates)

- Side-by-side previews in the options menu (see what a setting does before you pick it).
- Graphics presets (Low ... Ultra / Max).
- **Ultrawide support** (21:9 and wider) as an in-game setting: a wider view of the road instead of a stretched
  picture, with the HUD and menus kept in their 16:9 area.
- A benchmark button that tests your PC and recommends settings.
- Optional HD texture pack made on your own PC by a script (never shipped as files).

## Maybe, much later (no promises)

Steam Deck will be looked into. Other platforms are only ideas for now.

## Credits

- **shipa-2** - [Xerenge](https://github.com/shipa-2/Xerenge), the recompilation project this builds on.
  Xerenge is downloaded from its own repository by the installer; it is not copied here.
- **bikhe** - the Xerenge fork this work started from.
- **ReXGlue SDK** (rexglue-sdk) - BSD 3-Clause; by Tom Clay, based on Xenia by Ben Vanik and contributors.
  Its notice is kept; use of their names does not imply endorsement.
- **plume** (renderbag) - MIT. **XenosRecomp** (hedge-dev) - MIT.
- **SMAA** (Jimenez et al.), **stb_image**, **RenderDoc** API header - MIT; notices ship with the code.

Burnout and Burnout Revenge are trademarks of Electronic Arts. This project is not affiliated with or endorsed by
Electronic Arts or Criterion Games, and contains no game files.
