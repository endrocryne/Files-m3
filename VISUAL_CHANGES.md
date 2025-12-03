# Visual Changes: Fluent UI to Material Design 3

This document describes the visual differences users will see after switching from Windows 11 Fluent UI to Material Design 3.

## Color Palette Changes

### Light Theme

| Element | Fluent UI (Before) | Material Design 3 (After) |
|---------|-------------------|---------------------------|
| Primary Color | `#0070CB` (Blue) | `#6750A4` (Purple) |
| Background | `#FFFBFE` (White/Mica) | `#FFFBFE` (White) |
| Surface | Layer on Mica | `#FFFBFE` (Pure white) |
| Surface Variant | Card Background | `#E7E0EC` (Light purple) |
| Selected Tab | Mica layer | `#E8DEF8` (Light purple) |

### Dark Theme

| Element | Fluent UI (Before) | Material Design 3 (After) |
|---------|-------------------|---------------------------|
| Primary Color | `#50C0FF` (Light Blue) | `#D0BCFF` (Light Purple) |
| Background | `#1C1B1F` (Dark gray) | `#1C1B1F` (Same dark gray) |
| Surface | Card Background | `#1C1B1F` (Dark) |
| Surface Variant | Card Secondary | `#49454F` (Medium gray) |
| Selected Tab | Subtle fill | `#4A4458` (Purple-tinted gray) |

## Shape & Corner Radius Changes

| Component | Fluent UI | Material Design 3 | Difference |
|-----------|-----------|-------------------|------------|
| Buttons | 4px corners | **16px** corners | Much rounder |
| Cards | 4px corners | **12px** corners | Rounder |
| Text Fields | 4px corners | **4px** corners | Same |
| Dialogs | 8px corners | **12px** corners | Rounder |
| File Thumbnails | 2px corners | **12px** corners | Much rounder |
| Detail Thumbnails | 2px corners | **8px** corners | Rounder |

## Typography Changes

### Before (Fluent UI)
- Used Windows default type scale
- Font sizes: varies by component
- Font weight: Normal/SemiBold mix

### After (Material Design 3)
- Systematic type scale with 5 categories
- **Display**: 57px, 45px, 36px (large headings)
- **Headline**: 32px, 28px, 24px (section headers)
- **Title**: 22px, 16px, 14px (subsections)
- **Body**: 16px, 14px, 12px (main text)
- **Label**: 14px, 12px, 11px (buttons, labels)
- Font weight: Normal/Medium (500) emphasis

## Component Visual Changes

### Buttons

#### Fluent UI Style
- Subtle fills with transparency
- Minimal borders
- Small corner radius (4px)
- Acrylic/mica effects

#### Material Design 3 Style
- **Filled Buttons**: Bold, opaque primary color backgrounds
- **Filled Tonal Buttons**: Lighter container colors with higher contrast text
- **Outlined Buttons**: Transparent with visible 1px border
- **Text Buttons**: No background or border, just colored text
- Large corner radius (16px) - "pill-shaped"
- No transparency effects, solid colors

### Cards

#### Fluent UI Style
- Subtle background tints
- Very small corners (2-4px)
- Mica material effects
- Layered appearance

#### Material Design 3 Style
- **Filled Cards**: Solid surface variant color background
- **Elevated Cards**: Solid surface color (simulated elevation)
- **Outlined Cards**: Border with surface background
- Medium corner radius (12px)
- No material effects, flat colors

### Text Fields

#### Fluent UI Style
- Soft backgrounds
- Minimal borders
- Focus underline

#### Material Design 3 Style
- Surface variant backgrounds
- Visible 1px outline
- Corner radius: 4px (small, not rounded)
- Higher contrast borders

### Lists & Grids

#### Fluent UI Style
- Transparent backgrounds
- Subtle hover states
- Sharp corners on items

#### Material Design 3 Style
- Surface color backgrounds
- MD3 state layers on hover
- Rounded corners on items (8-12px)
- Higher contrast selection states

## Overall Visual Impact

### What Users Will Notice

1. **Rounder Everything**: Buttons, cards, and thumbnails are noticeably more rounded
2. **Different Color Accent**: Purple (#6750A4) instead of blue (#0070CB) for primary actions
3. **Higher Contrast**: More defined borders and clearer separation between elements
4. **Flatter Design**: Less use of transparency and material effects, more solid colors
5. **Warmer Tones**: Surface colors have subtle purple tints instead of blue/gray

### What Stays the Same

1. **Layout**: All UI elements remain in the same positions
2. **Functionality**: Every feature works exactly as before
3. **Icons**: Custom icons are unchanged
4. **High Contrast Mode**: Fully preserved for accessibility
5. **Dark/Light Themes**: Both continue to work

## Side-by-Side Comparison Examples

### File List Item
**Before**: Sharp rectangular selection with subtle blue tint  
**After**: Rounded selection (12px corners) with purple tint

### Navigation Sidebar
**Before**: Mica background with transparency  
**After**: Solid surface color background

### Toolbar Buttons
**Before**: Small rounded (4px) with subtle fills  
**After**: Large rounded (16px) with bold fills or clear outlines

### Property Dialog
**Before**: Card with 4px corners and mica background  
**After**: Card with 12px corners and solid surface background

### Selected Tab
**Before**: Layer on mica with subtle tint  
**After**: Secondary container color (#E8DEF8 light / #4A4458 dark)

## Design Philosophy Shift

### Fluent UI (Microsoft)
- Emphasizes depth through layers and transparency (mica, acrylic)
- Subtle, soft appearance
- Windows 11 integration
- Adaptive to system backdrop

### Material Design 3 (Google)
- Emphasizes clarity through color and shape
- Bold, confident appearance  
- Platform-agnostic design language
- Solid, opaque surfaces

## Accessibility Maintained

Both design systems meet accessibility standards:
- ✅ WCAG 2.1 AA contrast ratios
- ✅ Focus indicators
- ✅ Screen reader compatibility
- ✅ High contrast mode
- ✅ Keyboard navigation
- ✅ Touch target sizes

The visual change is purely aesthetic - all accessibility features remain intact or improved.
