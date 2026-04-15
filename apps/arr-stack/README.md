# Servarr Stack: Configuration & Usage Guide

This directory contains the configuration for the "Arr" ecosystem (**Servarr**), a suite of applications designed to automate the search, download, and organization of media content. All applications in this stack are routed through **Gluetun (VPN)** for enhanced privacy.

## 🚀 Stack Overview

The typical workflow is as follows:
1. **Prowlarr**: Manages the "Indexers" (torrent/usenet sources) and synchronizes them with the other applications.
2. **Sonarr/Radarr/Lidarr/Readarr**: Monitor your wishlists, search for content via Prowlarr, and send download requests to the client.
3. **qBittorrent**: Downloads the files requested by the above apps.
4. **Gluetun**: Acts as the VPN gateway for all download and search traffic.

### Included Services

| Application | Function | Access Port |
| :--- | :--- | :--- |
| **Prowlarr** | Indexer Management (Search) | 9696 |
| **Sonarr** | TV Shows & Anime | 8989 |
| **Radarr** | Movies | 7878 |
| **Lidarr** | Music | 8686 |
| **Readarr** | Books & eBooks | 8787 |
| **qBittorrent** | Torrent Client | 10228 |
| **Gluetun** | VPN Client (Traffic Protection) | - |

---

## 🛠️ General Configuration

For the stack to function correctly, you must configure the communication between services by following these steps:

### 1. Configure Prowlarr (Indexers)
Prowlarr is the heart of the search process.
- Access `http://<SERVER-IP>:9696`.
- Add your preferred indexers (public or private) under **Indexers**.
- Go to **Settings > Apps** and add Radarr, Sonarr, etc. You will need the **API Key** for each application (found in `Settings > General` within each app).

### 2. Configure Download Clients
In each application (Sonarr, Radarr, etc.):
- Go to **Settings > Download Clients**.
- Add **qBittorrent**.
- **Host**: `gluetun` (since they share the same network stack, or your server's IP if not using `network_mode: service:gluetun`).
- **Port**: `10228`.

### 3. Media Management
Ensure you configure the destination paths:
- **Root Folders**: Define where you want movies/shows to be permanently stored (e.g., `/media/Movies`).
- The apps will move or hardlink files from the qBittorrent download folder to your final library.

---

## 📚 Documentation & Useful Resources

For advanced configurations (Quality Profiles, Hardlinks to save space, etc.), it is recommended to consult:

- **[Servarr Wiki](https://wiki.servarr.com/)**: Official documentation for all applications.
- **[TRaSH Guides](https://trash-guides.info/)**: **Essential**. The definitive guides on setting up quality profiles (Custom Formats) and file naming.

---

## 🧩 Complementary Applications (Suggestions)

To take your Home Server to the next level, consider adding:

- **[Bazarr](https://www.bazarr.media/)**: Automates subtitle downloads in multiple languages.
- **[Overseerr](https://overseerr.dev/)** / **[Jellyseerr](https://github.com/fallenbagel/jellyseerr)**: A sleek interface for you or your users to request content without accessing Radarr/Sonarr.
- **[Tdarr](https://tdarr.io/)**: Automatically transcode your library to save space (e.g., converting everything to H265).
- **[Audiobookshelf](https://www.audiobookshelf.org/)**: The best server for audiobooks and podcasts, with excellent mobile apps.
- **[Alist](https://alist.nn.ci/)**: For mounting cloud storage (Google Drive, OneDrive) as local drives.
