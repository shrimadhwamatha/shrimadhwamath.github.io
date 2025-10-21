# AI Agent Instructions for shrimadhwamath.github.io

This is a Jekyll-based blog using the Chirpy theme. Here's what you need to know to work effectively with this codebase:

## Project Structure

- `_posts/` - Blog post content in Markdown format
- `_tabs/` - Static pages like About, Archives, etc.
- `_data/` - YAML files for configurable content (contact.yml, share.yml)
- `assets/` - Static assets (images, CSS, JS)
- `_config.yml` - Main Jekyll configuration
- `tools/` - Build and development scripts

## Development Workflow

### Local Development

1. Use the configured VS Code task "Run Jekyll Server" or run:
   ```bash
   ./tools/run.sh
   ```
   - Add `-p` flag for production mode
   - Add `-H hostname` to change host binding

2. For production builds use VS Code task "Build Jekyll Site" or:
   ```bash
   ./tools/test.sh
   ```
   This runs tests and HTML validation.

### Content Patterns

- Posts must be in `_posts/` with filename format: `YYYY-MM-DD-title.md`
- Front matter requirements:
  ```yaml
  ---
  title: Post Title
  date: YYYY-MM-DD HH:MM:SS +/-TTTT
  categories: [Category1, Category2]
  tags: [tag1, tag2]
  ---
  ```
- Images should be placed in `assets/img/` and referenced as `/assets/img/filename`

### Configuration

The site's main configuration is in `_config.yml`. Key sections:
- SEO settings (`title`, `tagline`, `description`)
- Social media links
- Analytics configurations
- Comments system setup (Disqus/Utterances/Giscus)

## Common Tasks

1. Adding a new post:
   - Create file in `_posts/` with correct date prefix
   - Include required front matter
   - Add images to `assets/img/` if needed

2. Modifying site navigation:
   - Edit files in `_tabs/` directory
   - Update `_data/*.yml` files for shared components

3. Theme customization:
   - CSS changes should be made via SASS in `_sass/` directory
   - Jekyll processes these during build

## Testing

The `tools/test.sh` script runs:
- Jekyll build in production mode
- HTML validation
- Link checking (internal only by default)