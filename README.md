# TemplateBot

We keep it simple. Here are the core packages driving this bot:

*   **[discord.js](https://discord.js.org/)** (v14): The main library for interacting with the Discord API.
*   **[dotenv](https://www.npmjs.com/package/dotenv)**: Keeps your secrets (like tokens) safe and out of your code.
*   **[nodemon](https://www.npmjs.com/package/nodemon)** (Dev): Automatically restarts your bot whenever you save a file, so you don't have to do it manually.

## ⚡ How to Get Started

Getting this up and running takes about 2 minutes.

### 1. Grab the Code
Clone this repo to your machine:
```bash
git clone https://github.com/HaskaZuki/TemplateBot.git
cd TemplateBot
```

### 2. Install Dependencies
Run this command to install the packages listed above:
```bash
npm install
```

### 3. Set Your Secrets
You'll see a file called `.env.example`. Rename it to just `.env` and paste your bot token and client ID inside.
```ini
DISCORD_TOKEN=your_token_goes_here
CLIENT_ID=your_client_id_goes_here
```
> **Note:** Never share your `.env` file with anyone!

### 4. Register Commands
Before you start, you need to tell Discord about your slash commands. We have a script for that:
```bash
npm run deploy
```

### 5. Launch 🚀
You're ready to go.
```bash
npm start
```
*Working on new features? Use `npm run dev` to watch for changes automatically.*

## 📂 Where things live
*   **`commands/`**: Drop your new command files here. We use subfolders (like `utility`) to keep things organized.
*   **`events/`**: Listen for things like `ready` or `interactionCreate` here.
*   **`index.js`**: The entry point. It handles the dynamic loading magic.

---
## 🛠 Support & Contact

If you encounter any issues or want to reach out directly, feel free to join our community or add me on Discord.

[![Discord Support](https://img.shields.io/badge/Discord-Support%20Server-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/9RWJqdCg)
[![Discord](https://img.shields.io/badge/Discord-Contact%20Me-white?style=for-the-badge&logo=discord&logoColor=5865F2)](https://discord.com/users/710245394533318676)

> **Discord Username:** `zuki96_`
