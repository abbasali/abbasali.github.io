# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Jekyll-based academic portfolio website using the al-folio theme. It's designed to showcase academic work, blog posts, CV, publications, and projects.

## Development Commands

### Jekyll Build and Serve
```bash
# Install dependencies
bundle install

# Serve locally with auto-reload
bundle exec jekyll serve

# Build for production
bundle exec jekyll build

# Clean build artifacts
bundle exec jekyll clean
```

### Formatting
```bash
# Format code with Prettier
npx prettier --write .
```

## Architecture

### Key Directories
- `_pages/`: Main site pages (about, blog, CV, projects, etc.)
- `_posts/`: Blog posts in Markdown format
- `_layouts/`: HTML templates for different page types
- `_includes/`: Reusable template components
- `_sass/`: SCSS stylesheets
- `_data/`: YAML data files (CV, repositories, socials)
- `_plugins/`: Custom Jekyll plugins
- `assets/`: Static assets (images, PDFs, JSON, CSS, JS)
- `_bibliography/`: BibTeX files for publications

### Content Management
- Blog posts use front matter with categories and tags
- CV data comes from `assets/json/resume.json` (JSON Resume format) or `_data/cv.yml`
- Publications are managed through BibTeX files in `_bibliography/`
- Social links and external data configured in `_data/` YAML files

### Key Features
- Responsive design with light/dark mode
- Blog with categorization and tagging
- Academic publications with BibTeX integration
- CV generation from structured data
- Image optimization with WebP conversion
- Math typesetting via MathJax
- Search functionality
- Analytics integration (Google Analytics)
- Comments via Giscus

### Configuration
- Main config: `_config.yml`
- Jekyll plugins and gems: `Gemfile`
- Package management: `package.json` (for Prettier only)

### Styling
- Bootstrap-based responsive design
- Custom SCSS in `_sass/` directory
- Theme colors configurable in `_sass/_themes.scss`
- Font Awesome icons supported

## Content Guidelines

### Blog Posts
- Place in `_posts/` with format: `YYYY-MM-DD-title.md`
- Use front matter for metadata (title, date, categories, tags)
- Categories and tags are used for organization and display

### Images
- Store in `assets/img/`
- Automatically optimized to WebP format at multiple sizes
- Use relative paths in Markdown

### Publications
- Add BibTeX entries to `_bibliography/papers.bib`
- Supports additional fields like PDF links, code repos, etc.

## Development Notes

- Site builds to `_site/` directory
- Uses Jekyll Scholar for publication management
- Imagemagick required for image optimization
- Supports Jupyter notebooks in `assets/jupyter/`
- External links automatically get security attributes