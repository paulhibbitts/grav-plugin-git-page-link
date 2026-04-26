# Git Page Link Plugin

Adds a link to Grav pages that connects visitors directly to the page's source Markdown file in the Git repository configured by the [Git Sync plugin](https://github.com/trilbymedia/grav-plugin-git-sync). Ideal for open authoring workflows where you want to invite readers to suggest edits or view page source — contributors with repository access land on the edit interface, while everyone else sees the file in the repository viewer. GitHub, GitLab, Gitea, Forgejo, and Codeberg are supported automatically.

## What It Does

- Renders a link at the top, bottom, or both ends of page content
- Link label is fully customisable — use "Edit this Page", "View Source", "Open on GitHub", or any text
- Styled as a plain text link (default) or a button
- Displays a built-in pencil, document, or Git branch SVG icon, a custom SVG, or no icon
- Opens the repository URL in a new tab
- Silently omits the link if Git Sync is not installed or has no remote configured
- Restricts display to specific page templates; leave the Page Types setting empty to show on all pages

## Requirements

- Grav 1.7+
- PHP 8.0+
- [Git Sync plugin](https://github.com/trilbymedia/grav-plugin-git-sync) installed and configured with a remote repository

## Installation

**Via the Grav Admin Panel:** Plugins → Add → search for `Git Page Link` → Install.

**Via GPM:**

```bash
bin/gpm install git-page-link
```

**Manual install:**

1. Download the plugin from [GitHub](https://github.com/paulhibbitts/grav-plugin-git-page-link)
2. Unzip and rename the folder to `git-page-link`
3. Copy the folder to `user/plugins/git-page-link`

## Plugin Settings

| Setting | Default | Description |
|---------|---------|-------------|
| Plugin Status | Enabled | Enable or disable the plugin |
| Link Label | Edit this Page | Text displayed on the link |
| Link Tooltip | _(empty)_ | Tooltip shown on hover (`title` attribute); leave empty for no tooltip |
| Link Position | Bottom | Where the link appears: Top, Bottom, or Both |
| Link Style | Plain text link | Display as a plain text link or a button |
| Dark Mode Support | Disabled | Load dark mode CSS for the button style; enable only if your theme supports dark mode |
| Icon | Pencil | Icon shown beside the link label: Pencil, Document, Git branch, Custom SVG, or None |
| Custom SVG | _(empty)_ | Full `<svg>` element or inner path content; used only when Icon is set to Custom SVG |
| Show on Page Types | _(empty)_ | Restrict the link to specific page templates; leave empty to show on all pages |

## Credits

Developed by [HibbittsDesign.org](https://hibbittsdesign.org) with the assistance of [Claude Code](https://claude.ai/claude-code).

Special thanks to [tucho235](https://github.com/tucho235) for the [Copy as Markdown Button](https://github.com/tucho235/grav-plugin-copy-as-markdown-button) plugin, which served as an example of injecting content at the top or bottom of Grav pages.
