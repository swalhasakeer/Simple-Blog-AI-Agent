# 🧠 **Simple Blog AI Agent**

A simple AI-powered blogging pipeline built using CrewAI. This project leverages Large Language Models (LLMs) to automatically plan, write, edit, and convert blog articles into web-ready content, all using autonomous agents.

## 📌 **Project Overview**

This project demonstrates how to build a multi-agent blog generation pipeline using CrewAI. The agents involved:

* 🧭 Content Planner Agent – Plans the structure, goals, and key ideas.

* ✍️ Content Writer Agent – Generates a detailed and engaging blog based on the plan.

* 🧹 Content Editor Agent – Refines the writing for clarity, tone, and grammar.

* 🌐 Web Developer Agent – Converts the blog into a web-ready markdown or HTML format.

The process is coordinated by a Crew, enabling task execution in logical order.

## 🧩 **Features**

✅ Multi-agent workflow (Planner → Writer → Editor → Web Developer)

✅ Customizable and modular design

✅ Clean, notebook-based implementation

✅ Backend-only (no HTML frontend required)

✅ Supports any topic dynamically using kickoff(inputs={"topic": "Your Topic"})

## 🧠 **What is Crew?**

CrewAI is a Python framework for building multi-agent LLM workflows. Instead of using one big model to do everything, Crew lets you define multiple agents with specific roles and responsibilities, just like a real team.

## 🎯 **Key Concepts**

* Agents: AI workers with specific roles (e.g., planner, writer)

* Tasks: Defined objectives assigned to agents

* Crew: Coordinates agents + tasks into a logical pipeline

* Supports various LLMs such as OpenAI, Claude, and Groq.

## 🚀 **Installation**

Make sure you have Python 3.8+ and run the following:

```bash

pip install crewai==0.86.0
pip install crewai-tools==0.25.0
pip install langchain_community==0.0.29
pip install serpapi==0.1.5
```

## ⚙️ **How It Works**
1. Import Required Modules

2. Set up your LLM

```bash
from crewai import LLM

llm = LLM(
    api_key="Enter_Your_API_KEY_Here",
    model="your preferred LLM"
)
```

3. Create Agents

* planner: Plans the blog's structure

* writer: Writes the article

* editor: Improves quality

* web_developer: Formats for web

4. Define Tasks

Tasks define what each agent should do (e.g., planning, writing, editing, formatting).

Form a Crew

```bash
crew = Crew(
    agents=[planner, writer, editor, web_developer],
    tasks=[plan, write, edit, webpage_creation],
    verbose=True
)
```

5. Kickoff Workflow

```bash
result = crew.kickoff(inputs={"topic": "Malayalam Cinema History"})
print(result)
```

The final result is a polished, structured blog ready for publishing.

## 🔑 **API Key**

You will need the following API keys to run this project:

* LLM Provider Key – For models like Groq, OpenAI, etc.

* SerpAPI Key – Used for web search tasks or enhancing agent responses with real-time data.

## 🤝 **Contribution**

Pull requests are welcome!
For major changes, please open an issue first to discuss what you'd like to add or improve.
