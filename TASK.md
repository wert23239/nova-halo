# Nova Halo - WebGL Ring Effect

Build a single-page web app called "Nova Halo" that renders a WebGL ring/halo effect with a controls panel.

## Visual Effect
- Dark/black background filling the entire viewport
- A glowing ring/halo in the center of the screen
- The ring should have 4-layer composition with:
  - Simplex noise edge breathing (organic wobbly edges)
  - Orbiting highlight (a bright spot that moves around the ring)
  - Gradient colors flowing through the ring
  - Glow/bloom effect around the ring
- The ring colors should blend between Color A (primary), Color B (secondary), with Color C as shadow
- Default colors: Color A = #ffd700 (gold/yellow), Color B = #9400d3 (purple), Color C = #260d33 (dark purple)

## Controls Panel (right side)
Dark semi-transparent panel with rounded corners containing:

### PALETTES section
- Row of ~10 clickable color palette circles (each a gradient of 2 colors)
- Palettes should include various combos: blue/cyan, green/yellow, red/orange, pink/magenta, purple/blue, cyan/white, etc.
- Clicking a palette updates Color A, B, C accordingly

### COLORS section
- Color A (Primary) - color swatch + hex input (#ffd700)
- Color B (Secondary) - color swatch + hex input (#9400d3)  
- Color C (Shadow) - color swatch + hex input (#260d33)
- Each should have a clickable color picker

### PARAMETERS section (sliders)
- Hue Shift (0-360, default ~0)
- Edge Density (0-500, default 263)
- Flow Speed (0-2, default 0.66)
- Breathing (0-1, default 0.56)
- Hover Distortion (0-1, default 0.30)
- A 6th slider below (0-1, default 0.26)

## Mouse Interaction
- Hovering near the ring should cause distortion (controlled by Hover Distortion parameter)

## Tech
- Single index.html file with inline CSS and JS
- Use WebGL shaders for the ring effect
- Use simplex noise (can inline a simplex noise GLSL function)
- No build tools, no frameworks - pure HTML/CSS/JS/WebGL
- Must look polished and production-ready

## Header
- Top-left: "Reference" label, then "Nova Halo" in green text
- Below: description "WebGL ring effect with 4-layer composition, simplex noise edge breathing, and orbiting highlight. Ported from Framer AI halo-glow component."

## Deploy
- Create a simple Express server (server.js) that serves index.html
- Create package.json with express dependency
- Create render.yaml for Render deployment (web service, node environment)

When completely finished, run: openclaw system event --text "Done: Nova Halo WebGL ring effect built and ready for Render deploy" --mode now
