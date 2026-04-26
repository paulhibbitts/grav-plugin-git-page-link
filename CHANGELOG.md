# v0.9.0
## 26-04-2026

1. [](#new)
    * ChangeLog started...
    * Configurable link pointing to the source Markdown file in the remote Git repository configured by the Git Sync plugin
    * Automatic host detection for GitHub, GitLab, Gitea, Forgejo, and Codeberg — each uses its host-specific URL pattern
    * Link position option — place the link at the top, bottom (default), or both ends of the content
    * Link style option — display as a plain text link (default) or a button
    * Link label option — customise the visible link text (e.g. "Edit this Page", "View Source")
    * Link tooltip option — optional hover tooltip via the `title` attribute
    * Icon option — choose between built-in pencil, document, or Git branch SVGs, a custom SVG, or no icon
    * Custom SVG option — accepts a full `<svg>` element or just inner path content
    * Page types option — restrict the link to specific page templates; empty means all pages
    * Silently omits the link if Git Sync is not installed or has no remote configured
    * Link always opens in a new tab with `rel="noopener noreferrer"`
    * Internationalisation via `languages.yaml` with support for English and French
    * Full Admin panel integration via `blueprints.yaml` with translated field labels
    * CSS namespaced under `.gpl-*` to prevent theme collisions, with optional dark mode support
    * CSS asset loaded only on pages where the link is displayed
