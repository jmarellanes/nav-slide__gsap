# GSAP Navigation - Slide Animation

A bold, high-impact navigation concept featuring a fluid typographic menu. The reveal sequence is orchestrated with a reversible GSAP Timeline, complete with directional line animations and snappy playback control.

## Overview

This project showcases a modern navigation system with advanced animations powered by **GSAP** (GreenSock Animation Platform). The menu system includes:

- **Reversible GSAP Timeline**: Play and reverse menu animations with smooth controls
- **Directional Line Animations**: Animated underlines and accent lines that respond to menu state
- **Fluid Typographic Menu**: Staggered text reveals with elegant transitions
- **Scroll-Lock Integration**: Prevents body scroll when menu is open
- **Responsive Design**: Adapts typography and layout to all screen sizes

## Features

✨ **Advanced Animations**

- GSAP timeline-based orchestration
- Reversible animations with play/pause control
- Smooth staggered transitions
- Power easing curves for natural motion

🎨 **Modern Design**

- Clean, elegant color palette
- Fluid menu overlay
- Responsive navigation layout
- Smooth typographic reveals

⚡ **Performance Optimized**

- Gulp-based build system
- Sass preprocessing for efficient styling
- Browser Sync for live reloading
- Minimal JavaScript footprint

🛠️ **Developer Experience**

- Babel transpilation for modern JavaScript
- Hot reloading with Browser Sync
- Module-based architecture
- Clean, maintainable code

## Tech Stack

- **Animation**: [GSAP](https://gsap.com/)
- **Build Tool**: [Gulp](https://gulpjs.com/) with Babel
- **CSS Preprocessing**: [Sass](https://sass-lang.com/)
- **Live Reload**: [Browser Sync](https://browsersync.io/)
- **Package Manager**: pnpm
- **Module System**: ES Modules

## Project Structure

```
.
├── index.html              # Main HTML entry point
├── js/
│   └── app.js             # GSAP timeline and event handlers
├── scss/
│   ├── _abstracts.scss    # Variables and mixins
│   ├── _base.scss         # Base styles and resets
│   ├── _components.scss   # Reusable components
│   ├── _layout.scss       # Layout grid and containers
│   ├── _partials.scss     # Partial styles
│   ├── _typography.scss   # Typography styles
│   ├── _variables.scss    # Design tokens and variables
│   └── app.scss           # Main stylesheet entry
├── css/
│   └── app.css            # Compiled CSS output
├── images/                # Project images and assets
├── gulpfile.babel.js      # Gulp task configuration
├── package.json           # Project dependencies
├── .babelrc              # Babel configuration
├── .prettierrc            # Code formatter configuration
└── pnpm-lock.yaml         # Dependency lock file
```

## Getting Started

### Prerequisites

- Node.js 14+ (recommended: 16 or higher)
- pnpm 6+ (or npm/yarn)

### Installation

1. Clone the repository:

```bash
git clone <repository-url>
cd gsap__nav-slide
```

2. Install dependencies:

```bash
pnpm install
```

### Development

Start the development server with live reloading:

```bash
pnpm start
```

This will:

- Watch for changes in SCSS files and recompile CSS
- Watch for JavaScript changes
- Launch Browser Sync for live reloading
- Serve the project at `http://localhost:3000` (or available port)

## Scripts

| Script       | Purpose                                            |
| ------------ | -------------------------------------------------- |
| `pnpm start` | Start development with Gulp watch and Browser Sync |

## How It Works

### Animation Flow

The project uses a single, reversible GSAP timeline to orchestrate the menu reveal sequence:

1. **Menu Overlay Appears**
   - Overlay fades into view
   - Creates a smooth entrance effect

2. **Navigation Items Reveal**
   - Menu links stagger in
   - Each item follows with a consistent delay

3. **Active Line Animation**
   - Animated underline reveals on the active menu item
   - Uses CSS custom properties for smooth animation

4. **Menu Interaction**
   - Timeline reverses on close
   - Smooth exit animation

### Key Components

**HTML** (`index.html`)

- Navbar with logo, site info, and burger menu toggle
- Full-screen overlay with menu items
- Active menu item with animated underline
- Semantic HTML structure

**SCSS** (`scss/`)

- `_variables.scss`: Design tokens and CSS custom properties
- `_components.scss`: Navigation and overlay styling
- `_base.scss`: Base styles and resets
- `_typography.scss`: Font and text styles
- `app.scss`: Main entry point that imports all partials

**JavaScript** (`js/app.js`)

- GSAP timeline for orchestrated animations
- Event listeners for burger menu toggle
- Class management for active states
- Reversible timeline using `reversed()` method

## Customization

### Menu Items

Edit the menu items in `index.html`:

```html
<div class="overlay">
  <div class="menu-item"><a href="#" class="active">Home</a></div>
  <div class="menu-item"><a href="#">About</a></div>
  <!-- Add more items as needed -->
</div>
```

### Colors & Design Tokens

Edit CSS variables in `scss/_variables.scss`:

```scss
// Update color variables, spacing, transitions, etc.
$primary-color: /* your color */;
$text-color: /* your color */;
$nav-scale: 1;
$line-width: 0%;
```

### Animations

Modify animation timing and easing in `js/app.js`:

- Duration values (in seconds)
- Stagger values
- Easing functions (e.g., `power4.inOut`, `power2.out`)
- Clip-path timing

## Browser Support

- Chrome/Edge: Latest versions
- Firefox: Latest versions
- Safari: Latest versions
- Mobile: Modern browsers with ES6 support

## Development Workflow

1. **Write Styles**: Create and modify SCSS files in `scss/`
2. **Watch Changes**: Files are automatically compiled to `css/app.css` via Gulp
3. **Live Reload**: Browser Sync automatically refreshes on file changes
4. **JavaScript Updates**: Modify `js/app.js` and refresh browser

## Troubleshooting

**Menu not animating?**

- Check browser console for JavaScript errors
- Ensure GSAP is properly imported
- Verify DOM element selectors match the HTML structure
- Clear browser cache and hard refresh

**Styles not updating?**

- Verify Gulp is running: `pnpm start`
- Check for SCSS syntax errors in the terminal
- Ensure CSS file is linked in `index.html`
- Check that SCSS files are in the `scss/` directory

**Build issues?**

- Clear node_modules: `rm -rf node_modules && pnpm install`
- Check Node.js version: `node --version` (should be 14+)
- Verify Gulp is installed: `npx gulp --version`

**Browser Sync not working?**

- Check if port 3000 is already in use
- Try closing other applications using the port
- Restart the dev server: `pnpm start`

## License

This project is licensed under the ISC License - see the [LICENSE](LICENSE) file for details.

Copyright (c) 2026 José Manuel Díaz

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Contact

For questions or feedback about this project, please reach out to the author.

---

**Last Updated**: April 2026
