# Brushtily - Inkarnate-inspired Texture Painting for Tiled

[![Tiled Version](https://img.shields.io/badge/Tiled-1.8%2B-blue)](https://www.mapeditor.org/)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)

A powerful JavaScript extension for Tiled that adds Inkarnate-inspired freeform brushing and object stamping capabilities, enabling smooth, non-grid-aligned brush strokes for creating beautiful terrain and textures.

## Features

- **Freeform Brush Strokes**: Paint with non-grid-aligned brush strokes
- **Custom Brush Textures**: Load PNG/JPG images as brush textures
- **Adjustable Properties**:
  - Brush Size (10-500 pixels)
  - Opacity (0-100%)
  - Softness (0-100%) - Edge feathering
  - Texture Scale (10-200%) - Scale texture independently from brush size
  - Rotation (0-360 degrees)
  - Blend Modes (Normal, Multiply, Screen, Overlay, Darken, Lighten, etc.)
- **Fill Mode**: Bucket fill with color tolerance
- **Pressure Sensitivity**: Velocity-based simulation for natural brush strokes
- **Brush Presets**: Save and load favorite brush configurations
- **Dual Layer Support**: Works on ImageLayer (smooth painting) and ObjectGroup (undo support)

## 📦 Installation

### Quick Install

1. **Download** `brushtily.mjs` from the [latest release](https://github.com/PersistenceOS/brushtily/releases) (or use the file in this repository)

2. **Copy to Tiled extensions folder**:
   - **Windows**: `%LOCALAPPDATA%\Tiled\extensions\` 
     - (Usually: `C:\Users\<USER>\AppData\Local\Tiled\extensions\`)
   - **macOS**: `~/Library/Preferences/Tiled/extensions/`
   - **Linux**: `~/.config/tiled/extensions/`

3. **Restart Tiled** (or the extension will auto-reload on file change)

4. **Verify**: The "Brushtily" tool should appear in the Tools toolbar

### Verify Installation

- Open Tiled
- Check Tools toolbar for "Brushtily" tool icon
- If not visible, check Tiled Console (View → Views → Console) for errors

## Usage

### Basic Painting

1. Select an ImageLayer or ObjectGroup layer
2. Activate the Brushtily tool from the toolbar
3. Click and drag to paint with the brush

### Loading Brush Textures

1. Click "Edit Brush" in the tool panel (or use the action)
2. Click "Select New Texture"
3. Choose a PNG or JPG image file
4. The texture will be cached and used for painting

### Adjusting Brush Properties

Use the toolbar actions to adjust:
- **Brush Size**: Controls overall brush diameter
- **Opacity**: Controls transparency
- **Softness**: Controls edge feathering (0 = hard edge, 100 = fully feathered)
- **Texture Scale**: Scales the texture within the brush (independent of brush size)
- **Rotation**: Rotates the brush texture
- **Blend Mode**: Changes how the brush composites with existing pixels

### Fill Mode

1. Toggle "Fill Mode" button
2. Click on an area to fill it with the current brush
3. Fill tolerance can be adjusted (default: 32)

### Saving Presets

1. Configure your brush settings
2. Click "Presets" button
3. Enter a name and click "Save"
4. Load presets from the dropdown

## Technical Details

- **File Format**: ES Module (`.mjs`) - no global scope pollution
- **Layer Support**: ImageLayer (immediate visual feedback, no undo) and ObjectGroup (undo support)
- **Performance**: Optimized with point density limiting and update throttling
- **Pressure Simulation**: Uses velocity-based calculation (faster movement = lighter pressure)

## Known Limitations

- ImageLayer painting has no undo support (per Tiled API limitations)
- Use ObjectGroup mode for undo support (creates MapObjects for each stamp)
- Tablet pressure not available in Tiled API - uses velocity simulation instead
- Complex blend modes may have performance impact with large brushes

## File Structure

```
extensions/
  brushtily.mjs          # Main plugin file
  brushtily/
    presets.json         # Saved brush presets (auto-created)
    brushes/             # Optional: default brush textures
```

## 🚀 Quick Start

1. Create or open a map in Tiled
2. Add an **Image Layer** (Layer → Add Image Layer)
3. Select the **Brushtily** tool from the toolbar
4. Click **"Edit Brush"** → **"Select New Texture"** to load a brush texture
5. Click and drag to paint!

## 📋 Requirements

- **Tiled 1.8 or later** (JavaScript extensions support required)
- JavaScript extensions enabled (default in Tiled)

## 🐛 Troubleshooting

**Tool not appearing?**
- Check Tiled Console (View → Views → Console) for errors
- Verify file is in correct extensions folder
- Ensure file is named `brushtily.mjs` (not `.js`)

**Brush not painting?**
- Make sure you have an **Image Layer** selected (not Tile Layer)
- Check that layer is visible and unlocked
- Verify brush texture is loaded (Edit Brush → Select New Texture)

**Performance issues?**
- Reduce brush size for large maps
- Disable debug logging (set `debugEnabled: false` in code)
- Close other applications to free up memory

## 📄 License

This project is licensed under the MIT License - see [LICENSE](LICENSE) file for details.

## 🤝 Contributing

Contributions welcome! Please feel free to submit issues, feature requests, or pull requests.

## 🙏 Acknowledgments

- Inspired by Inkarnate's freeform brushing and object stamping workflow
- Built for the Tiled Map Editor community
- Uses Tiled's JavaScript Extension API

## 👨‍💻 Credits

**Created by:** Leo Louvar

**Developed with:** [PersistenceAI](https://persistence-ai.github.io/Landing/) via vibe coding using model GLM 4.7

This project was programmed and created using [PersistenceAI](https://persistence-ai.github.io/Landing/)'s advanced AI-assisted development workflow, demonstrating the power of AI-human collaboration in software development.

**Learn more about PersistenceAI:** Visit [https://persistence-ai.github.io/Landing/](https://persistence-ai.github.io/Landing/) - The AI coding agent built for the terminal.

## 📞 Support

- **Issues**: Report bugs or request features on [GitHub Issues](https://github.com/PersistenceOS/brushtily/issues)
- **Questions**: Ask on [Tiled Forums](https://discourse.mapeditor.org/)
