# Video Background Music

## Português

Skill gratuita para pesquisar músicas licenciadas e adicioná-las a vídeos sem prejudicar a fala. Ela conversa sobre o clima da música, confirma o vídeo original e a pasta de destino, e mostra um preview com volume e transições para aprovação antes da entrega final.

### Instalação no Claude Code

```text
/plugin marketplace add spoliagency/video-background-music
/plugin install video-background-music@video-background-music
```

Depois, use `/video-background-music:video-background-music` e diga que quer adicionar música. A skill conduz a escolha naturalmente.

---

## English

Free, reusable instructions for researching appropriate licensed music and adding it to a video while keeping spoken audio easy to follow.

It guides an agent through current license checks, music selection, subtle dialogue-safe mixing, timing, fades, and verification of the final render.

## What it covers

- Instrumental music selection for software tutorials, demonstrations, talking-head videos, and business content.
- Research by topic, mood, energy, use case, creator/channel reference, or current YouTube trend.
- Current license, attribution, and Content ID checks from official music sources.
- Low-volume mixing, short fades, and a timeline that respects explanation-first speaking segments.
- Separate outputs and checks for duration, streams, speech, music, and the ending.
- A temporary audio-and-video preview for approval before the final delivery.

## Requirements

- A local video and audio tool such as FFmpeg.
- An internet connection when researching current licensing and official music sources.

## File locations

Before editing, the skill confirms which file is the original and asks where to place the finished copy: Downloads or a separate `Videos Editados` folder. It creates that folder when the student chooses it and reports the final path without overwriting the original.

## What happens after installation

The student does not need to understand FFmpeg before asking for help. They can invoke the skill and write a normal request, for example:

```text
Add subtle instrumental background music to this tutorial. Keep it very low and remove it while I speak directly to the camera.
```

They can also request a themed or trend-informed shortlist, for example:

```text
Find three licensed tracks with a clean, futuristic automation style that fit what is currently popular in YouTube productivity videos.
```

The skill will explain the next step, check whether a local video renderer is ready, and proceed if it is. If it is not ready, it identifies the student's operating system and asks whether it may download and install FFmpeg or a compatible renderer from an official source. After approval, it verifies the tool and continues from the same request.

## Guided conversation

If the student starts with “I want to add music,” the skill begins naturally with the desired feeling: clean and professional, energetic, calm, or futuristic. It then asks only what is still needed, such as whether music should play throughout or only between speaking segments, and whether the student wants a shortlist or already has a track. License checks happen in the background.

## Install in Claude Code

After this repository is published, run these commands in Claude Code:

```text
/plugin marketplace add spoliagency/video-background-music
/plugin install video-background-music@video-background-music
```

Then invoke it with:

```text
/video-background-music:video-background-music
```

## Install in Codex

Ask Codex to use its `skill-installer` skill to install this GitHub repository's skill at:

```text
plugins/video-background-music/skills/video-background-music
```

After installation, invoke it explicitly as `$video-background-music` or let Codex select it for a relevant audio-editing task.

## Privacy

This repository contains reusable guidance only. It intentionally excludes source videos, outputs, personal paths, music files, account data, credentials, and keys. Do not commit media or private configuration.

## License

[MIT](LICENSE)
