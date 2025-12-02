# Real-Time-Gesture-Controlled-Particle-Engine
A real-time, gesture-controlled 3D particle system using Three.js and MediaPipe. Morph shapes and control physics with hand movements in the browser
# 🌌 Kinetic Particle Interface

A touchless, interactive 3D particle simulation that morphs and reacts to hand gestures in real-time. Built with **Three.js** for high-performance rendering and **MediaPipe** for AI-powered hand tracking.

## ✨ Features

* **🖐️ Real-Time Hand Tracking:** Uses Computer Vision to detect hand landmarks instantly in the browser.
* **💠 Shape Morphing:** Seamlessly transition between mathematical forms (Heart, Sphere, Saturn, Galaxy, Fireworks).
* **📏 Gesture Scaling:** Move your hands apart to expand the universe; bring them closer to shrink it.
* **💥 Tension Physics:** Clench your fists to create "tension," causing particles to vibrate and explode chaotically.
* **🎨 Customization:** Modern UI to swap templates and adjust particle colors on the fly.

## 🕹️ Controls / How to Interact

Once the camera loads, the system tracks your hands:

| Gesture | Action |
| :--- | :--- |
| **Hands Apart / Together** | Controls the **Scale/Zoom** of the object. |
| **Clench Fist(s)** | Increases **Tension/Jitter** (Particles vibrate and scatter). |
| **Relax Hands** | Particles return to their smooth, ordered formation. |

## 🛠️ Tech Stack

* **Rendering:** [Three.js](https://threejs.org/) (WebGL)
* **Computer Vision:** [MediaPipe Hands](https://google.github.io/mediapipe/solutions/hands)
* **Language:** Vanilla JavaScript (ES6+)
* **Performance:** Uses `BufferGeometry` and `Float32Array` to handle 15,000+ particles at 60FPS.

## 🧠 Under the Hood

1.  **Particle System:** Instead of creating 15,000 individual objects, the system uses a single geometry object. Position data is updated directly in the memory buffer.
2.  **Morphing Logic:** The particles use Linear Interpolation (Lerp) to travel from their current coordinates to a mathematically calculated "Target" shape (e.g., Parametric Heart equations or Spiral Galaxy logic).
3.  **Interaction Math:** * *Scaling:* Calculated via Euclidean distance between the two wrist landmarks.
    * *Tension:* Calculated by measuring the distance between the wrist and the middle finger tip (normalized to detect a fist).

## ⬇️ Installation

This project is built with vanilla web technologies. No build step (npm/webpack) is required to run the basic version.

1.  **Clone the repo**
    ```bash
    git clone [https://github.com/yourusername/kinetic-particle-interface.git](https://github.com/yourusername/kinetic-particle-interface.git)
    ```

2.  **Run the file**
    * Simply open `index.html` in any modern browser (Chrome, Edge, Firefox).
    * *Note: For better performance or to avoid CORS issues with textures, it is recommended to use a local server (like Live Server in VS Code).*



*Created with ❤️ using Three.js and Computer Vision.*
