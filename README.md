# notspelledright.com

Personal website of Chris Merrill, built with Jekyll and hosted on GitHub Pages.

## Features

- Clean, minimal design with orange accent color (#F18D05)
- Responsive layout optimized for mobile and desktop
- Sections for bio, work history, contact info, hobbies, and projects
- GitHub Pages compatible

## Local Development

To run this site locally:

1. Install Ruby and Bundler (if not already installed)
2. Install dependencies:
   ```bash
   bundle install
   ```
3. Run the Jekyll server:
   ```bash
   bundle exec jekyll serve
   ```
4. Visit `http://localhost:4000` in your browser

## Deployment to GitHub Pages

This site is configured to deploy automatically to GitHub Pages at `https://cmerrill.github.io`.

1. Commit your changes:
   ```bash
   git add .
   git commit -m "Initial Jekyll site"
   ```
2. Push to GitHub:
   ```bash
   git push origin master
   ```
3. GitHub Pages will automatically build and deploy your site

## Customization

### Editing Content

- Main page content: Edit [`index.md`](index.md)
- Site configuration: Edit [`_config.yml`](_config.yml)

### Styling

- Custom styles: Edit [`assets/css/style.scss`](assets/css/style.scss)
- Primary orange color: `#F18D05`
- This stylesheet extends the Minima theme

### Adding Pages

Create new `.md` files in the root directory with front matter:

```yaml
---
layout: default
title: Page Title
---

Your content here...
```

## Project Structure

```
.
├── _config.yml          # Site configuration
├── index.md             # Home page content
├── Gemfile              # Ruby dependencies
├── assets/
│   └── css/
│       └── style.scss   # Custom styles
└── old/                 # Previous website files (excluded from build)
```

## License

Personal website - All rights reserved.
