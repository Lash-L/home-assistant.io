---
title: Snoo
description: Instructions on how to integrate Snoos into Home Assistant
ha_category:
  - Sensor
ha_iot_class: Cloud Push
ha_release: 2025.2
ha_config_flow: true
ha_codeowners:
  - '@Lash-L'
ha_domain: snoo
ha_platforms:
  - sensor
ha_integration_type: integration
---

The Snoo is a smart bassinet that helps get your baby to sleep and helps keep them asleep.


## Installing the integration
This integration follows standard integration installation. No extra steps are required.

{% include integrations/config_flow.md %}

## Sensors

### State

The Snoo can have one of 8 states
1. Baseline - This is the basic state the snoo starts with. It has not detected the need to do any further soothing.
2. Level 1 - This is the lowest level of soothing
3. Level 2
4. Level 3
5. Level 4
6. Stop - The snoo is no longer running
7. Pre-timeout - the snoo is preparing to go back to stop rotating
8. Timeout - the snoo is stopping rotating.

### Last Event
The snoo will send a message whenever a event occurs. This entity displays the last event that was sent. There are 9 possible events
1. Activity button - The activity button was pressed
2. Timer - A timer has started, and once the timer ends, it will go down a level.
3. Power Button - The power button has been pressed.
4. Cry - The snoo detected your baby is crying.
5. Command - A command was sent to the Snoo
6. Safety clip - A safety clip was either attached or detached.
7. Long activity press - The activity button was long pressed.
8. Restart - The Snoo was requested to restart.
9. Initial status requested - The status was requested at the beginning of a session.

## Time left
This describes how long until the Snoo will change levels or it is -1 if it is not currently planning to change levels.

## Removing the integration

This integration follows standard integration removal. No extra steps arerequired.

{% include integrations/remove_device_service.md %}
