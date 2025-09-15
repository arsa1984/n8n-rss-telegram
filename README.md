# n8n Workflow: RSS → LLM Summarization → Telegram

This project is an **automation workflow** built with [n8n](https://n8n.io) that:

- Fetches the latest news items from an (RSS) feed  
- Summarizes the content using an (LLM) (e.g. OpenAI)  
- Extracts the article image from the webpage  
- Sends the summary, link, and image to a (Telegram) channel  

---

## 📂 Files
- `workflow.json`  
  The full workflow definition (importable into n8n).  

---

## 🚀 How to Use
1. Install (n8n) locally or create an account at  
   [n8n.cloud](https://n8n.cloud)  
2. Import the workflow:  
   - Menu → Import from File → `workflow.json`  
3. Configure your credentials:  
   - (OpenAI API Key)  
   - (Telegram Bot Token) + (Chat ID)  
4. Activate the workflow to start automated runs.  

---

## 🔑 Setup Credentials
To use this workflow, you need to set up your own credentials in (n8n):  

- (OpenAI API Key) → Create a credential of type `(OpenAI API)` and enter your key.  
- (Telegram Bot Token) → Create a credential of type `(Telegram)` and paste your bot token.  
- (Chat ID) → Set the target chat/channel ID in the Telegram node configuration.  

---

## 🖼️ Example Output
Each Telegram message will contain:  
- Article title  
- Summary in 3–5 bullet points  
- Original link  
- Article image  
