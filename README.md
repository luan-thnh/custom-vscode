# Custom VSCode Setup

This guide provides steps to customize your VSCode with a custom theme using `custom-vscode.css`, and instructions on how to configure `settings.json` for a personalized development environment.

## Requirements

### Extensions

1. **Custom CSS and JS Loader**  
   This extension allows you to inject custom CSS and JavaScript into VSCode.

   - Install via VSCode Marketplace: [Custom CSS and JS Loader](https://marketplace.visualstudio.com/items?itemName=be5invis.vscode-custom-css)

2. **Background**  
   Add a custom background to your VSCode environment.

   - Install via VSCode Marketplace: [Background](https://marketplace.visualstudio.com/items?itemName=shalldie.background)

### Fonts

1. **Cascadia Code**  
   The default editor font will be set to Cascadia Code, which is a clean and modern monospaced font.

   - Download: [Cascadia Code](https://github.com/microsoft/cascadia-code/releases)

2. **CaskaydiaCove Nerd Font** (for terminal)  
   This patched version of Cascadia Code includes extra symbols for use in the terminal and development tools.

   - Download: [CaskaydiaCove Nerd Font](https://www.nerdfonts.com/font-downloads)

## Configuration

### `custom-vscode.css`

Create a `custom-vscode.css` file to apply your custom styles to VSCode. Example:

```css
/* custom-vscode.css */

body {
  background-color: #1e1e1e; /* Set a dark background color */
}

.monaco-editor .view-line {
  font-family: 'Cascadia Code', monospace; /* Editor font */
  font-size: 14px;
}

.terminal .xterm {
  font-family: 'CaskaydiaCove Nerd Font', monospace; /* Terminal font */
}
```

### `settings.json`

Update your VSCode `settings.json` to load the custom CSS and set up your fonts.

```json
{
  "editor.fontFamily": "'Cascadia Code', monospace",
  "editor.fontLigatures": true,
  "terminal.integrated.fontFamily": "'CaskaydiaCove Nerd Font', monospace",
  "workbench.colorTheme": "Default Dark+",
  "vscode_custom_css.imports": ["file:///path/to/custom-vscode.css"],
  "background.enabled": true,
  "background.customImages": ["file:///path/to/your/background/image.png"],
  "background.style": {
    "opacity": 0.15
  }
}
```

### Customizing the Background

To set a custom background image for your VSCode:

- Add the image path in `background.customImages` in the `settings.json`.
- Adjust the opacity using the `"opacity": 0.15` setting (or any value that suits your preference).

## Applying Changes

After setting up the `custom-vscode.css` and `settings.json`:

1. Press `Ctrl+Shift+P` (or `Cmd+Shift+P` on Mac) and type `Reload Custom CSS and JS`.
2. Select the option to reload and apply the custom settings.

You should now see your custom fonts and background applied to VSCode!

## Troubleshooting

- Ensure the path to the `custom-vscode.css` and background image is correct.
- If custom CSS doesn’t load, make sure that the `Custom CSS and JS Loader` extension is installed and enabled.
- If fonts do not render correctly, confirm that they are installed on your system and added to the `settings.json` file.

```

Replace `/path/to/` with the actual paths to your custom CSS and image files. This guide covers setting up your custom VSCode environment with custom styles, fonts, and background.
```
