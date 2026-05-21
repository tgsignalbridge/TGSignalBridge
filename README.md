# TGSignalBridge Trial v0.3.5

TGSignalBridge is a lightweight desktop application that automatically receives Telegram trading signals and executes trades on Pocket Option in real time.

It supports Demo and Real accounts, automatic CALL/PUT detection, Martingale management, minimum payout and balance protection, live statistics, trade history, and an easy-to-use interface designed for both beginners and advanced users.

---

# Features

- Fully Automatic Telegram → Pocket Option trading
- Automatic Signal, Time and Direction detection
- Pocket Option Demo & Real support
- Auto CALL / PUT execution
- Minimum payout & balance protection
- Adjustable Martingale system
- Real-time stats and trade history
- Fast and lightweight desktop GUI
- Start / Pause / Resume / Stop anytime
- Beginner-friendly and easy to use

---

# Disclaimer

TGSignalBridge is an automation tool designed to execute trades based on Telegram signals. Trading financial instruments involves significant risk and may result in loss of capital. The software does not guarantee profits or trading accuracy. Users are fully responsible for their trading decisions, account management, and financial results.
Use at your own risk.

---

# Requirements

- Windows 10 or higher
- Telegram Destop installed
- Google Chrome installed
- Matching ChromeDriver version

Download ChromeDriver:
https://googlechromelabs.github.io/chrome-for-testing/

---

# Installation

1. Download the repository files
2. Extract ChromeDriver into the same folder
3. Run: TGSignalBridge_free.exe

---
# Setup

Telegram
Get your Telegram API credentials from:
https://my.telegram.org

Fill: API_ID, API_HASH, PHONE, Channel Name, Channel Link / Username / ID

Pocket Option: Demo or Real account, Initial Amount, Minimum Payout %

Martingale: Enable Martingale, Coefficient, Maximum Steps

How to Start:

1. Configure the bot and press Save

2. Press Start

3. Enter Telegram login code

  Wait for connection
  
  Monitor signals, trades and logs

  If necessary, copy the Martingale sequence. (e.g [MG] Sequence: [1.00, 2.15, 4.62, 9.93, 21.35, 45.90, 98.68])

---
# Interface Overview

Left Panel:

Telegram settings

- Pocket Option settings

- Martingale settings

Top Controls:
- Start/Resume

- Pause

- Stop

Statistics:

- Runtime

- Win/Loss

- Profit

- Initial Balance

Trades Table:

- Side

- Expiration

- Asset

- Amount

- Profit

- Result

Log Console:

- Telegram messages

- Trade execution

- Warnings

- Errors

- System events

---
# Used Files:

config.json	-Stores configuration

noise_keywords.json	-Filters noise messages

trades_demo.csv	-Demo trades history

trades_real.csv	-Real trades history

Error Dir	-Error reports folder

---
# FAQ

-Is this a guaranteed profit bot?
No. TGSignalBridge only automates trade execution from Telegram signals. Profit is never guaranteed.

-Does it work with Real accounts?
Yes. Supports both QT Demo and QT Real accounts.

-Does it support OTC pairs?
Yes.

-Is the bot compatible with other binary trading applications (such as Quotex)? No; for the moment, the bot is configured exclusively for Pocket Option. (https://pocketoption.com/)

-Can I use multiple channels? Not for now, the architecture is prepared for future multi-channel support.

-Why is ChromeDriver required?
The bot automates Pocket Option through Chrome browser control.

-Can I trading by self without closing the app? Yes. You can use the Pause button anytime to stop the signals reading.

-Can I modify Pocket Option's operational settings? Yes, you can modify them; however, please remember that if the bot has initiated a trade [JOB] and it is currently in the "[INFO] Waiting for Direction..." state, the next trade will be executed using the current settings.
Note: If you modify the trade amount during the course of a Martingale sequence, an error will occur unless you reset the amount using a Martingale sequence. The bot follows the Martingale sequence to determine the amount for the next trade. (e.g [MG] Sequence: [1.00, 2.15, 4.62, 9.93, 21.35, 45.90, 98.68]). 

---

# Donations
I'll appreciate if you want to support future development:

Ko-fi: https://ko-fi.com/tgsignalbridge

USDT (TRC20): 0x1394592c21526d29c2339edb5ae7ba51a6ade944

# Support
For issues, suggestions or bug reports, open an Issue on GitHub or Email me to support.tgsignalbridge@gmail.com

Telegram: https://t.me/TGSignalBridge

# License

This project is provided for educational and automation purposes only.
