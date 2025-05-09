# Tech Context: Jekyll Static Site

**Technologies Used:**
- **Jekyll:** Static site generator written in Ruby. Used to build the site.
- **Ruby:** The programming language Jekyll is built with. Required to run Jekyll locally.
- **Bundler:** Ruby dependency manager (implied by `Gemfile`). Used to manage Jekyll and other Ruby gems.
- **Markdown:** Used for writing content in `_posts`.
- **Liquid:** Templating language used by Jekyll for layouts, includes, and dynamic content.
- **HTML5:** The final output generated by Jekyll.
- **CSS3/SCSS:** Used for styling, processed by Jekyll (via `assets/css/style.scss`).
- **Git:** For version control.
- **GitHub Pages:** For hosting the static website and automatically running the Jekyll build process.

**Development Setup:**
- Text editor (like VS Code).
- Web browser for previewing.
- **Ruby Installation:** Required for Jekyll.
- **Bundler Installation:** (`gem install bundler`) Required to manage dependencies.
- **Jekyll Installation:** Typically managed via Bundler (`bundle install` using the `Gemfile`).
- **Local Server:** Jekyll provides a built-in server (`bundle exec jekyll serve`) for local development and previewing.

**Technical Constraints:**
- The site must be buildable by the version of Jekyll supported by GitHub Pages.
- File paths for assets (images, CSS) must be relative and correctly handled by Jekyll/Liquid (e.g., using `{{ site.baseurl }}/assets/...` or relative paths from the generated file location).
- Custom plugins might not be supported by GitHub Pages unless explicitly allowed.

**Dependencies:**
- Ruby runtime.
- Gems listed in `Gemfile` (Jekyll, potentially themes, plugins).

**Tool Usage Patterns:**
- Editing Markdown (`.md`), HTML (`.html`), SCSS (`.scss`), and YAML (`.yml`) files.
- Running `bundle install` to install/update dependencies.
- Running `bundle exec jekyll serve` to build the site and run a local development server.
- Using `git` commands to commit changes and push to the GitHub repository. GitHub Pages automatically rebuilds the site upon pushing to the configured branch.
