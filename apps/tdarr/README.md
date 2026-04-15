# ⚙️ Tdarr

Tdarr is a distributed transcoding system for your media library. It allows you to automate the conversion of your files (e.g., from H264 to H265) to save massive amounts of storage space and ensure uniform compatibility across your devices.

## 🚀 Key Features
- **Distributed Processing**: Use multiple machines (Nodes) to process your library faster.
- **Transcode & Health Check**: Automated plugin-based workflow to transcode, strip unwanted subtitles/audio, and verify file integrity.
- **Space Saving**: Dramatically reduce the size of your movies and shows without losing noticeable quality.
- **GPU Acceleration**: Supports QSV, NVENC, and VAAPI for high-speed processing.

## 🛠️ Architecture

In this configuration, both the Server and a Node are included in the same `docker-compose.yml` for simplicity:

- **Tdarr Server**: The brain that manages the database, coordinates tasks, and provides the WebUI.
- **Tdarr Node**: The worker that actually performs the transcoding operations. Although included locally here, you can add more nodes on different hardware to scale your processing power.

## 📚 Useful Links
- **[Official Website](https://tdarr.io/)**
- **[Tdarr Documentation](https://docs.tdarr.io/)**
- **[GitHub Repository](https://github.com/HaveAGitGat/Tdarr)**
- **[Community Plugins](https://github.com/HaveAGitGat/Tdarr_Plugins)**
