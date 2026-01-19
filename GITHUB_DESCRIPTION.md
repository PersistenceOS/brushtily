# Brushtily - Professional Texture Painting Extension for Tiled

**Transform Tiled into a powerful terrain painting tool with Inkarnate-inspired freeform brushing and object stamping capabilities.**

Brushtily is a powerful plugin bridging freeform brushing into Tiled with easy object placement. This comprehensive JavaScript extension brings professional-grade texture painting features to Tiled Map Editor, enabling artists and level designers to create beautiful, organic terrain and textures with smooth, non-grid-aligned brush strokes.

---

## 🎨 Core Features

### **Freeform Texture Painting**
- **Non-grid-aligned brush strokes** - Paint naturally without being constrained to tile grids
- **Auto-smoothing brush layers** - Automatically smooths brush strokes to remove hard edges for natural, organic results
- **Native layer blending** - Native layer blending for natural appearances and seamless layer integration
- **Smooth continuous painting** - Real-time stroke rendering with optimized performance
- **Dual layer support** - Works seamlessly on ImageLayer (immediate visual feedback) and ObjectGroup (full undo support)

### **Custom Brush System**
- **Image-based brushes** - Load any PNG/JPG image as a brush texture
- **Tileset tile brushes** - Use tiles from your tilesets directly as brush textures
- **Multiple brush shapes** - Choose from Circular, Square, Ellipse, or Diamond brush shapes
- **Layer brush memory** - Automatically remembers your brush texture per layer for seamless workflow

### **Advanced Brush Properties**
- **Brush Size** (10-500 pixels) - Adjustable brush diameter
- **Opacity** (0-100%) - Control transparency of brush strokes
- **Softness** (0-100%) - Edge feathering for smooth, natural transitions
- **Texture Scale** (10-200%) - Scale texture independently from brush size
- **Rotation** (0-360°) - Rotate brush texture to any angle
- **Rotation Jitter** (0-360°) - Random rotation variation for organic, natural-looking strokes
- **Position Jitter** (0-100) - Add random position variation to prevent repetitive patterns
- **Spacing** (percentage) - Control distance between brush stamps for varied stroke density

### **Professional Blend Modes**
- **Normal, Multiply, Screen, Overlay, Darken, Lighten** - Full blend mode support for advanced compositing
- **Mask Modes** - Add, Subtract, or Multiply modes for precise control over how brushes interact with existing content

### **Pressure Sensitivity Simulation**
- **Velocity-based pressure** - Simulates pressure sensitivity based on brush stroke velocity
- **Pressure affects size** - Faster strokes create smaller, lighter marks
- **Pressure affects opacity** - Natural opacity variation based on stroke speed
- Creates organic, hand-drawn feel without requiring pressure-sensitive hardware

### **Fill & Erase Tools**
- **Bucket Fill Mode** - Fill areas with color tolerance control
- **Right-click erase** - Right-click and drag to erase painted areas with independent erase brush (separate size and softness controls)
- **Smart erase** - Maintains original image backup for precise erasing
- **Auto-smoothing** - Automatically removes hard edges for seamless blending
- **Native layer blending** - Native layer blending for natural appearances and seamless integration between layers

