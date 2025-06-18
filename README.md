# 💬 Sentiment Responder

An intelligent AI tool that **detects the sentiment** of a user review and generates an **appropriate response** automatically — whether it's praise or criticism.

🔗 **Live App**: [sentimentresponder.streamlit.app](https://sentimentresponder.streamlit.app/)

---

## 🧠 What It Does

This app performs the following tasks:

1. ✅ **Classifies the sentiment** of a user's feedback (either `positive` or `negative`).
2. 💬 **Generates a relevant response** tailored to the sentiment detected.

---

## 🎯 Use Cases

- Automate **customer feedback handling**
- Instantly respond to **positive reviews** with gratitude
- Address **negative reviews** politely and professionally
- Useful for product managers, support teams, and business owners

---

## 📌 Example

### Input Review:
> “I loved the product! It arrived early and works like a charm.”

### Output:
- **Sentiment**: Positive  
- **Response**: "Thank you so much for your kind words! We're thrilled to hear you're enjoying the product."

---

## ⚙️ How It Works

### 🧩 Modular Workflow

- **Sentiment Classification:**  
  Uses a structured LangChain prompt + Pydantic schema to identify sentiment.
  
- **Dynamic Response Generation:**  
  Uses conditional branching (`RunnableBranch`) to select the appropriate prompt based on sentiment.

### 🛠️ Tools & Libraries

| Component         | Tool/Library                         |
|------------------|--------------------------------------|
| UI               | [Streamlit](https://streamlit.io)    |
| LLM Backend      | [OpenAI GPT-4](https://openai.com)   |
| Orchestration    | [LangChain](https://www.langchain.com) |
| Schema Parsing   | `PydanticOutputParser`               |
| Branch Logic     | `RunnableBranch`, `RunnableLambda`   |
| Environment      | `python-dotenv`                      |



