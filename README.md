# PipeWire Audio and Video Test

## Introduction

This project provides a Python script to test audio and video functionalities under **PipeWire**. It plays a sine wave for audio testing and displays a test image for video testing.

---

## Table of Contents

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Setting Up a Virtual Environment](#setting-up-a-virtual-environment)
- [Usage](#usage)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)

---

## Features

- **Audio Test**: Generates a 440 Hz sine wave (A4 note) and plays it for 5 seconds.
- **Video Test**: Displays a gradient test image with text overlay.
- Fully compatible with **PipeWire**.

---

## Prerequisites

### Required Software

- **Python 3.6+**
- **PipeWire** installed and running on your system.

### Python Dependencies

Install the required Python libraries:
```bash
pip install sounddevice numpy opencv-python
```

### PipeWire Configuration

Ensure PipeWire is properly configured with an appropriate sample rate. Modify or create the configuration file:
```bash
nano ~/.config/pipewire/pipewire.conf
```

Set the following values:
```ini
default.clock.rate = 48000
default.clock.allowed-rates = [ 44100 48000 ]
```

Restart PipeWire:
```bash
systemctl --user restart pipewire pipewire-pulse
```

---

## Installation

Clone the repository and navigate into it:
```bash
git clone https://github.com/TUXPLAYER/pipewire-audio-video-test.git
cd pipewire-audio-video-test
```

---

## Setting Up a Virtual Environment

To ensure a clean and isolated Python environment, create and activate a virtual environment:

1. Create a virtual environment:
   ```bash
   python -m venv venv
   ```

2. Activate the virtual environment:
   - For Linux/Mac:
     ```bash
     source venv/bin/activate
     ```
   - For Windows:
     ```bash
     venv\Scripts\activate
     ```

3. Install the required dependencies within the virtual environment:
   ```bash
   pip install sounddevice numpy opencv-python
   ```

4. Verify the setup by running the script:
   ```bash
   python pipewire_audio_video_test.py
   ```

---

## Usage

Run the script to test audio and video functionalities:
```bash
python pipewire_audio_video_test.py
```

---

## Troubleshooting

### Common Issues

#### Invalid Sample Rate Error
- Ensure PipeWire's sample rate matches the script's sample rate (default: `48000 Hz`).
- Check the current configuration with:
  ```bash
  pactl info | grep "Default Sample Rate"
  ```

#### Audio Not Playing
- Verify the default audio sink is correctly configured:
  ```bash
  pactl list sinks
  ```

#### Video Not Displaying
- Ensure `opencv-python` is installed correctly:
  ```bash
  pip install opencv-python
  ```

---

## Contributing

Contributions are welcome! Follow these steps to contribute:

1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add feature-name"
   ```
4. Push to your branch:
   ```bash
   git push origin feature-name
   ```
5. Open a pull request.

---

## License

This project is licensed under the ## License
This project is licensed under the [MIT License](LICENSE). Use at your own risk. The author assumes no liability for damages or issues caused by the use of this script.
