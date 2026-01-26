# Novalysis Website

A Hugo-based marketing website for Novalysis - the Microsoft 365 Migration Planning platform.

## Development

### Prerequisites

- [Hugo Extended](https://gohugo.io/installation/) (v0.120.0 or later)
- Git

### Local Development

```bash
# Clone the repository
git clone https://github.com/glaicier/novalysis-website.git
cd novalysis-website

# Initialize theme submodule
git submodule update --init --recursive

# Start development server
hugo server -D
```

The site will be available at `http://localhost:1313/`

### Building for Production

```bash
hugo --minify
```

The built site will be in the `public/` directory.

## Deployment

This site is configured for deployment on Cloudflare Pages.

### Cloudflare Pages Setup

1. Connect your GitHub repository to Cloudflare Pages
2. Configure build settings:
   - **Build command:** `hugo --minify`
   - **Build output directory:** `public`
   - **Environment variable:** `HUGO_VERSION` = `0.154.5`

### Custom Domain

Configure your custom domain in Cloudflare Pages dashboard after initial deployment.

## Structure

```
novalysis-website/
├── content/           # Markdown content
│   ├── _index.md     # Homepage
│   ├── features.md   # Features page
│   ├── solutions.md  # Solutions page
│   ├── security.md   # Security page
│   ├── about.md      # About page
│   └── contact.md    # Contact page
├── static/           # Static assets (images, etc.)
├── themes/           # Hugo themes (PaperMod)
├── hugo.toml         # Hugo configuration
└── README.md         # This file
```

## Content Updates

Edit the Markdown files in `content/` to update website content. The site will automatically rebuild when changes are pushed to the main branch.

## Theme

This site uses the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme, included as a Git submodule.

To update the theme:

```bash
git submodule update --remote themes/PaperMod
```

## License

Website content © Novalysis. Theme (PaperMod) is MIT licensed.
