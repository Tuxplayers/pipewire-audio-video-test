# PipeWire Audio and Video Test

A simple Python script to test audio and video output under PipeWire. The script generates a sine wave for the audio test and displays a test image for the video test.

## Requirements

- Python 3.6 or higher
- Dependencies:
  ```bash
  pip install numpy pyaudio opencv-python
  ```

## Usage

1. Clone this repository:
   ```bash
   git clone https://github.com/TUXPLAYER/pipewire-audio-video-test.git
   cd pipewire-audio-video-test
   ```

2. Run the script:
   ```bash
   python pipewire_audio_video_test.py
   ```

## Features

- **Audio Test**: Generates a 440 Hz sine wave (A4 note) and plays it for 5 seconds.
- **Video Test**: Displays a gradient test image with text overlay.

## License

This project is licensed under the [MIT License](LICENSE).

**Disclaimer**: Use this script at your own risk. The author assumes no liability for any damages or issues caused by its use. Ensure you understand and verify the functionality before using it in critical environments.

---

Contributions are welcome! Feel free to open issues or submit pull requests.
