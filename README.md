# GitHub Theme for RStudio

RStudio editor themes that look like modern GitHub — the [Primer](https://primer.style) **Dark Default** and **Light Default** palettes used on github.com's code views and in the official [GitHub VS Code theme](https://github.com/primer/github-vscode-theme).

- `src/github-dark.rstheme` — GitHub Dark Default (primary)
- `src/github-light.rstheme` — GitHub Light Default

The dark theme is based on [rio-sanjuan/rstudio-themes](https://github.com/rio-sanjuan/rstudio-themes). It **preserves that theme's scrollbar styling** (scrollbar track/corner blend into the editor background) and **updates the syntax highlighting to GitHub's modern Primer palette** — red keywords (`#ff7b72`), light-blue strings (`#a5d6ff`), blue constants (`#79c0ff`), purple function calls (`#d2a8ff`), orange definitions (`#ffa657`) — plus retunes the rest of the IDE chrome (panes, tabs, menus, search boxes, borders) to GitHub's `#0d1117` / `#161b22` / `#21262d` surfaces.

## Install

### From R (recommended)

```r
# Dark
rstudioapi::addTheme(
  "https://raw.githubusercontent.com/Jonathan-kswm/rstudio-github-theme/main/src/github-dark.rstheme",
  apply = TRUE, force = TRUE
)

# Light
rstudioapi::addTheme(
  "https://raw.githubusercontent.com/Jonathan-kswm/rstudio-github-theme/main/src/github-light.rstheme",
  apply = TRUE, force = TRUE
)
```

### Manually

Download a `.rstheme` file from `src/`, then in RStudio go to
**Tools → Global Options → Appearance → Add…** and select the file.

## Notes

- RStudio's **Theme** (not Editor theme) must be set to **Modern** or **Sky** under
  **Global Options → Appearance** for the UI chrome styling to apply.
- The editor **font** is not set by the theme — configure it in
  **Global Options → Appearance → Editor font**.
- Comments are italic by default. To disable, edit `--comment-style: italic;`
  to `normal` in the `:root` block of the theme file.

## Credits

- Structural base and scrollbar styling: [rio-sanjuan/rstudio-themes](https://github.com/rio-sanjuan/rstudio-themes)
- Colors: [GitHub Primer](https://primer.style) / [primer/github-vscode-theme](https://github.com/primer/github-vscode-theme)
