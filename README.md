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

### 04 — Avviso allagamento con notifiche smartphone e Alexa

**Cosa fa:** quando un sensore rileva acqua, esegue le azioni di notifica impostate dall'utente. Nessuna condizione aggiuntiva.

**Richiede:** un sensore binario di allagamento (`binary_sensor` con classe `moisture`) e almeno un servizio di notifica funzionante. L'annuncio Alexa è facoltativo e richiede un'integrazione compatibile (ad esempio Alexa Media Player, non ufficiale).

[![Importa in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fsicurezza%2Favviso_allagamento.yaml)

**[Importa direttamente in Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fsicurezza%2Favviso_allagamento.yaml)**

**Importazione alternativa:** copia il **[link GitHub dell'automazione](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/sicurezza/avviso_allagamento.yaml)** e incollalo in **Impostazioni → Automazioni e scene → Progetti → Importa progetto**.

Dopo l'importazione seleziona il sensore. Nel campo **Notifiche da inviare** configura almeno un'azione di notifica sul tuo telefono e, se disponibile, un annuncio Alexa. Messaggio demo suggerito: **Attenzione. Rilevata presenza di acqua. Controlla subito.**

> **Stato:** versione da testare in Home Assistant prima di condividerla su TikTok. La notifica dipende dalla disponibilità delle integrazioni e della connessione, e non sostituisce un sistema di protezione antiallagamento.

### 05 — Controllo automatico umidità

**Cosa fa:** se l'umidità supera **65% per 2 minuti** (valori modificabili), imposta il climatizzatore in modalità **dry** e invia una notifica allo smartphone. Non ci sono condizioni aggiuntive né spegnimento automatico.

**Requisiti:** sensore di umidità, entità climatizzatore compatibile con la modalità `dry` e smartphone con app ufficiale Home Assistant configurata.

**Messaggio precompilato:** «L’umidità è troppo alta e il climatizzatore è stato acceso in modalità deumidificazione.»

[![Importa in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fclima%2Fcontrollo_umidita_deumidificazione.yaml)

**[Importa direttamente in Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fclima%2Fcontrollo_umidita_deumidificazione.yaml)**

**Importazione alternativa:** copia il **[link GitHub dell'automazione](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/clima/controllo_umidita_deumidificazione.yaml)** e incollalo in **Impostazioni → Automazioni e scene → Progetti → Importa progetto**.

> **Da verificare prima della condivisione su TikTok.** La modalità `dry` non è supportata da tutti i climatizzatori e l'azione non imposta un livello di umidità né spegne il dispositivo automaticamente. Il trigger scatta solo al superamento della soglia; un riavvio di Home Assistant durante i 2 minuti azzera l'attesa. È opportuno testare la notifica e la modalità HVAC prima di abilitare la nuova automazione.

### 06 — Spegnimento automatico deumidificazione

**Cosa fa:** quando l'umidità scende **sotto il 61% per 2 minuti**, imposta la modalità HVAC del climatizzatore su **off** e invia una notifica allo smartphone. Soglia e durata sono modificabili. Non sono presenti condizioni aggiuntive.

**Requisiti:** sensore di umidità, climatizzatore compatibile e smartphone con app Home Assistant. **Importante:** `off` spegne l'intero climatizzatore, non soltanto la modalità deumidificazione.

**Messaggio precompilato:** «L’umidità è tornata nei valori ideali e il climatizzatore in modalità deumidificazione è stato spento»

[![Importa in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fclima%2Fspegnimento_automatico_deumidificazione.yaml)

**[Importa direttamente in Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fclima%2Fspegnimento_automatico_deumidificazione.yaml)

**Importazione alternativa:** copia il **[link GitHub dell'automazione](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/clima/spegnimento_automatico_deumidificazione.yaml)** e incollalo in **Impostazioni → Automazioni e scene → Progetti → Importa progetto**.

> **Da testare prima di pubblicarla su TikTok.** Questa automazione è complementare ad AUTO 05. Se usata con AUTO 05, seleziona lo stesso sensore e climatizzatore, e mantieni la soglia di spegnimento inferiore a quella di accensione. La notifica viene inviata dopo il comando, senza verifica dello stato effettivo del climatizzatore.

### Dopo l'importazione

1. Apri il progetto appena importato e scegli **Crea automazione**.
2. Seleziona i dispositivi richiesti dall'automazione e configura eventuali messaggi.
3. Salva l'automazione.

> L'importazione non seleziona automaticamente i dispositivi e non crea una nuova automazione finché non completi i passaggi. Verifica il comportamento prima dell'uso quotidiano.

## Aggiornamenti e sicurezza

- I file sono esempi generici: non contengono credenziali, indirizzi o ID delle entità di una casa reale.
- Le modifiche su GitHub non aggiornano automaticamente i progetti già importati. Usa **Reimporta progetto** solo dopo aver valutato eventuali incompatibilità.

## Licenza

[MIT](LICENSE)
