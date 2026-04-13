# World Builder

**DE 722 — Computational Thinking in Design | Final Project Proposal**
**Spring 2025-26**

📍 **GitHub Repository:** [yuvraj-iitb/world-builder](https://github.com/yuvraj-iitb/world-builder)

---

## Concept

World Builder is a 2D fantasy map generator built in Processing (Java). It combines procedural generation with interactive drawing tools to let users craft rich, detailed world maps — from continents and coastlines down to rivers, roads, and settlements.

The goal is to create a flexible cartography tool that can serve a wide range of creative needs: designing campaign maps for tabletop RPGs, prototyping game worlds, generating decorative maps to print and hang on a wall, or simply exploring procedurally generated landscapes for fun.

## Aesthetic Direction

The visual language draws from **80s arcade games** and **early 2000s PC titles** — chunky pixels, limited color palettes, and clean tile-based rendering. Think of the overworld maps from classic RPGs or the terrain views of early strategy games.

Key principles:
- **Low-resolution, high-character** — pixel art style with deliberate constraints on resolution and color
- **Vintage palette** — muted, CRT-inspired tones with optional palette swaps (e.g., parchment, neon, monochrome green)
- **Performance-first** — lightweight rendering that runs smoothly even on modest hardware
- **Readable at a glance** — distinct, iconic tile graphics so terrain types are immediately identifiable

## Core Features

### Procedural Terrain Generation
- Perlin noise-based elevation and moisture maps to generate realistic landmasses
- Multiple biome types derived from elevation and climate: **ocean, coast, plains, forest, dense forest, desert, savanna, swamp/marsh, mountains, snow peaks, tundra, volcanic**
- Adjustable world parameters (sea level, continent size, terrain roughness, biome distribution)

### Interactive Drawing Tools
- **Shape drawing** — draw freeform shapes on the canvas that convert into landmasses or bodies of water (lakes, inland seas)
- **Line drawing** — trace paths that become rivers, roads, trade routes, or borders
- **Brush tools** — paint terrain types directly onto the map to override or refine generated results
- **Eraser/undo** — non-destructive editing with full undo history

### Terrain and Environment
- Terrain type selector with a full tile palette
- Elevation visualization (contour lines, color gradients, or heightmap overlay)
- Temperature and moisture gradients influencing biome placement

### Weather Systems
- Regional weather overlays: rain, snow, fog, sandstorms, thunderstorms
- Weather as visual markers on the map (hatching, animated particles, or icon overlays)
- Optional: weather influence on terrain appearance (snow accumulation, flooding)

### Flora and Fauna
- Biome-appropriate vegetation placement (trees, shrubs, cacti, coral, mushrooms)
- Fauna markers tied to habitat (forest creatures, desert dwellers, sea life, mountain beasts)
- Density and variety controls per region
- Optional: mythical/fantasy creature placement for worldbuilding flavor

### Export and Save
- Save/load world state for continued editing
- Export as image (PNG) for printing or sharing
- Print-ready export options with configurable resolution and paper sizes

## Expanded Feature Ideas

These are stretch goals and possibilities being explored for the project scope:

### Settlements and Civilization
- Procedural placement of villages, towns, and cities based on terrain suitability (near water, on trade routes, at resource-rich locations)
- Auto-generated settlement names using syllable-based or markov-chain name generators
- Visual indicators for settlement size and type (hamlet, village, town, city, capital)

### Map Legend and Annotations
- Auto-generated legend/key showing all terrain types and symbols present on the map
- Text annotation tool for labeling regions, landmarks, and points of interest
- Cartographic embellishments (compass rose, scale bar, decorative borders)

### Zoom and Detail Levels
- Multi-scale viewing: world overview, regional zoom, local detail
- Each zoom level could reveal additional detail (world map shows biomes; regional shows individual trees and buildings)

### Seed-Based Generation
- Numeric seed input for reproducible world generation
- Share seeds to let others explore the same world
- Seed history/bookmarking

### Time and Atmosphere
- Day/night cycle toggle affecting palette and mood
- Seasonal variation (summer greenery, autumn colors, winter snow cover, spring bloom)
- Atmospheric effects (mist, heat shimmer, aurora)

### Territory and Borders
- Draw political boundaries and territory regions
- Color-coded factions or kingdoms
- Border dispute/overlap visualization

### Exploration Mode
- Fog of war that reveals the map as you "explore" it
- Click-to-reveal or path-based unveiling
- Could serve as a DM tool for tabletop sessions — reveal areas to players as they travel

### Advanced Export
- Tiled export for large-format printing (split across multiple pages)
- Layered export (terrain only, labels only, etc.)
- Animated GIF export of generation process

## Technical Approach

| Component | Approach |
|---|---|
| **Platform** | Processing 4 (Java-based) |
| **Rendering** | Tile-based grid with pixel art sprites |
| **Terrain generation** | Perlin/Simplex noise for elevation + moisture maps |
| **Biome assignment** | Whittaker diagram-style mapping (temperature x moisture) |
| **Drawing input** | Processing mouse/keyboard event handling |
| **Data structure** | 2D grid array storing terrain type, elevation, metadata per cell |
| **Save format** | JSON or binary serialization of world grid |
| **Export** | Processing's built-in `save()` for PNG output |

## Status

> **This project is currently in the proposal stage.** The ideas outlined above represent the intended direction and feature possibilities. The scope will be refined as development progresses. Core terrain generation and drawing tools are the priority; expanded features will be implemented as time allows.

---

*World Builder — DE 722 Final Project Proposal*
