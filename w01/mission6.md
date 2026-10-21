6: Chatbot vs. RAG vs. Agent

## 1. Understanding the Concepts

**LLM (Large Language Model):** An AI model that understands prompts and generates text-based responses. Example: ChatGPT answering questions.

**AI Application:** Software that uses AI to perform a specific task. Example: An AI-powered language-learning app.

**RAG (Retrieval-Augmented Generation):** A method that retrieves relevant information from documents before generating an answer. Example: A chatbot answering questions using college documents.

**Tool-Using Assistant:** An AI assistant that uses external tools to perform tasks. Example: An assistant using a calculator to solve a problem.

**AI Agent:** An AI system that performs multiple steps and uses tools to achieve a goal. Example: An assistant that compares travel options and prepares a trip plan.

## 2. Flow Diagram

```text
      ┌──────────────┐
      │ User Request │
      └──────┬───────┘
             v
      ┌──────────────┐
      │   AI Model   │
      └──────┬───────┘
             v
      ┌──────────────┐
      │ Tool / RAG   │
      │  Retrieval   │
      └──────┬───────┘
             v
      ┌──────────────┐
      │ Check Result │
      └──────┬───────┘
             v
      ┌──────────────┐
      │Final Response│
      └──────────────┘
````

An agent can repeat the tool-use process when more steps are needed to complete a task.

## 3. Comparison Table

| System               | Main Function                          | Example                   |
| -------------------- | -------------------------------------- | ------------------------- |
| LLM                  | Generates text                         | ChatGPT                   |
| AI Application       | Uses AI for a task                     | Language-learning app     |
| RAG                  | Retrieves information before answering | College document chatbot  |
| Tool-Using Assistant | Uses external tools                    | Calculator assistant      |
| AI Agent             | Performs multiple steps toward a goal  | Travel-planning assistant |

## 4. What I Learned

I learned that a chatbot mainly answers questions, while RAG retrieves information to improve answers. Tool-using assistants can access external tools, and agents can combine these capabilities to complete multi-step tasks.

AI-generated information should still be verified, and important actions should require appropriate human approval.



**Next:** Save the file by clicking **Commit changes**.
```
