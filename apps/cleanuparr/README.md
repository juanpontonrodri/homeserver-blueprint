# 🧹 CleanupArr

CleanupArr is a utility script/container designed to help manage and clean up unmonitored files and folders within your Sonarr and Radarr libraries. It helps keep your storage efficient by removing orphaned files that are no longer tracked by your "Arr" services.

## 🚀 Key Features
- **Orphan File Detection**: Identifies files on disk that are not present in your Sonarr/Radarr database.
- **Dry Run Support**: Always run in dry-run mode first to see what *would* be deleted.
- **Automated Maintenance**: Can be scheduled to run periodically to keep your media folders clean.

## 🛠️ Configuration
- **API Keys**: Requires API keys for your Sonarr and/or Radarr instances.
- **Root Paths**: Must have access to the same root paths as your media servers to verify file existence.

## 📚 Useful Links
- **[GitHub Repository](https://github.com/cleanuparr/cleanuparr)**
- **[Capacitarr](https://github.com/Ghent/capacitarr)**: A new alternative worth considering for library cleanup.
- **[Radarr Documentation](https://wiki.servarr.com/radarr)** - General info on how Radarr handles files.
