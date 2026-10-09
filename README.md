<h1 align="center"><img src="docs/banner.png" alt="Burnout Revenge Remaster" width="860"></h1>

A Windows PC version of Burnout Revenge (Xbox 360), built on [Xerenge](https://github.com/shipa-2/Xerenge)
by shipa-2. **On hold - and I'd like your input.**

> **Update, 9 Oct 2026: the project is on hold.**
>
> Everything I built so far is a set of patches on top of Xerenge. Xerenge has no licence, and I don't have
> permission to publish work built on it, so I'm not releasing the installer or the patches. That's the
> author's right, and this isn't a dispute: Xerenge is great work, and it's the reason any of this runs.
>
> I'm deciding what to do next and would like to hear from you - see **[ROADMAP.md](ROADMAP.md)** for the
> options, and tell me what you think in **[Issues](../../issues)** ("On hold: what should this project do
> next?").

## What I built (tested privately, not published)

- PC graphics options in the game's own menus (Driver Details > Settings, and Options in the pause menu), saved
  between runs: render scale (75-200%), TAA or SMAA, ambient occlusion with its radius, texture filtering up to
  16x, texture sharpness, sharper reflections (2x/4x), the game's bloom in steps, sharpen, contrast, shadow lift,
  colour, dither and the takedown music volume.
- HD texture replacement, a texture-sampling (mipmap) fix, vertex-unpacking fixes, the HUD drawn on its own layer.
- EU and US discs, a test bot that drives full races by itself, and a Windows installer that builds the game from
  your own disc on your PC.

**No game files are or will be in this repository, and no Xerenge code either.** Much of this work was done with
AI assistance (Claude); if you would rather not use AI-assisted projects, that is completely fair.

## Other Burnout Revenge projects

This was never the first PC version of Burnout Revenge:

- **[Xerenge](https://github.com/shipa-2/Xerenge)** by shipa-2 - the recompilation this work is built on, with
  its own releases and installers for Windows, Linux and Android, frame generation, wide screens and online play.
- **[Xbox360-Native-Ports](https://github.com/CrownParkComputing/Xbox360-Native-Ports)** by CrownParkComputing -
  recompiled launchers for several Xbox 360 games, Burnout Revenge (USA) among them.

## Licence

This project's own code is under the [MIT Licence](LICENSE). Third-party parts keep their own licences (see the
credits in [ROADMAP.md](ROADMAP.md)).

Burnout and Burnout Revenge are trademarks of Electronic Arts. This project is not affiliated with or endorsed by
Electronic Arts or Criterion Games, and contains no game files.
