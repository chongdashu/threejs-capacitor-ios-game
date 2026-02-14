<img src="docs/preview.gif" alt="Pirate 3D character viewer" width="320"> <img src="docs/preview-02.gif" alt="Pirate 3D character viewer" width="320">

# Pirate 3D — Three.js + Capacitor for Desktop & iOS

This repo is the companion project for the YouTube build:
**"How I Vibe Code 3D Games With AI - Full Tutorial)"** ([watch on YouTube](https://www.youtube.com/watch?v=fu7NZ3t3sLM))

It includes:
- **Agent Skills** for Claude Code and Codex CLI — Three.js scene building, GLTF loading, and Capacitor iOS integration.
- **AI Prompts** used in the video to generate characters, backgrounds, voices, animations, and the Three.js scene.
- A **JSON animation index** (`assets_index.json`) that defines the animation contract for two characters (Pirate & Bartender) — clip names, durations, loop modes, and crossfade timing — showing how to structure metadata for GLB-based character animation.

This is a reference/template repo. It does not include runnable app code or GLB model files — those are built during the video using the skills and prompts provided here.

## Want more?

If you want the all-in-one workflow kit I use across **Claude Code, Codex CLI, and Cursor**—including ready-to-run agents/skills/rules and full source from my YouTube builds—check out [BuilderPack.ai](https://www.builderpack.ai/?utm_campaign=threejs_pirate_01&utm_source=github&utm_medium=readme). Game dev vibe coding resources like this are coming soon to BuilderPack.ai too.

---

## Using the Skills

Copy the skill folders into your project to give your AI coding agent context for Three.js and Capacitor iOS workflows.

**Three.js Builder** (`.claude/skills/threejs-builder/` or `.codex/skills/threejs-builder/`)
Covers scene setup, GLTF/GLB loading, animation mixing, shaders, post-processing, and game patterns like state machines and parallax.

**Capacitor iOS** (`.codex/skills/threejs-capacitor-ios/`)
Covers Capacitor native sync, SPM vs CocoaPods, common iOS gotchas, and the animation index metadata pattern.

## Using the Prompts

The `prompts/` folder contains the step-by-step AI prompts from the video:

1. **01-character-creation.txt** — Gemini 3D character generation (whimsical pirate, t-pose GLB)
2. **02-level-creation.txt** — 2.5D pre-rendered background image creation
3. **03-character-voice.txt** — Voice persona definitions
4. **04-animate-bg.txt** — Looping background animation hints
5. **05-asset-json.txt** — Generate `assets_index.json` from GLB model clips
6. **06-threejs-scene.txt** — Three.js viewer scene setup with orbit controls and touch input

## Animation Index

`public/assets/assets_index.json` defines the animation metadata contract for two characters. Each entry maps a friendly action name (idle, walk, run, talk) to the actual clip name inside the GLB, along with duration, loop mode, and default state. No GLB files are included — the JSON shows the expected structure so you can wire up your own models.

## Project Structure

```
.claude/skills/         # Claude Code agent skills
.codex/skills/          # Codex CLI agent skills
public/
  assets/
    assets_index.json   # Animation metadata (clip names, durations, loop modes)
prompts/
  01-character-creation.txt
  02-level-creation.txt
  03-character-voice.txt
  04-animate-bg.txt
  05-asset-json.txt
  06-threejs-scene.txt
docs/
  preview.gif           # Demo recordings
  preview-02.gif
```

## License

MIT
