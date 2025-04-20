<div align="center">
<a href="https://voltagent.dev/">
<img width="1800" alt="435380213-b6253409-8741-462b-a346-834cd18565a9" src="https://github.com/user-attachments/assets/452a03e7-eeda-4394-9ee7-0ffbcf37245c" />
</a>


<br/>
<br/>

<div align="center">
    <a href="https://voltagent.dev">Home Page</a> |
    <a href="https://voltagent.dev/docs/">Documentation</a> |
    <a href="https://github.com/voltagent/voltagent/tree/main/examples">Examples</a> |
    <a href="https://s.voltagent.dev/discord">Discord</a> |
    <a href="https://voltagent.dev/blog/">Blog</a>
</div>
</div>

<br/>

<div align="center">
    <strong>VoltAgent is an open source TypeScript framework for building and orchestrating AI agents.</strong><br>
Escape the limitations of no-code builders and the complexity of starting from scratch.
    <br />
    <br />
</div>

<div align="center">
    
[![npm version](https://img.shields.io/npm/v/@voltagent/core.svg)](https://www.npmjs.com/package/@voltagent/core)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.0-4baaaa.svg)](CODE_OF_CONDUCT.md)
[![Discord](https://img.shields.io/discord/1361559153780195478.svg?label=&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2)](https://s.voltagent.dev/discord)
[![Twitter Follow](https://img.shields.io/twitter/follow/voltagent_dev?style=social)](https://twitter.com/voltagent_dev)
    
</div>

<br/>

<div align="center">
<a href="https://voltagent.dev/">
<img width="896" alt="Screenshot 2025-04-20 at 22 44 38" src="https://github.com/user-attachments/assets/f0627868-6153-4f63-ba7f-bdfcc5dd603d" />
</a>


</div>

## VoltAgent: Build AI Agents Fast and Flexibly

VoltAgent is an open-source TypeScript framework for creating and managing AI agents. It provides modular components to build, customize, and scale agents with ease. From connecting to APIs and memory management to supporting multiple LLMs, VoltAgent simplifies the process of creating sophisticated AI systems. It enables fast development, maintains clean code, and offers flexibility to switch between models and tools without vendor lock-in.

## Try VoltAgent

Create a new VoltAgent project in seconds using the `create-voltagent-app` CLI tool:

```bash
npm create voltagent-app@latest
```

This command guides you through setup.

You'll see the starter code in `src/index.ts` to get you started with the VoltAgent framework.

```typescript
import { VoltAgent, Agent } from "@voltagent/core";
import { VercelAIProvider } from "@voltagent/vercel-ai"; // Example provider
import { openai } from "@ai-sdk/openai"; // Example model

// Define a simple agent
const agent = new Agent({
  name: "my-agent",
  description: "A helpful assistant that answers questions without using tools",
  // Note: You can swap VercelAIProvider and openai with other supported providers/models
  llm: new VercelAIProvider(),
  model: openai("gpt-4o-mini"),
});

// Initialize VoltAgent with your agent(s)
new VoltAgent({
  agents: {
    agent,
  },
});
```

Afterwards, navigate to your project and run:

```bash
npm run dev
```

Your agent is now running!
To interact with it:

Click the [VoltAgent Console](https://console.voltagent.dev) link in your terminal output (or copy-paste it into your browser).

![435419303-65a51ec9-62f1-4dea-a7cc-d0aa5064aec7](https://github.com/user-attachments/assets/0adbec33-1373-4cf4-b67d-825f7baf1cb4)

---


# Announcements and Official Blog Posts

- [VoltAgent v0.1: AI Development Reimagined for JavaScript/TypeScript](https://voltagent.dev/blog/introducing-voltagent/)
- [Escape the 'console.log': VoltAgent Developer Console](https://voltagent.dev/blog/voltagent-developer-console/)
- [Building Your First AI Agent with VoltAgent: A GitHub Repo Analyzer](https://voltagent.dev/blog/building-first-agent-github-analyzer/)



# Getting Started
- [Overview](https://voltagent.dev/docs/)
- [Quick Start](https://voltagent.dev/docs/quick-start/)

