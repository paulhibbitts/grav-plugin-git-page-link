# Git Edit Page Link Plugin

Adds an "Edit this Page" link to Grav pages, pointing directly to the source Markdown file in the remote Git repository configured by the [Git Sync plugin](https://github.com/trilbymedia/grav-plugin-git-sync). GitHub, GitLab, Gitea, Forgejo, and Codeberg are supported — the correct edit URL pattern is detected automatically from the remote URL.

## What It Does

- Renders an "Edit this Page" link at the top, bottom, or both ends of page content
- Styled as a plain text link (default) or a button
- Displays a built-in pencil, document, Markdown mark, or Git branch SVG icon, a custom SVG, or no icon
- Opens the remote edit URL in a new tab
- Silently omits the link if Git Sync is not installed or has no remote configured
- Skips modular sub-pages automatically
- Restricts display to specific page templates via the Page Types setting (empty = all pages)

## Requirements

- Grav 1.7+
- PHP 8.0+
- [Git Sync plugin](https://github.com/trilbymedia/grav-plugin-git-sync) installed and configured with a remote repository

## Installation

**Via the Grav Admin Panel:** Plugins → Add → search for `Git Edit Page Link` → Install.

**Via GPM:**

```bash
bin/gpm install git-edit-page-link
```

**Manual install:**

1. Download the plugin from [GitHub](https://github.com/paulhibbitts/grav-plugin-git-edit-page-link)
2. Unzip and rename the folder to `git-edit-page-link`
3. Copy the folder to `user/plugins/git-edit-page-link`

## Plugin Settings

| Setting | Default | Description |
|---------|---------|-------------|
| Plugin Status | Enabled | Enable or disable the plugin |
| Link Label | Edit this Page | Text displayed on the link |
| Link Tooltip | _(empty)_ | Tooltip shown on hover (`title` attribute); leave empty for no tooltip |
| Link Position | Bottom | Where the link appears: Top, Bottom, or Both |
| Link Style | Plain text link | Display as a plain text link or a button |
| Dark Mode Support | Disabled | Load dark mode CSS for the button style; enable only if your theme supports dark mode |
| Icon | Pencil | Icon shown beside the link label: Pencil, Document, Markdown mark, Git branch, Custom SVG, or None |
| Custom SVG | _(empty)_ | Full `<svg>` element or inner path content; used only when Icon is set to Custom SVG |
| Show on Page Types | _(empty)_ | Restrict the link to specific page templates; leave empty to show on all pages |

## Credits

Developed by [HibbittsDesign.org](https://hibbittsdesign.org) with the assistance of [Claude Code](https://claude.ai/claude-code).

Special thanks to [tucho235](https://github.com/tucho235) for the [Copy as Markdown Button](https://github.com/tucho235/grav-plugin-copy-as-markdown-button) plugin, which served as an example of injecting content at the top or bottom of Grav pages.
