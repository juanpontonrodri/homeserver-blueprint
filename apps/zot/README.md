# 📦 Zot Registry

Zot is a production-ready, vendor-neutral OCI image registry. It is a lightweight and performant alternative to other registries like Harbor, designed specifically for managing container images.

## 🚀 Key Features
- **OCI Compliant**: Fully supports OCI (Open Container Initiative) standards.
- **Lightweight**: Low resource consumption, making it ideal for home servers.
- **Secure**: Supports various authentication methods and vulnerability scanning.
- **Web UI**: Includes a built-in web-based interface for browsing images the repository.

## 🛠️ Usage
1. **Pushing Images**: Tag your image `docker tag <image> <SERVER-IP>:5000/<image>` and push `docker push <SERVER-IP>:5000/<image>`.
2. **Web Interface**: Access the UI at the port defined in your compose file (typically `5000` or `8080`).

## 📚 Useful Links
- **[Official Website](https://zotregistry.dev/)**
- **[Zot GitHub](https://github.com/project-zot/zot)**
