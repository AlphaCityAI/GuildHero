# GuildHero Bot

An all-in-one Telegram community management and engagement bot built for crypto-related group chats. Powered by AI analysis, gamification, and real-time crypto data.

## Features

### 🤖 AI Analysis
- **/summarize** `<#>` `[topic]` — AI-powered summary of recent chat messages, optionally filtered by topic
- **/bestof** `<#>` — Curated digest of the best messages (Most Humorous, Most Degen, Best Alpha, Most Helpful)
- **/vibecheck** `<#>` `[topic]` — Sentiment analysis with bullish/bearish classification

### 💰 Crypto Tools
- **/price** `<symbol>` — Live cryptocurrency price lookup with 24h change, market cap, and volume
- **/gm** — Daily "GM" tracking with streaks and a community leaderboard (`/gm board`)

### 📊 Leaderboards & Stats
- **/score** — Detailed AI-integrated contribution leaderboard with quality, tone, helpfulness, and humor scoring (admin only)
- **/publicscore** — Simple public leaderboard (admin only)
- **/mystats** — Personal stats including message count, rank, and badges
- **/stats** — Group-wide statistics and top contributors

### 🏅 Badges & Gamification
- **/mybadges** — View your earned badges
- **/allbadges** — See all available badges

| Badge | Name | Requirement |
|-------|------|-------------|
| ✍️ | Contributor | 100+ messages |
| 🦸 | Hero | 500+ messages |
| ⚡️ | God-like | 1,000+ messages |
| 👑 | Weekly Champion | #1 in weekly leaderboard |
| ✨ | High Quality | Quality score 18+ |
| 🙏 | Helping Hand | Helpfulness score 18+ |
| ☀️ | Early Bird | 7-day GM streak |
| 🔥 | GM Maxi | 30-day GM streak |
| 💎 | Diamond Hands | Active for 30+ days |

### 🗓️ Group Management
- **/calendar** — Interactive event calendar (admin only)
- **/events** — List upcoming events
- **/settimezone** `<timezone>` — Set timezone for event announcements (admin only)
- **/wallet** — Submit or check wallet address (private via DM)
- **/copypasta** — Generate a copypasta from your message history

### 🤝 Community
- Automatic new member welcome messages
- Event announcements at 8 AM in the group's timezone

## Setup

### Requirements
- Python 3.10+
- A [Telegram Bot Token](https://core.telegram.org/bots#botfather)
- An [OpenAI API Key](https://platform.openai.com/api-keys)
- [Replit](https://replit.com/) account (for database) or adapt the database layer

### Installation

```bash
pip install -r requirements.txt
```

### Environment Variables

| Variable | Description |
|----------|-------------|
| `TELEGRAM_BOT_TOKEN` | Your Telegram bot token from BotFather |
| `OPENAI_API_KEY` | Your OpenAI API key |

### Running

```bash
python "GuildHero/GuildHero Bot"
```

## Architecture

The bot is a single-file Python application using:
- **python-telegram-bot** — Telegram Bot API framework
- **OpenAI GPT-3.5** — AI-powered chat analysis and content generation
- **Replit DB** — Persistent key-value storage
- **CoinGecko API** — Real-time cryptocurrency price data
- **httpx** — Async HTTP client for API calls

## License

This project is provided as-is for community use.