### **Object Stamping System**
- **Drag-to-stamp workflow** - Paint objects by dragging (similar to Inkarnate's stamp tool)
- **Object Library Browser** - Visual browser with thumbnails, categories, and search
- **Automatic object placement** - Places objects along brush stroke path
- **Random variation** - Optional rotation and scale variation for natural object placement
- **Folder-based organization** - Automatically categorizes objects by folder structure

### **Brush Presets & Workflow**
- **Save & load presets** - Save your favorite brush configurations
- **Preset management** - Organize and quickly switch between brush setups
- **Persistent settings** - Brush settings persist across Tiled sessions

---

## 🚀 Key Advantages

### **Professional Workflow**
- **No grid constraints** - Paint freely without tile alignment restrictions
- **Smooth performance** - Optimized rendering with point density limiting and update throttling
- **Real-time feedback** - See your strokes immediately as you paint
- **Layer-aware** - Remembers brush settings per layer automatically

### **Versatile Painting Modes**
- **Texture painting** - Create terrain, textures, and backgrounds
- **Object stamping** - Quickly populate maps with trees, buildings, decorations
- **Mask painting** - Use subtract/multiply modes for advanced compositing
- **Fill painting** - Quick area fills with tolerance control

### **Artist-Friendly Features**
- **Natural brush behavior** - Pressure simulation creates organic strokes
- **Jitter & variation** - Prevent repetitive patterns with rotation and position jitter
- **Multiple brush sources** - Use images or tileset tiles as brushes
- **Professional blend modes** - Full compositing control

---

## 📋 Technical Specifications

- **Platform**: Tiled Map Editor 1.8+
- **Language**: JavaScript (ES Module)
- **File Format**: `.mjs` extension
- **Layer Support**: ImageLayer, ObjectGroup
- **Performance**: Optimized with throttling and point limiting
- **Compatibility**: Windows, macOS, Linux

---

## 🎯 Use Cases

- **Terrain painting** - Create natural-looking terrain with organic brush strokes
- **Texture blending** - Blend multiple textures seamlessly with blend modes
- **Map decoration** - Quickly stamp objects (trees, rocks, buildings) across maps
- **Background creation** - Paint custom backgrounds and atmospheres
- **Mask creation** - Use subtract/multiply modes for advanced map compositing
- **Art asset creation** - Generate textures and patterns directly in Tiled

---

## 💡 What Makes Brushtily Special

Unlike basic tile placement tools, Brushtily brings **professional digital painting capabilities** to Tiled:

1. **Freeform painting** - Not limited to grid-based tile placement
2. **Natural brush behavior** - Pressure simulation and jitter create organic results
3. **Advanced compositing** - Blend modes and mask modes for professional results
4. **Dual workflow** - Both texture painting and object stamping in one tool
5. **Layer intelligence** - Remembers settings per layer automatically
6. **Performance optimized** - Smooth painting even on large maps

---

## 🔧 Installation

1. Copy `brushtily.mjs` to your Tiled extensions folder:
   - **Windows**: `%LOCALAPPDATA%\Tiled\extensions\`
   - **macOS**: `~/Library/Preferences/Tiled/extensions/`
   - **Linux**: `~/.config/tiled/extensions/`

2. Restart Tiled (or extension auto-reloads on file change)

3. Find "Brushtily" in the Tools toolbar

---

## 📝 Requirements

- **Tiled 1.8 or later** (JavaScript extensions support required)
- JavaScript extensions enabled (default in Tiled)

---

## 🎨 Perfect For

- Game developers creating terrain and maps
- Level designers needing organic texture painting
- Artists working in Tiled who want digital painting tools
- Anyone who wants Inkarnate-inspired freeform brushing and object stamping in Tiled

---

## ⚠️ Known Limitations & Issues

### Limitations
- ImageLayer painting has no undo support (per Tiled API limitations)
- Use ObjectGroup mode for undo support (creates MapObjects for each stamp)
- Tablet pressure not available in Tiled API - uses velocity simulation instead
- Complex blend modes may have performance impact with large brushes

### Known Issues
- **Freeform Brush Rendering**: Freeform brush strokes may cause some visual rendering appearances during painting, but this does not impact the final outcome result
- **Object Stamping Precision**: Object stamping does not place objects at 100% precise grid/tile positions due to isometric design considerations, though placement remains precise and accurate

---

## 👨‍💻 Credits

**Created by:** Leo Louvar

**Developed with:** [PersistenceAI](https://persistence-ai.github.io/Landing/) via 1 hour of vibe coding using model GLM 4.7 and human review

This project was programmed and created using [PersistenceAI](https://persistence-ai.github.io/Landing/)'s advanced AI-assisted development workflow, demonstrating the power of AI-human collaboration in software development. Built in just 1 hour of vibe coding with GLM 4.7, followed by human review and refinement.

**Learn more about PersistenceAI:** Visit [https://persistence-ai.github.io/Landing/](https://persistence-ai.github.io/Landing/) - The AI coding agent built for the terminal.

---

## 📞 Support

- **Issues**: Report bugs or request features on [GitHub Issues](https://github.com/PersistenceOS/brushtily/issues)
- **Questions**: Ask on [Tiled Forums](https://discourse.mapeditor.org/)
- **Email**: Contact us at PersistenceAI@proton.me

---

**Transform your Tiled workflow with professional texture painting capabilities. Create beautiful, organic maps with the freedom of freehand brush strokes.**
