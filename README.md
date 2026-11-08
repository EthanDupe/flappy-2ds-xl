# Flappy Bird 2DS — Dual-Screen Arcade Edition (`.cia` & `.3dsx`)

A native C99 / `citro2d` / `libctru` / `NDSP` Flappy Bird built specifically for the **Nintendo 2DS & New Nintendo 2DS XL** with procedural 16-bit PCM NDSP sound effects, persistent SD high-score & medal saves, and wireless FBI installation.

## Dual-Screen Features & Controls

- **Top Screen (400×240, 60 FPS)**:
  - Multi-layer parallax sky (Day / Sunset / Night), sun & crescent moon with twinkling stars, clouds, city skyline, bush hedge, and scrolling diagonal-striped ground.
  - Shaded 3D-style pipes with lip caps, articulated Bird with pitch-rotation physics, flapping wings, and particle bursts.
  - Medal system (**Bronze** ≥ 10, **Silver** ≥ 20, **Gold** ≥ 30, **Platinum** ≥ 40).
- **Bottom Touch Screen (320×240)**:
  - **Touch Flap Pad (Left)**: Tap anywhere with your thumb or stylus to flap (with expanding ripple feedback).
  - **Trophy Case & Scoreboard (Right)**: Live score, per-difficulty high score, total pipes cleared, and unlocked medal badges (saved automatically to `sdmc:/3ds/flappy2ds/save.dat`).
  - **Settings Bar (Bottom)**: Tap to switch **Sky Theme** (`Day` / `Sunset` / `Night`), **Difficulty** (`Relaxed` / `Classic` / `Turbo`), or **SFX Mute**.
- **Physical Buttons**:
  - **A / B / X / L / R / D-Pad Up**: Flap wings / Start / Play Again
  - **Y**: Pause / Resume
  - **SELECT**: Cycle Day / Sunset / Night sky theme
  - **START**: Pause in-game, or exit cleanly to the 2DS HOME Menu from Title / Pause / Game Over

## Build & Install

Push this repository to GitHub to automatically build `flappy.cia` and `flappy.3dsx` via `.github/workflows/build_cia.yml`, or run `make cia` locally with devkitARM.

To install wirelessly over Wi-Fi via **FBI** (`Remote Install -> Receive URLs over the network`):
```bash
python3 tools/remote_install_cia.py <YOUR_2DS_IP> flappy.cia
```
