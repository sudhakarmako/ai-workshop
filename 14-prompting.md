# 💬 Prompting Guide for AI

Prompting is the skill of instructing a language model to produce useful, accurate, and structured responses. A well-crafted prompt can significantly improve the quality of the AI’s output.

---

## 🧠 What Is a Prompt?

A **prompt** is the input you give to an AI model — a question, instruction, command, or context — to generate a desired response.

> Think of it as "programming in natural language."

---

## 🧩 CRAFT Prompt Framework

Use the **CRAFT** method to create effective prompts:

| Component       | Description                                 | Example                                              |
| --------------- | ------------------------------------------- | ---------------------------------------------------- |
| **C** – Context | Provide background or situation             | "You're helping a student write a science report..." |
| **R** – Role    | Assign a persona or expertise to the AI     | "Act as a data scientist..."                         |
| **A** – Action  | Specify the task to complete                | "Summarize the following document..."                |
| **F** – Format  | Define the desired output style or layout   | "Return the result in markdown with bullet points."  |
| **T** – Tone    | Set the tone or personality of the response | "Use a formal, professional tone."                   |

---

## 🛠️ Core Prompting Techniques

### ✅ Clear Instruction

Be specific about what you want.

**Example:**

```
Summarize this text in 3 bullet points using simple language.
```

---

### 📄 Format Constraints

Tell the AI how to present the result.

**Example:**

```
Return output as JSON with keys: topic, summary, sentiment.
```

---

### ✍️ Role Prompting

Assign the AI a specific role or perspective.

**Example:**

```
You are a product manager preparing a launch deck.
```

---

### 🔁 Few-Shot Prompting

Provide 1–3 examples in the prompt to guide the model.

**Example:**

```
Q: Capital of France?
A: Paris
Q: Capital of Japan?
A: Tokyo
Q: Capital of Brazil?
A:
```

---

### 🧠 Chain-of-Thought Prompting

Encourage the model to show its reasoning.

**Example:**

```
Let's solve this step-by-step.
```

---

## 🔎 Prompting Styles

| Style                | Description                              | Use Case                       |
| -------------------- | ---------------------------------------- | ------------------------------ |
| **Zero-shot**        | Ask directly with no examples            | General Q&A                    |
| **Few-shot**         | Include examples of task behavior        | Text classification            |
| **Chain-of-Thought** | Encourage step-by-step reasoning         | Math, logic, complex decisions |
| **Instructional**    | Use clear step instructions              | Summarization, rewriting       |
| **Role-based**       | Assign persona/identity to the assistant | Coaching, simulations          |

---

## 🧪 Prompt Refinement Workflow

1. **Start simple** – Ask the core question or task
2. **Test** – Observe the output
3. **Add structure** – Specify format, tone, or constraints
4. **Use examples** – Show what you expect
5. **Iterate** – Tweak and improve based on results

---

## 🧰 Prompting Tools

| Tool/Library         | Purpose                             |
| -------------------- | ----------------------------------- |
| OpenAI Playground    | Interactive prompt experiments      |
| PromptLayer          | Track, version, and analyze prompts |
| LangChain Templates  | Prompt templating and routing       |
| PromptPerfect        | Automatic prompt optimization       |
| Tiktoken / Tokenizer | Estimate token usage                |

---

## 📝 Example Prompt Using CRAFT

```
Context: You're writing a product update for customers.
Role: Act as a SaaS copywriter.
Action: Write a short changelog of new features.
Format: Use markdown with 3 bullet points.
Tone: Friendly and enthusiastic.
```

---

> Prompting is a powerful interface between humans and machines — the better you write them, the more value you unlock from AI.
