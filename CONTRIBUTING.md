# Contributing to MCP Plugins Registry

## How to Submit a Plugin

1. **Fork the Repository**
   ```bash
   gh repo fork prismworks-ai/mcp-plugins-registry
   ```

2. **Add Your Plugin Entry**
   Edit `registry.json` and add your plugin following the schema.

3. **Validate Your Entry**
   ```bash
   npm run validate  # Coming soon
   ```

4. **Submit Pull Request**
   ```bash
   gh pr create --title "Add [Plugin Name] to registry"
   ```

## Plugin Requirements

### Must Have
- [ ] Working implementation using MCP Protocol SDK
- [ ] README with installation and usage instructions
- [ ] License file
- [ ] Example code
- [ ] Version compatibility specified

### Nice to Have
- [ ] CI/CD badges
- [ ] Test coverage
- [ ] Documentation site
- [ ] Demo video or GIF
- [ ] Benchmarks

## Review Process

1. Automated validation checks
2. Community review (48 hours)
3. Maintainer approval
4. Merge and deployment

## Code of Conduct

Be respectful, inclusive, and helpful. We're building a community together!

## Questions?

Open an issue or join our Discord community.
