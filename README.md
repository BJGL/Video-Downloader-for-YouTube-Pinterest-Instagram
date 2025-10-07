# Social Media Video Downloader

A simple Python tool for downloading videos from multiple platforms — including **YouTube**, **Pinterest**, and **Instagram Reels** — using the libraries **yt-dlp** and **instaloader**.

---

## Features

* **Multi-Platform Support:** Download videos from YouTube, Pinterest, and Instagram Reels.
* **Folder Management:** Specify a custom output directory to organize your downloads.
* **Silent Downloads:** Runs quietly without printing detailed logs to the console.
  
---

### Python Dependencies

Install the required libraries via **pip**:
!pip install yt-dlp instaloader

---

### External Tool

The YouTube downloader function (`youtube_downloader`) uses the **yt-dlp CLI tool**.
Make sure the **yt-dlp executable** is installed and accessible from your terminal (i.e., added to your system PATH).

> **Note:** The Python library `yt_dlp` installed via pip is different from the command-line binary.
> This script uses **both** for different parts of the process.

---

## Usage

1. **Save the Code:**
   Save the provided script as `social_video_downloader.py`.

2. **Run the Script:**
   Open your terminal or command prompt, navigate to the script’s folder, and run:

   python social_video_downloader.py

3. **Set Output Folder:**
   The script will ask for an output folder name (default: `downloaded_videos`).

4. **Select Platform:**
   Choose a platform:

   * `1` → YouTube
   * `2` → Pinterest
   * `3` → Instagram

5. **Paste the Video Link:**
   Enter the full video or reel URL. The file will be downloaded to the selected folder.

---

## Code Structure

The script is organized into platform-specific functions:

| Function                                 | Description                                                         |
| ---------------------------------------- | ------------------------------------------------------------------- |
| `youtube_downloader(link, output_dir)`   | Uses the **yt-dlp command-line binary** to download YouTube videos. |
| `pinterest_downloader(link, output_dir)` | Uses the **yt_dlp Python library** to download Pinterest videos.    |
| `instagram_downloader(link, output_dir)` | Uses the **instaloader** library to download Instagram Reels.       |
| `main()`                                 | Provides the interactive user menu and handles folder setup.        |

---

## Example

```text
Enter output folder name: Downloads
Choose an option
1: YouTube
2: Pinterest
3: Instagram
Choice: 2

Insert the Pinterest video link: https://pin.it/abc123
Download successfully
```

