# LinkedIn launch post

🚀 I’ve built and deployed an **AI Finance Operations Agent**.

The project explores how GenAI, deterministic business rules, and analytics can work together to automate a common finance workflow: invoice processing.

### What it does

📄 Extracts structured fields from invoice PDFs  
🤖 Uses Google Gemini for AI-assisted extraction  
🛡️ Falls back to deterministic parsing when AI is unavailable  
✅ Validates invoice totals independently  
🔁 Detects potential duplicate invoices  
📊 Flags unusual vendor spending  
⚠️ Assigns invoice risk levels  
📈 Presents finance KPIs and trends in a Streamlit dashboard

The demo dataset contains **7 invoices**, including examples of valid invoices, an invalid total, a duplicate invoice, and an unusually high vendor invoice.

One design principle I focused on was **not relying blindly on an LLM**. AI is used for extraction, while business rules independently validate the resulting data.

### Tech stack

Python | Streamlit | Pandas | Pydantic | PyPDF | Google Gemini

🌐 **Live Demo:** https://ai-finance-operations-agent-thkprarbd4kpd38cbba2qg.streamlit.app/

💻 **GitHub:** https://github.com/akkisakpal/AI-Finance-Operations-Agent

This project builds on my interest in **AI, data analytics, anomaly detection, and data engineering**, while focusing on a practical business workflow.

#Python #AI #GenAI #DataAnalytics #MachineLearning #Streamlit #DataEngineering #FinanceAutomation #GitHub
