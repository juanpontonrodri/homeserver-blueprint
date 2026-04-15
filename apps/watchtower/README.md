# 🛰️ Watchtower

Watchtower is a process for automating Docker container base image updates. It monitors your running containers and watches for changes to the images that those containers were originally started from. If it detects a change, it will automatically restart the container using the new image.

## 🚀 Key Features
- **Zero-Touch Updates**: Keep your entire stack up to date without manual intervention.
- **Selective Updating**: Use labels to include or exclude specific containers from the update process.
- **Cleanup**: Automatically removes old images after an update to save disk space.
- **Notifications**: Send alerts to various services when an update occurs.

## 🛠️ Usage
- **Manual Run**: You can run it once to update everything: `docker run --rm -v /var/run/docker.sock:/var/run/docker.sock containrrr/watchtower --run-once`.
- **Exclusion**: To exclude a container, add the label `com.centurylinklabs.watchtower.enable=false`.

## 📚 Useful Links
- **[Documentation](https://containrrr.dev/watchtower/)**
- **[GitHub Repository](https://github.com/containrrr/watchtower)**
