<div align="center">
    <h1>📟 JUPITER PYTHON CLI 🪐</h1>

https://github.com/0xTaoDev/jupiter-python-cli/assets/152310566/81f79ed5-8c47-469f-aeb8-c3be70c9541f

</div>

---

<p align="center">
    <img src="https://img.shields.io/github/stars/0xtaodev/jupiter-python-cli">
    <img src="https://img.shields.io/github/forks/0xtaodev/jupiter-python-cli">
    <br>
    <img src="https://img.shields.io/github/issues/0xtaodev/jupiter-python-cli">
    <img src="https://img.shields.io/github/issues-closed/0xtaodev/jupiter-python-cli">
    <br>
    <img src="https://img.shields.io/github/languages/top/0xtaodev/jupiter-python-cli">
    <img src="https://img.shields.io/github/last-commit/0xtaodev/jupiter-python-cli">
    <br>
</p>

# 📖 Introduction
**Jupiter Python CLI** is a Command Line Interface (CLI) where you can use **[Jupiter](https://jup.ag/) features** including a **Sniper Bot**.<br>

# ⚠️ Disclaimer
**Please note that I'm not responsible for any loss of funds, damages, or other libailities resulting from the use of this software or any associated services.<br>
This tool is provided for educational purposes only and should not be used as financial advice, it is still in expiremental phase so use it at your own risk.**

# ✨ Quickstart

This project has been made for Python 3.11

## 🛠️ Installation

💾 **Clone this repository**
```sh
git clone https://github.com/0xtaodev/jupiter-python-cli
```
💻 **Create a virtual environnment**
```sh
conda create --name jupiter-cli python=3.11

```
🌐 **Activate Virtual Environnement**
```sh
conda activate jupiter-cli
```

**Install requirements**
```sh
pip install -r requirements.txt
```

▶️ **Start CLI**
```sh
python main.py
```

# 🗺️ CLI Overview
```
📟 CLI
│
├── 🪐 Jupiter Exchange
│   ├── Swap
│   ├── Limit Order
│   │   ├── Open Limit Order
│   │   ├── Display Canceled Orders History
│   │   └── Display Filled Orders History
│   ├── DCA
│   │   ├── Open DCA Account
│   │   └── Manage DCA Accounts
│   ├── Token Sniper
│   │   ├── Add a token to snipe
│   │   ├── Watch token
│   │   └── Edit tokens
│   └── Change wallet
├── 💳 Manage Wallets
│   ├── Add wallet
│   ├── Edit wallet name
│   └── Delete wallet(s)
├── 🔧 CLI settings
│   ├── Solana RPC URL Endpoint
│   ├── Discord
│   └── Telegram
├── ❓ About
└── 🔚 Exit CLI
```

# 🤖 Sniper Bot
**In top of most of the Jupiter features that you can use, you are also able to snipe token.**<br>
❗**Please note that Sniper Bot is experimental and subject to change as there might be issues that I didn't see.**

### ⚙️ How it works
Every second, the bot will send a GET request to [Jupiter API Quote](https://quote-api.jup.ag/v6/quote).<br>
If there is a route available for this token, it will then execute it.<br>
Please note that only tokens with sufficient liquidity and on-chain metadata are listed in Jupiter API: min. 250$ liquidty and buy/sell price impact are below 30%.<br>
When these criteria are met, it will take a few minutes to automatically add the token.<br>

### 🆕 Add a token to snipe
- Token/Project name
- Token Address
- Amount ($) to buy
- Take Profit ($)
- Stop Loss ($)
- Slippage (%)

If token has a launch date:
- Month
- Day
- Hours
- Minutes

### 🔭 Watch token
You can watch your trading position by selecting the token.<br>
<img src="https://github.com/0xTaoDev/jupiter-python-cli/blob/main/images/sniper_bot_watch.png?raw=true" width="50%" height="50%">

### ✍🏻 Edit tokens
You can modify token info as follow:
- Name
- Address
- Selected Wallet
- Buy Amount
- Take Profit
- Stop Loss
- Slippage
- Launch date
- Delete

# 🗨️ Q&A
### Where are my private keys?
*Your private keys are stored in `wallets.json`.*
### Is there any fees when swapping using CLI?
*There are no additional fees when performing swaps via the CLI; the costs should be the same as using the Jupiter UI.*
### Does sniper bot remains running if I close the CLI?
*If you close the CLI, the sniper bot will stop running.*
### Is it possible to swap any tokens?
*You can only swap tokens that are listed on Jupiter based on their criterias.*

# 🚨 Known bugs
### ImportError: sync_native from spl.token.instructions
1. Go to https://github.com/michaelhly/solana-py/tree/master/src/spl/token and download ```instructions.py```
2. In your packages folder, replace ```spl/token/instructions.py``` with the one you just downloaded.
### Sometimes 0.01 is added when typying numbers
### Invalid DCA Accounts listed (and cannot be deleted)
### ~~Discord Webhook or Telegram API not being added in `config.json`~~
### Duplicating menus when resizing the window
### Sniper Bot: it's taking 10-20 seconds to get real trade position info after a swap route is found and executed

# 📝 TO-DO
- [ ] Clean up code ⚡
- [ ] Add docstrings 📑
- [ ] Display tokens owned 🪙
- [ ] Favorite tokens displayed in first tokens for swap/limit orders/dca... ⭐
- [ ] Wallet Duplication detection
- [ ] Display message when swap failed (slippage error...)
- [ ] Disable swap / limits orders / etc, if not enough $SOL to cover the tx fees
- [ ] Give possibility to exit current choice (swap, limit order, dca, donation...) 🏃🚪
- [ ] Adjust Wallets ID when one is deleted
- [ ] Bridge 🌉
- [ ] Perpetual 💸

# 🤝 Contributions
If you are interesting in contributing, fork the repository and submit a pull request in order to merge your improvements into the main repository.<br>
Contact me for any inquiry, I will reach you as soon as possible.<br>
[![Discord](https://img.shields.io/badge/Discord-%237289DA.svg?logo=discord&logoColor=white)](https://discord.gg/QxwPGcXDp7)
[![Twitter](https://img.shields.io/badge/Twitter-%231DA1F2.svg?logo=Twitter&logoColor=white)](https://twitter.com/_TaoDev_)

# 👑 Donations
This project doesn't include platform fees. If you find value in it and would like to support its development, your donations are greatly appreciated.<br>
You can donate through CLI in About menu.<br>
**SOLANA ADDRESS**
```sh
AyWu89SjZBW1MzkxiREmgtyMKxSkS1zVy8Uo23RyLphX
```
