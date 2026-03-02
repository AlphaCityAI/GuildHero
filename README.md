# GuildHero Bot

An all-in-one Telegram community management and engagement bot built for crypto-related group chats. Powered by AI analysis, gamification, real-time crypto data, and SUI blockchain airdrops.

## Features

### 🤖 AI Analysis
- **/summarize** `<#>` `[topic]` — AI-powered summary of recent chat messages, optionally filtered by topic
- **/bestof** `<#>` — Curated digest of the best messages (Most Humorous, Most Degen, Best Alpha, Most Helpful)
- **/vibecheck** `<#>` `[topic]` — Sentiment analysis with bullish/bearish classification

### 💰 Crypto Tools
- **/price** `<symbol>` — Live cryptocurrency price lookup with 24h change, market cap, and volume
- **/airdrop** `<count>` `<amount>` — Airdrop SUI tokens to top scorers by replying to a `/score` leaderboard (admin only)
- **/settoken** `<coin_type>` — Set the airdrop token type for the group (admin only, default: `0x2::sui::SUI`)

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
| 💎 | Diamond Hands | Active for 30+ days |

### 🗓️ Group Management
- **/calendar** — Interactive event calendar (admin only)
- **/events** — List upcoming events
- **/settimezone** `<timezone>` — Set timezone for event announcements (admin only)
- **/setwelcome** `on|off` — Toggle new member welcome messages (admin only, default: off)
- **/wallet** — Submit or check wallet address (private via DM)
- **/copypasta** — Generate a copypasta from your message history

### 🤝 Community
- Optional new member welcome messages (admin-configurable)
- Event announcements at 8 AM in the group's timezone

## Setup

### Requirements
- Python 3.10+
- A [Telegram Bot Token](https://core.telegram.org/bots#botfather)
- An [OpenAI API Key](https://platform.openai.com/api-keys)
- [Replit](https://replit.com/) account (for database) or adapt the database layer
- (Optional) A SUI wallet private key for airdrop functionality

### Installation

```bash
pip install -r requirements.txt
```

### Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| `TELEGRAM_BOT_TOKEN` | Yes | Your Telegram bot token from BotFather |
| `OPENAI_API_KEY` | Yes | Your OpenAI API key |
| `SUI_PRIVATE_KEY` | No | Hex-encoded 32-byte Ed25519 private key (64 hex characters) for the bot's SUI wallet (required for `/airdrop`) |
| `SUI_RPC_URL` | No | SUI JSON-RPC endpoint (defaults to `https://fullnode.mainnet.sui.io:443`) |

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
- **SUI JSON-RPC** — Blockchain token transfers for airdrops
- **PyNaCl** — Ed25519 signing for SUI transactions
- **httpx** — Async HTTP client for API calls

## License

This project is provided as-is for community use.
