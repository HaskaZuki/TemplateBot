# TemplateBot

A clean starter template for Discord.js v14 bots. Includes handler for slash commands and events.

## Setup

1. **Install dependencies**
   ```bash
   npm install
   ```

2. **Configuration**
   Copy `.env.example` to `.env` and fill in your values:
   ```txt
   DISCORD_TOKEN=your_token
   CLIENT_ID=your_id
   ```

3. **Deploy Commands**
   Run this once to register slash commands (or whenever you add new ones):
   ```bash
   npm run deploy
   ```

4. **Start**
   ```bash
   npm start
   # or for dev
   npm run dev
   ```

## Development

- **Commands**: Add new files to `commands/folder_name/`.
- **Events**: Add new files to `events/`. 

The bot automatically loads files from these directories on startup.

## License

MIT
