# 300 - File Structure

Each integration is stored inside a directory named after the integration domain. The domain is a short name consisting of characters and underscores. This domain has to be unique and cannot be changed. Example of the domain for the mobile app integration: ```mobile_app```. So all files for this integration are in the folder ```mobile_app/```. In our case we have a domain ```agility_game```.

The bare minimum content of this folder looks like this:

- ```manifest.json```: The manifest file describes the integration and its dependencies. [More info](https://developers.home-assistant.io/docs/creating_integration_manifest)
- ```__init__.py```: The component file. If the integration only offers a platform, you can keep this file limited to a docstring introducing the integration ```"""The Mobile App integration."""```.

## 100 - Integrating devices - ```light.py```, ```switch.py``` etc

If your integration is going to integrate one or more devices, you will need to do this by creating a platform that interacts with an entity integration. For example, if you want to represent a light device inside Home Assistant, you will create ```light.py```, which will contain a light platform for the light integration.

- More info on [available entity integrations](https://developers.home-assistant.io/docs/core/entity).
- More info on [creating platforms](https://developers.home-assistant.io/docs/creating_platform_index).

## 200 - Integrating services - ```services.yaml```




## 300 - Data update coordinator


## 400 - Where Home Assistant looks for integrations


=== WE ARE HERE ===
