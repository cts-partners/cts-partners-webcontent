# Deployment Guide

This document outlines how to deploy the CTS Partners website content from this repository to the Web3-hosted site.

## Architecture Overview

The CTS Partners website uses a decoupled architecture:

1. **Content Repository (GitHub):** This repository stores all content as markdown files
2. **Web3 Hosting:** The website is hosted on Web3 infrastructure
3. **Rendering System:** An HTML/JS application loads markdown content and renders it with consistent styling

## Content Loading System

### Approach

The website uses a JavaScript-based content loader that:

1. Fetches markdown files from this GitHub repository (or a CDN mirror)
2. Parses the markdown into HTML
3. Applies consistent styling (fonts, colors, spacing)
4. Injects the rendered content into the appropriate page sections

### Implementation

```javascript
// Example content loader structure
async function loadPageContent(pageName) {
  // Fetch markdown from GitHub or CDN
  const response = await fetch(`/content/pages/${pageName}.md`);
  const markdown = await response.text();
  
  // Parse markdown to HTML
  const html = markdownParser.parse(markdown);
  
  // Apply styling and inject into page
  document.getElementById('content').innerHTML = html;
  applyStyles();
}
```

### Benefits

- **Easy Updates:** Content can be updated without touching code
- **Version Control:** All changes tracked in Git
- **Separation of Concerns:** Content and presentation are decoupled
- **Web3 Compatible:** Static content that can be distributed across decentralized networks

## Deployment Workflow

### 1. Content Updates

```bash
# Make content changes locally
git checkout -b content/your-update

# Edit content files
vim content/pages/services.md

# Commit and push
git add .
git commit -m "Update services page with new offering"
git push origin content/your-update
```

### 2. Review and Merge

- Create pull request on GitHub
- Review changes
- Merge to `develop` branch for staging
- Test on staging environment
- Merge to `main` branch for production

### 3. Deployment

**Option A: Automatic Deployment (Recommended)**

Set up GitHub Actions to automatically deploy on merge to `main`:

```yaml
# .github/workflows/deploy.yml
name: Deploy to Web3
on:
  push:
    branches: [main]
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Deploy to IPFS
        run: |
          # Deploy content to IPFS or other Web3 storage
          # Update DNS records if needed
```

**Option B: Manual Deployment**

```bash
# Pull latest content
git pull origin main

# Deploy to Web3 hosting
# (specific commands depend on hosting provider)
```

## Content Structure for Rendering

### Page Format

Each page markdown file should follow this structure:

```markdown
# Page Title

## Section 1 Heading

Content for section 1...

## Section 2 Heading

Content for section 2...
```

### Frontmatter (Optional)

For advanced features, add YAML frontmatter:

```markdown
---
title: "Services | CTS Partners"
description: "Comprehensive M&A and technology advisory services"
keywords: ["technical due diligence", "M&A", "private equity"]
---

# Services

Content here...
```

## Styling Configuration

The rendering system should apply consistent styling:

```css
/* Example styling configuration */
h1 { 
  font-family: 'Inter', sans-serif;
  font-size: 3rem;
  font-weight: 700;
  color: #1a1a1a;
}

h2 {
  font-family: 'Inter', sans-serif;
  font-size: 2rem;
  font-weight: 600;
  color: #2a2a2a;
  margin-top: 2rem;
}

p {
  font-family: 'Inter', sans-serif;
  font-size: 1.125rem;
  line-height: 1.75;
  color: #4a4a4a;
}
```

## Testing

### Local Testing

1. Clone the repository
2. Run a local web server
3. Test content loading and rendering
4. Verify all links and formatting

### Staging Environment

- Deploy to `develop` branch first
- Test on staging URL
- Verify content, styling, and functionality
- Get approval before production deployment

### Production Deployment

- Merge to `main` branch
- Automatic or manual deployment to Web3
- Verify production site
- Monitor for issues

## Rollback Procedure

If issues are discovered after deployment:

```bash
# Revert to previous commit
git revert HEAD
git push origin main

# Or reset to specific commit
git reset --hard <commit-hash>
git push --force origin main
```

## Monitoring

- Monitor GitHub repository for content changes
- Track deployment success/failures
- Monitor website for broken links or rendering issues
- Set up alerts for deployment failures

## Troubleshooting

### Content Not Updating

1. Check if changes were merged to `main`
2. Verify deployment completed successfully
3. Clear browser cache
4. Check CDN cache (may need to invalidate)

### Rendering Issues

1. Validate markdown syntax
2. Check for special characters that need escaping
3. Verify frontmatter format (if used)
4. Test locally before deploying

### Performance Issues

1. Optimize image sizes in `assets/images/`
2. Consider lazy loading for large pages
3. Implement caching strategy
4. Use CDN for content delivery

## Security Considerations

- Repository should be private or carefully managed if public
- Use environment variables for any API keys
- Implement rate limiting on content API
- Regularly update dependencies
- Monitor for unauthorized changes

## Future Enhancements

Potential improvements to the deployment system:

- **Content Preview:** Preview changes before merging
- **A/B Testing:** Test different content variations
- **Analytics Integration:** Track content performance
- **Search Functionality:** Full-text search across content
- **Multi-language Support:** Internationalization of content

## Support

For deployment issues or questions:

- **Technical Issues:** Open an issue on GitHub
- **Content Questions:** Contact CTS Partners marketing team
- **Emergency:** Contact repository administrator

Last updated: January 2026
