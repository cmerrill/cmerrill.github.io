# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a personal website for Christopher Merrill built with Jekyll and deployed on GitHub Pages. The site uses the Minima theme with extensive custom styling featuring an orange accent color (#F18D05) that reflects the previous notspelledright.com design.

## Development Commands

### Local Development
```bash
# Install dependencies (first time setup)
bundle install

# Run local development server
bundle exec jekyll serve

# Access at http://localhost:4000
```

### Deployment
The site deploys automatically to GitHub Pages when pushing to the `gh-pages` branch.

## Architecture

### Site Structure
- **Content**: The main page content is in [index.md](index.md) using Jekyll's default layout
- **Configuration**: Site metadata and build settings in [_config.yml](_config.yml)
- **Styling**: Custom SCSS in [assets/css/style.scss](assets/css/style.scss) that extends the Minima theme
- **Theme**: Uses the `minima` theme via the `github-pages` gem (~> 232)

### Styling Architecture
The custom stylesheet ([assets/css/style.scss](assets/css/style.scss)) imports the base Minima theme and overrides it with custom styles:

- **Color Scheme**:
  - Primary orange: `#F18D05` (used for accents, borders, hovers)
  - Text gray: `#616161` (used for h3 headings)
  - Text black: `#000` (primary text)

- **Typography**:
  - Body: Helvetica Neue/Helvetica/Arial stack
  - Headings: Ubuntu font (loaded via Google Fonts)

- **Layout Components**:
  - `.home` sections: Each content section has orange bottom borders
  - `.contact-list`: Unstyled list for contact information
  - `.project-list`: Custom bullet styling with orange arrows (▸)
  - 800px max-width wrapper for content

- **Interactive Elements**:
  - Links: Black by default, orange on hover with bottom border transition
  - Site header: 5px orange top border

### Content Organization
The [index.md](index.md) file uses semantic HTML within markdown:
- Wrapped in `<div class="home">` for styling hooks
- Sections: About, Contact, Hobbies & Personal Projects
- Uses specific class names (`.contact-list`, `.project-list`) for targeted styling

## Important Configuration Details

- **GitHub Pages**: Uses `github-pages` gem for compatibility
- **Base URL**: Empty string for root domain deployment (cmerrill.github.io)
- **Excluded from build**: `old/` directory, Gemfile, Gemfile.lock, node_modules, vendor/
- **Jekyll Plugins**: jekyll-seo-tag included
- **Platform-specific**: Includes Windows-specific gems (wdm, tzinfo-data)

## Editing Guidelines

### Adding New Pages
Create `.md` files in the root directory with Jekyll front matter:
```yaml
---
layout: default
title: Page Title
---
```

### Modifying Styles
All custom styles are centralized in [assets/css/style.scss](assets/css/style.scss). The file uses SCSS syntax with variables and nesting. Maintain the orange color theme (#F18D05) for consistency.

### Content Updates
Edit [index.md](index.md) directly. The file mixes markdown with HTML for precise layout control. Maintain the existing section structure and class names to preserve styling.
