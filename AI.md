# AI Rules & Project Standards for laniksj.github.io

## Repository Overview

laniksj.github.io is a GitHub Pages site for personal web content and portfolio.

## Code Standards and Practices

### Web Standards

- Follow modern HTML5, CSS3, and JavaScript best practices.
- Implement responsive design for mobile and desktop.
- Ensure accessibility compliance (WCAG guidelines).
- Optimize for performance and loading speed.

### Documentation Standards

- Include clear content management and deployment procedures.
- Document site features, customization options, and themes.
- Provide contribution guidelines for content updates.
- Use markdown formatting consistently.

### Markdown Compliance Requirements (MANDATORY)

- **ALL markdown files (.md) MUST pass markdownlint validation with zero errors or warnings**
- Run `markdownlint <filename>` on every markdown file before considering it complete
- Follow the project's `.markdownlint.json` configuration strictly
- Address ALL markdownlint issues immediately - no exceptions or workarounds
- Common requirements include:
  - Maximum line length of 120 characters (MD013).
  - Consistent heading styles and hierarchy
  - Proper list formatting and indentation
  - Blank lines around headings and code blocks
  - Consistent link and reference formatting
  - No trailing whitespace
  - Files must end with newlines
  - Proper table formatting when applicable
- Use `markdownlint --fix <filename>` for auto-fixable issues when available
- Validate markdown files in CI/CD pipelines where applicable

## Development Guidelines

### When Making Changes

- Preserve existing functionality unless explicitly asked to change it
- Update documentation when adding new content or modifying site features
- Test changes across different browsers and devices
- **Always run markdownlint and fix all issues in markdown files before considering changes complete**

### GitHub Pages Standards

- Maintain Jekyll compatibility for static site generation.
- Implement proper front matter and markdown processing.
- Use appropriate GitHub Pages themes and configurations.
- Test deployment builds and final rendered output.

## GitHub & Automation Standards

These rules apply specifically to files in `.github/*` (workflows, templates, and documentation).

### Quality Gates (MANDATORY)

Before completing any change in `.github/`:

1. ✅ Run `markdownlint` validation (if .md file).
2. ✅ Ensure project standards are followed.
3. ✅ Verify contribution guidelines are up-to-date.
4. ✅ Check that automation maintains project standards.

### Templates and Workflows

- Ensure issue and pull request templates provide clear, actionable guidelines.
- Include project-specific troubleshooting sections in templates.
- Reference existing project documentation and standards.

### Documentation standards in .github/

- `.github/CONTRIBUTING.md` must include:
  - Development environment setup instructions.
  - Testing requirements and procedures.
  - Documentation standards for new features.
  - Project-specific contribution guidelines.

### Automation and CI/CD

- Project workflows must include automated testing stages.
- Code quality checks must be integrated into CI/CD.
- Release automation must be properly configured.

### Error Prevention

- NEVER generate markdown that violates line length or formatting rules.
- ALWAYS cross-reference with existing project practices before making changes.
- ENSURE all links and references are valid and current.
- VALIDATE that new requirements don't conflict with established workflows.
