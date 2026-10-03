# Kurtzon's Discord plugins

A set of voice, audio, and quality-of-life plugins for Discord. They ship built into [Kurtcord](https://github.com/kurtzonaudio/kurtcord) and also work as user plugins in Vencord and Equicord.

All plugins are MIT licensed and each one lives in its own repository:

| Plugin | What it does |
| --- | --- |
| [Stereo Guard](https://github.com/kurtzonaudio/stereo-guard) | Locally mutes anyone whose audio is not fully mono: panning, stereo width, panning around, and reverb tails. |
| [Mic Spam Guard](https://github.com/kurtzonaudio/mic-spam-guard) | Locally mutes anyone who gets too loud or spams their microphone. |
| [Voice State Fix](https://github.com/kurtzonaudio/voice-state-fix) | Corrects stuck mute and deafen states when Discord's server and your client disagree. |
| [Voice VU Meters](https://github.com/kurtzonaudio/voice-vu-meters) | Live vertical VU meters next to everyone in a call, stereo or mono. |
| [Kurtcord Voice Panel](https://github.com/kurtzonaudio/kurtcord-voice-panel) | A live Voice & Video panel in the user area: mic, EQ, reverb, codec, spatial, output, camera, and VST controls. |
| [Kurtcord Theme](https://github.com/kurtzonaudio/kurtcord-theme) | The Kurtcord wallpaper theme with an adjustable dim overlay. |
| [Camera Unlock](https://github.com/kurtzonaudio/camera-unlock) | Unlocks the camera and Go Live buttons in channels where the Stream permission check hides them. |
| [Click To Unmute](https://github.com/kurtzonaudio/click-to-unmute) | Click the mute icon next to a locally muted user to unmute them instantly. |
| [Auto Cam Off](https://github.com/kurtzonaudio/auto-cam-off) | Turns your camera off when a server owner, admin, or moderator joins your voice channel. |

## The voice guards

Stereo Guard, Mic Spam Guard, and Voice State Fix all work on the same principle: they watch the call and act locally on your side. The guards mute locally, so the other person is not told, nothing is reported, and nobody else is affected. Voice State Fix corrects your own server-side state when it gets stuck.

Every guard keeps a never-mute list. In Kurtcord you can add someone to it by right-clicking their name anywhere in Discord and picking the Allow entry for that guard. The same list is managed from each plugin's settings, and the two stay in sync.

## Installation

For Vencord or Equicord, clone the plugin repository into your userplugins folder and rebuild:

```
git clone https://github.com/kurtzonaudio/stereo-guard src/userplugins/StereoGuard
git clone https://github.com/kurtzonaudio/mic-spam-guard src/userplugins/MicSpamGuard
git clone https://github.com/kurtzonaudio/voice-state-fix src/userplugins/VoiceStateFix
git clone https://github.com/kurtzonaudio/voice-vu-meters src/userplugins/VoiceVUMeters
git clone https://github.com/kurtzonaudio/kurtcord-voice-panel src/userplugins/KurtcordVoicePanel
git clone https://github.com/kurtzonaudio/kurtcord-theme src/userplugins/KurtcordTheme
git clone https://github.com/kurtzonaudio/camera-unlock src/userplugins/CameraUnlock
git clone https://github.com/kurtzonaudio/click-to-unmute src/userplugins/ClickToUnmute
git clone https://github.com/kurtzonaudio/auto-cam-off src/userplugins/AutoCamOff
pnpm build
```

Restart Discord and enable the plugins you want in Settings, Plugins.

In Kurtcord, all of them are built in and can be managed from Plugins. The Kurtcord Voice Panel is already available as a button in the user area, and the guards are ready to configure.

## Notes

- The guards mute locally. They cannot affect what anyone else hears.
- The plugins analyze decoded audio, so they see exactly what your ears get.
- Kurtcord Voice Panel, the voice guards, and the meters are made for voice calls. They do nothing outside a call.
- Some controls in Kurtcord Voice Panel need the Kurtcord desktop client to apply, such as spatial audio, VST chains, and camera presets.

## License

MIT. Copyright (c) 2026 Kurtzon (Kurtzon Audio). See [LICENSE](LICENSE).

Built and maintained by Kurtzon.
