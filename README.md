WebXR Dimension Visualizer

A lightweight, single-file Augmented Reality (AR) web application that allows users to visualize real-world dimensions (Width, Height, Depth) in their physical space. Built with Three.js and the WebXR API, it works seamlessly across desktop browsers, Android devices, and iOS devices.

✨ Features

True WebXR AR (Android): Uses native WebXR device APIs to detect flat surfaces and place custom-dimensioned 3D boxes directly into your room.

Apple AR Quick Look (iOS): Automatically detects iOS Safari and dynamically generates .usdz files on the fly to trigger Apple's native AR viewer.

Desktop 3D Preview: Fallback 3D grid environment with orbital camera controls for users on desktop or unsupported devices.

Progressive Web App (PWA): Fully installable to your mobile device's home screen. Features custom SVG icons, manifest generation, and a standalone app-like experience—all generated dynamically without external assets.

Draggable & Collapsible UI: The floating input panel can be dragged around the screen or collapsed to prevent blocking the AR camera view.

Zero Dependencies: Everything is contained within a single index.html file, importing Three.js modules directly via CDNs.

🚀 How to Run

Because this app utilizes WebXR and native AR features, it must be served over a secure connection (HTTPS) or localhost. It will not work properly if you just double-click the HTML file (file:// protocol).

Option 1: Local Development Server (Recommended)

If you have Node.js, Python, or a VS Code Live Server extension installed:

Using Python:

Open a terminal in the folder containing index.html.

Run python -m http.server 8000 (Python 3) or python -m SimpleHTTPServer 8000 (Python 2).

Open http://localhost:8000 in your browser.

Using Node.js (npx):

Open a terminal in the folder.

Run npx serve .

Open the provided localhost link.

Option 2: Live Hosting

Simply upload index.html to any secure static hosting provider like GitHub Pages, Vercel, Netlify, or a standard web server with SSL enabled.

📱 Device Compatibility & Usage

On Android (Chrome)

Open the app.

Enter your desired Width, Height, and Depth in centimeters.

Tap START AR (appears at the bottom of the screen).

Point your camera at the floor and move it around slowly to detect planes.

Once a blue targeting ring appears, tap the screen to drop the object.

On iOS (Safari)

Open the app.

Enter your desired dimensions.

Tap the green View in AR button.

Apple's native AR Quick Look will open, allowing you to place and manipulate the object in your space.

On Desktop

Open the app in any modern browser.

Enter your desired dimensions.

Click Preview 3D to render the box on a virtual grid.

Click and drag to orbit the camera, scroll to zoom, and right-click to pan.

📥 PWA Installation

You can install this app directly to your mobile device for offline-like, full-screen access:

iOS: Tap the "Share" icon at the bottom of Safari, scroll down, and tap "Add to Home Screen".

Android: Tap the three-dot menu in the top right of Chrome and tap "Install App" or "Add to Home Screen".

🛠️ Technologies Used

HTML/CSS/JS: Core structure and logic.

Three.js (v160): 3D rendering engine, materials, and geometry.

WebXR API: For native browser AR session management.

USDZExporter: For converting Three.js meshes to iOS-compatible .usdz files on the fly.

📝 License

This project is open-source and free to use or modify.
