# PipeWire Audio and Video Test

## Introduction

This repository was created as a small test project while learning and experimenting with GitHub, Linux, Python, and PipeWire.

The original idea was to create a simple test program for checking basic audio and video functionality under PipeWire.

This was an experimental learning project and was **never intended to be a finished, production-ready, or actively maintained software project**.

---

## Project Status

**Status: Experimental / Archived**

This repository is preserved mainly as documentation of an early GitHub experiment.

The original executable/script file is no longer included in the repository.

The README describes the original project idea and contains example code for educational and experimental purposes.

---

## Original Project Idea

The original test was intended to provide basic functionality such as:

- **Audio Test:** Generate and play a 440 Hz sine wave (A4).
- **Video Test:** Display a simple test image with a text overlay.
- **PipeWire:** Use the Linux PipeWire audio infrastructure.
- **Python:** Use Python together with common audio and video libraries.

The original Python concept used libraries such as:

- `sounddevice`
- `numpy`
- `opencv-python`

---

## Important Notice

The code in this repository is provided for **educational and experimental purposes only**.

If you copy, modify, compile, execute, or otherwise use any code from this repository, **you do so at your own responsibility and risk**.

The author does not guarantee that the examples will work on your particular system, Linux distribution, PipeWire configuration, Python version, hardware, or software environment.

Anyone using or modifying the code should understand what the code does and should test it in their own environment before using it.

**Copying and pasting code does not transfer responsibility to the author.**

Every user is responsible for checking, adapting, testing, and safely using any code they copy from this repository.

---

## Example Bash Script

The following is a simple example of the kind of Linux test/automation script used during experimentation.

It is **not the missing original PipeWire Python program** and should not be interpreted as such.

```bash
#!/bin/bash
#
# Maker:        Heiko Schäfer (TUXPLAYER)
# Datum:        $(date '+%d.%m.%Y')
# Zeit:         $(date '+%H:%M:%S')
# Version:      1.0
# Beschreibung: Beispiel eines einfachen Linux-Testskripts
# Zweck:        System-Optimierung / Automatisierung
# --------------------------------------------------------------------------
# "I'm a Maker - All stupid people are bracker in my way"
#

echo "TUXPLAYER Linux Test Script"
echo "Datum: $(date '+%d.%m.%Y')"
echo "Zeit:   $(date '+%H:%M:%S')"

echo
echo "System:"
uname -a

echo
echo "PipeWire:"
if command -v pipewire >/dev/null 2>&1; then
    pipewire --version
else
    echo "PipeWire wurde nicht gefunden."
fi
