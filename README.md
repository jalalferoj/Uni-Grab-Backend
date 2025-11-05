Uni-Grab-Backend

This repository contains the Node.js Express server responsible for fetching, converting, and serving media files from external URLs (like YouTube and Facebook).

Prerequisites (Ubuntu Server)

Before running the Node.js server, you must install the following system dependencies:

Node.js & npm:

sudo apt update
sudo apt install nodejs npm -y


FFmpeg: This tool handles the video and audio conversion.

sudo apt install ffmpeg -y


yt-dlp: This is the primary media fetching utility.

sudo wget [https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp) -O /usr/local/bin/yt-dlp
sudo chmod a+rx /usr/local/bin/yt-dlp


Installation & Running

Clone the repository:

git clone [https://github.com/jalalferoj/Uni-Grab-Backend.git](https://github.com/jalalferoj/Uni-Grab-Backend.git) backend
cd backend


Install Node dependencies:

npm install


Start the server:

node server.js
# The server will run on http://localhost:3000


(Optional) Use nodemon for development:
If you install nodemon globally (npm install -g nodemon), you can use:

npm run dev


The server exposes the following endpoints:

POST /process: Handles download and conversion requests.

GET /downloads/[filename]: Serves the converted files.
