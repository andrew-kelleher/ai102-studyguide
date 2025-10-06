# Create Custom Agents

This section of the **Microsoft AI-102: Designing and Implementing a Microsoft Azure AI Solution** exam covers creating and managing **custom agents** using Azure AI Foundry. Below are study notes for each sub-topic, with links to Microsoft documentation, exam tips, and key facts.

---

## :material-lightbulb-on: Understand the Role and Use Cases of an Agent

📖 **Docs:** [Overview of Azure AI Agents](https://learn.microsoft.com/azure/ai-services/agents/overview)

**Overview**

- Agents are AI-powered entities designed to perform tasks, automate workflows, and interact with users or systems
- Use cases include:
    - Conversational assistants
    - Enterprise copilots
    - Automation of repetitive processes
    - Knowledge-grounded task execution

**Key Points**

- Agents can call external APIs, databases, and integrate with business logic
- Unlike static LLMs, agents can maintain context across workflows
- Support single-agent or multi-agent setups

!!! tip "Exam Tip"
    Expect scenario questions: *Which solution requires an agent vs. a standard LLM call?*

---

## :material-lightbulb-on: Configure the Necessary Resources to Build an Agent

📖 **Docs:** [Provision resources for AI agents](https://learn.microsoft.com/azure/ai-services/agents/how-to/provision)

**Overview**

- Requires setting up an **Azure AI Foundry hub/project**
- Linked resources:
    - **Azure AI Search** (for grounding)
    - **Azure Storage** (for data persistence)
    - **Azure OpenAI** (for language models)
- Networking and RBAC must be configured to ensure security

**Key Points**

- Quotas apply to Azure OpenAI (tokens/minute, requests/minute).
- Agents often require both vector search and LLM endpoints.

!!! warning "Limits"
    Regional availability and subscription quotas can restrict deployments.

---

## :material-lightbulb-on: Create an Agent with the Azure AI Foundry Agent Service

📖 **Docs:** [Create an agent](https://learn.microsoft.com/azure/ai-services/agents/how-to/create-agent)

**Overview**

- Use the **Azure AI Foundry Agent Service** to build, configure, and deploy agents
- Agents can be configured with:
    - Tools (APIs, functions)
    - Memory (short-term, long-term)
    - Prompt templates
    - Grounding sources

**Key Points**

- Agents can be hosted and exposed as APIs
- Agents inherit hub/project security
- Managed service handles scaling and monitoring

!!! example "Use Case"
    Building an enterprise helpdesk copilot that integrates with ticketing systems.

---

## :material-lightbulb-on: Implement Complex Agents with Semantic Kernel and Autogen

📖 **Docs:** [Semantic Kernel](https://learn.microsoft.com/semantic-kernel/overview) | [Autogen](https://microsoft.github.io/autogen/)

**Overview**

- **Semantic Kernel (SK):** SDK for orchestrating AI skills, plugins, and agents
- **Autogen:** Framework for multi-agent conversations, collaboration, and workflows
- Together, they enable advanced orchestration and complex reasoning

**Key Points**

- SK supports chaining skills, context memory, and plugin integration
- Autogen supports autonomous collaboration between multiple agents
- Suitable for scenarios like research copilots, coding assistants, or negotiation bots

!!! tip "Exam Tip"
    Know the difference:
    - *Agent Service* = managed, low-code.
    - *Semantic Kernel / Autogen* = developer SDKs for custom logic.

---

## :material-lightbulb-on: Implement Complex Workflows Including Orchestration for Multi-Agent Solutions

📖 **Docs:** [Multi-agent orchestration](https://learn.microsoft.com/azure/ai-services/agents/how-to/multi-agent)

**Overview**

- Multi-agent = collaboration between multiple specialized agents
- Supports:
    - Multiple users
    - Multiple tools
    - Autonomous reasoning and task delegation

**Key Points**

- Agents can pass tasks between each other
- Requires orchestration (Semantic Kernel, Autogen, or Foundry workflows)
- Useful for enterprise-scale copilots or automation across departments

!!! example "Use Case"
    - Travel planning assistant: one agent handles booking, another manages itineraries, another answers customer queries.

---

## :material-lightbulb-on: Test, Optimize and Deploy an Agent

📖 **Docs:** [Test and deploy agents](https://learn.microsoft.com/azure/ai-services/agents/how-to/test-deploy)

**Overview**

- Testing ensures groundedness, reliability, and safety
- Optimize prompts, tools, and grounding sources before production deployment
- Deployment exposes agents as endpoints for apps/services

**Key Points**

- Use evaluation datasets for reliability testing
- Agents can be deployed via CI/CD
- Monitoring includes usage, latency, and safety incidents

!!! info "Best Practices"
    - Always include guardrails (content filters, prompt templates)
    - Monitor with **Azure Monitor** and logging integrations

---

## :material-compass-outline: Quick‑fire revision sheet  

- 📌 Agents are context-aware, unlike static prompts
- 📌 Requires **Azure AI Foundry hub/project + linked resources**
- 📌 Know when to use **Agent Service** vs. **Semantic Kernel/Autogen**
- 📌 Multi-agent = orchestration and autonomous workflows
- 📌 Testing & deployment require monitoring, evaluation, and guardrails
