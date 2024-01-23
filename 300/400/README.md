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
manifest.jso



