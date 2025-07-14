# 🤖 Roles in AI Chat Systems (system, user, assistant, tool)

In modern conversational AI (e.g., OpenAI's ChatGPT, Anthropic's Claude, Google Gemini), messages are structured using roles that define **who is speaking** and **how the model should behave**.

---

## 🧠 What Are Roles?

Each message sent to or from the model is tagged with a **role** to establish the context of the dialogue. There are four primary roles:

- `system`
- `user`
- `assistant`
- `tool`

---

## 🔹 1. `system` Role

### Description:

The `system` message sets up the assistant’s behavior, tone, and limitations before the conversation starts.

### Purpose:

- Define the assistant's personality (e.g., friendly, formal, concise)
- Set rules or guardrails
- Provide high-level instructions

### Characteristics:

- Used once at the start
- Not shown to users in most interfaces

### Example:

```json
{
  "role": "system",
  "content": "You are a helpful, professional assistant that responds only in markdown format."
}
```

---

## 🙋‍♂️ 2. `user` Role

### Description:

Represents the **human user’s input** — instructions, questions, or prompts.

### Purpose:

- Drives the conversation
- Tells the assistant what to do

### Characteristics:

- Can appear multiple times in a conversation
- Can include context, commands, or follow-up questions

### Example:

```json
{
  "role": "user",
  "content": "Explain what reinforcement learning is in simple terms."
}
```

---

## 🤖 3. `assistant` Role

### Description:

Represents the model’s generated response to the user.

### Purpose:

- Provides output like answers, explanations, code, summaries, etc.

### Characteristics:

- Can reference both `system` and `user` messages
- Formatted in natural language or structured formats like code/JSON

### Example:

```json
{
  "role": "assistant",
  "content": "Reinforcement learning is a type of machine learning where an agent learns to make decisions by receiving rewards or penalties..."
}
```

---

## 🛠️ 4. `tool` Role

### Description:

Represents the **output from an external tool or function** that the assistant requested to use.

### Purpose:

- Enables AI agents to call tools, APIs, or databases
- Returns data for the assistant to process and respond to

### Characteristics:

- Usually part of function-calling or plugin-based systems
- Must include the `tool_call_id` to map to the original request

### Example:

```json
{
  "role": "tool",
  "tool_call_id": "func_001",
  "content": "{ \"temperature\": \"27°C\", \"condition\": \"Partly Cloudy\" }"
}
```

---

## 🔄 Full Example Flow

```json
[
  { "role": "system", "content": "You are a helpful assistant." },
  { "role": "user", "content": "What's the weather in Chennai?" },
  {
    "role": "assistant",
    "tool_calls": [
      { "function": "getWeather", "arguments": "{ \"city\": \"Chennai\" }" }
    ]
  },
  {
    "role": "tool",
    "tool_call_id": "func_001",
    "content": "{ \"temperature\": \"32°C\", \"condition\": \"Sunny\" }"
  },
  {
    "role": "assistant",
    "content": "It's currently 32°C and sunny in Chennai."
  }
]
```

---

## 🧩 Summary Table

| Role        | Represents             | Typical Use Case                                 |
| ----------- | ---------------------- | ------------------------------------------------ |
| `system`    | Setup prompt           | Define assistant's behavior, tone, constraints   |
| `user`      | Human input            | Ask questions, give instructions or prompts      |
| `assistant` | Model’s response       | Generated replies to user inputs                 |
| `tool`      | External function/tool | Return of structured data to model from a plugin |

---

> These roles help maintain structured, logical, and extensible AI conversations. Understanding and using them effectively is key to building advanced AI agents and chatbots.
