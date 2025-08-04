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

[VoltAgent](https://github.com/VoltAgent/voltagent) is an open-source TypeScript framework for creating and managing AI agents. It provides modular components to build, customize, and scale agents with ease. From connecting to APIs and memory management to supporting multiple LLMs, VoltAgent simplifies the process of creating sophisticated AI systems. It enables fast development, maintains clean code, and offers flexibility to switch between models and tools without vendor lock-in.

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




# Documentation

## Getting Started
- [Overview](https://voltagent.dev/docs/) - Introduction to VoltAgent framework
- [Quick Start](https://voltagent.dev/docs/getting-started/quick-start/) - Get up and running in minutes
- [MCP Docs Server](https://voltagent.dev/docs/getting-started/mcp-docs-server/) - Model Context Protocol documentation server


## Agents
- [Overview](https://voltagent.dev/docs/agents/overview/) - Understanding agents in VoltAgent
- [Prompts](https://voltagent.dev/docs/agents/prompts/) - Crafting effective agent prompts
- [Tools](https://voltagent.dev/docs/agents/tools/) - Adding capabilities to your agents
- [Providers](https://voltagent.dev/docs/agents/providers/) - LLM provider integration
- [Sub-Agents](https://voltagent.dev/docs/agents/subagents/) - Building multi-agent systems
- [Context](https://voltagent.dev/docs/agents/context/) - Managing agent context
- [Dynamic Agents](https://voltagent.dev/docs/agents/dynamic-agents/) - Creating agents dynamically
- [Hooks](https://voltagent.dev/docs/agents/hooks/) - Lifecycle hooks and event handling
- [MCP](https://voltagent.dev/docs/agents/mcp/) - Model Context Protocol integration
- [Multi-Modal](https://voltagent.dev/docs/agents/multi-modal/) - Working with images and other media
- [Voice](https://voltagent.dev/docs/agents/voice/) - Voice capabilities for agents

### Memory
- [Overview](https://voltagent.dev/docs/agents/memory/overview/) - Memory management concepts
- [In-Memory](https://voltagent.dev/docs/agents/memory/in-memory/) - In-memory storage
- [PostgreSQL](https://voltagent.dev/docs/agents/memory/postgres/) - PostgreSQL memory store
- [Supabase](https://voltagent.dev/docs/agents/memory/supabase/) - Supabase integration
- [LibSQL](https://voltagent.dev/docs/agents/memory/libsql/) - LibSQL/Turso memory store

## Workflows
- [Overview](https://voltagent.dev/docs/workflows/overview/) - Workflow orchestration
- [Execute API](https://voltagent.dev/docs/workflows/execute-api/) - Workflow execution API
- [Hooks](https://voltagent.dev/docs/workflows/hooks/) - Workflow lifecycle hooks
- [Schemas](https://voltagent.dev/docs/workflows/schemas/) - Workflow schema definitions
- [Suspend & Resume](https://voltagent.dev/docs/workflows/suspend-resume/) - Workflow state management

### Workflow Steps
- [andAgent](https://voltagent.dev/docs/workflows/steps/and-agent/) - Execute agent in workflow
- [andAll](https://voltagent.dev/docs/workflows/steps/and-all/) - Parallel execution
- [andRace](https://voltagent.dev/docs/workflows/steps/and-race/) - Race conditions
- [andTap](https://voltagent.dev/docs/workflows/steps/and-tap/) - Side effects
- [andThen](https://voltagent.dev/docs/workflows/steps/and-then/) - Sequential execution
- [andWhen](https://voltagent.dev/docs/workflows/steps/and-when/) - Conditional execution

## RAG (Retrieval-Augmented Generation)
- [Overview](https://voltagent.dev/docs/rag/overview/) - RAG concepts and implementation
- [Custom Retrievers](https://voltagent.dev/docs/rag/custom-retrievers/) - Building custom retrievers
- [Chroma](https://voltagent.dev/docs/rag/chroma/) - Chroma vector database
- [Pinecone](https://voltagent.dev/docs/rag/pinecone/) - Pinecone integration
- [Qdrant](https://voltagent.dev/docs/rag/qdrant/) - Qdrant vector store

## Providers
- [Overview](https://voltagent.dev/docs/providers/overview/) - Provider system architecture
- [Anthropic AI](https://voltagent.dev/docs/providers/anthropic-ai/) - Claude integration
- [Google AI](https://voltagent.dev/docs/providers/google-ai/) - Google AI models
- [Groq AI](https://voltagent.dev/docs/providers/groq-ai/) - Groq LPU integration
- [Vercel AI](https://voltagent.dev/docs/providers/vercel-ai/) - Vercel AI SDK
- [xsAI](https://voltagent.dev/docs/providers/xsai/) - xsAI provider
- [Contributing](https://voltagent.dev/docs/providers/contributing/) - Add new providers

## Tools
- [Overview](https://voltagent.dev/docs/tools/overview/) - Tool system and creation
- [Reasoning Tool](https://voltagent.dev/docs/tools/reasoning-tool/) - Chain of thought reasoning

## Integrations
- [Overview](https://voltagent.dev/docs/integrations/overview/) - Available integrations
- [Next.js](https://voltagent.dev/docs/integrations/nextjs/) - Next.js integration guide
- [Vercel AI](https://voltagent.dev/docs/integrations/vercel-ai/) - Vercel AI SDK integration

## Observability
- [Overview](https://voltagent.dev/docs/observability/overview/) - Monitoring and debugging
- [Developer Console](https://voltagent.dev/docs/observability/developer-console/) - Built-in console
- [Langfuse](https://voltagent.dev/docs/observability/langfuse/) - Langfuse integration
- [Logging](https://voltagent.dev/docs/observability/logging/) - Logging configuration

## API Reference
- [Overview](https://voltagent.dev/docs/api/overview/) - Complete API documentation

## Utils
- [Create Prompt](https://voltagent.dev/docs/utils/create-prompt/) - Prompt utilities




# Examples

## Core Examples
- [Base](https://github.com/VoltAgent/voltagent/tree/main/examples/base/) - Basic agent setup and configuration
- [Tools](https://github.com/VoltAgent/voltagent/tree/main/examples/with-tools/) - How to add and use tools with your agents
- [Sub-Agents](https://github.com/VoltAgent/voltagent/tree/main/examples/with-subagents/) - Creating multi-agent systems
- [Workflow](https://github.com/VoltAgent/voltagent/tree/main/examples/with-workflow/) - Agent workflow orchestration
- [Dynamic Parameters](https://github.com/VoltAgent/voltagent/tree/main/examples/with-dynamic-parameters/) - Dynamic parameter handling
- [Dynamic Prompts](https://github.com/VoltAgent/voltagent/tree/main/examples/with-dynamic-prompts/) - Dynamic prompt generation
- [Custom Endpoints](https://github.com/VoltAgent/voltagent/tree/main/examples/with-custom-endpoints/) - Custom API endpoints
- [Thinking Tool](https://github.com/VoltAgent/voltagent/tree/main/examples/with-thinking-tool/) - Chain of thought reasoning

## LLM Provider Examples
- [Anthropic](https://github.com/VoltAgent/voltagent/tree/main/examples/with-anthropic/) - Using Anthropic's Claude
- [Google AI](https://github.com/VoltAgent/voltagent/tree/main/examples/with-google-ai/) - Google AI integration
- [Google Vertex AI](https://github.com/VoltAgent/voltagent/tree/main/examples/with-google-vertex-ai/) - Vertex AI integration
- [Groq AI](https://github.com/VoltAgent/voltagent/tree/main/examples/with-groq-ai/) - Groq AI provider
- [Vercel AI](https://github.com/VoltAgent/voltagent/tree/main/examples/with-vercel-ai/) - Vercel AI SDK integration
- [xsAI](https://github.com/VoltAgent/voltagent/tree/main/examples/with-xsai/) - xsAI provider

## Vector Database & RAG Examples
- [Retrieval](https://github.com/VoltAgent/voltagent/tree/main/examples/with-retrieval/) - Basic RAG implementation
- [Chroma](https://github.com/VoltAgent/voltagent/tree/main/examples/with-chroma/) - Chroma vector database
- [Pinecone](https://github.com/VoltAgent/voltagent/tree/main/examples/with-pinecone/) - Pinecone vector database
- [Qdrant](https://github.com/VoltAgent/voltagent/tree/main/examples/with-qdrant/) - Qdrant vector database
- [RAG Chatbot](https://github.com/VoltAgent/voltagent/tree/main/examples/with-rag-chatbot/) - Complete RAG chatbot

## Database Examples
- [PostgreSQL](https://github.com/VoltAgent/voltagent/tree/main/examples/with-postgres/) - PostgreSQL integration
- [Supabase](https://github.com/VoltAgent/voltagent/tree/main/examples/with-supabase/) - Supabase integration
- [Turso](https://github.com/VoltAgent/voltagent/tree/main/examples/with-turso/) - Turso database

## MCP (Model Context Protocol) Examples
- [MCP](https://github.com/VoltAgent/voltagent/tree/main/examples/with-mcp/) - Basic MCP integration
- [Composio MCP](https://github.com/VoltAgent/voltagent/tree/main/examples/with-composio-mcp/) - Composio MCP integration
- [Google Drive MCP](https://github.com/VoltAgent/voltagent/tree/main/examples/with-google-drive-mcp/) - Google Drive via MCP
- [Hugging Face MCP](https://github.com/VoltAgent/voltagent/tree/main/examples/with-hugging-face-mcp/) - Hugging Face models via MCP
- [Peaka MCP](https://github.com/VoltAgent/voltagent/tree/main/examples/with-peaka-mcp/) - Peaka data integration
- [Zapier MCP](https://github.com/VoltAgent/voltagent/tree/main/examples/with-zapier-mcp/) - Zapier automation via MCP

## Voice & Audio Examples
- [Voice (ElevenLabs)](https://github.com/VoltAgent/voltagent/tree/main/examples/with-voice-elevenlabs/) - ElevenLabs voice synthesis
- [Voice (OpenAI)](https://github.com/VoltAgent/voltagent/tree/main/examples/with-voice-openai/) - OpenAI voice capabilities
- [Voice (xsAI)](https://github.com/VoltAgent/voltagent/tree/main/examples/with-voice-xsai/) - xsAI voice integration

## Framework Integration Examples
- [Next.js](https://github.com/VoltAgent/voltagent/tree/main/examples/with-nextjs/) - Next.js integration
- [Playwright](https://github.com/VoltAgent/voltagent/tree/main/examples/with-playwright/) - Web automation with Playwright

## Monitoring & Observability Examples
- [SDK Trace Example](https://github.com/VoltAgent/voltagent/tree/main/examples/sdk-trace-example/) - Tracing and debugging
- [VoltAgent Exporter](https://github.com/VoltAgent/voltagent/tree/main/examples/with-voltagent-exporter/) - Metrics export

## Complete Applications
- [GitHub Repo Analyzer](https://github.com/VoltAgent/voltagent/tree/main/examples/github-repo-analyzer/) - Full-featured repository analysis agent


# VoltOps - LLM Observability & Monitoring

## Core Concepts
- [Overview](https://voltagent.dev/voltops-llm-observability-docs/) - Introduction to VoltOps observability platform
- [Why Observability](https://voltagent.dev/voltops-llm-observability-docs/why/) - Understanding the importance of LLM monitoring with VoltOps
- [Concepts](https://voltagent.dev/voltops-llm-observability-docs/concept/) - Key VoltOps observability concepts
- [LLM Usage & Costs](https://voltagent.dev/voltops-llm-observability-docs/llm-usage-and-costs/) - Track LLM usage and manage costs with VoltOps

## Tracing
- [Overview](https://voltagent.dev/voltops-llm-observability-docs/tracing/overview/) - Distributed tracing with VoltOps
- [Concepts](https://voltagent.dev/voltops-llm-observability-docs/tracing/concept/) - VoltOps tracing fundamentals
- [Agent Visualization](https://voltagent.dev/voltops-llm-observability-docs/tracing/agent-visualization/) - Visualize agent interactions in VoltOps
- [Multimodal Tracing](https://voltagent.dev/voltops-llm-observability-docs/tracing/multimodal-tracing/) - Trace multimodal interactions with VoltOps
- [Sessions](https://voltagent.dev/voltops-llm-observability-docs/tracing/sessions/) - Session-based tracing in VoltOps
- [Metadata](https://voltagent.dev/voltops-llm-observability-docs/tracing/metadata/) - Enriching VoltOps traces with metadata
- [Tags](https://voltagent.dev/voltops-llm-observability-docs/tracing/tags/) - Organizing traces with VoltOps tags
- [Trace ID](https://voltagent.dev/voltops-llm-observability-docs/tracing/trace-id/) - Working with VoltOps trace identifiers
- [Release Versioning](https://voltagent.dev/voltops-llm-observability-docs/tracing/release-versioning/) - Version tracking in VoltOps

## Dashboard & Analytics
- [LLM Call Overview](https://voltagent.dev/voltops-llm-observability-docs/dashboard/llm-call-overview/) - Monitor LLM calls with VoltOps dashboard
- [LLM Call Success Rates](https://voltagent.dev/voltops-llm-observability-docs/dashboard/llm-call-success-rates/) - Track success metrics in VoltOps
- [LLM Cost Overview](https://voltagent.dev/voltops-llm-observability-docs/dashboard/llm-cost-overview/) - Cost analysis with VoltOps
- [Trace Counts](https://voltagent.dev/voltops-llm-observability-docs/dashboard/trace-counts/) - VoltOps trace statistics
- [Trace Metrics](https://voltagent.dev/voltops-llm-observability-docs/dashboard/trace-metrics/) - Performance metrics in VoltOps
- [User Cost Overview](https://voltagent.dev/voltops-llm-observability-docs/dashboard/user-cost-overview/) - Per-user cost tracking with VoltOps

## Framework Integrations
- [VoltAgent Framework](https://voltagent.dev/voltops-llm-observability-docs/voltagent-framework/) - Native VoltAgent integration with VoltOps
- [Vercel AI](https://voltagent.dev/voltops-llm-observability-docs/vercel-ai/) - Monitor Vercel AI SDK with VoltOps
- [LangChain](https://voltagent.dev/voltops-llm-observability-docs/langchain/) - LangChain integration with VoltOps
- [LlamaIndex](https://voltagent.dev/voltops-llm-observability-docs/llamaindex/) - LlamaIndex monitoring via VoltOps
- [OpenAI SDK](https://voltagent.dev/voltops-llm-observability-docs/openai-sdk/) - Track OpenAI SDK with VoltOps
- [Hugging Face](https://voltagent.dev/voltops-llm-observability-docs/huggingface/) - Monitor Hugging Face models with VoltOps
- [Pydantic AI](https://voltagent.dev/voltops-llm-observability-docs/pydantic-ai/) - Pydantic AI support in VoltOps
- [AutoGen](https://voltagent.dev/voltops-llm-observability-docs/autogen/) - Microsoft AutoGen with VoltOps
- [CrewAI](https://voltagent.dev/voltops-llm-observability-docs/crewai/) - CrewAI framework monitoring in VoltOps
- [Agno](https://voltagent.dev/voltops-llm-observability-docs/agno/) - Agno integration with VoltOps
- [Semantic Kernel](https://voltagent.dev/voltops-llm-observability-docs/semantic-kernel/) - Microsoft Semantic Kernel with VoltOps
- [Spring AI](https://voltagent.dev/voltops-llm-observability-docs/spring-ai/) - Spring AI monitoring via VoltOps

## Cloud Provider Integrations
- [Amazon Bedrock](https://voltagent.dev/voltops-llm-observability-docs/amazon-bedrock/) - AWS Bedrock monitoring with VoltOps
- [Google Vertex AI](https://voltagent.dev/voltops-llm-observability-docs/google-vertex-ai/) - Vertex AI observability via VoltOps

## SDKs & APIs
- [JavaScript/TypeScript SDK](https://voltagent.dev/voltops-llm-observability-docs/js-ts-sdk/) - VoltOps JS/TS SDK integration
- [Python SDK](https://voltagent.dev/voltops-llm-observability-docs/python-sdk/) - VoltOps Python SDK integration
- [REST API](https://voltagent.dev/voltops-llm-observability-docs/rest-api/) - VoltOps REST API access

## Advanced Features
- [Evaluation](https://voltagent.dev/voltops-llm-observability-docs/evaluation/) - Model evaluation and testing with VoltOps
- [Prompting](https://voltagent.dev/voltops-llm-observability-docs/prompting/) - Prompt engineering and optimization in VoltOps


## Official Resources
- [VoltAgent Tutorial Introduction](https://voltagent.dev/tutorial/introduction/) - Official interactive tutorial
- [VoltAgent Documentation](https://voltagent.dev/docs/) - Comprehensive documentation
- [API Reference](https://voltagent.dev/docs/api/) - Complete API documentation
- [Quick Start Guide](https://voltagent.dev/docs/quick-start/) - Get up and running in minutes
- [VoltAgent Blog](https://voltagent.dev/blog/) - Latest updates and tutorials

## Community Videos
- [How to use Voltagent Framework with Gaia AI](https://www.youtube.com/watch?v=SNxfQFHbYVE) - Integration with Gaia AI
- [VoltAgent: This Open-Source TypeScript Framework Makes Building Multi-Agent AI Systems Super Easy ](https://www.youtube.com/watch?v=IJYgMv1wH30) - Framework overview and capabilities
- [Do AI with Voltagent, Composio and R2R](https://www.youtube.com/watch?v=m4DMNSVtcCE) - Using VoltAgent with Composio and R2R
- [Integra WhatsApp Business API a tu Agente de Voltagent: Tutorial + Repo de Código en GitHub](https://www.youtube.com/watch?v=mDKXbcfwCYM) - WhatsApp Business API integration (Spanish)
- [【これ最強】AIエージェント開発の「voltagent」が熱い！画面で見やすく、シンプルで柔軟なTypescriptベースのフレームワーク](https://www.youtube.com/watch?v=5WARn6C9ITM) - VoltAgent framework overview (Japanese)
- [¿Agentes de IA sin Complicaciones? ¡Este Framework es la Clave!](https://www.youtube.com/watch?v=Om03tXjDfJs) - Building AI agents simplified (Spanish)
- [Creamos un agente que verifica stock con VoltAgent](https://www.youtube.com/watch?v=HW_cqz_3Q38)



## Community Resources
- [Discord Community](https://s.voltagent.dev/discord) - Get help and share projects
- [GitHub Discussions](https://github.com/VoltAgent/voltagent/discussions) - Q&A and feature requests
- [Twitter/X](https://twitter.com/voltagent_dev) - Latest news and updates
- [Reddit](https://www.reddit.com/user/voltagent_dev/)
- [Linkedin](https://www.linkedin.com/company/voltagent)

