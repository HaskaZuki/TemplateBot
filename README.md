# TemplateBot

A simple, clean, and extensible Discord.js bot template to help you get started with bot development quickly.

## Features

- **Slash Commands**: Modern command handling using Discord's interaction system.
- **Event Handling**: Modular event system to keep your code organized.
- **Easy Configuration**: Uses `.env` for secure token and ID storage.
- **Dynamic Loading**: Automatically loads new commands and events without needing to edit the main file.
- **MIT API**: Free to use and modify.

## Prerequisites

- [Node.js](https://nodejs.org/) (v16.9.0 or higher)

## Setup Guide

### 1. Clone or Download
Clone this repository or download the ZIP file and extract it to a folder.

### 2. Install Dependencies
Open a terminal in the project folder and run:
\```bash
npm install
\```

### 3. Configure Environment Variables
1. Rename `.env.example` to `.env`.
2. Open `.env` and fill in your details:
   - `DISCORD_TOKEN`: Your bot's token from the [Discord Developer Portal](https://discord.com/developers/applications).
   - `CLIENT_ID`: Your bot's Application ID (User ID).

### 4. Deploy Commands
Before running the bot, you need to register the slash commands with Discord. Run:
\```bash
npm run deploy
\```
You should see a message saying "Successfully reloaded application (/) commands."

### 5. Run the Bot
Start the bot using:
\```bash
npm start
\```
or for development (auto-restarts on save):
\```bash
npm run dev
\```

## Adding New Commands

1. Go to the `commands` folder.
2. You can create new subfolders (categories) or use the existing `utility`.
3. Create a new `.js` file (e.g., `hello.js`).
4. Paste the following template:

\```javascript
const { SlashCommandBuilder } = require('discord.js');

module.exports = {
	data: new SlashCommandBuilder()
		.setName('hello')
		.setDescription('Says hello!'),
	async execute(interaction) {
		await interaction.reply('Hello there!');
	},
};
\```
5. Run `npm run deploy` to update the commands on Discord.
6. Restart the bot (if not using `npm run dev`).

## Project Structure

- `index.js`: The main entry point of the bot.
- `deploy-commands.js`: Script to register commands.
- `commands/`: Folder for all your slash commands.
- `events/`: Folder for event handlers (like `ready`, `interactionCreate`).
- `.env`: Stores secret keys (DO NOT SHARE THIS FILE).

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
