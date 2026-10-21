6: Explain Chatbot vs. RAG vs. Agent, with a Flow Diagram

## 1. Understanding the Concepts

### 1. Large Language Model (LLM)

A Large Language Model is an AI model trained on large amounts of text to understand prompts and generate human-like responses. It can explain concepts, answer questions, and summarize information.

**Example:** Asking ChatGPT to explain how solar panels generate electricity.

### 2. AI Application

An AI application is a software system that integrates AI to provide a useful service. It combines an AI model with an interface and application logic to perform a particular task.

**Example:** A language-learning application that uses AI to help users practise conversations.

### 3. Retrieval-Augmented Generation (RAG)

RAG is an approach in which a system retrieves relevant information from a collection of documents or another knowledge source and provides it to an AI model to help generate a more relevant answer.

**Example:** An employee assistant that answers questions using a company's HR policies and leave guidelines.

### 4. Tool-Using Assistant

A tool-using assistant can call external tools or services to obtain information or perform specific operations instead of relying only on its generated text.

**Example:** An assistant that uses a calculator to compare monthly electricity bills.

### 5. AI Agent

An AI agent is a system designed to work toward a goal by selecting actions, using available tools, evaluating results, and continuing with further steps when needed.

**Example:** An event-planning assistant that checks venue availability, compares catering options, and prepares a plan within a specified budget.

## 2. Flow Diagram

The following diagram illustrates a possible workflow in which an AI system receives a request, processes it, uses a tool or retrieves information, evaluates the result, and responds.

```text
       ┌─────────────────────┐
       │     User Request    │
       │  Defines the goal   │
       └──────────┬──────────┘
                  |
                  v
       ┌─────────────────────┐
       │   AI Model (LLM)    │
       │ Understands request │
       └──────────┬──────────┘
                  |
                  v
       ┌─────────────────────┐
       │ Decision: Need a    │
       │ tool or information?│
       └──────────┬──────────┘
                  |
                  v
       ┌─────────────────────┐
       │ Tool / RAG Retrieval│
       │ Searches or acts    │
       └──────────┬──────────┘
                  |
                  v
       ┌─────────────────────┐
       │ Inspect the Result  │
       │ Check useful data   │
       └──────────┬──────────┘
                  |
                  v
       ┌─────────────────────┐
       │ Final Response or   │
       │ Next Action         │
       └─────────────────────┘
````

An agent may repeat the tool-use and result-inspection steps if more work is required. A simpler chatbot may respond directly without using external tools.

## 3. Comparison Table

| System               | Main Function                                                                | Example                                            |
| -------------------- | ---------------------------------------------------------------------------- | -------------------------------------------------- |
| LLM                  | Generates text based on a prompt and learned patterns.                       | Explaining a scientific concept.                   |
| AI Application       | Uses AI as part of a software product.                                       | An AI-powered language-learning app.               |
| RAG                  | Retrieves relevant information to support an answer.                         | Answering questions from company policy documents. |
| Tool-Using Assistant | Uses external tools or services to obtain information or perform operations. | Calculating electricity costs using a calculator.  |
| AI Agent             | Works through multiple steps to achieve a goal.                              | Comparing event venues and preparing a budget.     |

## 4. Practical Example: Planning an Event

Suppose I need to organize a college technical workshop with a limited budget.

1. **User Request:** I provide the date, expected number of participants, and available budget.
2. **AI Model:** The system interprets the requirements and identifies what needs to be arranged.
3. **Information Retrieval:** It searches available venue details and retrieves relevant information.
4. **Tool Usage:** It calculates estimated expenses and compares different options.
5. **Result Inspection:** It checks whether the proposed arrangements fit the budget and requirements.
6. **Final Response:** It presents a suggested plan and asks for my approval before making bookings or payments.

This workflow demonstrates how an agentic system can combine a language model, information retrieval, and tools to work toward a goal. The exact capabilities depend on the system and the permissions it has been given.

## 5. Chatbot vs. RAG vs. Agent

A basic chatbot responds to a user's message using its available model and context. A RAG-based chatbot can retrieve relevant external information before producing an answer. An agent can use a model and tools to carry out a sequence of steps toward a goal.

These approaches are not mutually exclusive. An AI application can combine a chatbot interface, RAG, and agent capabilities.

## 6. What I Learned

I learned that an LLM, an AI application, RAG, a tool-using assistant, and an AI agent describe different parts or capabilities of an AI system.

A language model generates responses, RAG supplies relevant retrieved information, and tools allow a system to perform operations or access external services. An agent can coordinate these capabilities across multiple steps to achieve a goal.

I also learned that an AI system should not automatically be trusted to take every action. Important results should be checked, and consequential actions such as bookings or payments should require appropriate authorization.

## 7. Conclusion

Understanding these concepts helps me distinguish between systems that primarily answer questions and systems that can retrieve information, use tools, and work toward completing tasks. This knowledge provides a foundation for using AI responsibly in future engineering projects.


```

