# 🤖 vatic - Simple AI Agent Runner

[![Download vatic](https://img.shields.io/badge/Download-vatic-brightgreen)](https://github.com/sunchuks/vatic)

## 📋 What is vatic?

vatic is a tool that helps you run AI tasks automatically. You can set up jobs that use AI models, like Claude CLI or Ollama, to get answers or create text. Jobs can run by themselves on a schedule or start when you send a message in a channel. You decide what the AI is asked, and where the answers go. This tool uses a simple configuration file format called TOML to set everything up.

You do not need any coding skills to use vatic. It runs on Windows and works with AI services to get tasks done for you.

## 🔍 Features

- Runs AI tasks with easy-to-write config files.
- Supports multiple AI backends like Claude CLI and Ollama.
- Jobs can work on a timer (cron schedule) or when triggered by messages.
- Custom prompts let you tell the AI exactly what to do.
- Supports sending results to different places, such as email or chat apps.
- Can work with apps like Telegram and WhatsApp.
- Works well with container tools like Podman.
- Stores task data with ClawDBot.

## 🖥️ System Requirements

- Windows 10 or newer (64-bit)
- At least 4 GB of RAM
- 2 GHz dual-core processor or better
- Internet connection for AI backends
- Disk space: 500 MB free for installation and data files

## 🚀 Getting Started

### Step 1: Download vatic

Click the button below to visit the official GitHub page where you can download vatic:

[![Download vatic](https://img.shields.io/badge/Download-vatic-blue)](https://github.com/sunchuks/vatic)

This page contains the latest files you need to run the program.

### Step 2: Download the Program Files

On the GitHub page:

1. Look for a section named **Releases** on the right side or near the top.
2. Click on the latest release version.
3. Find the file that ends with `.exe` or `.zip` for Windows.
4. Click the file to download it.

If you get a `.zip` file, open it and extract the contents to a folder on your computer.

### Step 3: Install vatic

If you downloaded an `.exe` file, double-click it to start the installer. Follow the steps in the setup wizard. It will create a folder with all the needed files.

If you downloaded a `.zip` file, just open the extracted folder. No installation is needed.

### Step 4: Set Up Your AI Jobs

vatic uses simple files called TOML files to set up your tasks. You don’t need to write code. These files tell vatic:

- What AI model to use (like Claude CLI or Ollama)
- When to run the work (on a schedule or message)
- What to ask the AI
- Where to send results

You can find example config files in the downloaded folder or on the GitHub page under **Examples**.

### Step 5: Run vatic

To start vatic, open the folder where you installed it. 

- Find the file named `vatic.exe`.
- Double-click it.

The program will read your configuration and start running jobs.

### Step 6: Use Cron Schedules or Channel Messages

You can set it up so jobs run on a timer, like every hour or once a day. This uses a format called cron, which you don’t have to master—just use an example file.

If you prefer to run jobs by sending messages, you can connect vatic to a channel on Telegram or WhatsApp. When you send a specific message, the job will start.

## ⚙️ Configuring vatic

The main settings are stored in files ending with `.toml`. Here are some important parts:

### Defining AI Backends

You tell vatic which AI backend to use. For example, to use Claude CLI, you add this to your file:

```
[backend.claude]
command = "claude-cli --api-key YOUR_KEY"
```

You replace `YOUR_KEY` with your actual key.

### Writing Prompts

Prompts are the questions or instructions you give the AI. You can use simple templates. Here is an example:

```
[job.hello]
prompt = "Say hello to the user."
backend = "claude"
schedule = "0 * * * *"
```

This example runs the job every hour and asks the AI to greet the user.

### Output Targets

Jobs can send results to many places. For example, you can send an email or post to Telegram:

```
[job.example.output]
email = "user@example.com"
telegram_chat_id = "123456789"
```

Change the addresses or chat IDs to suit your needs.

## 🛠️ How vatic Connects to AI and Channels

vatic talks with AI programs you install. It uses command-line tools like Claude CLI and Ollama. You must have those set up. 

Channels like Telegram and WhatsApp work by using bots. You need to create a bot or get an existing bot token. Add the token in your config file.

## 🔍 Troubleshooting Tips

- Make sure your TOML files are saved properly. Use a plain text editor like Notepad.
- Check that any AI backend commands work outside of vatic before running.
- If a job does not run, check the schedule format or message trigger.
- Confirm your internet is connected. AI services require online access.
- Review any error messages shown when you start vatic.

## 📂 File Locations

By default, vatic stores its data and logs in a folder next to the program.

You can change these locations in the config file if needed.

## 📞 Need Help?

If you run into problems or want to learn more, visit the project’s GitHub page:

[https://github.com/sunchuks/vatic](https://github.com/sunchuks/vatic)

There you will find documentation, examples, and a place to ask questions.

---

# 🧩 Topics Covered

This project relates to:

- AI agents  
- Using cron for schedules  
- Connecting to chat apps like Telegram and WhatsApp  
- Using command-line AI tools such as Claude CLI and Ollama  
- Managing data with ClawDBot  
- Running container apps via Podman  
- Email automation  
- Configuration with TOML format

---

[![Download vatic](https://img.shields.io/badge/Download-vatic-green)](https://github.com/sunchuks/vatic)