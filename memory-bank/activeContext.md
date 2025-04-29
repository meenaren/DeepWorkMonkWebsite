# Active Context: Jekyll Site Setup & Content Migration

**Current Focus:**
- Updating Memory Bank documentation to accurately reflect the project as a Jekyll site.
- Verifying the migrated content within the Jekyll structure.

**Recent Changes:**
- **Discovery:** Realized the project is a Jekyll site, not a single static HTML page as initially assumed.
- Updated `memory-bank/systemPatterns.md` to describe Jekyll architecture.
- Updated `memory-bank/techContext.md` to list Jekyll-related technologies and setup.
- Previous changes (before Jekyll discovery):
    - Created core Memory Bank files (based on initial incorrect assumption).
    - Created initial `index.html` (now understood as the Jekyll site homepage).
    - Created `_posts/2025-04-28-books-i-recommend.html` containing the migrated content.
    - Added original links to book cover images within the post file.
    - Moved resized images to `assets/images/books/`.
    - Adjusted title alignment in the post layout/CSS (needs verification in Jekyll context).

**Next Steps:**
1.  **Update `memory-bank/progress.md`** to reflect the Jekyll context and current status.
2.  **Verify Post Content & Layout:**
    - Read `_posts/2025-04-28-books-i-recommend.html` to confirm content and image paths (`/assets/images/books/...`).
    - Read relevant layout file (likely `_layouts/post.html`) and CSS (`assets/css/style.scss`) to understand how the post is rendered and styled.
    - Check if the title alignment change was applied correctly within the Jekyll structure (e.g., in `style.scss` or the post layout).
3.  **Local Preview (Optional but Recommended):** Use `bundle exec jekyll serve` to build and preview the site locally, specifically checking the `/blogs/books-i-recommend.html` page (or similar, depending on permalink settings). This requires Ruby/Bundler/Jekyll setup.
4.  **(User Task)** Ensure GitHub repository is set up and configured for GitHub Pages (using the correct branch).
5.  **(User Task)** Commit and push all project files (`_config.yml`, `Gemfile`, `index.html`, `_posts/`, `_layouts/`, `_includes/`, `assets/`, `memory-bank/`, etc.) to the repository.

**Active Decisions & Considerations:**
- The project uses Jekyll. All further actions must account for Jekyll's structure and build process.
- Image paths in the post file must be correct relative to the generated site structure (e.g., `/assets/images/books/`).
- Styling changes (like title alignment) should be applied within the Jekyll framework (e.g., `style.scss`).
- Preserving original external links for book images remains the decision.

**Important Patterns & Preferences:**
- Maintain accurate Memory Bank documentation reflecting the Jekyll structure.
- Follow Jekyll best practices for content, layouts, and assets.

**Learnings & Insights:**
- The project is a Jekyll-based website hosted on GitHub Pages.
- The migrated content exists as a post within the `_posts` directory.
- Initial assumptions about a single static HTML file were incorrect. Verification steps (like viewing `index.html`) are crucial.
- Understanding the specific Jekyll theme/layout (`_layouts/post.html`, `assets/css/style.scss`) is necessary to confirm styling and structure.
