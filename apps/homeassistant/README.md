# 🏠 Home Assistant

Home Assistant is an open-source home automation platform that puts local control and privacy first. It is the brain of your smart home, allowing you to unify all your devices and create complex automations.

## 🚀 Key Features
- **Local Control**: All data stays in your network; no cloud requirement for core functionality.
- **Vast Integrations**: Supports thousands of devices and services (Zigbee, Z-Wave, WiFi, etc.).
- **Powerful Automations**: Create sophisticated rules based on triggers, conditions, and actions.
- **Custom Dashboards**: Build beautiful, responsive interfaces to control your home from any device.

## 🛠️ Configuration
- **Network Mode**: Running in `network_mode: host` is highly recommended for discovery of smart devices (mDNS, UPnP).
- **Persistence**: Your configuration is stored in the `./config` directory.
- **Zigbee/Z-Wave**: If using USB dongles, you will need to map the device path (e.g., `/dev/ttyUSB0`) to the container.

## 📚 Useful Links
- **[Official Website](https://www.home-assistant.io/)**
- **[Documentation](https://www.home-assistant.io/docs/)**
- **[Home Assistant Community](https://community.home-assistant.io/)**
- **[HACS (Home Assistant Community Store)](https://hacs.xyz/)** - Essential for custom cards and integrations.
