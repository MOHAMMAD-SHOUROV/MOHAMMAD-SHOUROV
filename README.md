# 🤖 SHOUROV-BOT

A powerful Facebook Messenger bot built by [Shourov](https://www.facebook.com/www.xsxx.com365) with modular command support, cookie-based login, and OpenAI integration.

---

## 🚀 Features

- ✅ Cookie login system (no Page Access Token)
- 🤖 Chat with OpenAI GPT
- 🎥 Video & media downloader API
- 📜 Modular command handler
- 🧩 Event-based system
- 💬 Group reply, auto welcome
- ⚙️ Hosted on **Vercel** and **Render**

---

## 🌐 Live Endpoints

- 🔗 **Webhook URL** (Vercel):  
  `https://fb-webhook-bot-mjxc.vercel.app/api/webhook`

- 🧠 **Video API (Render)**:  
  ``

---

## 🛠️ How to Run

```bash
# Step 1: Clone the repository
git clone https://github.com/MOHAMMAD-SHOUROV/MOHAMMAD-SHOUROV.git
cd SHOUROV-BOT

# Step 2: Install dependencies
npm install

# Step 3: Create .env or .enu in bot folder
echo "OPENAI_API_KEY=your-key-here" > bot/.enu

# Step 4: Run the bot
npm start

---

## 🚀 GitHub Actions Deployment

Automatically installs dependencies and prepares bot on every push to `main`.

```yaml


---



## name: SHOUROV-BOT Deployment

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  deploy:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout Repository
        uses: actions/checkout@v3

      - name: Setup Node.js
        uses: actions/setup-node@v3
        with:
          node-version: '18'

      - name: Install Dependencies
        run: npm install

      - name: Show Directory Tree (for debug)
        run: tree -L 2 || ls

      - name: Check for .env file
        run: |
          if [ ! -f ".env" ]; then
            echo ".env file not found, skipping..."
          fi

      - name: Run Bot (preview)
        run: |
          echo "✅ SHOUROV-BOT setup complete. You can add custom deploy scripts here."
