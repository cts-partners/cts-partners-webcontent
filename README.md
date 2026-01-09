# CTS Partners Website Content Repository

This repository contains all content for the CTS Partners website, organized as markdown files for easy maintenance and Web3 hosting.

## Repository Structure

```
cts-partners-webcontent/
├── README.md                          # This file
├── CONTRIBUTING.md                    # Guidelines for content updates
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

## Deployment

This content is designed to be consumed by a Web3-hosted website that:

1. Loads markdown files from this repository
2. Renders them with consistent styling
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
