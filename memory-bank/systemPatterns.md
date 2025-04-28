# System Patterns: Static HTML Site for GitHub Pages

**Architecture:**
- Single static HTML file (`index.html`).
- Basic CSS for styling, potentially embedded within the HTML or in a separate `style.css` file. (Decision: Start with embedded CSS for simplicity, can be extracted later if needed).
- Images stored locally within the project structure.

**Key Technical Decisions:**
- **Static Site:** No server-side logic or database required. Suitable for GitHub Pages.
- **HTML Structure:** Use standard semantic HTML tags (`<h1>`, `<h2>`, `<p>`, `<img>`, etc.) to structure the content logically based on the source material.
- **Styling:** Minimal CSS to ensure readability and basic layout. Avoid complex frameworks for this simple page.
- **Image Handling:** Use the pre-resized images located in the `resized/` directory relative to the HTML file.

**Component Relationships:**
- `index.html` will contain all the text content and references to the image files.
- Image files (`*.jpg`) located in `resized/` will be displayed by `index.html`.
- (Optional) `style.css` would contain styling rules applied to `index.html`.

**Critical Implementation Paths:**
- Extracting relevant text content from the source URL content.
- Mapping source content structure (headings, paragraphs) to appropriate HTML tags.
- Correctly referencing the local image paths.
