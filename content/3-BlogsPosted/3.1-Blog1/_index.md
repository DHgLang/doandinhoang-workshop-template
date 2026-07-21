---
title: "Blog 1"
date: 2026-07-21
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

# Why Amazon Bedrock AgentCore Chose Cedar to Control AI Agent Permissions

AI Agents are increasingly able to act on behalf of people — reading documents, calling APIs, accessing databases, and working with many other services. That raises an important question:

**How do we ensure an AI Agent only performs actions it is allowed to do?**

AWS explains in detail why AgentCore uses **Cedar** as its policy language, instead of relying only on prompts or simple validation rules.

## 1. The problem

In many AI applications today, access rights are checked only once at the start of a session. For example:

- The user signs in successfully.
- The Agent receives a request.
- The Agent calls multiple tools in sequence (tool calling).

However, an Agent’s permissions should not be checked only once.

Suppose the Agent needs to:

- read internal documents,
- query a database,
- send email,
- create a ticket,
- call another system’s API.

Each action has a different sensitivity level and may need its own conditions. If permissions are checked only at session start, the Agent may perform operations beyond the intended scope.

## 2. What is Cedar?

Cedar is a policy language developed by AWS for fine-grained authorization.

Instead of hard-coding permissions in the application, Cedar clearly describes:

- **Principal** — who is acting?
- **Action** — what are they allowed to do?
- **Resource** — on which resource?
- **Context** — under which conditions?

In the **AgentCore Gateway** context, this maps roughly as follows: Principal is often the User or Agent session identity (typically via an OAuth/IAM token) when calling a tool; Action is the tool invocation (MCP tool call); Resource is the tool/API or data being accessed; Context adds conditions such as input parameters or session attributes.

Every request is evaluated against these components before it is allowed.

## 3. Why does an Agent need a Policy Engine?

What I find most interesting in the article is that AWS fully separates an Agent’s **capability** from its **permissions**.

An Agent may know how to:

- call APIs,
- read documents,
- run workflows,
- use many different tools.

That does not mean the Agent is always allowed to perform every action.

The Policy Engine acts as an independent control layer associated with the Gateway: it evaluates each request before the Agent accesses a resource. In particular, AgentCore Gateway follows **Default Deny** — by default, all tool calls are blocked. The Agent may only perform what is explicitly allowed in a Cedar policy (for example `permit(...)`).

Cedar does more than block at runtime. It also supports **Tool Filtering** (partial evaluation): tools the Agent definitely cannot use are hidden from the available tool list (for example in `list_tools`). If the Agent cannot see a tool, the risk of calling it — intentionally or by mistake — drops sharply.

This helps reduce risks such as:

- Prompt injection causing the Agent to take unintended actions.
- Accidental access to sensitive data.
- Tools being misused beyond granted permissions.

## 4. Conclusion

For me, the key lesson is not that Cedar is a new policy language, but that AWS separates **authorization** from Agent logic.

This is similar to modern web applications: we do not hard-code access rights inside every API; we use a centralized authorization layer.

Applied to AI Agents, this approach makes permission management clearer as Agents use more tools and run more complex workflows.

Still, a Policy Engine is not the only safeguard. A secure Agent system should also combine:

- IAM and least privilege,
- sandboxing for code execution,
- Guardrails for content control,
- logging and monitoring of the full Agent trajectory,
- human-in-the-loop for high-risk actions.

In short: **Policy decides what an Agent is allowed to do; Guardrails help shape how the Agent should respond.** These layers complement each other — they do not replace each other.

## References

- [Why Policy in Amazon Bedrock AgentCore chose Cedar for securing agentic workflows](https://aws.amazon.com/blogs/security/why-policy-in-amazon-bedrock-agentcore-chose-cedar-for-securing-agentic-workflows/)
- [Amazon Bedrock AgentCore Policy](https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/policy.html)
