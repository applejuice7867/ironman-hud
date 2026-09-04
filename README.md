# JARVIS VR HUD

A browser-based monocular VR HUD inspired by an Iron Man-style heads-up display. The app mirrors a live camera feed into left and right eye viewports, adds telemetry and targeting overlays, and supports optional YouTube media and voice controls.

<!-- Replace this placeholder with a hero screenshot. -->
![JARVIS VR HUD preview](docs/images/hud-preview.png)

## Features

- Split-screen left and right eye camera views
- Adjustable lens zoom, HUD scale, field of view, and lens separation (IPD)
- Optional YouTube player displayed in one eye to avoid double audio and visual overlap
- Device orientation tracking and orientation calibration
- Camera selection and fullscreen landscape mode
- Object detection powered by TensorFlow.js and COCO-SSD
- Hand gesture tracking powered by TensorFlow.js HandPose
- Voice commands for media playback and visual questions
- Optional Gemini Vision analysis of the area around the crosshair
- Live telemetry, clock, battery status, map imagery, and HUD notifications

<!-- Replace this placeholder with a controls or UI screenshot. -->
![HUD controls](docs/images/hud-controls.png)

## Using Normally

Through github pages this project already is hosted, go to [the website](https://applejuice7867.github.io/ironman-hud/)


## Getting Started

1. Open the page from `localhost` or another secure HTTPS origin.
2. Allow camera, microphone, motion, and fullscreen permissions when prompted.
3. Select a camera source.
4. Adjust the lens, HUD, IPD, and media settings.
5. Optionally enter a YouTube video ID or URL.
6. Select **ENGAGE VR HUD**.

The app stores display preferences such as eye selection and slider values in browser storage. The Gemini API key is kept in session storage and is sent directly from the browser to the Google Generative Language API when visual questions are asked.

## Voice Commands

When supported by the browser, the voice assistant recognizes:

- `play`, `resume`, or `start`
- `pause` or `stop`
- `skip`, `skip ads`, or `next`
- Any other spoken phrase as a visual question when a Gemini API key is provided

## Browser Requirements

- A browser with webcam access and JavaScript enabled
- A secure context: `localhost` or HTTPS is recommended
- WebGL support for TensorFlow.js
- Speech Recognition support for voice commands
- Device orientation support for head-tracking behavior
- Permissions for camera, microphone, motion sensors, and fullscreen as needed

Feature availability varies by browser and device, especially on iOS and Safari.

## External Services

The app loads or calls these services directly from the browser:

- TensorFlow.js, COCO-SSD, and HandPose from jsDelivr
- YouTube IFrame Player API
- ArcGIS World Imagery map tiles
- Google Gemini Vision API, only when a key is supplied

Review each service's terms, quotas, and privacy requirements before using the project in production.

<!-- Replace this placeholder with a photo or diagram of the intended device setup. -->
![Device setup](docs/images/device-setup.jpg)

## Project Structure

```text
.
├── index.html       # Complete application: markup, styles, and JavaScript
└── docs/images/     # Suggested location for README images you add later
```

## License

No license has been specified yet.

<!-- Replace this placeholder with a short demo GIF or video thumbnail. -->
![HUD demo](docs/images/hud-demo.gif)
