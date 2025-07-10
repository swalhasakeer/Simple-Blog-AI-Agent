# 🧠 **Simple Blog AI Agent**

A simple AI-powered blogging agent pipeline using CrewAI. This project leverages large language models to automatically plan and write blog articles.

## 📌 **Project Overview**

This project demonstrates how to build a two-agent blog generation pipeline:

- **Content Planner Agent**: Plans the structure, goals, and key ideas for the blog.
- **Content Writer Agent**: Writes a detailed and readable blog article using the planner's output.

Powered by LLMs (such as `groq/llama3-70b-8192`) using the `crewai` and `langchain_community` libraries.

## 🧩 **Features**

- Agent-based architecture (Planner + Writer)
- Modular and customizable for any blog topic
- Clean and notebook-based implementation

## 🧠 **What is Crew?**

Crew is a Python framework that helps you build multi-agent AI workflows. Instead of using a single large language model (LLM) for everything, Crew lets you create a team of AI agents, each with its own role, goal, and responsibilities. These agents work together like a real crew to complete complex tasks more efficiently.

### ✅ **Key Features:**

* Each Agent can think and act based on its role (e.g., planner, writer, researcher).

* You can define Tasks that are assigned to different agents.

* A Crew coordinates all agents and tasks into a workflow.

* Works with popular LLMs like OpenAI, Groq, Claude, etc.


## 🚀 **Installation**

Make sure you have Python 3.8+ and run the following in your terminal or notebook:

```bash
pip install crewai-tools==0.25.0
pip install crewai==0.86.0
pip install langchain_community==0.0.29
```
## 🧠 **How It Works**

1. Import Required Modules

2. Set up your LLM

  ```bash
from crewai import LLM

llm = LLM(
    api_key="Enter_Your_API_KEY_Here",
    model="Give_Model"
)
```

3. Create Agents

* Content Planner: Plans structure, sections, and facts.

* Content Writer: Writes blog content based on the planner's work.

4. Define Tasks

* It defines what the agent needs to do within the crew, such as planning, writing. Tasks help organize the workflow by breaking down the overall objective into clear, manageable steps.

5. Run the Crew

## ✍️ **Sample Use**

* You can define a topic (e.g., "Write a blog abou the topic "Politics") and run the pipeline to generate an informative blog post in multiple sections.

## 🔑 **API Key**

* You will need an API key for the LLM provider (like Groq or OpenAI). Make sure to set your key in the notebook or script:

## 🤝 **Contribution**

Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.
