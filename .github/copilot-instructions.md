# JDVP Portfolio - Copilot Instructions

## Project Overview
Personal portfolio website for **Mark Gian Jacob** using a **Mecha Cyberpunk** theme with neon aesthetics, glassmorphism, and futuristic design elements. Static HTML/CSS project served via XAMPP.

## Architecture

### File Structure
```
├── index.html      # Main landing page with hero section
├── style.css       # All styles (CSS variables, animations, responsive)
├── profile.jpg     # Profile image (hexagonal frame display)
└── .github/        # GitHub configuration
```

### Design System (style.css)
- **CSS Variables** defined in `:root` - always use these for colors/fonts
- **Core colors**: `--neon-cyan: #00f3ff` (primary accent), `--bg-dark: #030810`
- **Fonts**: `Orbitron` (display/headings), `Rajdhani` (body text)
- **Glass panels**: Use `.glass-panel` class for frosted glass effect

## Styling Conventions

### Component Patterns
```css
/* Buttons use clip-path for angular mecha style */
.btn-cyber {
    clip-path: polygon(0 0, calc(100% - 10px) 0, 100% 10px, 100% 100%, 10px 100%, 0 calc(100% - 10px));
}

/* Neon glow effect for accent elements */
.neon-text {
    text-shadow: 0 0 5px var(--neon-cyan), 0 0 10px var(--neon-cyan), 0 0 20px var(--neon-cyan);
}
```

### Animation Naming
- `orbPulse`, `glowPulse` - pulsing/breathing effects
- `textFlicker` - neon sign flickering
- `floatAround` - floating decorative elements
- `gridMove` - background grid animation

### HTML Structure Patterns
- Background effects: Place at top of `<body>` (`.cyber-grid`, `.scanlines`, `.neon-orb`)
- Mecha frames: Corner decorations using `.mecha-frame` with position classes
- Glass panels: Wrap content sections in `.glass-panel` for consistent styling

## Key Conventions

1. **Color changes**: Only modify CSS variables in `:root`, never hardcode colors
2. **New sections**: Follow existing pattern - wrap in `.glass-panel`, use `.neon-text` for accents
3. **Responsive**: Breakpoints at `900px` and `600px` - check both when adding content
4. **Profile image**: Hexagonal frame auto-displays placeholder if image fails to load
5. **Font usage**: `var(--font-display)` for headings/labels, `var(--font-body)` for paragraphs

## Local Development
- **Server**: XAMPP Apache (access via `http://localhost/JDVP%20Portfolio%20Jacob/`)
- **No build step**: Edit HTML/CSS directly, refresh browser to see changes
- **Browser**: Test in Chrome/Edge for best `backdrop-filter` support
