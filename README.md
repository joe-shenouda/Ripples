
# Ripples

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Stars](https://img.shields.io/github/stars/joe-shenouda/Ripples.svg)](https://github.com/joe-shenouda/Ripples/stargazers)
[![Forks](https://img.shields.io/github/forks/joe-shenouda/Ripples.svg)](https://github.com/joe-shenouda/Ripples/network/members)

## Table of Contents
- [About](#about)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Customization](#customization)
  - [Modifying Colors](#modifying-colors)
  - [Adjusting Ripple Speed and Duration](#adjusting-ripple-speed-and-duration)
  - [Adding More Ripples](#adding-more-ripples)
- [Screenshots](#screenshots)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)
- [Contact](#contact)

## About

Ripples is an interactive WebGL-based visualization project that creates stunning ripple effects in response to user interactions. This project leverages GLSL shaders to render complex and beautiful patterns that react dynamically to mouse movements and clicks. The goal is to provide an aesthetically pleasing and highly responsive visual experience.

## Features

- **Interactive Ripples**: Real-time ripple effects that respond to mouse movements and clicks.
- **Advanced Shaders**: Utilizes GLSL shaders for complex and beautiful visual effects.
- **Customizable**: Easy to modify colors, speeds, and other parameters.
- **High Performance**: Optimized for smooth performance across different devices.

## Installation

### Prerequisites

- A modern web browser that supports WebGL.
- Node.js and npm installed on your machine (for development).

### Steps

1. Clone the repository:
    ```sh
    git clone https://github.com/joe-shenouda/Ripples.git
    cd Ripples
    ```

2. Open `index.html` in your web browser to view the ripples effect.

## Usage

Simply open the `index.html` file in a WebGL-compatible browser. Move your mouse around the screen to see the ripples interact with your cursor. Click to generate additional ripple effects.

## Customization

### Modifying Colors

You can change the color palette by editing the `palette` function in the fragment shader (`index.html`):
```glsl
vec3 palette(float t) {
    return mix(vec3(0.3, 0.1, 0.4), vec3(1.0, 0.8, 0.5), abs(sin(t * 6.28318)));
}
```

### Adjusting Ripple Speed and Duration

Modify the `ripple` function in the fragment shader:
```glsl
float rippleSpeed = 0.1; // Slow down the ripple expansion
float rippleRadius = t * rippleSpeed; // Adjust the radius based on time
```

### Adding More Ripples

Increase the number of clicks tracked by adjusting the arrays in the JavaScript section:
```javascript
let clicks = [];
let clickTimes = [];
const maxClicks = 20; // Increase from 10 to 20
```

## Screenshots



## Contributing

Contributions are welcome! 

## License

Distributed under the MIT License. See `LICENSE` for more information.

## Acknowledgements

- [Three.js](https://threejs.org/) - JavaScript 3D library
- [GLSL Sandbox](http://glslsandbox.com/) - Inspiration for shader effects
- [WebGL Fundamentals](https://webglfundamentals.org/) - Tutorials on WebGL

## Contact

Joe Shenouda - [@joe-shenouda](https://github.com/joe-shenouda)

Project Link: [https://github.com/joe-shenouda/Ripples](https://github.com/joe-shenouda/Ripples)

---
