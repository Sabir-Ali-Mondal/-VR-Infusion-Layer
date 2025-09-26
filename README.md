# 🥽 VR Infusion Layer (VIL)

**Transform any website into an immersive VR experience with a single click**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![A-Frame](https://img.shields.io/badge/A--Frame-1.4.0-FF3333)](https://aframe.io)
[![WebXR](https://img.shields.io/badge/WebXR-Compatible-00FFFF)](https://immersiveweb.dev)
[![Bundle Size](https://img.shields.io/badge/Bundle%20Size-<50KB-brightgreen)]()

> A revolutionary lightweight JavaScript library that adds immersive VR navigation to any existing website. No complex setup, no framework dependencies - just drop in and experience the future of web browsing.

[View Demo](https://your-demo-url.com) • [Report Bug](https://github.com/username/vr-infusion-layer/issues) • [Request Feature](https://github.com/username/vr-infusion-layer/issues)

---

## ✨ Features

- 🚀 **Lightweight** - Under 50KB total footprint with intelligent lazy loading
- 🔧 **Zero Configuration** - Works out-of-the-box by auto-detecting navigation links
- 🎨 **Brand Adaptive** - Automatically inherits your site's colors and branding
- 📱 **Universal Support** - Compatible with VR headsets, mobile devices, and desktop browsers
- ⚡ **High Performance** - Optimized for 60+ FPS with geometry instancing and texture optimization
- 🌐 **WebXR Ready** - Full support for modern WebXR standards with graceful fallbacks
- 🎭 **Professional UI** - Sci-fi inspired interface with glass morphism and neon effects
- 🔄 **Smooth Transitions** - Cinematic animations between 2D and VR modes

## 🚀 Quick Start

### Installation

Simply add these two script tags before your closing `</body>` tag:

```
<!-- A-Frame CDN -->
<script src="https://aframe.io/releases/1.4.0/aframe.min.js"></script>

<!-- VR Infusion Layer -->
<script src="path-to/vr-infusion-layer.js"></script>

<script>
document.addEventListener('DOMContentLoaded', () => {
    new VRInfusionLayer({
        accentColor: '#00ffff',
        welcomeMessage: 'Welcome to VR Hub'
    });
});
</script>
```

That's it! Your website now has VR navigation capabilities.

### Basic Usage

The VIL automatically detects navigation links in your HTML:

```
<nav>
    <a href="/about" data-vr-title="About Us" data-vr-description="Learn about our company">About</a>
    <a href="/products" data-vr-title="Products" data-vr-description="Explore our product line">Products</a>
    <a href="/contact" data-vr-title="Contact" data-vr-description="Get in touch with us">Contact</a>
</nav>
```

## 🛠️ Configuration

### Basic Configuration

```
new VRInfusionLayer({
    accentColor: '#00ffff',           // Primary accent color
    welcomeMessage: 'VR Nexus Hub',   // Welcome text in VR
    linkSelector: 'nav a, .main-nav a', // CSS selector for links
    maxPortals: 8,                    // Maximum number of portals
    minLinks: 2                       // Minimum links required
});
```

### Advanced Configuration

```
new VRInfusionLayer({
    // Visual Settings
    accentColor: '#00ffff',
    backgroundType: 'starfield',      // 'starfield', 'gradient', 'solid'
    platformStyle: 'glow',            // 'glow', 'minimal', 'tech'
    
    // Performance Settings
    starCount: 200,                   // Number of background stars
    portalAnimations: true,           // Enable portal hover effects
    
    // Interaction Settings
    gazeTimeout: 1500,                // MS before gaze selection
    transitionDuration: 800,          // MS for scene transitions
    
    // Responsive Settings
    mobileOptimized: true,            // Enable mobile optimizations
    vr Headset Support: true          // Enable VR headset features
});
```

### Data Attributes

Enhance your links with VR-specific metadata:

```
<a href="/page" 
   data-vr-title="Custom VR Title"
   data-vr-description="Detailed description shown in VR"
   data-vr-portal="true">
   Link Text
</a>
```

## 🎮 User Experience

### Desktop
- Mouse to look around the VR environment
- Click on portals to navigate
- Keyboard shortcuts: ESC (exit), H (help)

### VR Headsets
- Natural head tracking for navigation
- Gaze-based portal selection
- Controller trigger for activation

### Mobile Devices  
- Touch and drag to explore
- Tap portals to navigate
- Optimized performance for mobile GPUs

## 📱 Browser Support

| Browser | Desktop | Mobile | VR Support |
|---------|---------|--------|------------|
| Chrome | ✅ | ✅ | ✅ |
| Firefox | ✅ | ✅ | ✅ |
| Safari | ✅ | ✅ | ❌ |
| Edge | ✅ | ✅ | ✅ |

## 🏗️ Architecture

### Core Components

- **VRInfusionLayer Class** - Main library controller
- **Portal Generator** - Dynamic 3D portal creation system  
- **Environment Engine** - Starfield and lighting system
- **Interaction Handler** - Cross-platform input management
- **Transition Manager** - Smooth 2D/VR mode switching

### Performance Optimizations

- Geometry instancing for repeated elements
- Texture atlasing for reduced draw calls
- Selective rendering based on user view
- Dynamic LOD (Level of Detail) system
- Memory management for large scenes

## 🔧 Development

### Prerequisites

- Modern web browser with WebXR support
- Basic HTML/CSS/JavaScript knowledge
- Optional: VR headset for testing

### Local Development

1. Clone the repository
```
git clone https://github.com/username/vr-infusion-layer.git
cd vr-infusion-layer
```

2. Open the demo file
```
open demo/index.html
# or serve with any local server
python -m http.server 8000
```

3. Test VR functionality
- Click the VR button in bottom-right
- Use mouse/keyboard for desktop testing
- Connect VR headset for full experience

### Build Process

```
# Install dependencies
npm install

# Build minified version
npm run build

# Run tests
npm run test

# Start development server
npm run dev
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

### Development Guidelines

1. Follow the existing code style
2. Add tests for new features
3. Update documentation for API changes
4. Test across multiple browsers and devices

### Reporting Issues

When reporting issues, please include:
- Browser and version
- Device type (desktop/mobile/VR headset)
- Steps to reproduce
- Expected vs actual behavior
- Console errors (if any)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [A-Frame](https://aframe.io) - WebVR framework
- [WebXR Device API](https://immersiveweb.dev) - VR standards
- [Three.js](https://threejs.org) - 3D graphics library
