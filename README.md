# BlueScreenOfDeath-Python

A harmless Python prank application that simulates a fake Windows Blue Screen of Death (BSOD) experience using Python.

The program creates a fullscreen overlay, plays sound effects, displays a sequence of custom BSOD images, and opens a webcam face-detection window for additional prank effects.

<img width="850" height="601" alt="bsod11" src="https://github.com/user-attachments/assets/62af29df-5826-42df-af23-a06534435145" />

## Features

* Fake BSOD screen simulation
* Fullscreen desktop overlay
* Multiple image-based visual effects
* Sound effects and audio sequences
* Webcam face detection using OpenCV
* Face highlighting after sustained detection
* Keyboard blocking during the prank sequence
* Multi-stage scare/troll animation

## Preview

The application:

1. Takes a screenshot of the current desktop.
2. Displays it in a fullscreen window.
3. Waits for user interaction.
4. Starts a sequence of fake BSOD screens and sound effects.
5. Opens a webcam window with face detection.
6. Continues through multiple visual stages.

## Requirements

* Python 3.9+
* Windows
* A connected webcam

### Python Libraries

```bash
pip install pyautogui pillow opencv-python numpy keyboard --upgrade
```

## Project Structure

```text
BlueScreenOfDeath-Python/
│
├── Main.py
├── FaceRecognitionProjectForBsod.py
│
├── bsod1.png
├── bsod2.png
├── ...
│
├── noise1.wav
├── noise2.wav
├── noise3.wav
├── loop.wav
└── sound1.wav
```

> `desktop.png` is generated at runtime (a screenshot of your desktop) and is not part of the repository.

## How To Run

```bash
python Main.py
```

## ⚠️ How To Stop The Program

Once the prank sequence starts (after you click the screen), the app blocks `Ctrl`, `Alt`, `Win`, and `Delete` system-wide and keeps its window fullscreen and always-on-top. This means the usual escape routes are disabled:

* `Ctrl+Alt+Del` / `Ctrl+Shift+Esc` (Task Manager) — blocked
* `Alt+F4` — blocked
* `Win+D` / Start menu — blocked

Pressing `ESC` only closes the small webcam preview window, not the main BSOD screen.

The sequence is designed to end on its own after the final animation, but if you need to stop it immediately, you'll need to kill the process another way, for example:

* End the `python.exe` / `Main.py` process from another machine over the network (e.g. `psexec`, SSH, or remote desktop).
* Use a scheduled task, startup script, or second account session to run `taskkill /IM python.exe /F`.
* As a last resort, force a shutdown/restart via the power button.

Because of this, only run the prank on a machine (and with input, like a webcam) you own or have explicit permission to use, and consider having a way to terminate the process remotely before you start it.

## Disclaimer

This project is intended for educational, entertainment, and prank purposes only.

It does **not** damage files, modify the operating system, install malware, or perform any destructive actions.

Use responsibly and only on systems where you have permission to run it.

## Copyright Notice

Some images, sounds, visual assets, or screenshots included in this repository may be copyrighted by their respective owners.

If you are the copyright holder of any asset used in this project and would like it removed or credited differently, please open an issue or contact the repository owner.

Users are responsible for ensuring they have the rights to distribute any assets included in their forks or modifications of this project.

## License

This project is provided as-is for educational purposes.
