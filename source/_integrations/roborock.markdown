---
title: Roborock
description: Instructions on how to integrate Roborock vacuums into Home Assistant
ha_category:
  - Vacuum
  - Select
ha_iot_class: Local Polling
ha_release: 2023.5
ha_config_flow: true
ha_codeowners:
  - '@humbertogontijo'
  - '@Lash-L'
ha_domain: roborock
ha_platforms:
  - vacuum
ha_integration_type: integration
---

The Roborock integration allows you to control your [Roborock](https://us.roborock.com/pages/robot-vacuum-cleaner) vacuum while continuing to use the Roborock app.

In contrast to [Xiaomi Miio](/integrations/xiaomi_miio/) integration, this integration provides more complete support but requires cloud access to set up and device configuration using the Roborock app.

Once you log in with your Roborock account, the integration will automatically discover your Roborock devices and get the needed information to communicate locally with them. Please ensure your Home Assistant instance can communicate with the local IP of your device. We recommend setting a static IP for your Roborock Vacuum to help prevent future issues.

# Prerequisites
- You must login to this integration with Roborock credentials - not Mi Home credentials.
- Some older Roborock devices are not supported by this integration - as they cannot be added to the Roborock app. If that is the case, you should use the [Xiaomi Miio](/integrations/xiaomi_miio/) integration instead.
- This integration was primarily tested on the S7 series - some vacuums may be missing fan or mop codes, device-specific modes will be coming in a future release.

{% include integrations/config_flow.md %}
