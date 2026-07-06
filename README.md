# TGSignalBridge Trial 

TGSignalBridge Trial is an automation tool lightweight desktop application designed to execute trades based on Telegram signals. It is automatically receives Telegram trading signals and executes trades on Pocket Option in real time.

It supports Demo and Real accounts, automatic signal detection, Martingale management, simultaneous trades, minimum payout and balance protection, live statistics, trade history logs, and an easy-to-use interface designed for both beginners and advanced users.

---

# Version notes

TGSignalBridge Trial is designed to run as a trial for 14 days or 300 trades opened in base mode (not Martingale), unless the author grants an exception.

---

# Disclaimer

 Trading financial instruments involves significant risk and may result in loss of capital. The software does not guarantee profits or trading accuracy. Users are fully responsible for their trading decisions, account management, and financial results.

Please, Test the bot at Demo mode first to try diferents configuratios and validate the system. Use it at your own risk.

---

# Features

- Fully Automatic Telegram to Pocket Option trading
- Pocket Option Demo & Real account support
- Automatic Signal, Time and Direction detection
- Auto CALL / PUT execution
- Minimum payout & balance protection
- Anti-Popup Bonus windows
- Adjustable Martingale system
- Recovery Pool system with recovery Factor 
- Real-time stats and trade Logs history
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
3. Run: TGSignalBridge_Trial14.exe

---
# Setup

- TELEGRAM:: API_ID, API_HASH, PHONE
  Get your Telegram API credentials from https://my.telegram.org

- Channel: Name, Link/Username/ID, Telegram UTC Offset, Local UTC Offset

- Pocket Option: Demo or Real account, Initial Amount, Minimum Payout %, Minimum Payout MG (%)

- Signal: Signal Type, signal pattern vars, 

- Martingale: Enable Martingale, MG Coefficient, Maximum Steps, On Max Step

- Protection: Recovery Factor, Recovery Threshold, Max Concurrent Trades

How to Start:
---

1. Open Telegram Desktop and select your Signal channel

2. Open TGSignalBridge and configure the Telegram, Pocket Option and Signal parameters in Setting option, press Save.

3. Press Start to begin read signals

  4. For the first time, Enter Telegram login Code and Login to Pocket Option

    Wait for connection
  
    Note: Watch for the initial signals and check the logs to verify that the parameters are correct, the signals are being received and processed, and trades are being executed properly. If the signals are not being captured correctly, or an ERROR occurs, you can Stop the bot, return to the Settings to adjust the parameters, and Save the changes. Then, press Start again to begin.

    If necessary, copy the Martingale sequence if use it. (e.g [MG] Sequence: [1.00, 2.15, 4.62, 9.93, 21.35, 45.90, 98.68])

---
# Interface Overview

Left Panel
---

- Telegram settings
  
  Field / Option	| Description
  
  API_ID	| Telegram API ID obtained from my.telegram.org.
  
  API_HASH	| Telegram API HASH linked to the API_ID.
  
  PHONE	| Telegram phone number including country code.
  
  SIGNAL CHANNEL | Display name of the Telegram TGSignalBridge channel.
  

- Pocket Option settings

  Field / Option	| Description
  
  Account	| Select trading account mode: QT Real or QT Demo.
  
  Initial Amount	| Initial trade amount used for the first entry and restarting from Martingale.
  
  Minimum Payout Init (%)	| Minimum payout required to execute the initial trade.\nSignals below this percentage are ignored..

  Minimum Payout MG (%) | Minimum payout required to execute Martingale recovery trades.

- Risk Management settings
  
  Field / Option	| Description
  
  Enable Martingale	| Enables Martingale money management.
  
  MG Coefficient	| Multiplier used to calculate next Martingale amount after loss.
  
  Maximum Steps	| Maximum Martingale steps allowed.

  On Max Step | Defines what happens after the Maximum Martingale steps are reached.

  Recovery Factor | Percentage of the Recovery Pool added to the next trade after a win.

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
  
  Note: Statistics over the Logs Trade table attempt to reflect a summary of daily trades.


- Trades Table:

  The trades table displays the latest executed trades loaded from the history files.

  Column	| Meaning
  
  Side	| Trade direction (CALL or PUT).
  
  Expiration	| Expiration timeframe such as M1 or M2.
  
  Asset	| Trading asset/pair.

  Accuracy | Accuracy of the signal, if it have.
  
  Time	| Trade execution/result time.
  
  Amount	| Trade amount used.
  
  Profit	| Profit or loss result.
  
  Payout	| Current payout percentage.
  
  Result	| WIN or LOSS.
  
  Note: Table attempt to reflect the daily trades.

