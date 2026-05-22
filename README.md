# TGSignalBridge Trial v0.3.6

TGSignalBridge is a lightweight desktop application that automatically receives Telegram trading signals and executes trades on Pocket Option in real time.

It supports Demo and Real accounts, automatic CALL/PUT detection, Martingale management, minimum payout and balance protection, live statistics, trade history, and an easy-to-use interface designed for both beginners and advanced users.

---

# Disclaimer

TGSignalBridge is an automation tool designed to execute trades based on Telegram signals. Trading financial instruments involves significant risk and may result in loss of capital. The software does not guarantee profits or trading accuracy. Users are fully responsible for their trading decisions, account management, and financial results.
Use at your own risk.

---

# Features

- Fully Automatic Telegram to Pocket Option trading
- Pocket Option Demo & Real account support
- Automatic Signal, Time and Direction detection
- Auto CALL / PUT execution
- Minimum payout & balance protection
- Adjustable Martingale system
- Real-time stats and trade history
- Start / Pause / Resume / Stop anytime
- Fast and lightweight desktop GUI
- Beginner-friendly and easy to use

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

1. Download the repository files to a folder
2. Extract ChromeDriver into the same folder
3. Run: TGSignalBridge_free.exe

---
# Setup

- Telegram:
Get your Telegram API credentials from https://my.telegram.org

Fill: API_ID, API_HASH, PHONE, Channel Name, Channel Link / Username / ID

- Pocket Option: Demo or Real account, Initial Amount, Minimum Payout %

- Martingale: Enable Martingale, Coefficient, Maximum Steps

How to Start:
---

1. Configure the bot and press Save

2. Press Start

3. Enter Telegram login code

  Wait for connection
  
  Monitor signals, trades and logs

  If necessary, copy the Martingale sequence. (e.g [MG] Sequence: [1.00, 2.15, 4.62, 9.93, 21.35, 45.90, 98.68])

---
# Interface Overview

Left Panel
---

- Telegram settings
  
  Field / Option	| Description
  
  API_ID	| Telegram API ID obtained from my.telegram.org.
  
  API_HASH	| Telegram API HASH linked to the API_ID.
  
  PHONE	| Telegram phone number including country code.
  
  CHANNEL > Name	| Display name of the Telegram channel/group.
  
  CHANNEL > Link / Username / ID	| Telegram invite link, username, or numeric channel ID.

- Pocket Option settings

  Field / Option	| Description
  
  Account	| Select trading account mode: QT Real or QT Demo.
  
  Initial Amount	| Initial trade amount used for the first entry and restarting from Martingale.
  
  Minimum Payout Init (%)	| Minimum payout percentage required to allow opening a trade.

- Martingale settings
  
  Field / Option	| Description
  
  Enable	| Enables Martingale money management.
  
  COEFFICIENT	| Multiplier used to calculate next Martingale amount after loss.
  
  STEPS	| Maximum Martingale steps allowed.

Rigth Panel
---

- Top Controls:

  Button	| Function
  
  Start/Resume	| Starts the bot, initializes the Browser and Telegram connections and trade worker.
  
  Pause	| Temporarily pauses signal processing without closing the bot.
  
  Stop	| Stops the bot and disconnects Telegram client.


- Statistics:

  •	Time: Total runtime of the bot session.
  
  •	Win/Loss: Current amount of winning and losing trades.
  
  •	Init Balance: Initial Pocket Option balance detected when the bot started.
  
  •	Profit: Current accumulated profit/loss.
  
  Note: Statistics attempt to reflect a summary of daily trades.


- Trades Table:

  The trades table displays the latest executed trades loaded from the CSV history files.

  Column	| Meaning
  
  Side	| Trade direction (CALL or PUT).
  
  Expiration	| Expiration timeframe such as M1 or M2.
  
  Asset	| Trading asset/pair.
  
  Time	| Trade execution/result time.
  
  Amount	| Trade amount used.
  
  Profit	| Profit or loss result.
  
  Payout	| Current payout percentage.
  
  Result	| WIN or LOSS.
  
  Note: Table attempt to reflect the daily trades.

- Log Console commands:

  •	[INFO] Normal operational messages.
  
  •	[TELEGRAM] Telegram messages received.
  
  •	[JOB] Job in queue processed
  
  •	[✅ CALL] / [🔻 PUT] Trade executed
  
  •	[QUEUE] Result in queue to be checked at time
  
  •	[WARN] Warning messages.
  
  •	[ERROR] Error or failure messages.
  
  •	[CRITICAL ERROR SAVED] Please send this file to support.tgsignalbridge@gmail.com: errors/file
  
  •	Trade execution and Martingale events are logged here.

---
# Used Files:

  File	| Purpose
  
  •	config.json	| Stores GUI configuration and credentials.
  
  •	noise_keywords.json	| Keywords of noise to discard messages without signals.
  
  •	Trades_demo.csv	| Trade history for demo account mode.
  
  •	Trades_real.csv	| Trade history for real account mode.
  
  •	Error Dir	| Save error document folder.

---
# FAQ

-Is this a guaranteed profit bot?
No. TGSignalBridge only automates trade execution from Telegram signals. Profit is never guaranteed.

-Does it work with Real accounts?
Yes. Supports both QT Demo and QT Real accounts.

-Does it support OTC pairs?
Yes.

-Are my credentials secure? Yes, the bot only stores the configuration, trades, and errors locally in the files described (Used files).

-Is the bot compatible with other binary trading applications (such as Quotex)? No; for the moment, the bot is configured exclusively for Pocket Option. (https://pocketoption.com/)

-Can I use multiple channels? Not for now, the architecture is prepared for future multi-channel support.

-Why is ChromeDriver required?
The bot automates Pocket Option through Chrome browser control.

-Can I trade on my own without closing the application? Yes. You can use the Pause button at any time to stop receiving signals and trade on your own.

-Can I modify Pocket Option's operational settings? Yes, you can modify them; however, please remember that if the bot has initiated a trade job [JOB] and it is currently in the "[INFO] Waiting for Direction..." state, the next trade will be executed using the current settings.

- Note: If you modify the trade amount during the course of a Martingale sequence, an error will occur unless you reset the amount using a Martingale sequence. The bot follows the Martingale sequence to determine the amount for the next trade. (e.g [MG] Sequence: [1.00, 2.15, 4.62, 9.93, 21.35, 45.90, 98.68]). 

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
