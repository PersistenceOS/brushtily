# Brushtily v1.1.0 - Bug Fixes & Improvements

## 🐛 Bug Fixes

### Fixed Artifacting Issues
- **Fixed discoloration when erasing or adding image layers**
  - Resolved color shift problems that occurred during brush operations
  - Improved color accuracy by properly handling premultiplied alpha channels
  - Enhanced image layer compositing to prevent visual artifacts

## 🔧 Changes

- Removed redundant button from toolbar to streamline the interface
- Improved overall stability and performance

## 📦 Installation

1. **Download** `brushtily.mjs` from this release
2. **Copy to Tiled extensions folder**:
   - **Windows**: `%LOCALAPPDATA%\Tiled\extensions\`
   - **macOS**: `~/Library/Preferences/Tiled/extensions/`
   - **Linux**: `~/.config/tiled/extensions/`
3. **Restart Tiled**
4. Find "Brushtily" in the Tools toolbar

## 📋 Requirements

- Tiled 1.8 or later
- JavaScript extensions enabled (default)

## 🐛 Known Issues

- Freeform brush strokes may show visual rendering appearances during painting (does not affect final result)
- Object stamping precision may vary slightly in isometric maps due to design considerations

## 🙏 Credits

**Created by:** Leo Louvar  
**Developed with:** [PersistenceAI](https://persistence-ai.github.io/Landing/) using model GLM 4.7 and human review and refinement.

---

Enjoy creating beautiful maps with Brushtily! 🎨
