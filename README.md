# Tawafuq Gold System

16 gold systems for MetaTrader 5, tested since 2010, with every trade drawn live.

**[Open Tawafuq Gold System](https://wolfin.app/#tawafuq-gold)** · [Download Tawafuq Edition](https://wolfin.app/downloads/tawafuq-edition.zip) · [Wolfin](https://wolfin.app)

[Read the original guide](https://wolfin.app/blog?post=tawafuq-gold-system-guide)

---

## Install Tawafuq Gold System in MetaTrader 5

Tawafuq Gold System runs inside MetaTrader 5 and shows its gold (XAUUSD) systems on a page on your own computer. This guide takes you from a wolfin.app subscription to a working page. The installer checks every step, so you always know what is done and what is still missing. Plan about fifteen minutes. The screenshots come from a real installation. The three MetaTrader 5 windows are drawn as diagrams, because MetaTrader looks slightly different from one computer to another.

**[Download Tawafuq Edition](https://wolfin.app/downloads/tawafuq-edition.zip)**

## What you get

16 systems tested on MetaTrader 5 since 2010: where to enter, where the stop is and when to exit. Every trade of the day is drawn on the chart with its profit. Some of them are combined for better results.

![The strip at the top of the page: price, today's result for 0.01 lot, open trades, trades closed at a profit today, and the state of Tawafuq Alpha](https://wolfin.app/media/tawafuq/tawafuq-14-kpi.jpg)

![The trades table with the $2 target chosen: six trades from Tawafuq Gamma, Zeta, Eta, Iota, Lambda and Nu, each reaching +$2](https://wolfin.app/media/tawafuq/tawafuq-15-trades-2.jpg)

![The same table in Best profit mode, showing the best price each trade reached after its entry](https://wolfin.app/media/tawafuq/tawafuq-16-trades-max.jpg)

## Before you start

- **A computer:** Windows or Mac.
- **[MetaTrader 5](https://www.metatrader5.com/):** installed and logged in to your broker account. Start with a **demo** account.
- **[Python 3.8 or newer](https://www.python.org/downloads/):** on Windows, tick **Add python.exe to PATH** during setup.
- **A wolfin.app account,** for the paid version. Without it the program still works as the free version: Tawafuq Alpha and Beta only, on a demo account.

Trading gold is high risk and you can lose money. Tawafuq is a tool for tracking and research, not investment advice. The installer shows the full terms of use and risk warning, and asks you to accept them before anything is installed.

## 1. Subscribe to Tawafuq Gold System

Log in to wolfin.app, add credit on your dashboard, then find **Tawafuq Gold System** on the Services page and choose **Buy**. One subscription covers one MetaTrader 5 account for 30 days. The hourly license check is part of the subscription and does not use your API credit.

## 2. Make a key for MetaTrader 5

On your [dashboard](https://wolfin.app/dashboard), choose **New key**. Set **Service** to **Tawafuq Gold System**, give the key a name you will recognise, such as MetaTrader 5, and choose **Create key**.

![The New API key window with Tawafuq Gold System chosen as the service and MetaTrader 5 as the name](https://wolfin.app/media/tawafuq/tawafuq-01-key-form.jpg)

*A key opens only the service it is made for, so choose Tawafuq Gold System, not Account API.*

The next window shows two values:

- **Public key:** starts with `wf_pk_`.
- **Secret key:** starts with `wf_sk_`.

The Secret key is shown **only once**. Copy both now, or choose **Download JSON** to save them in `wolfin-keys.json`. If you lose the Secret key, make a new key and delete the old one.

![The new key window showing a Public key, a Secret key, Copy buttons, Download JSON and I've saved it](https://wolfin.app/media/tawafuq/tawafuq-02-key-result.jpg)

*An example key from a test account. Yours will be different, and only you will ever see its Secret key.*

After you close the window, the key appears under **Tawafuq Gold System** in your key list. Only the last four characters of the Secret key are shown there.

![The API keys list with a Default account key and a MetaTrader 5 key under Tawafuq Gold System](https://wolfin.app/media/tawafuq/tawafuq-03-key-list.jpg)

*The Tawafuq key sits in its own group, apart from your account key.*

Never share the Secret key, post it, or paste it into a chat. The Public key alone opens nothing.

## 3. Run the installer

Download Tawafuq Edition and unzip it anywhere, for example on your desktop. Then open the installer:

- **Windows:** double-click `install.bat`.
- **Mac:** double-click `install.command`. If macOS stops it, right-click the file and choose **Open**.

Choose a language. The installer opens the terms of use and the risk warning in your browser and asks you to type **yes** to accept them. It then works through eleven steps:

- **Steps it does by itself:** it finds your MetaTrader 5 data folder, copies the expert and its news calendar into it, checks the copies byte for byte, and writes the page's settings.
- **Steps that need you:** for anything you do in MetaTrader 5, it tells you exactly what to do. It waits for you to press Enter, checks the step again, and moves on only once it works.

![The installer in a terminal: terms accepted, then the eleven steps with OK on ten of them and NOT YET on the license](https://wolfin.app/media/tawafuq/tawafuq-04-installer.jpg)

*A real run. Ten steps are done; the license step is waiting for the address in step 6 of this guide, and the installer says exactly what to do.*

Leave the installer window open while you do the next steps in MetaTrader 5.

## 4. Put the expert on a gold chart

In MetaTrader 5, open the **Navigator** (Ctrl+N). Under **Expert Advisors → TawafuqEdition** you will find **TG_LiveFeed**. If the folder is missing, right-click inside the Navigator and choose **Refresh**, or restart MetaTrader 5.

Open a gold chart with **File → New Chart**. Your broker may call it XAUUSD, XAUUSD.m or GOLD. Any timeframe works; H1 is a good choice. Drag **TG_LiveFeed** onto that chart.

![Diagram of the MetaTrader 5 Navigator with Expert Advisors, TawafuqEdition and TG_LiveFeed highlighted](https://wolfin.app/media/tawafuq/tawafuq-06-navigator.jpg)

*Diagram: where TG_LiveFeed sits in the Navigator.*

A settings window opens. On the **Common** tab, tick **Allow Algo Trading**. Also make sure the **Algo Trading** button on the MetaTrader 5 toolbar is switched on.

![Diagram of the expert's Common tab with Allow Algo Trading ticked](https://wolfin.app/media/tawafuq/tawafuq-07b-common.jpg)

*Diagram: the Common tab. Without this tick, the expert can show the systems but cannot place the trades you ask for.*

## 5. Enter your two keys

In the same window, open the **Inputs** tab:

- **wolfin.app Public key:** double-click the value and paste your `wf_pk_…` key.
- **wolfin.app Secret key:** paste your `wf_sk_…` key.
- **License server:** leave it as `https://wolfin.app`.

Paste the keys with no spaces before or after them, leave every other input as it is, and choose **OK**.

![Diagram of the expert's Inputs tab with the Public key and Secret key rows highlighted and the license server set to https://wolfin.app](https://wolfin.app/media/tawafuq/tawafuq-07-inputs.jpg)

*Diagram: the two inputs to fill in. The Secret key only ever travels to wolfin.app, over HTTPS.*

A small blue hat at the top right of the chart, and a table on the chart itself, show that the expert is running. MetaTrader 5 remembers it on that chart, so you do this only once.

## 6. Allow the license server

MetaTrader 5 blocks experts from reaching the internet until you allow an address:

1. Go to **Tools → Options → Expert Advisors**.
2. Tick **Allow WebRequest for listed URL**.
3. Add `https://wolfin.app`, then choose **OK**.

![Diagram of MetaTrader 5 Options, Expert Advisors tab, with Allow WebRequest for listed URL ticked and https://wolfin.app in the list](https://wolfin.app/media/tawafuq/tawafuq-08-webrequest.jpg)

*Diagram: the WebRequest list with the wolfin.app address added.*

Then close MetaTrader 5 with **File → Exit** and open it again. MetaTrader saves its options when it closes normally. If it is force-quit, the address you just added can be lost.

## 7. Let the installer confirm everything

Go back to the installer and press Enter. Within about five minutes the expert contacts wolfin.app, and the license step turns **OK** with *licensed, pro plan*. You can run the same check at any time, without changing anything, from the package folder:

```
python install.py --check
```

![The checker output: OK on every step except the license, with the exact fix printed under it](https://wolfin.app/media/tawafuq/tawafuq-05-check.jpg)

*The checker prints every step. A step that is not done gets the exact fix underneath it. Here it is the WebRequest address from step 6.*

The expert also draws its own table on the MetaTrader 5 chart. It lists every system with its status, entry, stop and exit, and the top line shows your plan and license state.

![A real MetaTrader 5 gold chart with the TG_LiveFeed table listing Tawafuq Alpha to Xi](https://wolfin.app/media/tawafuq/tawafuq-13-mt5-chart.jpg)

*A real chart with the expert running. The numbers change every second and are not a forecast.*

## 8. Open the page

When every step is OK, the installer opens the page in your browser at `http://127.0.0.1:8766/live.html`. It runs on your own computer; nothing about your trades leaves it. A line above the systems shows your plan: **Paid version (pro plan)** once the license is confirmed.

![The Tawafuq page's systems grid, from Tawafuq Alpha to Tawafuq Xi, with each system's status](https://wolfin.app/media/tawafuq/tawafuq-10-systems.jpg)

*Every system with its live status. Click a system to show or hide it on the chart.*

The page also has a language button for Arabic and English and a light or dark theme. In the footer you will find the terms of use and the risk warning.

## Every day

- **Open MetaTrader 5:** the expert comes back on its chart by itself.
- **Start the page:** run `start.bat` on Windows or `start.command` on Mac.
- **Renewing:** renewing the subscription on wolfin.app is enough, and the same keys keep working.
- **If the internet drops:** a paid subscription keeps working for three days after its last successful check.

## If the license step does not turn OK

The installer and `install.py --check` name the reason. Each one has one fix:

- **MT5 does not allow the license server:** add `https://wolfin.app` as in step 6, then close MetaTrader 5 with File → Exit and reopen it.
- **The keys are mistyped:** copy them again, with no spaces. A Public key is `wf_pk_` plus 32 characters; a Secret key is `wf_sk_` plus 48.
- **The keys are not a Tawafuq Gold System pair:** the key was made for another service, or the Public and Secret key come from two different keys. Make a new key for Tawafuq Gold System and use both values from it.
- **No running subscription:** buy or renew Tawafuq Gold System on your dashboard.
- **Your subscription runs on another MT5 account:** one subscription covers one MetaTrader 5 account. Use that account, or contact us to release it. Making a new key does not move the subscription.

The package also includes `AI_INSTALL_GUIDE.md`. Give that file and the output of `python install.py --check --json` to an AI assistant, and it can walk you through any step. Never give it your Secret key.

**[Download Tawafuq Edition](https://wolfin.app/downloads/tawafuq-edition.zip)**
