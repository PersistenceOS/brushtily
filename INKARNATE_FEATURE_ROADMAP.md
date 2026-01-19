# Brushtily Feature Roadmap - Only Non-Native Features

## Core Principle
**Only add features that:**
1. ✅ Don't exist in Tiled natively
2. ✅ Are convenient/useful for users
3. ✅ Enhance workflow without duplicating existing functionality

---

## What Tiled Already Has (Don't Duplicate!)

### ✅ Tiled Native Features:
- **Object Layers** - Full object placement system
- **Tile Objects** - Place tiles as objects (position, rotate, scale)
- **Polylines** - Draw paths/lines (for roads, rivers)
- **Text Objects** - Text labels on maps
- **Tilesets** - Organized tile collections
- **Object Properties** - Custom properties on objects
- **Placement Tools** - Dedicated tools for different object types

---

## Features to Add (Missing & Convenient)

### 🔥 HIGH PRIORITY - High Value, Missing Features

#### 1. **Object Stamping / Brush Mode** ⭐⭐⭐
**What it is**: Drag to "paint" multiple objects at once (like Inkarnate's stamp tool)

**Why it's missing**: 
- Tiled requires clicking each object individually
- No drag-to-stamp workflow for objects
- Very slow for decorating maps (forests, cities, etc.)

**Why it's convenient**:
- Much faster than clicking each object
- Natural workflow for populating areas
- Works with Tiled's existing object system

**Implementation**:
- Use Tiled's `ObjectGroup` and `MapObject` API
- Add "Object Brush Mode" to Brushtily
- Drag stroke → place objects along path
- Random rotation/scale variation

**Effort**: 6-10 hours

---

#### 2. **Object Library Browser** ⭐⭐
**What it is**: Visual panel with thumbnails, categories, search for objects

**Why it's missing**:
- Tiled has tilesets but no visual browser panel
- Must browse tilesets in separate view
- No thumbnail previews or categories

**Why it's convenient**:
- Quick visual selection
- Better organization than folder browsing
- Faster workflow

**Implementation**:
- Scan folders for object images
- Create thumbnail grid
- Category system (folder-based)
- Search/filter

**Effort**: 4-6 hours

---

#### 3. **Brush Rotation Jitter** ⭐
**What it is**: Random rotation variation for each brush stamp

**Why it's missing**:
- Tiled doesn't have this for texture painting
- Current brush always uses same rotation

**Why it's convenient**:
- More natural, organic look
- Prevents repetitive patterns
- Easy to add

**Implementation**:
- Add rotation jitter slider (0-360°)
- Random rotation per stamp
- Integrate with existing brush system

**Effort**: 2-3 hours (quick win!)

---

#### 4. **Pressure Affects Opacity** ⭐
**What it is**: Brush opacity varies with pressure (velocity)

**Why it's missing**:
- Tiled doesn't have pressure sensitivity
- We have pressure→size, but not opacity

**Why it's convenient**:
- More natural brush strokes
- Common in digital art tools
- Easy to add

**Implementation**:
- Extend existing pressure system
- Add `pressureAffectsOpacity` flag
- Calculate opacity from velocity

**Effort**: 2-3 hours (quick win!)

---

### 🟡 MEDIUM PRIORITY - Nice Enhancements

#### 5. **Scene Prefabs / Object Groups** ⭐
**What it is**: Group multiple objects into reusable "scenes"

**Why it's missing**:
- Tiled has object grouping but no scene system
- Can't save/load object groups as prefabs
- Must manually recreate common layouts

**Why it's convenient**:
- Speed up map creation
- Maintain consistency
- Reuse common layouts (houses, dungeons, etc.)

**Implementation**:
- Select objects → "Create Scene"
- Save scene with name
- Place scene as single unit
- Scene library panel

**Effort**: 10-14 hours

---

#### 6. **Path Tool with Width & Texture** ⭐
**What it is**: Draw paths/roads with automatic width and texture painting

**Why it's missing**:
- Tiled has polylines (lines) but no width control
- Can't paint texture along path width
- Must manually create paths with objects

**Why it's convenient**:
- Common map element (roads, rivers)
- Faster than manual creation
- Better than freeform painting for paths

**Implementation**:
- Click to start path, add points, double-click to end
- Width control (constant or variable)
- Paint texture along path width
- Smooth curve interpolation

**Effort**: 6-8 hours

---

### 🟢 LOW PRIORITY - Future Enhancements

#### 7. **Advanced Masking / Terrain Tools**
**What it is**: Land/water masks, terrain carving tools

**Why it's missing**: Tiled doesn't have mask-based terrain tools

**Effort**: 8-10 hours

---

#### 8. **Custom Brush Shape from Image**
**What it is**: Load image as brush shape mask

**Why it's missing**: Current shapes are geometric only

**Effort**: 3-4 hours

---

## ❌ Features We're NOT Adding (Tiled Already Has)

- ❌ **Object Placement** - Tiled has this (tile objects, object layers)
- ❌ **Text Labels** - Tiled has text objects
- ❌ **Path Drawing** - Tiled has polylines (we enhance with width/texture)
- ❌ **Object Properties** - Tiled has custom properties
- ❌ **Layer Management** - Tiled has full layer system

---

## Recommended Implementation Order

### Phase 1: Quick Wins & Core Features (v1.1)
1. **Brush Rotation Jitter** (2-3h) - Easy, high value
2. **Pressure Affects Opacity** (2-3h) - Easy, high value
3. **Object Stamping Mode** (6-10h) - Core feature
4. **Object Library Browser** (4-6h) - Needed for #3

**Timeline**: 14-22 hours
**Result**: Object stamping capability + brush enhancements

---

### Phase 2: Advanced Tools (v1.2)
5. **Path Tool with Width** (6-8h)
6. **Scene Prefabs** (10-14h)

**Timeline**: 16-22 hours
**Result**: Complete enhancement suite

---

### Phase 3: Polish (v1.3+)
7. **Advanced Masking** (8-10h)
8. **Custom Brush Shapes** (3-4h)

**Timeline**: 11-14 hours

---

## Feature Comparison Table

| Feature | Tiled Native | Brushtily | Priority | Effort | Add? |
|---------|--------------|-----------|----------|--------|------|
| Texture Painting | ❌ | ✅ | - | - | ✅ |
| Object Placement | ✅ | - | - | - | ❌ |
| **Object Stamping** | ❌ | ❌ | HIGH | 6-10h | ✅ |
| **Object Library Browser** | ⚠️ Tilesets only | ❌ | HIGH | 4-6h | ✅ |
| **Rotation Jitter** | ❌ | ❌ | HIGH | 2-3h | ✅ |
| **Pressure→Opacity** | ❌ | ❌ | HIGH | 2-3h | ✅ |
| Path Tool | ⚠️ Polyline (no width) | ❌ | MEDIUM | 6-8h | ✅ |
| Scene Prefabs | ❌ | ❌ | MEDIUM | 10-14h | ✅ |
| Text Labels | ✅ | - | - | - | ❌ |
| Advanced Masking | ❌ | ⚠️ Partial | MEDIUM | 8-10h | ✅ |
| Custom Brush Shapes | ❌ | ❌ | LOW | 3-4h | ✅ |

**Legend:**
- ✅ = Supported / Should add
- ⚠️ = Partially supported
- ❌ = Not supported
- "-" = Not applicable

---

## Summary

**Focus on:**
1. ✅ Object stamping (drag-to-place workflow)
2. ✅ Object library browser (visual selection)
3. ✅ Brush enhancements (rotation jitter, pressure→opacity)
4. ✅ Path tool with width (enhances Tiled's polyline)
5. ✅ Scene prefabs (reusable object groups)

**Don't add:**
- ❌ Anything Tiled already does well
- ❌ Duplicate existing functionality
- ❌ Features that aren't convenient

**Total High Priority Features**: 4 features, 14-22 hours
**Total Medium Priority Features**: 2 features, 16-22 hours

---

## Next Steps

1. **Start with Quick Wins** - Rotation jitter, pressure→opacity (4-6 hours total)
2. **Add Object Stamping** - Core missing feature (6-10 hours)
3. **Add Object Library** - Needed for stamping (4-6 hours)
4. **Iterate based on feedback**

**Ready to implement?** Start with the quick wins for immediate value, then move to object stamping!
