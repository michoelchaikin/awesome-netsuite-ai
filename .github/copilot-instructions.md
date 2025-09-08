# Copilot Instructions for Awesome NetSuite AI

## Project Overview
This is a curated **awesome list** focused on NetSuite AI resources, specifically the NetSuite AI Connector Service and MCP (Model Context Protocol) integration. It follows the [awesome list guidelines](https://github.com/sindresorhus/awesome) and uses `awesome-lint` for quality assurance.

## Key Architecture & Structure

### Content Organization
- **Main file**: `README.md` - Single source of truth containing all curated resources
- **Categories**: 6 main sections with emoji prefixes (🏢 Official Resources, 📚 Articles & Guides, etc.)
- **TOC Requirements**: Table of Contents must exactly match headings (including emojis) for lint compliance

### Quality Standards
- All entries must relate to NetSuite AI, MCP, or AI Connector Service
- Include author names for articles/guides and brief value descriptions
- Alphabetical ordering within sections
- Working links verified during contribution process

## Critical Developer Workflows

### Linting & Testing
```bash
npm run lint    # Runs awesome-lint with strict TOC validation
npm test        # Alias for lint command
```

### TOC Lint Rule Specifics
- TOC heading must be exactly "Contents" (not "📋 Contents")
- TOC links must match heading text exactly (including emojis)
- Anchor links use GitHub slugger format (emojis stripped)
- Example: `[🏢 Official Resources](#-official-resources)` → `## 🏢 Official Resources`

### CI/CD Pipeline
- GitHub Actions runs `awesome-lint` on all PRs and main branch pushes
- Node.js 18 environment with npm cache
- Lint failures block merges

## Project-Specific Conventions

### Link Descriptions
- Format: `[Title](url) - Description by Author Name.`
- Include author attribution for articles/guides
- End descriptions with periods
- Focus on value proposition, not feature lists

### Content Categories
- **Official Resources**: Oracle/NetSuite documentation
- **Articles & Guides**: Step-by-step tutorials and deep dives
- **Sample Code & Tools**: Downloadable code and custom tools
- **Videos & Tutorials**: Video content with clear learning outcomes
- **Use Cases & Examples**: Real-world implementations and demonstrations
- **Community**: Slack channels, forums, discussion spaces

### Adding New Entries
1. Verify link works and provides genuine value
2. Place in appropriate category alphabetically
3. Follow description format with author attribution
4. Run `npm run lint` to validate TOC compliance
5. Check that emoji headings match TOC links exactly

## Integration Points
- **awesome-lint**: Validates awesome list standards and TOC structure
- **GitHub Slugger**: Generates anchor links (strips emojis from headings)
- **GitHub Actions**: Automated linting on repository changes
- **CC0-1.0 License**: Public domain dedication for community contributions

## Common Pitfalls
- TOC links breaking when headings change (must update both simultaneously)
- Emoji handling in anchors (TOC text includes emojis, anchors strip them)
- Description format inconsistency (missing author names or periods)
- Category misplacement (content not matching section purpose)
