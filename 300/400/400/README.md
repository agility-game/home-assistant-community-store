# 400 - Integration Type

Integrations are split into multiple integration types. Each integration must provide an ```integration_type``` in their manifest, that describes its main focus.

In our case, Agility Game has integration type ```hub```, with multpile devices, like Philips Hue.

**DANGER**: When not set, we currently default to ```hub```. This default is temporary during our transition period, every integration should set an ```integration_type``` and it thus will become mandatory in the future.

| Type | Description |
| -- | -- |
| ```device``` | Provides a single device like, for example, ESPHome. |


MORE ...
