# Contributing to CTS Partners Website Content

Thank you for contributing to the CTS Partners website content! This guide will help you make effective content updates.

## Before You Start

- Familiarize yourself with the brand voice and style guidelines in `docs/style-guide.md`
- Review the content structure in `README.md`
- Ensure you have the necessary permissions to edit content

## Content Update Process

### 1. Identify the Content to Update

Determine which file(s) need to be updated:

- **Page content:** `content/pages/`
- **Team bios:** `content/sections/team/`
- **Testimonials:** `content/sections/testimonials/`
- **Shared content:** `content/shared/`

### 2. Make Your Changes

#### For Small Updates (Typos, Minor Edits)

1. Navigate to the file on GitHub
2. Click the "Edit" button (pencil icon)
3. Make your changes in the web editor
4. Preview your changes using the "Preview" tab
5. Add a descriptive commit message
6. Commit directly to the `develop` branch

#### For Larger Updates (New Sections, Major Rewrites)

1. Clone the repository:
   ```bash
   git clone https://github.com/cts-partners/cts-partners-webcontent.git
   cd cts-partners-webcontent
   ```

2. Create a new branch:
   ```bash
   git checkout -b content/descriptive-name
   ```

3. Make your changes in your preferred editor

4. Preview your changes locally (if you have a markdown previewer)

5. Commit your changes:
   ```bash
   git add .
   git commit -m "Brief description of changes"
   ```

6. Push your branch:
   ```bash
   git push origin content/descriptive-name
   ```

7. Create a pull request on GitHub

### 3. Review and Approval

- All content changes should be reviewed before merging to `main`
- Tag appropriate reviewers in your pull request
- Address any feedback or requested changes
- Once approved, merge to `develop` first, then to `main`

## Content Standards

### Markdown Formatting

- Use consistent header levels (`#`, `##`, `###`)
- Leave blank lines between paragraphs
- Use `**bold**` for emphasis, not `*italic*` (unless specifically needed)
- Use `-` for unordered lists, `1.` for ordered lists
- Indent nested lists with 2 spaces

### Writing Guidelines

**DO:**
- Write in active voice
- Use specific, concrete examples
- Keep paragraphs focused on one idea
- Use headers to organize content
- Include metrics and results where possible

**DON'T:**
- Use excessive jargon or buzzwords
- Write in passive voice
- Create walls of text without breaks
- Make unsubstantiated claims
- Use overly promotional language

### Brand Voice Checklist

Before submitting content, ask yourself:

- [ ] Is this written in a professional yet approachable tone?
- [ ] Does it focus on client outcomes and value?
- [ ] Is it specific and concrete (not vague or generic)?
- [ ] Does it demonstrate expertise without being arrogant?
- [ ] Is it forward-looking and innovation-focused?

## Commit Message Guidelines

Write clear, descriptive commit messages:

**Good:**
- `Update team bio for Matt Gordon with recent achievements`
- `Add new case study to Value Creation page`
- `Fix typo in Services page header`

**Bad:**
- `Update`
- `Changes`
- `Fix stuff`

## Questions or Issues?

If you have questions about:

- **Content strategy:** Contact the CTS Partners marketing team
- **Technical issues:** Open an issue on GitHub
- **Repository access:** Contact the repository administrator

## Code of Conduct

- Be respectful and professional in all communications
- Provide constructive feedback on pull requests
- Keep content accurate and up-to-date
- Maintain confidentiality of proprietary information
