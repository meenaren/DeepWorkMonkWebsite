# System Patterns: Jekyll Static Site for GitHub Pages

**Architecture:**
- **Jekyll Static Site Generator:** Uses Jekyll to build the static website from source files.
- **Content:** Blog posts are written in Markdown (`.md`) and stored in the `_posts` directory.
- **Layouts:** HTML structure templates are defined in the `_layouts` directory (e.g., `default.html`, `post.html`). Posts specify which layout to use via front matter.
- **Includes:** Reusable HTML snippets (like navigation) are stored in the `_includes` directory and included in layouts.
- **Configuration:** Site-wide settings are managed in `_config.yml`.
- **Styling:** CSS is handled via `assets/css/style.scss`, which Jekyll processes.
- **Assets:** Images and other static assets are stored in the `assets` directory. The migrated book images are specifically in `assets/images/books/`.
- **Output:** Jekyll generates the final static HTML site (typically in a `_site` directory, though this is often gitignored). GitHub Pages runs Jekyll automatically.

**Key Technical Decisions:**
- **Jekyll:** Chosen as the static site generator, likely due to its native support by GitHub Pages and suitability for blogging.
- **Markdown:** Used for writing post content for ease of writing.
- **Liquid Templating:** Used within layouts and includes for dynamic content insertion (e.g., post content, site variables).
- **Directory Structure:** Follows Jekyll conventions (`_posts`, `_layouts`, `_includes`, `assets`).
- **Image Handling:** Migrated book images are stored in `assets/images/books/` and referenced from the post file.

**Component Relationships:**
- `_config.yml` provides global site configuration.
- Markdown files in `_posts/` contain the content for individual blog posts.
- Layout files in `_layouts/` define the overall HTML structure for pages and posts.
- Include files in `_includes/` provide reusable components like navigation.
- `assets/css/style.scss` defines the visual styling.
- Jekyll processes these components to generate the final static HTML files.

**Critical Implementation Paths:**
- Ensuring correct Markdown formatting in post files (`_posts/2025-04-28-books-i-recommend.html`).
- Correctly referencing image paths within the post file (e.g., `/assets/images/books/image.jpg`).
- Configuring layouts and includes appropriately.
- Setting up `_config.yml` with necessary site details (title, description, etc.).
- Understanding the Jekyll build process (handled automatically by GitHub Pages).
