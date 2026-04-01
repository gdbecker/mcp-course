## 01_ Theory: Agentic AI and Tool Use - How do they work?

### Understanding Agentic AI Behavior
- When you send a message request to an LLM API
  - You're also sending a system prompt, chat history, max output tokens - along with the message you typed
  - The response you get also includes a stop reason, output tokens, and price for the API request
- You can expose your own code functionality to LLMs and connect it to work together