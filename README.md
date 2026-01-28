<div align="center">

# 🤖 Discord Bot Template

[![Discord.js](https://img.shields.io/badge/discord.js-v14-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.js.org/)
[![Node.js](https://img.shields.io/badge/node.js-v16.9+-43853D?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/)
[![License](https://img.shields.io/badge/license-MIT-blue?style=for-the-badge)](LICENSE)

A robust, modular, and extensible **Discord.js** bot boilerplate designed to jumpstart your development. Built with modern JavaScript standards, slash commands, and a scalable project structure.

[Getting Started](#-getting-started) • [Features](#-features) • [Project Structure](#-project-structure) • [License](#-license)

</div>

---

## ✨ Features

- **🚀 Modern Architecture**: Built on Discord.js v14 with full support for Slash Commands (*Interactions*).
- **📂 Modular Design**: Separate handlers for Commands and Events to keep your codebase clean and maintainable.
- **⚡ Dynamic Loading**: Automatically registers new commands and events on startup—no manual imports required.
- **🔒 Secure**: Environment variable management using `dotenv` to keep your tokens safe.
- **🛠️ Developer Ready**: Includes scripts for development (hot-reload) and deployment.

## 🚀 Getting Started

Follow these steps to get your bot up and running in minutes.

### Prerequisites

- **[Node.js](https://nodejs.org/)** (v16.9.0 or newer)
- **[npm](https://www.npmjs.com/)** (comes with Node.js)
- A **[Discord Account](https://discord.com/)** and a created Application in the [Developer Portal](https://discord.com/developers/applications).

### Installation

1.  **Clone the Repository**
    ```bash
    git clone https://github.com/your-username/TemplateBot.git
    cd TemplateBot
    ```

2.  **Install Dependencies**
    ```bash
    npm install
    ```

3.  **Configuration**
    - Rename the `.env.example` file to `.env`.
    - Open `.env` and configure your credentials:
      ```ini
      DISCORD_TOKEN=your_bot_token_here
      CLIENT_ID=your_application_id_here
      ```

4.  **Register Commands**
    Publish your slash commands to Discord:
    ```bash
    npm run deploy
    ```

5.  **Start the Bot**
    ```bash
    # Production mode
    npm start

    # Development mode (auto-restarts on file changes)
    npm run dev
    ```

---

## 🛠️ Development

### Adding a New Command

1.  Navigate to `commands/utility/` (or create a new folder under `commands/`).
2.  Create a new file, e.g., `hello.js`.
3.  Use the following template:

    ```javascript
    const { SlashCommandBuilder } = require('discord.js');

    module.exports = {
        data: new SlashCommandBuilder()
            .setName('hello')
            .setDescription('Responds with a greeting!'),
        async execute(interaction) {
            await interaction.reply('Hello, world!');
        },
    };
    ```
4.  Run `npm run deploy` to register the new command.

### Adding a New Event

1.  Navigate to the `events/` folder.
2.  Create a new file with the name of the event, e.g., `guildMemberAdd.js`.
3.  Structure it as follows:

    ```javascript
    const { Events } = require('discord.js');

    module.exports = {
        name: Events.GuildMemberAdd,
        execute(member) {
            console.log(`New member joined: ${member.user.tag}`);
        },
    };
    ```

---

## 📂 Project Structure

```plaintext
TemplateBot/
├── commands/             # Slash command files organized by category
│   └── utility/
├── events/               # Event handler files
├── node_modules/         # Dependencies
├── .env                  # Environment variables (Ignored by Git)
├── .env.example          # Example environment configuration
├── .gitignore            # Git ignore rules
├── deploy-commands.js    # Script to register slash commands
├── index.js              # Main entry point
├── package.json          # Project metadata and scripts
└── README.md             # Project documentation
```

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
