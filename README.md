# DevOne Theme

DevOne is a custom Visual Studio Code color theme landing between Solarized Light's warm neutrals and Spacegray Ocean Light's blue-forward chrome, while borrowing the saturated pink highlight you liked in Mermaid Light. This folder exists so future contributors know the scope for this area of the repository.

## Contents
- `package.json`: VS Code extension manifest (publisher `Dev1`) that registers this theme and now references the icon/marketplace metadata.
- `themes/devone-color-theme.json`: the theme definition consumed by the manifest.
- `icon.png`: 128x128-ish square icon that VS Code shows in the Extensions view and marketplace listing.
- `README.md`: this file, which captures palette intent, structure, and setup steps until a broader documentation home exists.

## Usage
1. Rename/copy this folder to `%USERPROFILE%\.vscode\extensions\Dev1.devone-theme-0.0.1` so VS Code treats it as an installed extension.
2. Reload VS Code (Command Palette → `Developer: Reload Window`).
3. Run `Preferences: Color Theme` and select **DevOne (Light)**.

## Packaging
- Install the VS Code extension tooling once: `npm install -g @vscode/vsce`.
- From this directory run `vsce package` to build `devone-theme-0.0.1.vsix`.
- Distribute/install via `code --install-extension devone-theme-0.0.1.vsix` or the Extensions view (⋮ → Install from VSIX...).
- To publish straight to the marketplace run `vsce publish` (requires a Personal Access Token with the `Dev1` publisher). Use `vsce publish minor` or `vsce publish patch` as you rev versions.

## Marketplace Metadata
- `package.json` now includes `icon`, `keywords`, a gallery banner, and placeholder repository/issue links pointing at `https://github.com/Dev1/TouchScreen`. Update those URLs if the canonical repository lives elsewhere.
- Keep the icon under 256 KB and at least 128×128 px; replace `icon.png` if you iterate on branding.
- The `categories` array is limited to VS Code's schema—stick with `Themes` for this package.

## Palette Posts
- Base background: soft sandstone `#F4F0E6` to stay warmer than Spacegray while lighter than Solarized.
- Contrast canvas: `#FFFFFF` editor widgets and `#E4E8ED` panels for crisp boundaries.
- Primary text: deep slate `#1F2A30` for strong readability.
- Accents: ocean blue `#2272CF` for activity states, blush pink `#D6488B` for highlights, plus amber `#C47E1F` for warnings.
- Neutral greys: `#63707A` mid-tones to bridge UI separators without drifting too cool.

These decisions are captured directly inside the theme JSON as well so palette intent stays discoverable alongside the code, and the manifest documents the structure for future iterations.
