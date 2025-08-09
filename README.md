# MCP Plugins Registry

> 🌐 Community-maintained registry for Model Context Protocol plugins - discover, share, and distribute MCP plugins

## Overview

The MCP Plugins Registry is a central hub for discovering and sharing plugins built with the [MCP Protocol SDK](https://github.com/prismworks-ai/mcp-protocol-sdk). This registry helps developers find existing plugins and share their own creations with the community.

## 🔍 Finding Plugins

### Browse the Registry

View the complete list of plugins in [registry.json](registry.json) or use our search API.

### Categories

- **Database**: PostgreSQL, MongoDB, MySQL, Redis connectors
- **Integrations**: Stripe, Slack, Discord, GitHub, GitLab
- **AI/ML**: OpenAI, Anthropic, Hugging Face, LangChain
- **Cloud**: AWS, Azure, GCP, Cloudflare
- **DevOps**: Docker, Kubernetes, Terraform, Ansible
- **Analytics**: Prometheus, Grafana, DataDog, New Relic
- **Communication**: Email, SMS, Push notifications
- **Storage**: S3, MinIO, FTP, SFTP
- **Utilities**: JSON/XML processing, encryption, compression

## 📦 Submitting Your Plugin

### Requirements

1. Plugin must be built with MCP Protocol SDK
2. Include proper documentation
3. Provide example usage
4. Specify compatible MCP SDK version
5. Include license information

### Submission Process

1. Fork this repository
2. Add your plugin to `registry.json`
3. Update category listings if needed
4. Submit a pull request

### Registry Entry Format

```json
{
  "name": "your-plugin-name",
  "version": "1.0.0",
  "description": "Brief description of what your plugin does",
  "author": "Your Name or Organization",
  "repository": "https://github.com/username/plugin-repo",
  "category": ["primary-category", "secondary-category"],
  "keywords": ["mcp", "plugin", "your", "keywords"],
  "mcp_sdk_version": ">=0.6.0",
  "license": "MIT",
  "homepage": "https://your-plugin-docs.com",
  "pricing": "free" | "paid" | "freemium",
  "marketplace_url": "optional-marketplace-listing-url"
}
```

## 🚀 Using Plugins

### Installation

Plugins can be installed directly from their repositories:

```bash
# Using cargo
cargo add plugin-name --git https://github.com/author/plugin-name

# Or add to Cargo.toml
[dependencies]
plugin-name = { git = "https://github.com/author/plugin-name" }
```

### Basic Usage

```rust
use mcp_protocol_sdk::plugin::PluginLoader;
use your_plugin::YourPlugin;

#[tokio::main]
async fn main() -> Result<(), Box<dyn std::error::Error>> {
    let mut loader = PluginLoader::new();
    loader.register_plugin(YourPlugin::new()).await?;
    
    // Plugin is now available in your MCP application
    Ok(())
}
```

## 🛠️ API Access

### REST API Endpoints

- `GET /api/plugins` - List all plugins
- `GET /api/plugins/:name` - Get specific plugin details
- `GET /api/categories` - List all categories
- `GET /api/search?q=query` - Search plugins

### Example API Usage

```bash
# Search for database plugins
curl https://api.mcp-registry.dev/search?category=database

# Get specific plugin info
curl https://api.mcp-registry.dev/plugins/postgres-connector
```

## 🌟 Featured Plugins

### Most Popular

1. **postgres-connector** - Full-featured PostgreSQL integration
2. **stripe-payments** - Complete Stripe payment processing
3. **openai-bridge** - OpenAI API integration with streaming
4. **slack-bot** - Slack workspace integration
5. **s3-storage** - AWS S3 compatible storage

### New & Noteworthy

- **mongodb-atlas** - MongoDB Atlas cloud database connector
- **discord-events** - Discord bot and event handling
- **github-actions** - GitHub Actions workflow integration

## 📊 Statistics

- Total Plugins: **0** (registry just created!)
- Categories: **10**
- Contributors: **0**
- Weekly Downloads: **0**

## 🤝 Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

### Ways to Contribute

1. Submit your plugins
2. Improve registry infrastructure
3. Add search/filter features
4. Create plugin templates
5. Write documentation
6. Review submissions

## 📄 License

This registry is MIT licensed. Individual plugins may have their own licenses.

## 🔗 Resources

- [MCP Protocol SDK](https://github.com/prismworks-ai/mcp-protocol-sdk)
- [Plugin Development Guide](https://github.com/prismworks-ai/mcp-plugins)
- [MCP Developer Tools](https://github.com/prismworks-ai/mcp-dev)
- [Official Documentation](https://prismworks.ai/docs)
- [Community Discord](https://discord.gg/mcp-community)

## 🏢 Professional Support

For advanced features, automated containerization, and marketplace distribution, check out [MCP Platform](https://prismworks.ai/platform).

---

*Maintained by the MCP community. Not officially affiliated with Anthropic.*
