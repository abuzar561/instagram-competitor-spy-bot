🕵️♂️ Instagram Competitor Spy Bot

🚀 Overview

This project is an automated Social Media Intelligence Tool designed to track competitors' activity on Instagram.
Instead of manually scrolling, this bot:
Scrapes the latest posts from a list of target accounts.
Calculates the Engagement Rate (Likes + Comments) / Followers in real-time.
Stores all data in Google Sheets for historical analysis.
Alerts me instantly on Discord if a post goes "Viral" (crosses a specific engagement threshold).

⚙️ Architecture
graph LR
A[Python Script] -- Scrapes Data --> B(n8n Webhook)
B -- Filter & Sort --> C{Is Viral?}
C -- Yes --> D[Discord Alert 🚨]
C -- No --> E[Google Sheets 📊]
D --> E

✨ Features
Smart Scraping: Fetches only the latest 5 posts to save resources.
Duplicate Prevention: Uses a local JSON history file to avoid sending the same post twice.
Viral Detection: Automatically flags posts that perform better than average.
Cloud Integration: Connects local Python scripts to n8n Cloud workflows.
Data Visualization: formatted data storage in Google Sheets.
🛠️ Tech Stack
Language: Python (Instaloader, Requests)
Orchestration: n8n (Workflow Automation)
Database: Google Sheets
Notifications: Discord Webhooks

📥 Installation
1. Clone the Repository
git clone [https://github.com/yourusername/instagram-competitor-spy-bot.git](https://github.com/yourusername/instagram-competitor-spy-bot.git)
cd instagram-competitor-spy-bot
2. Install Python Dependencies
pip install -r requirements.txt
3. Setup n8n Workflow
Import the n8n_workflow.json file (included in this repo) into your n8n instance.
Connect your Google Sheets credentials.
Add your Discord Webhook URL.
Activate the workflow and copy the Production Webhook URL.
4. Configure Python Script
Open spy.py and update the following:
COMPETITORS = ['competitor1', 'competitor2']
N8N_WEBHOOK_URL = "YOUR_N8N_PRODUCTION_URL"

🏃♂️ Usage
Run the script manually:
python spy.py
Or set it up on Windows Task Scheduler / Cron Job to run every 4 hours automatically.
📸 Screenshots
(Add screenshots of your n8n workflow and Discord alerts here)
⚠️ Disclaimer
This tool is for educational purposes only. Please respect Instagram's Terms of Service and API rate limits. Use a dummy account for scraping if necessary.

🤝 Contributing
Contributions are welcome! Please open an issue or submit a pull request.
📄 License
MIT Licens
