```markdown
# 🎬 Advanced Telegram Video Compressor Bot

![Python](https://img.shields.io/badge/Python-3.11%2B-blue.svg)
![Pyrogram](https://img.shields.io/badge/Pyrogram-v2.0%2B-informational.svg)
![FFmpeg](https://img.shields.io/badge/FFmpeg-Optimized-success.svg)
![Docker](https://img.shields.io/badge/Docker-Supported-2496ED.svg)

A high-performance, asynchronous Telegram bot designed to compress large video files efficiently while maintaining excellent visual quality. Built with Python, Pyrogram, and FFmpeg, this bot is optimized for speed, reliability, and easy deployment across any cloud or VPS environment.

## ✨ Key Features

* **⚡ Lightning Fast Compression:** Utilizes FFmpeg with `libx264` for optimal size-to-quality ratios.
* **📦 Large File Support:** Processes and uploads videos up to Telegram's 2GB file limit.
* **🖼️ Custom Thumbnails:** Users can set a custom thumbnail for their compressed videos.
* **📊 Dynamic Progress Bars:** Real-time ETA, speed, and percentage tracking for both downloads and uploads.
* **⚙️ Selectable Quality Tiers:** Users can choose between Low, Medium, and High compression presets.
* **📢 Admin Broadcast System:** Built-in mass-messaging utility for bot administrators.
* **🐳 Universal Deployment:** Fully containerized with Docker for seamless hosting on VPS, Render, Railway, or Koyeb.
* **🌐 Web Server Integration:** Includes an `aiohttp` web server to bind to cloud-hosting ports and keep the bot awake.

## 🛠️ Prerequisites

Before deploying, ensure you have your Telegram API credentials:
1. **API_ID** and **API_HASH** (Get these from [my.telegram.org](https://my.telegram.org))
2. **BOT_TOKEN** (Get this from [@BotFather](https://t.me/BotFather))

## ⚙️ Environment Variables

Create a `.env` file in the root directory and add the following variables:

```env
API_ID=your_api_id_here
API_HASH=your_api_hash_here
BOT_TOKEN=your_bot_token_here

```
## 🚀 Deployment Instructions
### Method 1: Docker (Recommended)
Deploy instantly on any VPS or local machine using Docker. This method automatically handles FFmpeg and Python dependencies.
```bash
# Clone the repository
git clone [https://github.com/YourUsername/VideoCompressorBot.git](https://github.com/YourUsername/VideoCompressorBot.git)
cd VideoCompressorBot

# Build the Docker image
docker build -t yorichii-compressor .

# Run the container in the background
docker run -d --name compressor-bot --env-file .env yorichii-compressor

```
### Method 2: Local Server / VPS (Linux)
If you prefer running it directly on your server OS without Docker:
```bash
# 1. Install system dependencies (FFmpeg is required)
sudo apt update && sudo apt install -y ffmpeg python3 python3-pip

# 2. Clone the repository
git clone [https://github.com/YourUsername/VideoCompressorBot.git](https://github.com/YourUsername/VideoCompressorBot.git)
cd VideoCompressorBot

# 3. Install Python dependencies
pip3 install -r requirements.txt

# 4. Run the bot
python3 main.py

```
### Method 3: Cloud Platforms (Render, Railway, Koyeb)
Because this repository includes a standard Dockerfile and an exposed web port (10000), you can deploy it to modern PaaS providers directly via GitHub integration. Simply link your repository, set the .env variables in their dashboard, and the platform will handle the rest.
## 👨‍💻 Developer & Credits
Designed, coded, and maintained by **Yorichii**.
 * 💬 **Developer Telegram:** @Yorichiiprime
 * 📢 **Official Channel:** Yori Federation
*If you found this project helpful, don't forget to star ⭐ the repository!*
```

```text
.env
*.session
downloads/
temp/
__pycache__/

```
