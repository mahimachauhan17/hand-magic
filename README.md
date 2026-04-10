# 🎭 Hand Magic - Advanced Hand Tracking AR

An immersive real-time hand tracking augmented reality experience with neon effects, gesture detection, and interactive audio feedback.

## ✨ Features

### 🖐️ Hand Tracking
- Real-time hand detection using **MediaPipe Hands**
- Support for dual hand tracking
- Skeleton visualization with neon glow effects
- Fingertip detection and particle effects

### 🎨 Visual Effects
- **Multiple Theme Modes:**
  - 🌈 Rainbow - Vibrant multi-color gradients
  - 🔴 Cyberpunk - Neon red and cyan colors
  - 🔥 Lava - Warm orange and red tones
  - 🌊 Ocean - Cool blue and cyan hues
  - 🌌 Galaxy - Purple and violet cosmos theme

- **Particle System:**
  - White glittery magic particles at fingertips
  - Dynamic beam particles connecting hands
  - Shockwave ripples on pinch gestures
  - Motion blur and gravity physics

- **Matrix Rain Background:**
  - Animated matrix-style falling characters
  - Speed-responsive to hand movement
  - Screen-blended neon bloom effects

### 🎯 Gesture Recognition
- **Pinch Detection** - Thumb and index finger proximity
- **Hand Spread** - Open hand vs. closed fist detection
- **Cross-Hand Lightning** - Electric arc effects when hands approach
- **Mandala Drawing** - Geometric patterns connecting all fingertips

### 🔊 Audio Engine
- Continuous harmonic hum modulated by hand distance
- Zap sound effects on pinch gestures
- Frequency and volume respond to hand proximity
- Web Audio API integration

### 📊 Real-Time HUD
- Hand detection counter
- FPS monitor
- Current gesture display
- Hand spread percentage

## 🚀 Getting Started

### Requirements
- Modern web browser with webcam support
- Camera permissions enabled
- Internet connection (CDN dependencies)

### Running the Project

**Option 1: Using Python HTTP Server**
```bash
python -m http.server 8000 --directory "path/to/Hand magic"
```
Then open `http://localhost:8000/text.html` in your browser.

**Option 2: Using Node.js HTTP Server**
```bash
npx http-server "path/to/Hand magic" -p 8000
```

**Option 3: Direct File Access**
Simply open `text.html` in your web browser (limited functionality may apply).

## 🎮 How to Use

1. **Grant Permissions**: Click "Enter Experience" and allow camera access
2. **Calibrate**: Let the app detect your hands (show both palms to camera)
3. **Interact:**
   - Move your hands freely to see neon trails
   - Bring hands close together for magical beam effects
   - Pinch your fingers (thumb + index) for shockwave effects
   - Open and close hands to see gesture recognition
4. **Switch Themes**: Click theme buttons at the bottom center to change colors

## 🎛️ Controls

| Action | Effect |
|--------|--------|
| Show Hands | Start tracking |
| Move Hands | Create particle trails |
| Bring Hands Close | Generate beam particles |
| Pinch (Thumb + Index) | Trigger shockwave & zap sound |
| Open/Close Hand | Toggle open hand/fist gesture |
| Theme Buttons | Change visual theme |

## 🏗️ Architecture

### Core Components
- **MediaPipe Hands**: Hand detection and landmark tracking
- **Canvas Rendering**: Dual-canvas system (background + effects)
- **Physics Engine**: Particle system with gravity and velocity
- **Audio Context**: Web Audio API for sound synthesis
- **Theme System**: Dynamic color configuration

### Technical Stack
- Pure JavaScript (No frameworks)
- HTML5 Canvas for rendering
- Web Audio API
- MediaPipe ML Kit
- CSS Grid & Flexbox for UI

## 📁 File Structure

```
Hand magic/
├── text.html       # Single-file application
└── README.md       # This file
```

## 🎨 Customization

### Add New Themes
Edit the `themes` object in the script section:
```javascript
const themes = {
    'MyTheme': (t, index, total) => `hsl(${color}, saturation%, lightness%)`
};
```

### Adjust Particle Behavior
Modify in `createMagicGlitter()` function:
- `count` - Number of particles per spawn
- `size` - Particle radius
- `life` - Fade-out speed

### Change Audio Frequencies
Edit in `initAudio()` function:
- `humOsc.frequency.value` - Base hum frequency
- Modify frequency ranges in `updateHum()`

## ⚙️ Browser Compatibility

| Browser | Status |
|---------|--------|
| Chrome/Chromium | ✅ Fully Supported |
| Firefox | ✅ Fully Supported |
| Safari | ⚠️ Limited (iOS requires special setup) |
| Edge | ✅ Fully Supported |

## 📦 Dependencies

All dependencies are loaded via CDN:
- [@mediapipe/hands](https://mediapipe.dev) - Hand tracking
- [@mediapipe/camera_utils](https://mediapipe.dev) - Camera handling
- [@mediapipe/drawing_utils](https://mediapipe.dev) - Utility functions
- [@mediapipe/control_utils](https://mediapipe.dev) - UI controls

## 🐛 Troubleshooting

**Camera not working:**
- Check browser permissions for camera access
- Ensure no other app is using the camera
- Try a different browser

**Low FPS/Performance:**
- Close other applications
- Reduce browser tabs
- Move your webcam to a well-lit area
- Lower background complexity in UI

**No hand detection:**
- Ensure adequate lighting
- Position hands clearly in frame
- Move hands slowly for best tracking
- Keep hands fully visible

**Audio not playing:**
- Check system volume
- Verify Web Audio API support in browser
- Ensure page loaded successfully (check console)

## 🎓 Learning Resources

- [MediaPipe Documentation](https://mediapipe.dev)
- [Web Audio API Guide](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API)
- [Canvas API Reference](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)
- [Gesture Recognition Techniques](https://en.wikipedia.org/wiki/Gesture_recognition)

## 📝 License

This project is open source and available for personal and educational use.

## 🤝 Contributing

Feel free to fork, modify, and enhance this project!

Suggested improvements:
- Add more gesture types (swipe, grab, pointing)
- Create additional visual themes
- Implement recording/export functionality
- Add hand tracking statistics
- Optimize performance further

## 📧 Support

For issues or questions, please check:
1. Browser console for error messages
2. Troubleshooting section above
3. MediaPipe documentation

---

