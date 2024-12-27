# 🤖 EissaBot

Integrated Twitch & Discord bot with OBS support 🎮

## ✨ Features

### 🎭 OBS Integration
- 🎬 Scene control via chat and voice
- 🔄 Automatic scene switching
- 📡 WebSocket connection with OBS

### 💬 Twitch
- 🤝 Automatic greetings
- 📎 Automatic clip creation
- 🎯 Customizable commands
- 🔗 Direct Discord integration

### 🎮 Discord
- 📢 Live stream notifications
- 🎥 Automatic clip sharing
- 👥 Live streaming roles
- 🗣️ Voice control via Deepgram
- 🎙️ Voice commands for stream control

## ⚙️ Requirements

- Node.js v16 or higher
- OBS Studio with WebSocket enabled
- Twitch bot account
- Discord bot account
- Deepgram API key

## 🚀 Installation

1. Install packages:

```bash
npm install
```

2. Configure `config.json`:

```json
{
    "OBS": {
        "address": "ws://localhost:4455",
        "password": "your-obs-password"
    },
    "twitch": {
        "channel": "your-channel",
        "command": "!scene"
    },
    "deepgram": {
        "apiKey": "your-deepgram-key"
    }
}
```

## 📝 Commands

### Voice Commands
- Change scene: "hey bot switch scene to ..."
- Create clip: "hey bot create clip"
- Change title: "hey bot change title to ..."

### Twitch
- `!clip` - Create clip of current moment
- `!rank` - Show Valorant rank
- `!scene` - Change OBS scene
- `!mouse` - Mouse information
- `!sens` - Sensitivity settings

### Discord
- `/alert` - Add channel to alerts
- `/refresh` - Update commands

## 📊 Logging System

- 📁 Error logs in `logs/error.log`
- 📁 Combined logs in `logs/combined.log`
- 🎨 Colorized console logging
- 📊 Timestamped operations

## 🛠️ Customization

### Auto Responses
Modify responses in `src/twitch/config/auto-responses.js`:

```js
module.exports = {
    greetings: {
        'hello': (username) => `@${username} Welcome!`,
    },
    homies: {
        'username': 'custom-response'
    }
};
```

### Voice Commands
Customize voice commands and add new ones in `src/voice/commands/`:
- Modify command keywords
- Add new commands
- Customize voice responses

## 📄 License

MIT
