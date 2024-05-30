# Reflexion Agent

The main goal is to generate a detailed article on a given topic, enriched with real-time data and citations from the web, along with a quality critique loop to ensure high-quality answers.

The reflection agent includes tools like an online search tool to fetch real-time data to enhance responses. It utilizes advanced prompt engineering to ensure the agent can process feedback effectively and improve over time.

The architecture and concept come from a paper [Reflexion](https://arxiv.org/pdf/2303.11366) and the implementation is inspired by a [LangChain blog](https://blog.langchain.dev/reflection-agents/) and [Eden Marco Udemy Course](https://www.udemy.com/course/langgraph/). The implementation has been simplified for better understanding.

### Tools and Technologies:

- GPT-4 Turbo: Used for writing text and critiques with strong reasoning capabilities.
- Function Calling: Essential for the implementation.
- Search Engine (Tavileh): Optimized for LLM applications to fetch real-time data.
- LangSmith for Tracing: Helps trace the complex architecture easily.

### Graph Nodes

- Responder Node: Generates an initial response, adds a critique, and suggests search terms.
- Execute Tools Node: Uses search engines to retrieve real-time data based on search terms.
- Reviser Node: Incorporates new data and critique to revise and improve the response, and provides new critiques and search terms for further improvement.

![Reflexion Architecture](https://blog.langchain.dev/content/images/size/w1600/2024/02/reflexion.png)

Continuous Improvement Loop: The agent continuously revises its responses based on new data and critiques until a stopping condition is met, ensuring the final output is of high quality. The reflection agent aims to dynamically fetch and incorporate relevant information from the web, provide detailed and high-quality responses, and continually improve through iterative critique and revision.
