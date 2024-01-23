# 400 - Manifest

Every integration has a manifest file to specify its basic information. This file is stored as ```manifest.json``` in your integration directory. It is required to add such a file.

```
{
  "domain": "hue",
  "name": "Philips Hue",
  "after_dependencies": ["http"],
  "codeowners": ["@balloob"],
  "dependencies": ["mqtt"],
  "documentation": "https://www.home-assistant.io/components/hue",
  "integration_type": "hub",
  "iot_class": "local_polling",
  "issue_tracker": "https://github.com/balloob/hue/issues",
  "loggers": ["aiohue"],
  "requirements": ["aiohue==1.9.1"],
  "quality_scale": "platinum"
}
```
manifest.json

Or a minimal example that you can copy into your project:

```
{
  "domain": "your_domain_name",
  "name": "Your Integration",
  "codeowners": [],
  "dependencies": [],
  "documentation": "https://www.example.com",
  "integration_type": "hub",
  "iot_class": "cloud_polling",
  "requirements": []
}
```
manifest.json

## 100 - Domain

See [README.md](./100/README.md)

## 200 - Name

See [README.md](./200/README.md)

## 300 - Version

See [README.md](./300/README.md)

## 400 - Integration Type

See [README.md](./400/README.md)

## 500 - Documentation

See [README.md](./500/README.md)

## 600 - Issue Tracker

See [README.md](./600/README.md)

## 700 - Dependencies

See [README.md](./700/README.md)

## 800 - After dependencies

See [README.md](./800/README.md)

## 900 - Code Owners

See [README.md](./900/README.md)

## 1000 - Config Flow

See [README.md](./1000/README.md)

## 1100 - Requirements

See [README.md](./1100/README.md)

## 1200 - Loggers

See [README.md](./1200/README.md)

## 1300 - Bluetooth

See [README.md](./1300/README.md)

## 1400 - Zeroconf

See [README.md](./1400/README.md)

## 1500 - SSDP

See [README.md](./1500/README.md)

## 1600 - HomeKit

See [README.md](./1600/README.md)

## 1700 - MQTT

See [README.md](./1700/README.md)

## 1800 - DHCP

See [README.md](./1800/README.md)

## 1900 - USB

See [README.md](./1900/README.md)

## 2000 - Integration Quality Scale

See [README.md](./2000/README.md)

## 2100 - IoT Class

See [README.md](./2100/README.md)

## 2200 - Virtual Integration

See [README.md](./2200/README.md)
