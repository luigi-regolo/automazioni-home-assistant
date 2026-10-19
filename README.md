# Home Assistant Automation Blueprints

[![TikTok | Segui](assets/tiktok-segui.svg)](https://www.tiktok.com/@luigi.regolo)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue?style=flat-square)](LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/luigi-regolo/automazioni-home-assistant?style=flat-square)](https://github.com/luigi-regolo/automazioni-home-assistant/stargazers)

## Overview

A collection of **20 ready-to-import automation blueprints** for Home Assistant. Import them through the Home Assistant interface without copying YAML and without HACS. Select the entities, devices, and actions available in your own installation.

## Features

- Direct import using the official **My Home Assistant** blueprint badges.
- Blueprints covering lighting, sensors, water leaks, climate, heating, NFC, covers, and dashboards.
- Configurable devices and actions through blueprint inputs and the Home Assistant automation editor.
- A source YAML link for each blueprint.

## Installation

1. Choose a blueprint from the catalog below and click its **Import into Home Assistant** badge.
2. Review the import preview and import the blueprint into your Home Assistant instance.
3. Go to **Settings → Automations & scenes → Blueprints**, select the blueprint, and create an automation.
4. Configure the required devices, actions, and options; test the behavior and save the automation.

**Alternative import:** open the **Blueprint YAML on GitHub** link under the chosen blueprint, copy its URL, and paste it into **Settings → Automations & scenes → Blueprints → Import blueprint**. This is useful when badges cannot open Home Assistant from an in-app browser.

**Important:** importing a blueprint does **not** automatically create or enable an automation.

## Available Blueprints

### 01 — Turn on entrance light when the door opens

**What it does:** Turns on the selected light when the door opens, only after sunset or before sunrise.

**Requirements:** A configured door contact sensor and light.

**Notes and limitations:** The light is not turned off automatically.

[![Import into Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fingresso%2Faccendi_luce_apertura_porta.yaml)

[Import directly into Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fingresso%2Faccendi_luce_apertura_porta.yaml) · [Blueprint YAML on GitHub](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/ingresso/accendi_luce_apertura_porta.yaml)

### 02 — Turn off entrance light when motion ends

**What it does:** Turns off the selected light when motion ends, if the door is closed and it is after sunset or before sunrise.

**Requirements:** A motion sensor, a door contact sensor, and a light.

**Notes and limitations:** No additional delay is applied.

[![Import into Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fingresso%2Fspegni_luce_fine_movimento.yaml)

[Import directly into Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fingresso%2Fspegni_luce_fine_movimento.yaml) · [Blueprint YAML on GitHub](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/ingresso/spegni_luce_fine_movimento.yaml)

### 03 — Update selected entities every 20 seconds

**What it does:** Calls `homeassistant.update_entity` for selected entities every 20 seconds.

**Requirements:** Entities whose integrations support on-demand updates.

**Notes and limitations:** This does not force a phone to report a new GPS position. Frequent requests can increase load or trigger cloud rate limits; some entities will not refresh.

[![Import into Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fsensori%2Faggiorna_entita_ogni_20_secondi.yaml)

[Import directly into Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fsensori%2Faggiorna_entita_ogni_20_secondi.yaml) · [Blueprint YAML on GitHub](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/sensori/aggiorna_entita_ogni_20_secondi.yaml)

### 04 — Water leak alert with phone and optional Alexa notifications

**What it does:** Runs the user-configured notification actions when a moisture sensor detects water.

**Requirements:** A moisture-class `binary_sensor` and at least one working notification action. Alexa announcements are optional and need a compatible integration.

**Notes and limitations:** Alexa Media Player is an example of an unofficial integration. Notifications are not a substitute for physical leak protection. Suggested message: “Attenzione. Rilevata presenza di acqua. Controlla subito.”

[![Import into Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fsicurezza%2Favviso_allagamento.yaml)

[Import directly into Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fsicurezza%2Favviso_allagamento.yaml) · [Blueprint YAML on GitHub](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/sicurezza/avviso_allagamento.yaml)

### 05 — Start dehumidification when humidity is high

**What it does:** When humidity stays above 65% for 2 minutes (configurable), sets the air conditioner to `dry` and sends a phone notification.

**Requirements:** A humidity sensor, a climate entity supporting `dry`, and Home Assistant phone notifications.

**Notes and limitations:** Does not automatically stop the air conditioner or set a target humidity. Restarting Home Assistant resets the 2-minute wait. Default message: “L’umidità è troppo alta e il climatizzatore è stato acceso in modalità deumidificazione.”

[![Import into Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fclima%2Fcontrollo_umidita_deumidificazione.yaml)

[Import directly into Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fclima%2Fcontrollo_umidita_deumidificazione.yaml) · [Blueprint YAML on GitHub](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/clima/controllo_umidita_deumidificazione.yaml)

### 06 — Stop dehumidification when humidity falls

**What it does:** When humidity stays below 61% for 2 minutes (configurable), sets the climate entity to `off` and sends a notification.

**Requirements:** A humidity sensor, a compatible climate entity, and Home Assistant phone notifications.

**Notes and limitations:** `off` turns off the entire air conditioner, not only dehumidification. If paired with blueprint 05, choose the same devices and a lower stop threshold. Default message: “L’umidità è tornata nei valori ideali e il climatizzatore in modalità deumidificazione è stato spento”.

[![Import into Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fclima%2Fspegnimento_automatico_deumidificazione.yaml)

[Import directly into Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fclima%2Fspegnimento_automatico_deumidificazione.yaml) · [Blueprint YAML on GitHub](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/clima/spegnimento_automatico_deumidificazione.yaml)

### 07 — Switch dashboard selection based on motion

**What it does:** After at least 1 second of motion, selects a configured option in an `input_select` helper.

**Requirements:** A motion sensor, an `input_select` helper with matching options, and a dashboard configured to react to that helper.

**Notes and limitations:** Does not create a dashboard or directly navigate the browser. The selected option must exactly match an existing helper option.

[![Import into Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fdashboard%2Fdashboard_automatica_movimento.yaml)

[Import directly into Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fdashboard%2Fdashboard_automatica_movimento.yaml) · [Blueprint YAML on GitHub](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/dashboard/dashboard_automatica_movimento.yaml)

### 08 — Toggle a smart plug using an NFC tag

**What it does:** Toggles a selected `switch` each time the configured NFC tag is scanned.

**Requirements:** An NFC tag registered in Home Assistant, a device capable of scanning it, and a smart plug exposed as a `switch`.

**Notes and limitations:** Use only plugs and appliances suited to remote power switching, respecting electrical load and safety limits.

[![Import into Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fnfc%2Ftoggle_presa_con_tag.yaml)

[Import directly into Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fnfc%2Ftoggle_presa_con_tag.yaml) · [Blueprint YAML on GitHub](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/nfc/toggle_presa_con_tag.yaml)

### 09 — Schedule a coffee machine smart plug

**What it does:** At 07:00, Monday to Friday, turns on the selected plug only when the chosen person or tracker is `home`; time is configurable.

**Requirements:** A smart plug (`switch`), a compatible coffee machine, and a `person` or `device_tracker` entity.

**Notes and limitations:** There is no automatic switch-off and no guarantee that coffee preparation starts. Use only appliances rated for unattended power-on; presence tracking may be inaccurate.

[![Import into Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fprese%2Faccensione_programmata_con_presenza.yaml)

[Import directly into Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fprese%2Faccensione_programmata_con_presenza.yaml) · [Blueprint YAML on GitHub](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/prese/accensione_programmata_con_presenza.yaml)

### 10 — Notify when Home Assistant begins shutting down

**What it does:** Attempts to send a smartphone notification when Home Assistant begins shutdown or restart.

**Requirements:** The official Home Assistant companion app with working push notifications.

**Notes and limitations:** Delivery is not guaranteed during shutdown. Crashes, power failures, and network outages require independent external monitoring. Default title: “Server di casa”; message: “Home Assistant si sta spegnendo”.

[![Import into Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fsistema%2Favviso_spegnimento_home_assistant.yaml)

[Import directly into Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fsistema%2Favviso_spegnimento_home_assistant.yaml) · [Blueprint YAML on GitHub](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/sistema/avviso_spegnimento_home_assistant.yaml)

### 11 — Open a shutter on weekdays at a set time

**What it does:** Opens the selected `cover` at 07:00, Monday to Friday; time is configurable.

**Requirements:** A cover entity that supports the opening command.

**Notes and limitations:** Also runs on public holidays that fall on weekdays, regardless of occupancy; does not close the shutter automatically. Verify safe physical operation.

[![Import into Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Ftapparelle%2Fapertura_programmata_tapparella.yaml)

[Import directly into Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Ftapparelle%2Fapertura_programmata_tapparella.yaml) · [Blueprint YAML on GitHub](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/tapparelle/apertura_programmata_tapparella.yaml)

### 12 — Reduce heating when a window opens

**What it does:** When a window changes from closed to open, applies a preset selected in the automation editor.

**Requirements:** A window contact sensor and a thermostat supporting the chosen preset.

**Notes and limitations:** Choose frost protection only if actually supported. The automation does not restore the previous mode when the window closes.

[![Import into Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Friscaldamento%2Friduzione_riscaldamento_finestra_aperta.yaml)

[Import directly into Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Friscaldamento%2Friduzione_riscaldamento_finestra_aperta.yaml) · [Blueprint YAML on GitHub](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/riscaldamento/riduzione_riscaldamento_finestra_aperta.yaml)

### 13 — Apply a heating preset when a window closes

**What it does:** After the window remains closed for 1 minute, applies the configured thermostat preset.

**Requirements:** A window contact sensor and thermostat supporting the selected preset.

**Notes and limitations:** For use with blueprint 12, select the same window and thermostat. The “Schedule” preset is only an example, and this does not necessarily restore the previously active state.

[![Import into Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Friscaldamento%2Fripristino_riscaldamento_finestra_chiusa.yaml)

[Import directly into Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Friscaldamento%2Fripristino_riscaldamento_finestra_chiusa.yaml) · [Blueprint YAML on GitHub](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/riscaldamento/ripristino_riscaldamento_finestra_chiusa.yaml)

### 14 — Notify when heating valves become active

**What it does:** Sends a notification when a selected climate entity reports `hvac_action: heating` for at least 5 seconds.

**Requirements:** At least one thermostat or radiator valve reporting `hvac_action`, plus the Home Assistant phone app.

**Notes and limitations:** Reports the integration state, not a verified physical valve position. Default title: “Riscaldamento acceso”; message: “Le valvole si sono attivate e il riscaldamento è partito”.

[![Import into Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fclima%2Favviso_climatizzazione_attiva.yaml)

[Import directly into Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fclima%2Favviso_climatizzazione_attiva.yaml) · [Blueprint YAML on GitHub](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/clima/avviso_climatizzazione_attiva.yaml)

### 15 — Notify when heating valves stop heating

**What it does:** Sends a notification when `hvac_action` changes from `heating` to `off` and stays there for 5 seconds.

**Requirements:** A thermostat or valve exposing the `heating` and `off` values and the Home Assistant phone app.

**Notes and limitations:** Devices changing to `idle` instead of `off` do not trigger it. Default title: “Riscaldamento”; message: “Le valvole hanno terminato il riscaldamento”.

[![Import into Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fclima%2Favviso_riscaldamento_spento.yaml)

[Import directly into Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fclima%2Favviso_riscaldamento_spento.yaml) · [Blueprint YAML on GitHub](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/clima/avviso_riscaldamento_spento.yaml)

### 16 — Reduce heating when away on weekdays

**What it does:** After the person is away for 5 minutes on Monday–Friday between 00:00 and 23:59, applies the selected thermostat preset.

**Requirements:** A configured `person` entity and compatible thermostats with supported presets.

**Notes and limitations:** The “Away” preset is an example, not universally supported. GPS tracking can report false departures; no return-home restoration is included.

[![Import into Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Friscaldamento%2Friduci_riscaldamento_assenza_feriali.yaml)

[Import directly into Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Friscaldamento%2Friduci_riscaldamento_assenza_feriali.yaml) · [Blueprint YAML on GitHub](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/riscaldamento/riduci_riscaldamento_assenza_feriali.yaml)

### 17 — Restore a heating preset when home on weekdays

**What it does:** After the person is home for 15 seconds on Monday–Friday between 00:00 and 23:59, applies the configured thermostat preset.

**Requirements:** A configured `person` entity and thermostats supporting the preset.

**Notes and limitations:** Pair with blueprint 16 using the same person and thermostats. “Schedule” is an example; false GPS arrivals can occur and the previous preset is not restored.

[![Import into Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Friscaldamento%2Fripristina_riscaldamento_rientro_feriali.yaml)

[Import directly into Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Friscaldamento%2Fripristina_riscaldamento_rientro_feriali.yaml) · [Blueprint YAML on GitHub](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/riscaldamento/ripristina_riscaldamento_rientro_feriali.yaml)

### 18 — Reduce heating when away at weekends

**What it does:** After a person is away for 2 minutes during the weekend, applies the selected heating preset and sends a smartphone notification.

**Requirements:** A configured `person` entity, thermostats supporting the preset, and Home Assistant phone notifications.

**Notes and limitations:** GPS tracking may be inaccurate and the automation does not restore heating on return. Default title: “Riscaldamento sospeso”; message: “Il riscaldamento è stato fermato perché nel weekend non sei a casa”.

[![Import into Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Friscaldamento%2Friduci_riscaldamento_assenza_weekend.yaml)

[Import directly into Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Friscaldamento%2Friduci_riscaldamento_assenza_weekend.yaml) · [Blueprint YAML on GitHub](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/riscaldamento/riduci_riscaldamento_assenza_weekend.yaml)

### 19 — Apply scheduled heating on weekend return

**What it does:** After a person is home for 5 minutes during the weekend, applies the configured thermostat schedule preset.

**Requirements:** A configured `person` entity and thermostats supporting the selected preset.

**Notes and limitations:** The “Schedule” preset must exist on the device. Presence tracking may be inaccurate, and this applies a preset rather than recovering the prior state.

[![Import into Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Friscaldamento%2Fripristina_riscaldamento_rientro_weekend.yaml)

[Import directly into Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Friscaldamento%2Fripristina_riscaldamento_rientro_weekend.yaml) · [Blueprint YAML on GitHub](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/riscaldamento/ripristina_riscaldamento_rientro_weekend.yaml)

### 20 — Notify a tablet when occupancy is detected

**What it does:** After 1 second of occupancy, checks whether the chosen person or device is `home`, then sends a tablet notification titled “Dashboard” with message “Apri”.

**Requirements:** A compatible occupancy sensor, a tracked person or device, and a tablet configured for Home Assistant notifications.

**Notes and limitations:** The notification does not itself guarantee that the Home Assistant app or dashboard opens; behavior depends on tablet and app configuration.

[![Import into Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fdashboard%2Fapri_home_assistant_tablet.yaml)

[Import directly into Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fdashboard%2Fapri_home_assistant_tablet.yaml) · [Blueprint YAML on GitHub](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/dashboard/apri_home_assistant_tablet.yaml)

## Compatibility and Requirements

- A Home Assistant installation supporting automation blueprints is required.
- Only the devices, entities, and integrations described for the selected blueprint are needed.
- Some blueprints require Companion App notifications; Alexa support is optional and depends on a compatible integration.
- **HACS, a paid API, and a subscription are not required to install these blueprints.** Any existing cloud integrations may have separate terms or costs.
- No specific minimum Home Assistant version has been verified across all 20 blueprints.

## Updates, Privacy and Safety

- Before enabling an automation, review the selected entities, device effects, and the notes above.
- Changes on GitHub do not automatically update previously imported blueprints. Re-importing can change the behavior of existing automations; review changes before doing so.
- The repository contains generic blueprint files. Do not add credentials, private IP addresses, or actual Home Assistant instance identifiers to public examples.
- Notifications and Home Assistant integrations configured by the user may communicate with external services under their respective terms and privacy policies.
- Water-leak and shutdown notifications do not replace independent safety or monitoring systems.

## Copyright & License

Copyright © 2026 **luigi-regolo**.

Original project created and maintained by **luigi-regolo**.

Licensed under the **MIT License**. See [LICENSE](LICENSE) for the complete terms.

The software is provided without warranty to the extent permitted by applicable law.
