# 🚀 Tubely

Tubely is a scalable backend system for handling **media uploads, processing, and delivery**, inspired by real-world platforms like YouTube. It demonstrates how modern applications manage files using **cloud storage (AWS S3)** and **CDNs (CloudFront)**.

---

## ✨ Features

* 📤 Upload images and videos
* 🗂️ Store and manage media assets
* 🎬 Process videos using FFmpeg
* ☁️ Cloud storage integration with AWS S3
* 🌍 Fast delivery via CDN (CloudFront)
* 🗃️ Lightweight database using SQLite
* ⚡ RESTful API built with Go

---

## 🛠️ Tech Stack

* **Language:** Go (Golang)
* **Storage:** AWS S3
* **CDN:** AWS CloudFront
* **Database:** SQLite
* **Media Processing:** FFmpeg
* **CLI Tools:** AWS CLI

---

## 📦 Installation

### 1. Clone the repository

```bash
git clone https://github.com/Ocidemus/tubely.git
cd tubely
```

---

### 2. Install dependencies

#### Go modules

```bash
go mod download
```

#### FFmpeg

```bash
# Ubuntu/Debian
sudo apt update
sudo apt install ffmpeg

# macOS
brew install ffmpeg
```

#### SQLite (optional, for inspection)

```bash
sudo apt install sqlite3
```

#### AWS CLI

Install from: https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html

---

## 📁 Sample Media

Download sample images and videos:

```bash
./samplesdownload.sh
```

---

## ⚙️ Environment Setup

Create your environment file:

```bash
cp .env.example .env
```

Update the `.env` file with your credentials:

```env
PORT=
DB_URL=
AWS_ACCESS_KEY=
AWS_SECRET_KEY=
S3_BUCKET=
CLOUDFRONT_URL=
```

---

## ▶️ Running the Server

```bash
go run .
```

After running:

* `tubely.db` → database will be created
* `assets/` → stores uploaded files
* Server will start on the configured port

---

## 📡 API Overview

| Method | Endpoint    | Description          |
| ------ | ----------- | -------------------- |
| POST   | /upload     | Upload media file    |
| GET    | /assets     | Fetch all assets     |
| GET    | /assets/:id | Fetch specific asset |
| DELETE | /assets/:id | Delete an asset      |

---

## 🧠 What This Project Demonstrates

* Designing scalable file storage systems
* Integrating backend services with AWS
* Handling large media efficiently
* Using CDNs for performance optimization
* Writing clean and modular Go code

---

## 🔐 Security Note

Sensitive credentials are stored in `.env` and are **not committed**.
Always rotate keys if exposed.

---

## 📌 Future Improvements

* 🔐 Authentication & authorization
* 🎞️ Video streaming support (HLS/DASH)
* 📊 Analytics dashboard
* 🧵 Background job processing (queues)
* 🐳 Dockerized deployment

---

## 🙌 Acknowledgements

Inspired by real-world media systems and cloud architecture patterns.

---

## ⭐ Show your support

If you like this project, give it a ⭐ on GitHub!
