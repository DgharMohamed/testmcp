---
layout: default
title: MCP — Model Context Protocol
---

<section class="hero">
  <div class="hero-inner">
    <div class="badge-row">
      <span class="badge badge-purple">Model Context Protocol</span>
      <span class="badge badge-pink">AI Powered</span>
      <span class="badge badge-teal">Open Standard &middot; 2024</span>
    </div>
    <h1>MCP</h1>
    <p class="subtitle"><em>The USB-C of AI Integration</em></p>
    <p class="tagline">
      An open standard that lets AI models securely connect to any tool,
      data source, or service &mdash; in a unified, plug-and-play way.
    </p>
    <div class="hero-cta">
      <a href="#what" class="btn btn-primary">Learn More</a>
      <a href="https://modelcontextprotocol.io" target="_blank" class="btn btn-outline">Official Docs &#x2197;</a>
    </div>
  </div>
</section>

<div class="divider"></div>

<section id="what" class="reveal">
  <p class="section-label">Overview</p>

  ## What is MCP?

  **Model Context Protocol** is an open protocol introduced by Anthropic in late 2024.
  It defines a universal language for AI assistants to communicate with external tools and live data sources.

  <div class="diagram">

  ```
  WITHOUT MCP                        WITH MCP
  ─────────────────────────────      ──────────────────────────────────────
  AI -- custom glue --> GitHub       AI
  AI -- custom glue --> Database      +---> MCP Client
  AI -- custom glue --> Filesystem              +---> MCP Server ---> GitHub
  AI -- custom glue --> Slack                   +---> MCP Server ---> Database
  AI -- custom glue --> AWS                     +---> MCP Server ---> Filesystem

       n x integrations                   1 standard, infinite tools
  ```

  </div>
</section>

<div class="divider"></div>

<section id="why" class="reveal">
  <p class="section-label">Importance</p>

  ## Why Does MCP Matter?

  Five reasons MCP is a fundamental shift in how AI agents are built.

  <div class="feature-grid">
    <div class="feature-card">
      <div class="feature-icon">🔒</div>
      <h3>Security First</h3>
      <p>Credentials stay inside the MCP server. The AI model never touches raw tokens or passwords. Every operation is scoped and auditable.</p>
    </div>
    <div class="feature-card">
      <div class="feature-icon">🔌</div>
      <h3>Plug-and-Play</h3>
      <p>Build one MCP server and any compatible AI can use it. No more writing custom glue code for every model or tool combination.</p>
    </div>
    <div class="feature-card">
      <div class="feature-icon">🌍</div>
      <h3>Open Standard</h3>
      <p>Community-driven and vendor-neutral. Works with Claude, Kiro, and any future system that adopts the protocol.</p>
    </div>
    <div class="feature-card">
      <div class="feature-icon">⚡</div>
      <h3>Real-Time Context</h3>
      <p>AI models read <em>live</em> data &mdash; current files, fresh API responses, real database records &mdash; not stale training snapshots.</p>
    </div>
    <div class="feature-card">
      <div class="feature-icon">🧩</div>
      <h3>Composability</h3>
      <p>Chain GitHub + Database + Browser tools in a single AI session. Servers compose without extra orchestration code.</p>
    </div>
    <div class="feature-card">
      <div class="feature-icon">📈</div>
      <h3>Growing Ecosystem</h3>
      <p>Hundreds of community servers already exist &mdash; GitHub, Slack, AWS, Postgres, Notion, Docker and more.</p>
    </div>
  </div>
</section>

<div class="divider"></div>

<section id="how" class="reveal">
  <p class="section-label">Architecture</p>

  ## How It Works

  MCP follows a clean three-layer client-server model.

  | Component | Role | Example |
  |-----------|------|---------|
  | 🧠 **MCP Host** | The AI application that wants access to tools | Kiro IDE, Claude Desktop |
  | 🔗 **MCP Client** | Lives inside the host, manages server connections | Built into Kiro |
  | ⚙️ **MCP Server** | Exposes tools, resources, and data | GitHub MCP, Postgres MCP |

</section>

<div class="divider"></div>

<section id="setup" class="reveal">
  <p class="section-label">Quick Start</p>

  ## Set Up in 30 Seconds

  Add an MCP server to Kiro IDE by editing one JSON file:

  ```json
  {
    "mcpServers": {
      "github-mcp-server": {
        "url": "https://api.githubcopilot.com/mcp/",
        "headers": {
          "Authorization": "Bearer YOUR_GITHUB_TOKEN"
        },
        "disabled": false
      }
    }
  }
  ```

  That's it. Kiro reconnects automatically and your AI can now interact with GitHub. ✅

</section>

<div class="divider"></div>

<section id="compare" class="reveal">
  <p class="section-label">Comparison</p>

  ## MCP vs Traditional APIs

  | Feature | Traditional API | MCP |
  |---------|----------------|-----|
  | Setup per tool | ✅ Required every time | ❌ One standard for all |
  | Credential exposure | ⚠️ Risk of leakage | ✅ Stays in server |
  | AI compatibility | ❌ Per-model custom work | ✅ Universal |
  | Composability | ❌ Hard to chain tools | ✅ Built-in |
  | Community servers | ❌ None | ✅ Hundreds and growing |
  | Live data access | ⚠️ Manual implementation | ✅ Native |

</section>

<div class="divider"></div>

<section id="ecosystem" class="reveal">
  <p class="section-label">Ecosystem</p>

  ## Available MCP Servers

  The community has already built servers for the most popular tools and platforms.

  <div class="pill-grid">
    <span class="pill">GitHub</span> <span class="pill">GitLab</span>
    <span class="pill">Jira</span> <span class="pill">Notion</span>
    <span class="pill">Slack</span> <span class="pill">PostgreSQL</span>
    <span class="pill">SQLite</span> <span class="pill">MongoDB</span>
    <span class="pill">AWS</span> <span class="pill">Google Cloud</span>
    <span class="pill">Cloudflare</span> <span class="pill">Puppeteer</span>
    <span class="pill">Playwright</span> <span class="pill">Filesystem</span>
    <span class="pill">Docker</span> <span class="pill">Kubernetes</span>
    <span class="pill">Linear</span> <span class="pill">Figma</span>
    <span class="pill">Stripe</span> <span class="pill">Twilio</span>
  </div>
</section>

<div class="divider"></div>

<section id="summary" class="reveal summary-section">
  <p class="section-label">TL;DR</p>

  ## The Bottom Line

  <div class="quote-box">
    MCP turns your AI from a smart chatbot into a capable agent that can act in the real world &mdash;
    reading files, calling APIs, managing repos, querying databases &mdash; all securely,
    and with a single open standard.
  </div>

  <a href="https://modelcontextprotocol.io" target="_blank" class="btn btn-primary">Read the Official Docs &#x2197;</a>
</section>
