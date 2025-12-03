# Material Design 3 Theme for Files

This document describes the Material Design 3 theme implementation for the Files application.

## Overview

The Files application has been updated to use Google's Material Design 3 (MD3) design system instead of Windows 11 Fluent UI. This provides a modern, consistent, and accessible user interface while maintaining all existing functionality.

## What Changed

### Color System
- Replaced Fluent UI color tokens with Material Design 3 color roles
- Implemented both Light and Dark theme variants
- Used MD3 semantic color tokens:
  - **Primary**: Main brand color used for key components
  - **Secondary**: Accents and less prominent components
  - **Tertiary**: Contrasting accents
  - **Error**: Error states
  - **Surface**: Component backgrounds
  - **Background**: Screen backgrounds
  - **Outline**: Borders and dividers

### Typography
- Updated font sizes to use Material Design 3 type scale:
  - Display (Large, Medium, Small): 57px, 45px, 36px
  - Headline (Large, Medium, Small): 32px, 28px, 24px
  - Title (Large, Medium, Small): 22px, 16px, 14px
  - Body (Large, Medium, Small): 16px, 14px, 12px
  - Label (Large, Medium, Small): 14px, 12px, 11px
- Adjusted font weights to match MD3 guidelines

### Shape System
- Increased corner radius values to match Material Design 3:
  - Extra Small: 4px (text fields)
  - Small: 8px
  - Medium: 12px (cards, dialogs)
  - Large: 16px (buttons, FABs)
  - Extra Large: 28px
  - Full: 999px (circular)

### Components
Created Material Design 3 styled components:

#### Buttons
- **Filled Button** (`MD3FilledButtonStyle`): High emphasis, primary actions
- **Filled Tonal Button** (`MD3FilledTonalButtonStyle`): Medium emphasis
- **Outlined Button** (`MD3OutlinedButtonStyle`): Medium emphasis with border
- **Text Button** (`MD3TextButtonStyle`): Low emphasis, subtle actions

#### Cards
- **Filled Card** (`MD3FilledCardStyle`): Surface variant background
- **Elevated Card** (`MD3ElevatedCardStyle`): Surface background with subtle elevation
- **Outlined Card** (`MD3OutlinedCardStyle`): Surface with border

#### Controls
- TextBox, ComboBox, CheckBox, RadioButton styles updated with MD3 colors and shapes
- ListView and GridView styled with MD3 surface colors

## Files Modified

1. **App.xaml** - Updated to include Material Design 3 resource dictionaries
2. **Styles/MaterialDesign3.xaml** - Core MD3 color tokens, typography, and shape definitions
3. **Styles/MaterialDesign3Buttons.xaml** - Button component styles
4. **Styles/MaterialDesign3Cards.xaml** - Card component styles
5. **Styles/MaterialDesign3Controls.xaml** - Input control styles
6. **Styles/TextBlockStyles.xaml** - Updated typography styles

## Usage

### Using MD3 Colors
```xml
<Border Background="{ThemeResource MD3.PrimaryBrush}" />
<TextBlock Foreground="{ThemeResource MD3.OnPrimaryBrush}" />
```

### Using MD3 Buttons
```xml
<Button Style="{StaticResource MD3FilledButtonStyle}" Content="Primary Action" />
<Button Style="{StaticResource MD3OutlinedButtonStyle}" Content="Secondary Action" />
```

### Using MD3 Cards
```xml
<Border Style="{StaticResource MD3FilledCardStyle}">
    <TextBlock Text="Card content" />
</Border>
```

### Using MD3 Typography
```xml
<TextBlock Text="Headline" FontSize="{StaticResource MD3.Typography.Headline.Large.Size}" />
<TextBlock Text="Body text" FontSize="{StaticResource MD3.Typography.Body.Medium.Size}" />
```

### Using MD3 Shapes
```xml
<Border CornerRadius="{StaticResource MD3.Shape.CornerRadius.Medium}" />
```

## Accessibility

The Material Design 3 theme maintains accessibility features:
- High contrast mode is preserved with dedicated theme dictionary
- All color combinations meet WCAG contrast requirements
- Focus indicators are maintained
- Screen reader compatibility is unchanged

## Functional Preservation

All existing functionality remains intact:
- File navigation and management
- Search and filtering
- Properties and customization
- All keyboard shortcuts
- All context menus
- All settings and preferences

The change is purely visual - the underlying functionality, logic, and features are unchanged.

## Additional Notes

- Material Design 3 uses state layers (hover, focus, pressed) with opacity overlays
- WinUI 3 doesn't have native elevation/shadow support like Android, so we simulate it with subtle borders
- The theme respects Windows system theme (Light/Dark mode)
- High Contrast mode continues to work as before for accessibility

## References

- [Material Design 3 Guidelines](https://m3.material.io/)
- [Material Design 3 Color System](https://m3.material.io/styles/color/overview)
- [Material Design 3 Typography](https://m3.material.io/styles/typography/overview)
- [Material Design 3 Components](https://m3.material.io/components)
