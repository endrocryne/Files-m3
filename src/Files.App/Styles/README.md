# Material Design 3 Styles

This directory contains Material Design 3 (MD3) theme resources for the Files application.

## Files Overview

### Core Theme Resources

**MaterialDesign3.xaml**
- MD3 color palette (Light/Dark/HighContrast themes)
- Typography scale (Display, Headline, Title, Body, Label)
- Shape system (corner radii from 4px to 28px)
- Opacity constants for component states
- Global WinUI resource overrides

### Component Styles

**MaterialDesign3Buttons.xaml**
- Filled Button (`MD3FilledButtonStyle`)
- Filled Tonal Button (`MD3FilledTonalButtonStyle`)
- Outlined Button (`MD3OutlinedButtonStyle`)
- Text Button (`MD3TextButtonStyle`)

**MaterialDesign3Cards.xaml**
- Filled Card (`MD3FilledCardStyle`)
- Elevated Card (`MD3ElevatedCardStyle`)
- Outlined Card (`MD3OutlinedCardStyle`)

**MaterialDesign3Controls.xaml**
- TextBox (`MD3TextBoxStyle`)
- ComboBox (`MD3ComboBoxStyle`)
- CheckBox (`MD3CheckBoxStyle`)
- RadioButton (`MD3RadioButtonStyle`)
- ListView (`MD3ListViewStyle`)
- GridView (`MD3GridViewStyle`)

**TextBlockStyles.xaml**
- Updated to use MD3 typography scale
- Base, Body, BodyStrong, Caption, Subtitle styles

### Legacy Styles
Other XAML files in this directory maintain existing app-specific styles (icons, shimmer, etc.)

## Quick Reference

### Using MD3 Colors
```xml
<Border Background="{ThemeResource MD3.PrimaryBrush}" 
        Foreground="{ThemeResource MD3.OnPrimaryBrush}" />
```

### Using MD3 Buttons
```xml
<Button Style="{StaticResource MD3FilledButtonStyle}" Content="Save" />
<Button Style="{StaticResource MD3OutlinedButtonStyle}" Content="Cancel" />
```

### Using MD3 Cards
```xml
<Border Style="{StaticResource MD3FilledCardStyle}">
    <TextBlock Text="Card content" />
</Border>
```

### Using MD3 Typography
```xml
<TextBlock Text="Headline" 
           FontSize="{StaticResource MD3.Typography.Headline.Large.Size}" />
```

### Using MD3 Shapes
```xml
<Border CornerRadius="{StaticResource MD3.Shape.CornerRadius.Medium}" />
```

## Design Tokens

### Color Roles
- **Primary**: Main brand color and key actions
- **Secondary**: Less prominent actions
- **Tertiary**: Contrasting accents
- **Error**: Error states
- **Surface**: Component backgrounds
- **Background**: Screen backgrounds
- **Outline**: Borders and dividers

### Typography Sizes
| Category | Large | Medium | Small |
|----------|-------|--------|-------|
| Display  | 57px  | 45px   | 36px  |
| Headline | 32px  | 28px   | 24px  |
| Title    | 22px  | 16px   | 14px  |
| Body     | 16px  | 14px   | 12px  |
| Label    | 14px  | 12px   | 11px  |

### Shape Sizes
| Name        | Radius | Use Case            |
|-------------|--------|---------------------|
| None        | 0px    | No rounding         |
| Extra Small | 4px    | Text fields         |
| Small       | 8px    | Chips, small cards  |
| Medium      | 12px   | Cards, dialogs      |
| Large       | 16px   | Buttons, FABs       |
| Extra Large | 28px   | Large components    |
| Full        | 999px  | Circular elements   |

## Implementation Notes

### WinUI Adaptations
- Button hover/pressed states use opacity changes instead of pure state layer overlays for better WinUI integration
- Elevation is simulated with solid colors since WinUI doesn't have native shadow support like Android
- Global corner radius overrides ensure consistent MD3 appearance across all controls

### Accessibility
- All color combinations meet WCAG 2.1 AA contrast requirements
- High Contrast mode is fully preserved
- Focus indicators and screen reader support unchanged

## Learn More

See the root-level documentation files:
- `MATERIAL_DESIGN_3.md` - Comprehensive implementation guide
- `VISUAL_CHANGES.md` - Visual comparison with Fluent UI

Official Material Design 3 resources:
- [Material Design 3 Guidelines](https://m3.material.io/)
- [MD3 Color System](https://m3.material.io/styles/color/overview)
- [MD3 Typography](https://m3.material.io/styles/typography/overview)
