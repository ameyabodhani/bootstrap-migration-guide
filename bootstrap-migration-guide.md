# Bootstrap v3 to v5 Migration Guide

## Class Name Changes

### Layout & Display
- `text-right` → `text-end`
- `text-left` → `text-start`
- `hidden` → `d-none`
- `display: block` → `display: flex` (evaluate case by case)
- `img-responsive` → `img-fluid`

### Components
- `.label` → `.badge` (evaluate case by case)
- `panel` → `card` (evaluate case by case)
- `panel-body` → `card-body`
- `panel-title` → `card-title`
- `panel-heading` → `card-header`
- `panel panel-default` → `card`
- `panel panel-info` → `card border-info`
- `panel-group` → `card-group`

### Buttons & Navigation
- `btn-default` → `btn-light`
- `btn-secondary` → `btn-default`
- `active` → `nav-link active` (for `nav nav-pills`)
- `navbar-header` → `navbar-brand`
- `navbar-toggle` → `navbar-toggler`
- `navbar-left` → `navbar-nav me-auto`
- `navbar-right` → `navbar-nav ms-auto`

### Forms
- `form-group` → `form-group row` (evaluate case by case)
- `input-group-addon` → `input-group-text`

## Data Attribute Changes
- `data-toggle` → `data-bs-toggle`
- `data-parent` → `data-bs-parent`
- `data-target` → `data-bs-target`
- `data-dismiss` → `data-bs-dismiss`
- `data-target` → `data-bs-slide` (for carousel controls)

## Icon Migration
### Glyphicon to Font Awesome
- `glyphicon glyphicon-trash` → `fa fa-trash-o`
- `glyphicon glyphicon-ok` → `fa fa-check`
- `glyphicon glyphicon-pencil` → `fa fa-pencil`
- `glyphicon glyphicon-eye-open` → `fa fa-eye`
- `fa fa-remove` → `fa fa-times`

### Removed Features
- `<span class="caret"></span>` is removed in Bootstrap 5
  - Replace with `<span class="dropdown-toggle"></span>`

## jQuery Updates
1. Update jQuery files:
   - Copy new jquery.js and jquery UI files to project folder
   - Update file references in JSP files
   - Remove old JS files
   - Replace jquery.min.js in jqGrid-4.1.2/js/i18n/ with new version

2. Verification:
   - Check jQuery version in browser console
   - Test all jQuery-dependent functionality

## Grid System Updates
Example of updated grid classes:
```html
<div class="offset-sm-2 offset-md-2 offset-lg-2 col-sm-4 col-md-4 col-lg-4">
```

## Migration Checklist
1. Update Bootstrap CDN or local files to v5
2. Update jQuery and related dependencies
3. Search and replace class names systematically
4. Update data attributes
5. Replace Glyphicon icons with Font Awesome equivalents
6. Test responsive layouts
7. Verify component functionality
8. Check for browser compatibility

## Common Issues to Watch For
1. Layout shifts due to spacing/margin changes
2. Icon rendering issues after Glyphicon replacement
3. jQuery compatibility with new Bootstrap version
4. Form validation behavior changes
5. Modal and dropdown functionality
6. Responsive navigation behavior

## Additional Notes
- Always test thoroughly after migration
- Consider browser compatibility
- Document any custom fixes or workarounds
- Keep Bootstrap 5 documentation handy for reference
