# Automazioni pronte per Home Assistant

Una raccolta di automazioni pronte da importare in **Home Assistant**. Scegli i tuoi dispositivi e salva: non serve copiare codice YAML o installare HACS.

## Automazioni disponibili

### 01 — Accendi luce ingresso all'apertura della porta

**Cosa fa:** quando si apre una porta, accende la luce scelta solo **dopo il tramonto oppure prima dell'alba**. La luce **non viene spenta automaticamente**.

**Requisiti:** sensore di apertura porta e luce già configurati in Home Assistant.

[![Importa in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fingresso%2Faccendi_luce_apertura_porta.yaml)

**[Importa direttamente in Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fingresso%2Faccendi_luce_apertura_porta.yaml)**

**Importazione alternativa:** se il pulsante non apre la tua istanza (ad esempio da un browser interno a un social), copia il **[link GitHub dell'automazione](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/ingresso/accendi_luce_apertura_porta.yaml)** e incollalo in **Home Assistant → Impostazioni → Automazioni e scene → Progetti → Importa progetto**.

### Dopo l'importazione

1. Apri il progetto appena importato e scegli **Crea automazione**.
2. Seleziona il sensore porta e la luce della tua installazione.
3. Salva l'automazione.

> L'importazione non seleziona automaticamente i dispositivi e non crea una nuova automazione finché non completi i passaggi. Verifica il comportamento prima dell'uso quotidiano.

## Aggiornamenti e sicurezza

- I file sono esempi generici: non contengono credenziali, indirizzi o ID delle entità di una casa reale.
- Le modifiche su GitHub non aggiornano automaticamente i progetti già importati. Usa **Reimporta progetto** solo dopo aver valutato eventuali incompatibilità.

## Licenza

[MIT](LICENSE)
