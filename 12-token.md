# 🔡 AI Tokens – What They Are and Why They Matter

In AI and machine learning (especially for LLMs), a **token** is a unit of text that a model reads, processes, and predicts.

> Think of tokens as the "words" or "building blocks" that AI models use to understand and generate language.

---

## 🧩 What is a Token?

A **token** can be:

- A word: `"hello"`
- A subword: `"un", "believ", "able"`
- A character: `"a", "b", "c"`
- A symbol or space: `" ", ".", ","`

> Tokens are not always full words. LLMs use tokenizers to split text in ways that balance efficiency and meaning.

---

## ✂️ How Tokenization Works

Tokenization is the process of converting raw text into **tokens** that the model understands.

### Examples:

| Text                        | Tokens (approximate)                                  |
| --------------------------- | ----------------------------------------------------- |
| `"Hello world"`             | `["Hello", " world"]`                                 |
| `"Don't do that!"`          | `["Don", "'", "t", " do", " that", "!"]`              |
| `"The cat sat on the mat."` | `["The", " cat", " sat", " on", " the", " mat", "."]` |

> Most models use **Byte Pair Encoding (BPE)** or **SentencePiece** as their tokenizer.

---

## 📏 Token ≠ Word

- A **word** may consist of 1–3 tokens
- English text: ~1 token ≈ 0.75 words
- Example: `"Internationalization"` → `["Intern", "ational", "ization"]`

---

## 🧮 Why Tokens Matter

### 1. Pricing

AI APIs charge **per token** for input and output.

| Provider     | Token Pricing Example (2025)              |
| ------------ | ----------------------------------------- |
| OpenAI GPT-4 | 1M tokens = $10–30 (varies by model tier) |
| Anthropic    | Claude charges per 1M input/output tokens |
| Mistral      | Per-token pricing for open hosted models  |

---

### 2. Context Limit

Models have a **token limit** (aka context window). This is the max number of tokens they can process at once.

| Model       | Context Limit (tokens) |
| ----------- | ---------------------- |
| GPT-3.5     | 4K                     |
| GPT-4 Turbo | 128K                   |
| Claude 3.5  | ~200K                  |
| Gemini 1.5  | 1 million              |

> If your prompt + input + output exceeds this limit, the model will truncate or fail.

---

## 📌 Key Token Concepts

| Term                 | Meaning                                                  |
| -------------------- | -------------------------------------------------------- |
| **Input tokens**     | Tokens you send to the model                             |
| **Output tokens**    | Tokens the model generates in response                   |
| **Token limit**      | Max tokens (input + output) the model can handle at once |
| **Tokenizer**        | Algorithm that breaks text into tokens                   |
| **Embedding tokens** | Tokens converted into numerical vectors (for similarity) |
| **Prompt tokens**    | Tokens that come from instructions or examples           |

---

## 🧠 Token Tips

- Use tools like [OpenAI Tokenizer](https://platform.openai.com/tokenizer) to estimate token usage.
- Shorter prompts save tokens and money.
- Use **few-shot prompting** wisely to balance clarity and token cost.
- In RAG pipelines, filter documents to avoid overloading the context.

---

## 🧪 Example Calculation

Prompt:

“Summarize the following: The mitochondria is the powerhouse of the cell.”

→ ~12–14 tokens (depending on model)

If the model responds with:

“The mitochondria produces energy for the cell.”

→ ~9–10 tokens

**Total tokens billed**: ~22 tokens

---

> In summary, tokens are the language of AI models — understanding them helps you write better prompts, manage costs, and stay within model limits.

---
