# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Hugo static site generator project for Nikita Fedosov's personal website (fedosov.net). The site uses the "hello-friend-ng" theme and is configured for Russian language content.

## Common Commands

### Development and Building
```bash
# Serve the site locally with live reload (requires Hugo installation)
hugo server

# Build the static site for production
hugo

# Build with drafts included
hugo -D
```

### Theme Management
```bash
# Update theme submodule
git submodule update --remote themes/hello-friend-ng

# Initialize theme submodule (if cloning fresh)
git submodule update --init --recursive
```

## Project Structure

- `hugo.toml` - Main Hugo configuration file with site settings, theme configuration, and menu structure
- `content/` - Markdown content files:
  - `about.md` - About page content in Russian
  - `index.md123` - Home page content with portrait image shortcode
  - `images/` - Content images (portrait photo)
- `themes/hello-friend-ng/` - Git submodule containing the Hugo theme
- `static/` - Static assets (favicons, icons)
- `public/` - Generated static site (build output, should be ignored)
- `resources/` - Hugo's generated resources cache

## Key Configuration

The site is configured in `hugo.toml` with:
- Russian language (`ru-ru`)
- Personal branding for Nikita Fedosov (TeamLead | QAA Engineer)
- Social links to GitHub, Telegram, and email
- Custom logo and portrait settings
- Disabled sharing buttons and language menu

## Content Management

- Content is written in Markdown with Hugo front matter
- The site uses Hugo shortcodes (e.g., `{{< image >}}` for the portrait)
- Menu structure is defined in the configuration file
- The theme supports both light and dark modes

## Prerequisites

This project requires Hugo to be installed locally for development and building. The theme is managed as a Git submodule.