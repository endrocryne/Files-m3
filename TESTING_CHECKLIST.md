# Testing Checklist for Material Design 3 Implementation

This checklist helps verify that the Material Design 3 implementation works correctly when built on Windows.

## Pre-Testing Setup

### Build Requirements
- [ ] Windows 10/11 with latest updates
- [ ] Visual Studio 2022 with WinUI workload
- [ ] .NET 9.0 SDK or later
- [ ] Windows App SDK 1.8 or later

### Build Steps
1. [ ] Open Files.slnx in Visual Studio 2022
2. [ ] Restore NuGet packages
3. [ ] Select Debug configuration
4. [ ] Select x64 platform
5. [ ] Build solution (should succeed with no errors)
6. [ ] Run the application

## Visual Testing - Light Theme

### Color Verification
- [ ] Primary color is purple (#6750A4), not blue
- [ ] Selected items show purple highlight
- [ ] Tabs show purple when selected
- [ ] Buttons have purple primary color
- [ ] Background is clean white/off-white

### Shape Testing
- [ ] Buttons have noticeably rounded corners (16px)
- [ ] Cards and dialogs have medium rounded corners (12px)
- [ ] File thumbnails have rounded corners (12px)
- [ ] Text fields have small rounded corners (4px)
- [ ] Overall appearance is "rounder" than before

### Typography Check
- [ ] Text appears clear and readable
- [ ] Font sizes are consistent and appropriate
- [ ] Headings are properly sized
- [ ] Body text is 14-16px
- [ ] Labels are 12-14px

### Component Appearance
- [ ] Navigation sidebar looks good
- [ ] Address bar renders correctly
- [ ] Toolbar buttons appear styled
- [ ] File list displays properly
- [ ] Properties pane shows correctly
- [ ] Context menus render properly

## Visual Testing - Dark Theme

### Switch to Dark Theme
- [ ] Open Settings
- [ ] Change to Dark theme
- [ ] Application switches smoothly

### Dark Theme Colors
- [ ] Primary color is light purple (#D0BCFF), not light blue
- [ ] Background is dark (#1C1B1F)
- [ ] Text is readable with good contrast
- [ ] Selected items show purple container color
- [ ] All colors appear intentional and harmonious

### Dark Theme Shapes
- [ ] All corner radii same as Light theme
- [ ] Buttons still rounded (16px)
- [ ] Cards still medium rounded (12px)
- [ ] Everything looks consistent

## Accessibility Testing

### High Contrast Mode
- [ ] Enable Windows High Contrast mode
- [ ] Application still works
- [ ] Text is readable
- [ ] Focus indicators visible
- [ ] UI elements distinguishable
- [ ] No visual regressions

### Keyboard Navigation
- [ ] Tab key moves focus correctly
- [ ] Focus indicators are visible
- [ ] All keyboard shortcuts still work
- [ ] Enter/Space activate buttons
- [ ] Arrow keys work in lists

### Screen Reader (Optional)
- [ ] Enable Windows Narrator
- [ ] UI elements are announced
- [ ] Navigation makes sense
- [ ] No missing labels

## Functional Testing

### File Operations
- [ ] Browse folders
- [ ] Open files
- [ ] Copy files
- [ ] Move files
- [ ] Delete files
- [ ] Rename files
- [ ] Create new folders

### Navigation
- [ ] Click folders to navigate
- [ ] Use address bar
- [ ] Use back/forward buttons
- [ ] Use sidebar navigation
- [ ] Switch between tabs

### Search
- [ ] Search for files
- [ ] Filter results
- [ ] Advanced search works
- [ ] Tag search works

### View Options
- [ ] Switch to List view
- [ ] Switch to Grid view
- [ ] Switch to Columns view
- [ ] Adjust view settings
- [ ] Sort by different columns

### Properties
- [ ] View file properties
- [ ] Edit file metadata
- [ ] Change permissions (if applicable)
- [ ] View file details

### Settings
- [ ] Open settings
- [ ] Change preferences
- [ ] Customize appearance (beyond theme)
- [ ] All settings tabs work

## Edge Cases

### Window Resizing
- [ ] Resize window to minimum size
- [ ] Resize to maximum size
- [ ] UI adapts responsively
- [ ] No layout issues

### Multiple Tabs
- [ ] Open multiple tabs
- [ ] Switch between tabs
- [ ] Close tabs
- [ ] Tab styling looks correct

### Context Menus
- [ ] Right-click files
- [ ] Right-click folders
- [ ] Right-click in empty space
- [ ] All menu items visible and functional

### Different DPI Settings
- [ ] Test at 100% DPI
- [ ] Test at 125% DPI (if available)
- [ ] Test at 150% DPI (if available)
- [ ] Rounded corners scale properly
- [ ] Text remains readable

## Performance Check

### Responsiveness
- [ ] UI feels snappy
- [ ] No noticeable lag
- [ ] Smooth animations (if any)
- [ ] No performance regression from before

### Resource Usage
- [ ] Memory usage normal
- [ ] CPU usage normal
- [ ] No excessive resource consumption

## Documentation Review

### Check Documentation Files
- [ ] Read MATERIAL_DESIGN_3.md
- [ ] Read VISUAL_CHANGES.md
- [ ] Read IMPLEMENTATION_SUMMARY.md
- [ ] Read src/Files.App/Styles/README.md
- [ ] All documentation is accurate

## Issues to Watch For

### Common Potential Issues
- [ ] ⚠️ Missing resources (check Output window for errors)
- [ ] ⚠️ Broken StaticResource references
- [ ] ⚠️ Colors not applying correctly
- [ ] ⚠️ Corner radius not showing (still sharp corners)
- [ ] ⚠️ Text too small or too large
- [ ] ⚠️ Contrast issues in Dark theme
- [ ] ⚠️ High Contrast mode broken

### If Issues Found
1. Check Visual Studio Output window for XAML errors
2. Check for missing resource references
3. Verify all MaterialDesign3*.xaml files are included in build
4. Check that App.xaml correctly references all MD3 files
5. Report issues with screenshots if possible

## Final Verification

### Overall Assessment
- [ ] Visual appearance matches Material Design 3 style
- [ ] All functionality works as before
- [ ] No regressions in features
- [ ] Accessibility maintained
- [ ] Performance acceptable
- [ ] Ready for production use

### Screenshots (Recommended)
Take screenshots of:
1. [ ] Light theme - main window
2. [ ] Dark theme - main window
3. [ ] Example of rounded buttons
4. [ ] Example of rounded cards/dialogs
5. [ ] Example of file list with rounded thumbnails

## Sign-Off

Date Tested: _______________

Tested By: _______________

Build Configuration: _______________

Platform: _______________

Result: ⬜ Pass  ⬜ Pass with minor issues  ⬜ Fail

Notes:
_______________________________________
_______________________________________
_______________________________________

## Next Steps After Testing

### If Tests Pass
- [ ] Merge PR to main branch
- [ ] Update changelog
- [ ] Consider creating release notes
- [ ] Share screenshots with team

### If Tests Fail
- [ ] Document all issues found
- [ ] Take screenshots of problems
- [ ] Report back to developer
- [ ] Request fixes before merging
