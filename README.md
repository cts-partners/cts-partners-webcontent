# CTS Partners Website Content Repository

This repository contains all content for the CTS Partners website, organized as markdown files for easy maintenance and Web3 hosting.

## Repository Structure

```
cts-partners-webcontent/
├── README.md                          # This file
├── CONTRIBUTING.md                    # Guidelines for content updates
├── markdown-renderer.html             # Standalone markdown renderer for Web3
├── content/                           # Main content directory
│   ├── pages/                         # Page-level content
│   │   ├── about.md                   # About page content
│   │   ├── value-creation.md          # Value Creation page content
│   │   ├── ma-strategy.md             # M&A Strategy page content
│   │   ├── services.md                # Services page content
│   │   ├── aria.md                    # ARIA page content
│   │   └── home.md                    # Homepage content
│   ├── sections/                      # Reusable section content
│   │   ├── hero/                      # Hero section variants
│   │   ├── team/                      # Team member bios
│   │   └── testimonials/              # Client testimonials
│   └── shared/                        # Shared content snippets
│       ├── footer.md                  # Footer content
│       ├── contact-info.md            # Contact information
│       └── legal.md                   # Legal disclaimers
├── assets/                            # Media assets
│   ├── images/                        # Image files
│   └── documents/                     # Downloadable documents
└── docs/                              # Documentation
    ├── content-guidelines.md          # Content writing guidelines
    ├── style-guide.md                 # Brand voice and style guide
    └── deployment.md                  # Deployment instructions
```

## Content Organization

### Pages

Each page in the website has a corresponding markdown file in the `content/pages/` directory. These files contain the main content for each page, organized by sections.

### Sections

Reusable sections (like team bios, testimonials, etc.) are stored in `content/sections/` and can be referenced by multiple pages.

### Shared Content

Common elements like footer content, contact information, and legal text are stored in `content/shared/` for consistency across the site.

## Content Format

All content is written in GitHub-flavored Markdown with the following conventions:

- **Headers:** Use `#` for page titles, `##` for major sections, `###` for subsections
- **Emphasis:** Use `**bold**` for key terms and concepts
- **Lists:** Use `-` for unordered lists, `1.` for ordered lists
- **Links:** Use `[text](url)` for inline links
- **Tables:** Use standard Markdown table syntax for structured data

## Editing Content

### Quick Edits

For minor content updates:

1. Navigate to the file you want to edit
2. Click the "Edit" button (pencil icon)
3. Make your changes
4. Commit with a descriptive message

### Major Updates

For significant content changes:

1. Clone the repository locally
2. Create a new branch: `git checkout -b content/your-update-name`
3. Make your changes
4. Commit and push: `git push origin content/your-update-name`
5. Create a pull request for review

## Content Guidelines

### Voice and Tone

- **Professional yet approachable:** We are experts, but we speak in clear, accessible language
- **Action-oriented:** Focus on outcomes and value delivered
- **Confident without arrogance:** Demonstrate expertise through results, not claims
- **Forward-looking:** Emphasize innovation, AI, and the future of M&A

### Writing Style

- Use active voice whenever possible
- Keep sentences concise and clear
- Avoid jargon unless necessary (and define it when used)
- Write in complete paragraphs, not bullet points (except for lists)
- Use specific examples and metrics where available

### SEO Considerations

- Include relevant keywords naturally in content
- Use descriptive headers that reflect page content
- Write meta descriptions for each page (stored in frontmatter)
- Use alt text for all images

## Markdown Renderer

This repository includes `markdown-renderer.html`, a standalone HTML file that fetches and renders markdown content with professional styling.

### Quick Start

**Option 1: Embed with URL Parameter**
```html
<iframe src="markdown-renderer.html?url=YOUR_RAW_GITHUB_URL" width="100%" height="600" frameborder="0"></iframe>
```

**Option 2: Embed Code Block**
Paste the entire HTML file content into your Web3 platform's embed code block.

**Option 3: Direct Link**
Open `markdown-renderer.html` in a browser - it loads `home.md` by default.

### Features

- **Embeddable:** Single HTML file designed for iframe or code block embedding
- **Transparent background:** 80% transparent with purple gradient border
- **No controls:** Clean interface, content only
- **URL parameter loading:** Pass content via `?url=` or `?md=` parameter
- **Responsive:** Fills container width naturally
- **Professional styling:** Dark theme with golden ratio typography
- **Web3 ready:** Can be hosted on IPFS, Arweave, or traditional web servers
- **Complete markdown support:** Headers, lists, tables, code blocks, images, etc.

### Getting Raw URLs from GitHub

1. Navigate to any `.md` file in this repository
2. Click the "Raw" button
3. Copy the URL from your browser (starts with `raw.githubusercontent.com`)
4. Use as the `?url=` parameter

**Example URLs:**
- Home: `?url=https://raw.githubusercontent.com/cts-partners/cts-partners-webcontent/main/content/pages/home.md`
- About: `?url=https://raw.githubusercontent.com/cts-partners/cts-partners-webcontent/main/content/pages/about.md`
- Services: `?url=https://raw.githubusercontent.com/cts-partners/cts-partners-webcontent/main/content/pages/services.md`

### Customization

The renderer uses CSS variables for easy customization. Edit the `:root` section in the HTML file to change:

- Colors (background, text, accent)
- Typography (font sizes, families, weights)
- Spacing (margins, padding)

### Design System

**Typography Scale (Golden Ratio: 1.618)**
- H1: 76px (bold)
- H2: 47px (semi-bold)
- H3: 29px (semi-bold)
- Body: 18px (normal)

**Color Palette**
- Background: #0a0e1a (dark navy)
- Text Primary: #ffffff (white)
- Text Secondary: #b8c1d9 (light gray)
- Accent: #6c5ce7 (purple)

**File Size:** ~6KB (well under Web3 embedding limits)

## Deployment

This content is designed to be consumed by a Web3-hosted website that:

1. Loads markdown files from this repository
2. Renders them with consistent styling using `markdown-renderer.html`
3. Applies the appropriate layout and navigation

See `docs/deployment.md` for detailed deployment instructions.

## Version Control

- **Main branch:** Production content (deployed to live site)
- **Develop branch:** Staging content (for review before deployment)
- **Feature branches:** Individual content updates (merged to develop, then main)

## Contact

For questions about content or repository access, contact:

- **Content Owner:** CTS Partners Team
- **Repository:** https://github.com/cts-partners/cts-partners-webcontent
- **Website:** https://www.cts-partners.com

## License

© 2025 Convergence Technology Solutions. All rights reserved.

This content is proprietary and confidential. Unauthorized use, reproduction, or distribution is prohibited.
