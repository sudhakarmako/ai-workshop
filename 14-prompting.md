# 💬 Prompting Basics for AI

Prompting is the art of **giving clear, structured instructions to an AI** to get the best possible output.

> Think of it like programming with plain English — the better the prompt, the better the result.

---

## 🧠 What is a Prompt?

A **prompt** is the input you send to an AI model. It can be:

- A question: `"What is quantum computing?"`
- A task: `"Summarize this article:"`
- A command: `"Translate this to French:"`
- A dialogue: `"You are a helpful assistant..."`

---

## 🛠️ Core Prompting Techniques

### 1. ✅ Clear Instruction

Be explicit. State what you want and how you want it.

**Example:**

```
Summarize the following text in 3 bullet points using simple language.
```

---

### 2. 📄 Format Constraints

Set output structure expectations.

**Example:**

```
Write a JSON object with keys: title, author, and summary.
```

---

### 3. ✍️ Role Prompting

Give the AI a persona or perspective.

**Example:**

```
You are a senior frontend developer. Review this code and suggest improvements.
```

---

### 4. 🔁 Few-Shot Prompting

Provide 1–3 examples in the prompt to guide the model.

**Example:**

```
Q: What's the capital of France?
A: Paris
Q: What's the capital of Japan?
A: Tokyo
Q: What's the capital of Brazil?
A:
```

---

### 5. 🧠 Chain-of-Thought Prompting

Ask the model to **show its reasoning steps**.

**Example:**

```
Let's think step-by-step to solve this math problem.
```

---

## 🔎 Advanced Prompting Styles

| Style                | Description                                   | Use Case                          |
| -------------------- | --------------------------------------------- | --------------------------------- |
| **Zero-shot**        | Ask a question without examples               | Simple Q&A                        |
| **Few-shot**         | Provide task examples in the prompt           | Text classification, translations |
| **Chain-of-Thought** | Encourage reasoning by showing thinking steps | Math, logic, coding               |
| **Instructional**    | Give clear task instructions                  | Summarization, rewriting          |
| **Role-based**       | Assign a persona or job to the model          | Simulations, advice               |

---

## 📋 Prompting Best Practices

- ✅ Be clear, specific, and goal-oriented
- ✅ Include examples when possible
- ✅ Define the format (e.g., bullet list, JSON, markdown)
- ✅ Use constraints ("Limit to 100 words", "Use only 3 sentences")
- ❌ Avoid vague or ambiguous instructions

---

## 🧪 Prompt Refinement Workflow

1. **Start simple** – Try a basic version
2. **Test** – See what kind of output you get
3. **Add structure** – Specify output format or tone
4. **Include examples** – Guide behavior
5. **Adjust tone** – Formal, casual, technical, etc.

---

## 🧰 Tools & Helpers

| Tool                                                        | Use                                     |
| ----------------------------------------------------------- | --------------------------------------- |
| [OpenAI Playground](https://platform.openai.com/playground) | Experiment with prompts                 |
| PromptLayer                                                 | Track, debug, and version prompts       |
| LangChain / LlamaIndex                                      | Prompt templating and orchestration     |
| PromptPerfect                                               | Suggests optimizations for your prompts |
| VS Code Extensions                                          | Inline LLM prompt testers               |

---

## 🎯 Example Prompts

**1. Markdown Output**

```
Convert the following into markdown with headers and bullet points.
```

**2. LLM-as-Critic**

```
You are an AI writing tutor. Review this paragraph and suggest improvements in grammar, clarity, and style.
```

**3. Chat Memory Simulation**

```
Here's what we talked about earlier: [paste chat history]
Now, based on that, continue the conversation.
```

---

## 🧠 Prompting Framework: The CRAFT Method

Use the **CRAFT** formula to create clear, powerful prompts for AI models.

| Step            | Description                             | Example                                                |
| --------------- | --------------------------------------- | ------------------------------------------------------ |
| **C** – Context | Provide background or situation         | "You are helping a user write a professional email..." |
| **R** – Role    | Assign a persona or expertise to the AI | "Act as a UX designer..."                              |
| **A** – Action  | Specify the task you want the AI to do  | "Summarize this text in 3 bullet points..."            |
| **F** – Format  | Define the desired output format        | "Respond in markdown with headings and bullets..."     |
| **T** – Tone    | Set the tone/style of the response      | "Use a friendly, conversational tone..."               |

---

## 📝 Example Prompt Using CRAFT

```txt
Context: You’re preparing slides for a product launch.
Role: Act as a senior marketing strategist.
Action: Create 3 slide titles with supporting bullet points for the pitch deck.
Format: Present the output in markdown.
Tone: Persuasive and energetic.
```

---

> Try using **CRAFT** next time you interact with an AI tool. It helps you get clearer, more reliable, and useful results — fast.

---

> Prompting is a skill — the more you practice, the better your results. Think like a UX designer, teacher, and engineer all at once.
