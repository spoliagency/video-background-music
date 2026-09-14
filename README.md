# Video Background Music

Free, reusable instructions for researching appropriate licensed music and adding it to a video while keeping spoken audio easy to follow.

It guides an agent through current license checks, music selection, subtle dialogue-safe mixing, timing, fades, and verification of the final render.

## What it covers

- Instrumental music selection for software tutorials, demonstrations, talking-head videos, and business content.
- Current license, attribution, and Content ID checks from official music sources.
- Low-volume mixing, short fades, and a timeline that respects explanation-first speaking segments.
- Separate outputs and checks for duration, streams, speech, music, and the ending.

## Requirements

- A local video and audio tool such as FFmpeg.
- An internet connection when researching current licensing and official music sources.

## What happens after installation

The student does not need to understand FFmpeg before asking for help. They can invoke the skill and write a normal request, for example:

```text
Add subtle instrumental background music to this tutorial. Keep it very low and remove it while I speak directly to the camera.
```

The skill will explain the next step, check whether a local video renderer is ready, and proceed if it is. If it is not ready, it explains why a renderer is needed and offers installation guidance for the student's operating system; it never installs software without their approval. Once the renderer is available, the conversation continues from the same request.

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
