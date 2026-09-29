# Parallax Scroll Animation

A scroll-driven landing page built with vanilla HTML, CSS, and JavaScript, animated with [GSAP](https://gsap.com/) and ScrollTrigger. A 3D sphere of image cards rotates as you scroll, captions change with scroll progress, and a closing section adds a parallax card layout. The UI uses a dark, clay-style design.

**[Live Demo](https://parallax-scroll-animation-two.vercel.app)**

---

## Features

- **3D image sphere** — cards are distributed evenly on a sphere (Fibonacci layout) using CSS 3D transforms.
- **Scroll-scrubbed rotation** — GSAP ScrollTrigger ties the sphere's rotation directly to scroll position.
- **Dynamic captions** — title and description cross-fade as you scroll.
- **Focus highlighting** — cards near the active position switch from muted grayscale to full color.
- **Parallax card scatter** — floating cards drift at different speeds in the closing section.
- **Clay-style UI** — soft inset shadows, chunky buttons, and a subtle grid overlay.
- **Responsive** — layout and sphere size adapt on smaller screens.
- **No build step** — GSAP and ScrollTrigger are bundled locally, so the project runs without npm or a bundler.

## Tech Stack

- HTML5
- CSS3 (custom properties, 3D transforms, layered shadows)
- Vanilla JavaScript (ES6)
- GSAP + ScrollTrigger

## Project Structure

```
.
├── index.html          # Page markup
├── style.css           # Styles and design tokens
├── script.js           # Sphere generation and scroll animations
├── gsap.js             # GSAP library (local copy)
├── ScrollTrigger.js    # GSAP ScrollTrigger plugin (local copy)
├── LICENSE
└── README.md
```

## Getting Started

No installation is required.

**Open directly**

Open `index.html` in a modern browser.

**Or run a local server (recommended)**

```bash
# Clone the repository
git clone https://github.com/asad-developer99/parallax-scroll-animation.git
cd parallax-scroll-animation

# Python
python3 -m http.server 8000

# or Node
npx serve .
```

Then visit `http://localhost:8000`.

> Card images may be loaded from external URLs, so an internet connection is needed to see them.

## Customization

- **Images and captions** — edit the image list and caption data at the top of `script.js`.
- **Sphere size and card count** — adjust the `radius` value and the number of cards in `script.js`.
- **Rotation amount** — change the rotation values in the ScrollTrigger tween.
- **Theme** — colors, shadows, and spacing are defined as CSS variables in `:root` in `style.css`.

## Deployment

The project is a static site and can be deployed to any static host. The live demo runs on [Vercel](https://vercel.com/). To deploy your own copy:

1. Push the repository to GitHub.
2. Import it in Vercel (or enable GitHub Pages under **Settings → Pages**).
3. No build command or output directory is needed.

## Browser Support

Works in current versions of Chrome, Edge, Firefox, and Safari. The 3D effects rely on `transform-style: preserve-3d`, `position: sticky`, and `backdrop-filter`, which older browsers may not support.

## Contributing

Suggestions and improvements are welcome. Fork the repository, create a feature branch, and open a pull request.

## License

Released under the [MIT License](LICENSE).
