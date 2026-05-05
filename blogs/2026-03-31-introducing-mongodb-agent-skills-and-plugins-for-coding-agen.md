---
title: "Introducing MongoDB Agent Skills and Plugins for Coding Agents"
url: "https://www.mongodb.com/company/blog/product-release-announcements/introducing-mongodb-agent-skills"
date: "Tue, 31 Mar 2026 13:00:00 GMT"
author: ""
feed_url: "https://www.mongodb.com/blog/rss"
---
<p>Software engineering is evolving into agentic engineering. According to the Stack Overflow Developer Survey 2025, 84% of respondents use or plan to use AI tools in their development, up from 76% the previous year. At this rate, the tooling needs to keep pace.</p>
<p>Last year, we introduced the MongoDB MCP Server to give agents the connectivity they need to interact with MongoDB, helping them generate context-aware code. But connectivity was only the start. Agents are generalists by design, and they don't inherently know the best practices and design patterns that real-world production systems demand.</p>
<p>Today, we're addressing this by introducing official MongoDB Agent Skills: structured instructions, best practices, and resources that agents can discover and apply to generate more reliable code across the full development lifecycle, from schema design and performance optimization to implementing advanced capabilities like AI retrieval.</p>
<p>To bring this directly into the tools you use, we're also launching plugins for Claude Code, Cursor, Gemini CLI, and VS Code, combining the MongoDB MCP Server and Agent Skills in a single, ready-to-use package.</p>
<p>Turning coding agents into MongoDB experts
Coding agents are great at producing working code, but they still make common mistakes in production systems, often defaulting to relational thinking that doesn't translate well to MongoDB, such as:</p>
<p>Over-normalizing schemas, ignoring MongoDB's document-oriented strengths.</p>
<p>Underusing compound indexes, causing performance bottlenecks at scale.</p>
<p>Misusing indexes and search indexes, overlooking the consistency trade-off for high-performance full-text search.</p>
<p>Because these pitfalls mirror common human errors, they are naturally reflected in agent outputs. MongoDB Agent Skills address this by providing expert guidance to agents, like schema design heuristics, indexing strategies, query patterns, and operational safeguards, enabling agents to ship more reliable, more consistent code faster.</p>
<p>Agent Skills were introduced by Anthropic as an open standard and have since been adopted by the leading AI development tools, including Claude Code, Cursor, Codex, and more.</p>
<p>This initial release covers the full application development lifecycle on MongoDB, from connection management and schema design to guidance on implementing advanced capabilities. We will continue to update and expand our skills library based on user needs.</p>
<p>Figure 1. MongoDB Agent Skills.</p>
<p>Scaling agentic engineering with MongoDB
As organizations embrace agentic software engineering, existing processes and workflows must be reimagined. The MongoDB MCP Server and MongoDB Agent Skills are built for this shift and work best together, giving builders and agents the tools to move fast without sacrificing guardrails or control.</p>
<p>The MongoDB MCP Server serves as the connectivity layer for your MongoDB deployments. It manages authentication and defines exactly what agents can access and do. Combined with MongoDB’s native authorization, it ensures agents operate with only the permissions they need, while giving teams governance through configurable controls like disabling specific tools.</p>
<p>Agent Skills ensure agents follow best practices from the start, reducing architectural risk, accelerating implementation, and raising the baseline quality of every agent-generated code.</p>
<p>While some skills can be used independently, others work in conjunction with the MongoDB MCP Server for workflows that require it. To simplify setup, the MCP Server and skills are now packaged together as plugins and extensions for Claude Code, Cursor, Gemini CLI, and VS Code, bringing these capabilities directly into your preferred tools.</p>
<p>Figure 2. MongoDB for Claude plugin in action.</p>
<p>We also encourage you to build your own skills as your agentic workflows mature. Whether enforcing internal naming conventions, custom data modeling patterns, or team-specific workflows, skills give you a practical way to codify institutional knowledge and ensure every agent and every developer works from the same playbook.</p>
<p>How to get started
Whether you’re using Claude Code, Cursor, Gemini CLI, or other AI development tools, you can install the MongoDB MCP Server and Agent Skills in seconds.</p>
<p>For example, in Claude Code, install the plugin that bundles both:</p>
<p>Code Snippet
/plugin marketplace add mongodb/agent-skills
/plugin install mongodb@mongodb-plugins</p>
<p>For Cursor, Gemini CLI, and VS Code extensions, refer to their respective documentation.</p>
<p>You can also install the skills for most coding agents using the Vercel Skills CLI (requires Node.js):</p>
<p>Code Snippet
npx skills add mongodb/agent-skills</p>
<p>If you prefer, you can manually clone the GitHub repository and copy the skills into the appropriate folder for your agent.</p>
<p>Similarly, to install the MongoDB MCP Server, use the following command:</p>
<p>Code Snippet
npx mongodb-mcp-server@latest setup</p>
<p>Agentic engineering is changing how teams work, and it is changing fast. Agents need the context and guidance to meet the standards of real-world production applications. With the official MongoDB Agent Skills and plugins, builders can move faster with confidence, and organizations can adopt coding agents knowing that MongoDB best practices are embedded directly into every workflow.</p>
<p>Next Steps
Ship faster, more reliable apps on MongoDB with Agent Skills. Install for Claude Code, Cursor, Gemini CLI and VS Code!</p>
