# 🚨 class-prometheus-grafana-telegram-alerts - Monitor Metrics with Telegram Alerts

[![Download the app](https://img.shields.io/badge/Download%20Release-blue?style=for-the-badge&logo=github)](https://github.com/Fulminant-funiculitis672/class-prometheus-grafana-telegram-alerts/releases)

## 📌 What this app does

`class-prometheus-grafana-telegram-alerts` is a containerized monitoring setup for Windows users who want to see app metrics in Grafana and get alerts in Telegram.

It helps you:

- collect sample metrics from a running app
- view charts and graphs in Grafana
- send alert messages to a Telegram chat
- run the full setup with minimal manual work

This project is built for end users who want a ready-made monitoring stack without setting up each tool by hand.

## 🖥️ What you need

Before you start, make sure your PC has:

- Windows 10 or Windows 11
- At least 8 GB of RAM
- 10 GB of free disk space
- Internet access
- Administrator access on your computer
- Docker Desktop installed and running

You also need:

- a Telegram account
- a Telegram bot token
- your Telegram chat ID

## 📥 Download the app

Visit this page to download the latest release:

[Go to Releases](https://github.com/Fulminant-funiculitis672/class-prometheus-grafana-telegram-alerts/releases)

On that page, look for the latest release files and download the Windows package if one is listed. If the release includes a `.zip` file, download it and keep it in a folder you can find easily, such as `Downloads` or `Desktop`.

## 🛠️ Install Docker Desktop

This app runs in containers, so Docker Desktop must be installed first.

### Steps

1. Open the Docker Desktop download page in your browser.
2. Download the Windows version.
3. Run the installer.
4. Follow the on-screen steps.
5. Restart your computer if Windows asks for it.
6. Open Docker Desktop and wait until it shows that it is running.

If Docker Desktop opens without errors, you are ready for the next step.

## 📦 Set up the release files

After you download the release:

1. Find the downloaded `.zip` file.
2. Right-click it and choose **Extract All**.
3. Pick a folder you can reach easily, such as `C:\class-prometheus-grafana-telegram-alerts`.
4. Open the extracted folder.

You should see project files that help start the monitoring stack.

## 🔐 Prepare Telegram alerts

To receive alerts in Telegram, you need two things:

- a bot token
- a chat ID

### Create a bot token

1. Open Telegram.
2. Search for `BotFather`.
3. Start a chat with BotFather.
4. Send the command to create a new bot.
5. Copy the token it gives you.

### Get your chat ID

1. Open a chat with the bot or a group where you want alerts.
2. Add the bot to the chat if needed.
3. Send a test message.
4. Use a chat ID lookup method that matches your Telegram setup.
5. Copy the chat ID value.

Keep both values ready for the next step.

## ⚙️ Configure the app

Open the extracted folder and look for a settings file such as `.env`, `config.yml`, or a similar file.

Set these values:

- Telegram bot token
- Telegram chat ID
- alert name
- app name
- any default ports listed in the files

If you see a sample file, copy it first and rename it to the active config file name. Then edit the copied file with Notepad.

Use plain text values only. Save the file when done.

## ▶️ Start the monitoring stack

Use the files in the extracted folder to start the app.

### Common ways to start it

You may see one of these:

- `start.bat`
- `run.bat`
- `docker-compose.yml`
- `docker compose up`

If you see a `.bat` file:

1. Double-click the file.
2. Wait while Windows opens a terminal window.
3. Let the containers start.

If you see a Docker Compose file:

1. Open the folder in File Explorer.
2. Click the address bar.
3. Type `cmd` and press Enter.
4. In the terminal, run the start command shown in the project files.

Wait until the setup finishes loading. The first run can take a few minutes.

## 🌐 Open the dashboards

After the services start, open your browser and check the web pages used by the stack.

You will usually see:

- Grafana for charts and dashboards
- Prometheus for metric data
- the sample app or metric source

Common local addresses may include:

- `http://localhost:3000`
- `http://localhost:9090`
- `http://localhost:8080`

If the project files list different ports, use those values instead.

## 📊 Use Grafana

Grafana shows your monitoring data in charts and panels.

### What to do

1. Open Grafana in your browser.
2. Sign in if the app asks for a login.
3. Open the dashboard list.
4. Pick the monitoring dashboard included with the project.
5. Review the graphs for CPU, memory, request rate, or app errors.

If the dashboard is already set up, you should see data within a short time after the app starts.

## 🚨 Test Telegram alerts

Once the stack is running, test the alert flow.

### Basic test

1. Trigger a sample alert if the project includes a test button or test script.
2. Wait for the alert rule to fire.
3. Check your Telegram chat.
4. Confirm that the message arrives.

### What the alert should show

A normal alert message may include:

- alert name
- severity
- time it fired
- short message about the issue

If no message arrives, check the bot token, chat ID, and network connection.

## 🧩 Folder layout

A typical release folder may contain:

- `docker-compose.yml` — starts the containers
- `.env` — stores settings
- `grafana/` — dashboard files and config
- `prometheus/` — metric config and alert rules
- `alerts/` — Telegram alert settings
- `scripts/` — helper files for start and stop tasks
- `README.md` — project notes

These files help the stack run in a repeatable way.

## 🔄 Stop the app

When you are done, stop the containers.

### If you used a batch file

Close the terminal window or use the stop file if one is included.

### If you used Docker Compose

In the terminal, press:

- `Ctrl + C`

Then wait for the containers to stop.

You can also stop them from Docker Desktop if you prefer.

## 🧰 Common problems

### Docker Desktop does not start

- Restart your PC
- Open Docker Desktop as administrator
- Check that virtualization is turned on in BIOS
- Make sure Windows has the latest updates

### Grafana does not open

- Check that Docker Desktop is running
- Wait a minute and try again
- Confirm the port in the project files
- Make sure nothing else uses the same port

### No Telegram alerts arrive

- Check the bot token
- Check the chat ID
- Send a test message in Telegram
- Confirm the bot is in the chat
- Make sure the alert rule is active

### The app starts, but no data appears

- Wait a few minutes for the sample metrics to load
- Refresh the browser
- Confirm the containers are running
- Check the log output for errors

## 🔍 Useful checks

If you want to confirm everything works, look for these signs:

- Docker Desktop shows running containers
- Grafana opens in the browser
- charts show data
- Telegram receives alert messages
- the sample app or metric source stays online

## 🗂️ Suggested first run order

1. Download the release from GitHub
2. Install Docker Desktop
3. Extract the release files
4. Set the Telegram token and chat ID
5. Start the containers
6. Open Grafana
7. Test the alert message

## 📎 Download link

Use the release page here:

[https://github.com/Fulminant-funiculitis672/class-prometheus-grafana-telegram-alerts/releases](https://github.com/Fulminant-funiculitis672/class-prometheus-grafana-telegram-alerts/releases)

## 📄 Notes for use

- Keep the Telegram token private
- Keep the chat ID in the config file
- Do not rename files unless the project files tell you to
- Use the release files from the latest version
- Save changes before starting the app

## 🧪 What you can expect

After setup, this app gives you a simple local monitoring lab where you can:

- watch metrics in Grafana
- test alert rules
- send messages to Telegram
- learn how alerts work in a live setup
- keep the whole stack in containers