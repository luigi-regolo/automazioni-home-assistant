# Automazioni pronte per Home Assistant

Una raccolta di automazioni pronte da importare in **Home Assistant**. Scegli i tuoi dispositivi e salva: non serve copiare codice YAML o installare HACS.

## Automazioni disponibili

### 01 — Accendi luce ingresso all'apertura della porta

**Cosa fa:** quando si apre una porta, accende la luce scelta solo **dopo il tramonto oppure prima dell'alba**. La luce **non viene spenta automaticamente**.

**Requisiti:** sensore di apertura porta e luce già configurati in Home Assistant.

[![Importa in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fingresso%2Faccendi_luce_apertura_porta.yaml)

**[Importa direttamente in Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fingresso%2Faccendi_luce_apertura_porta.yaml)**

**Importazione alternativa:** se il pulsante non apre la tua istanza (ad esempio da un browser interno a un social), copia il **[link GitHub dell'automazione](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/ingresso/accendi_luce_apertura_porta.yaml)** e incollalo in **Home Assistant → Impostazioni → Automazioni e scene → Progetti → Importa progetto**.

### 02 — Spegni luce ingresso quando termina il movimento

**Cosa fa:** quando termina il movimento, spegne la luce selezionata **solo se la porta è chiusa** e se siamo **dopo il tramonto oppure prima dell'alba**. Non prevede ritardi.

**Requisiti:** sensore di movimento, sensore di apertura porta e luce già configurati in Home Assistant.

[![Importa in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fingresso%2Fspegni_luce_fine_movimento.yaml)

**[Importa direttamente in Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fingresso%2Fspegni_luce_fine_movimento.yaml)**

**Importazione alternativa:** copia il **[link GitHub dell'automazione](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/ingresso/spegni_luce_fine_movimento.yaml)** e incollalo in **Home Assistant → Impostazioni → Automazioni e scene → Progetti → Importa progetto**.

### 03 — Aggiorna entità selezionate ogni 20 secondi

**Cosa fa:** richiede ogni 20 secondi l'aggiornamento delle entità scelte dall'utente tramite l'azione ufficiale `homeassistant.update_entity`.

**Requisiti:** una o più entità che supportano l'aggiornamento su richiesta. L'effetto dipende dall'integrazione: le entità che non supportano il polling potrebbero non aggiornarsi.

**Attenzione:** non è una soluzione ai falsi positivi GPS. Aggiornare un'entità persona **non** forza il telefono a comunicare una nuova posizione. Un intervallo di 20 secondi può aumentare il carico o causare limitazioni delle integrazioni cloud. Usala solo per entità compatibili e realmente necessarie.

[![Importa in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fsensori%2Faggiorna_entita_ogni_20_secondi.yaml)

**[Importa direttamente in Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fsensori%2Faggiorna_entita_ogni_20_secondi.yaml)**

**Importazione alternativa:** copia il **[link GitHub dell'automazione](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/sensori/aggiorna_entita_ogni_20_secondi.yaml)** e incollalo in **Home Assistant → Impostazioni → Automazioni e scene → Progetti → Importa progetto**.

### Dopo l'importazione

1. Apri il progetto appena importato e scegli **Crea automazione**.
2. Seleziona i sensori e la luce richiesti dall'automazione.
3. Salva l'automazione.

> L'importazione non seleziona automaticamente i dispositivi e non crea una nuova automazione finché non completi i passaggi. Verifica il comportamento prima dell'uso quotidiano.

## Aggiornamenti e sicurezza

- I file sono esempi generici: non contengono credenziali, indirizzi o ID delle entità di una casa reale.
- Le modifiche su GitHub non aggiornano automaticamente i progetti già importati. Usa **Reimporta progetto** solo dopo aver valutato eventuali incompatibilità.

## Licenza

[MIT](LICENSE)
