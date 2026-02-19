# Spotify-AI-agent

## 📌 Description

AI Spotify Mood Playlist Agent est un agent d’intelligence artificielle permettant de générer automatiquement des playlists Spotify personnalisées à partir des émotions exprimées par un utilisateur via Telegram.

L’agent utilise le modèle Mistral pour analyser l’émotion détectée dans le message (nostalgie, tristesse, joie, etc.), puis interroge l’API Spotify afin de créer une playlist adaptée à l’humeur et aux préférences de l’utilisateur.

# Spotify AI Agent 🤖🎵

An intelligent Telegram bot that analyzes your mood through conversation and creates personalized Spotify playlists using Mistral AI and Spotify API.

## Features

- 💬 **Natural Conversation**: Chat naturally with the bot about your feelings
- 🧠 **AI Mood Analysis**: Uses Mistral AI to understand your emotional state
- 🎵 **Smart Playlist Creation**: Automatically generates playlists based on your mood
- ⚡ **Energy Level Detection**: Analyzes energy levels to match music tempo
- 🎶 **Genre Matching**: Suggests appropriate genres based on your mood

## Prerequisites

- Python 3.8 or higher
- A Telegram Bot Token (get it from [@BotFather](https://t.me/botfather))
- A Mistral API Key (get it from [Mistral AI](https://mistral.ai))
- Spotify Developer Account with:
  - Client ID
  - Client Secret
  - Redirect URI configured

## Setup

### 1. Clone or Download the Project

```bash
cd spotify_test
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Configure Environment Variables

1. Copy `.env.example` to `.env`:
   ```bash
   copy .env.example .env
   ```

2. Edit `.env` and fill in your credentials:
   ```
   TELEGRAM_BOT_TOKEN=your_telegram_bot_token_here
   MISTRAL_API_KEY=your_mistral_api_key_here
   SPOTIFY_CLIENT_ID=your_spotify_client_id_here
   SPOTIFY_CLIENT_SECRET=your_spotify_client_secret_here
   SPOTIFY_REDIRECT_URI=http://localhost:8888/callback
   ```

### 4. Get Your API Keys

#### Telegram Bot Token
1. Open Telegram and search for [@BotFather](https://t.me/botfather)
2. Send `/newbot` and follow instructions
3. Copy the token you receive

#### Mistral API Key
1. Go to [Mistral AI Platform](https://console.mistral.ai/)
2. Sign up or log in
3. Navigate to API Keys section
4. Create a new API key

#### Spotify Credentials
1. Go to [Spotify Developer Dashboard](https://developer.spotify.com/dashboard)
2. Create a new app
3. Copy Client ID and Client Secret
4. Add `http://localhost:8888/callback` to Redirect URIs in app settings

### 5. First-Time Spotify Authorization

When you first run the bot, it will need to authorize Spotify access:

1. Run the bot: `python main.py`
2. The first time you use `/create_playlist`, it will prompt you to authorize
3. A browser window will open (or you'll get a URL)
4. Log in to Spotify and authorize the app
5. The authorization token will be cached in `.spotify_cache`

## Usage

### Starting the Bot

```bash
python main.py
```

### Using the Bot

1. **Start a conversation**: Send `/start` to begin
2. **Chat naturally**: Tell the bot how you're feeling, what your mood is, etc.
   - Example: "I'm feeling really energetic today and want to work out!"
   - Example: "I'm a bit sad and need some comforting music"
   - Example: "Feeling nostalgic and want to remember good times"
3. **Create playlist**: When ready, send `/create_playlist`
4. **Get your playlist**: The bot will create a playlist and send you the Spotify link!

### Commands

- `/start` - Initialize the bot and start a new conversation
- `/create_playlist` - Generate a playlist based on your mood
- `/help` - Show help message

## How It Works

1. **Conversation Tracking**: The bot stores your messages to understand context
2. **Mood Analysis**: Mistral AI analyzes your messages to determine:
   - Emotional mood (happy, sad, energetic, etc.)
   - Energy level (1-10 scale)
   - Preferred genres
   - Mood description
3. **Playlist Generation**: Spotify API creates a playlist with:
   - Personalized name based on mood
   - Recommended tracks matching your energy and genres
   - 30 tracks by default
4. **Delivery**: You receive a direct link to your new Spotify playlist

## Project Structure

```
spotify_test/
├── main.py                 # Entry point
├── telegram_bot.py         # Telegram bot handler
├── mood_analyzer.py        # Mistral AI integration for mood analysis
├── spotify_manager.py      # Spotify API integration
├── requirements.txt        # Python dependencies
├── .env.example           # Environment variables template
├── .env                   # Your actual credentials (not in git)
└── README.md              # This file
```

## Troubleshooting

### Bot not responding
- Check that `TELEGRAM_BOT_TOKEN` is correct
- Make sure the bot is running (`python main.py`)

### Spotify authorization issues
- Delete `.spotify_cache` file and try again
- Verify `SPOTIFY_REDIRECT_URI` matches your Spotify app settings
- Check that Client ID and Secret are correct

### Mood analysis not working
- Verify `MISTRAL_API_KEY` is correct
- Check your Mistral API quota/credits

### Playlist creation fails
- Ensure you've authorized Spotify access
- Check that your Spotify account is active
- Verify API credentials are correct

## Security Notes

- Never commit `.env` file to version control
- Keep your API keys secret
- The `.env` file is already in `.gitignore`

## License

This project is for personal/educational use.

## Contributing

Feel free to fork and modify for your own use!