- Log Console commands examples:

  •	[INFO] Normal operational messages.
  
  •	[TELEGRAM]  Telegram messages received.
  
  •	[✅ CALL] / [🔻 PUT] Trade executed
  
  •	[QUEUE] Result in queue to be checked at time
  
  •	[WARN] Warning messages.

  •	[MG] Martingale messages
  
  •	[LOG] Record the trade after obtaining the result.

  •	[ERROR] Error or failure messages.
  
  •	[CRITICAL ERROR SAVED] Please send this file to support.tgsignalbridge@gmail.com: errors/file
  
  •	Trade execution and Martingale events are logged here.

---
# Used Files:

  File	| Purpose
  
  •	config.json	| Stores bot Setting configuration.
  
  •	noise_keywords.json	| Keywords of noise to discard messages without signals.
  
  •	Trades_demo.csv	| Trade history for demo account mode.
  
  •	Trades_real.csv	| Trade history for real account mode.
  
  •	Error Dir	| Save error document folder.

---
# Frequently Asked Questions (FAQ)

## General

### Is TGSignalBridge a guaranteed profit bot?
No. TGSignalBridge automates trade execution based on signals received from the Telegram channel and the parameters configured in the bot. Trading always involves risk, and profitability depends on market conditions and the user's configuration.

### Is the software free?
TGSignalBridge includes a free Trial version for testing. Future editions may provide advanced features.

### Why is ChromeDriver required?
The bot controls Pocket Option by automating the Chrome browser through ChromeDriver.

## Pocket Option

### Does it work with Real accounts?
Yes. The bot supports both **QT Demo** and **QT Real** accounts. It is strongly recommended to test TGSignalBridge in Demo mode before trading with real funds.

### Does TGSignalBridge support OTC assets?

Yes. The bot supports both OTC and regular market assets available on Pocket Option, including Forex, Cryptocurrencies, Stocks, and Commodities.

### Is the bot compatible with other trading platforms such as Quotex?
No. At the moment, TGSignalBridge is designed exclusively for Pocket Option.

---

## Trading

### Does the software execute trades automatically?
Yes. The bot automatically detects signals from the TGSignalBridge channel and executes trades on Pocket Option.

### Can I trade manually while the bot is running?
It is not recommended. Manual trading or changing Pocket Option settings while the bot is executing trades may interfere with its operation and produce unexpected results.

### Can I temporarily stop automated trading?
Yes. Use the **Pause** button to temporarily stop processing new Telegram signals. You can then trade manually and resume the bot whenever you wish.

---

## Martingale & Protection

### Does the bot support Martingale?
Yes. The software includes configurable Martingale settings, including MG Coefficient, Maximum Steps, and configurable behavior through On Max Step.

### Does the bot verify the payout before trading?
Yes. You can configure independent Minimum Payout percentages for both the Initial trade and Martingale trades.

### How does TGSignalBridge protect my balance?
Several protection mechanisms are included:

- Verifies that sufficient account balance exists before placing the next trade.
- Validates the complete Martingale sequence before starting.
- Includes an Recovery Pool protection and ajustable Factor of recovery to reduce the impact of extended losing streaks.

### Can I manually change the trade amount?
It is not recommended while a Martingale sequence is active. The bot calculates the next amount according to the configured sequence.

Example:

```
1.00 → 2.15 → 4.62 → 9.93 → 21.35 → 45.90 → 98.68
```

If the amount is modified manually during the sequence, Martingale recovery may become inconsistent.

---

## Channels & Signals

### Can I use multiple Telegram signal channels?
Not yet. The current version supports one active channel, although the architecture has been designed to support multiple channels in future releases.

### Why isn't the bot processing my Telegram signals?

If the bot ignores some Telegram signals, the selected signal may not match the format used by your channel.

Try the following:

- Choose a different **Signal Type**.
- Configure the signal patterns for your channel.
- Verify that the Telegram messages follow a standar signal format.
- Contact **TGSignalBridge Support (https://t.me/TGSignalBridgeSupport)** on Telegram if you need help configuring your channel.
---

## Security

### Are my credentials secure?
Yes. Your Telegram credentials or Login User/Password, settings and trade logs files are stored locally on your computer. No personal information is transmitted to external site.

### Is Telegram or Pocket Option login automated?
No. For security reasons, you must log in manually the first time to your Telegram account and to Pocket Option account before starting the bot.


---

# Support
For issues, suggestions or bug reports, Email me to support.tgsignalbridge@gmail.com

Telegram Group: https://t.me/TGSignalBridgeSupport

# License

TGSignalBridge is proprietary commercial software.

The Trial version is provided for evaluation purposes only. Future editions may require the purchase of a valid license.

Unauthorized copying, modification, redistribution, reverse engineering, or resale of this software is strictly prohibited.

© 2026 TGSignalBridge. All rights reserved.
