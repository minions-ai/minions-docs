# Minions: An Extensible Agentic AI Framework for Java

**Minions** is a powerful, MCP-compliant agentic AI framework designed for the enterprise Java ecosystem. Built with idiomatic Spring practices, it provides a robust foundation for creating and orchestrating autonomous AI agents in complex and regulated environments.

The framework is architected around a core philosophy:

> **The Open/Closed Principle:** The system is **open for extension** but **closed for modification**.

This means you can build anything from a simple ReAct-style agent to a sophisticated planner-executor pipeline without ever needing to alter the core framework code.

---

## Why Minions?

While many agentic frameworks exist for Python, Minions uniquely brings this cutting-edge capability to enterprise Java development. It's designed from the ground up to support the demands of modern, secure, and scalable applications.

- **Idiomatic Spring Integration:** Leverages Spring Boot auto-configuration, dependency injection, and familiar idioms for seamless development.
- **Modular & Extensible:** Easily add new components—tools, memory systems, or agent steps—as standard Spring Beans.
- **Governance by Design:** Built with features like audit hooks, multi-tenant data isolation, and memory privacy for regulated industries.
- **Multi-Tiered Memory:** Features a sophisticated memory architecture with pluggable strategies for querying, persistence, and summarization.
- **Enterprise-Grade Persistence:** Integrates seamlessly with Spring Data for robust, scalable data storage.

---

## Core Design Principles

- **Extensibility First** Minions utilizes proven design patterns, such as the _Factory Registry_ and _Chain of Responsibility_, to ensure seamless integration of custom components.

- **MCP Compliance** Adherence to the [Model Context Protocol (MCP)](https://modelcontextprotocol.io/introduction) ensures architectural clarity, composability, and interoperability between different models and tools.

- **Enterprise Readiness** With features like structured evaluation and memory management designed for privacy, Minions is ready for deployment in finance, healthcare, and insurance.


---

## Sophisticated Memory Architecture

Minions features a pluggable, multi-tiered memory system that you can customize to your needs. Out of the box, it provides a powerful layered approach:

- **Short-Term Memory:** Manages the active context for immediate tasks.
- **Episodic Memory:** Stores a chronological history of events and interactions.
- **Vector Memory:** Enables semantic search over vast amounts of information.
- **Long-Term Memory:** Provides persistent, long-term knowledge storage.

Each subsystem is managed by pluggable strategies for **querying**, **persistence**, **summarization**, and **privacy**, giving you full control over how your agent remembers and forgets.

---

## Agent Recipes

Every agent in Minions is configured using a **Recipe**. A recipe is a blueprint that defines the agent's behavior and capabilities.

A recipe specifies:

- The agent's **system prompt** and ultimate **goal**.
- The **step graph**, which outlines its reasoning and action flow.
- Its complete **memory configuration**, including which subsystems to use and how they behave.
- The **toolchains** and **observers** available to the agent.

Minions includes several pre-built recipes to get you started, such as `ReActAgentRecipe` and `PlannerExecutorObserverRecipe`, with a clear path to creating your own.