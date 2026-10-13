# Automazioni pronte per Home Assistant

Automazioni da importare in Home Assistant e personalizzare selezionando i propri dispositivi. Non serve copiare YAML né installare HACS.

## Automazioni disponibili

### Accendi luce ingresso all'apertura della porta

**Cosa fa:** quando il sensore segnala l'apertura della porta, accende la luce selezionata **solo dopo il tramonto oppure prima dell'alba**. Non spegne automaticamente la luce.

**Cosa serve:** un sensore binario di apertura porta e una luce configurati in Home Assistant.

**[Importa in Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fingresso%2Faccendi_luce_apertura_porta.yaml)**

[Visualizza il file dell'automazione](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/ingresso/accendi_luce_apertura_porta.yaml)

### Come utilizzarla

1. Apri il link **Importa in Home Assistant**.
2. Seleziona la tua istanza Home Assistant e importa il progetto.
3. In Home Assistant crea un'automazione dal progetto importato.
4. Seleziona il tuo sensore porta e la luce, poi salva.

> Versione demo da verificare prima dell'uso quotidiano. L'automazione accende la luce e non la spegne: replica intenzionalmente la logica originale. L'importazione non assegna automaticamente i dispositivi.

## Aggiornamenti e sicurezza

Le modifiche pubblicate qui non aggiornano automaticamente le copie già importate. Controlla le modifiche prima di scegliere **Reimporta progetto** in Home Assistant.

I file pubblicati non contengono nomi di persone, indirizzi, identificativi di entità domestiche o credenziali.

## Licenza

[MIT](LICENSE)
