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

**[Importa direttamente in Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fclima%2Fspegnimento_automatico_deumidificazione.yaml)**

**Importazione alternativa:** copia il **[link GitHub dell'automazione](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/clima/spegnimento_automatico_deumidificazione.yaml)** e incollalo in **Impostazioni → Automazioni e scene → Progetti → Importa progetto**.

> **Da testare prima di pubblicarla su TikTok.** Questa automazione è complementare ad AUTO 05. Se usata con AUTO 05, seleziona lo stesso sensore e climatizzatore, e mantieni la soglia di spegnimento inferiore a quella di accensione. La notifica viene inviata dopo il comando, senza verifica dello stato effettivo del climatizzatore.

### 07 — Dashboard automatica in base al movimento

**Cosa fa:** quando un sensore rileva movimento per almeno **1 secondo**, imposta l'opzione scelta in un aiutante **input_select**. Una dashboard già configurata per leggere quel selettore può quindi mostrare l'ambiente corrispondente.

**Requisiti:** un sensore di movimento, un aiutante a tendina (`input_select`) con le opzioni desiderate e una dashboard già predisposta per reagire al suo valore. **Questo progetto non crea la dashboard e non cambia direttamente la pagina aperta nel browser.**

[![Importa in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fdashboard%2Fdashboard_automatica_movimento.yaml)

**[Importa direttamente in Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fdashboard%2Fdashboard_automatica_movimento.yaml)**

**Importazione alternativa:** copia il **[link GitHub dell'automazione](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/dashboard/dashboard_automatica_movimento.yaml)** e incollalo in **Impostazioni → Automazioni e scene → Progetti → Importa progetto**.

> **Da verificare prima della condivisione su TikTok.** Dopo l'importazione seleziona il sensore, l'aiutante e inserisci esattamente il testo di una delle opzioni esistenti. Per ogni ambiente si può creare una distinta automazione dal medesimo progetto. Il comportamento visivo dipende dalla dashboard configurata dall'utente.

### 08 — Accendi o spegni una presa con tag NFC

**Cosa fa:** quando viene scansionata l'etichetta NFC scelta, cambia lo stato della presa smart: se è accesa la spegne, se è spenta la accende. Nessuna condizione aggiuntiva.

**Requisiti:** un tag NFC configurato in Home Assistant, un dispositivo capace di effettuare la scansione (ad esempio l'app Companion) e una presa smart esposta come entità `switch`.

[![Importa in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fnfc%2Ftoggle_presa_con_tag.yaml)

**[Importa direttamente in Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fnfc%2Ftoggle_presa_con_tag.yaml)**

**Importazione alternativa:** copia il **[link GitHub dell'automazione](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/nfc/toggle_presa_con_tag.yaml)** e incollalo in **Impostazioni → Automazioni e scene → Progetti → Importa progetto**.

> **Da testare prima della condivisione su TikTok.** Durante la creazione dell'automazione, nel campo **Scansione del tag NFC** scegli **Tag** e seleziona la tua etichetta; nel campo **Presa smart** scegli lo switch. Verifica che il carico elettrico sia compatibile con la presa. Il comando cambia l'alimentazione ma non garantisce l'avvio o l'arresto sicuro di un elettrodomestico. Evita il controllo di apparecchi ad alta potenza senza dispositivi adeguati.

### 09 — Accensione programmata presa smart con presenza

**Cosa fa:** alle **06:45**, dal **lunedì al venerdì**, accende una presa smart **solo se la persona o il dispositivo scelto risulta a casa**. L'orario è modificabile. Non è previsto uno spegnimento automatico.

**Requisiti:** una presa smart con entità `switch` e un'entità `person` o `device_tracker` che rilevi lo stato `home`.

[![Importa in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fprese%2Faccensione_programmata_con_presenza.yaml)

**[Importa direttamente in Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fprese%2Faccensione_programmata_con_presenza.yaml)**

**Importazione alternativa:** copia il **[link GitHub dell'automazione](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/prese/accensione_programmata_con_presenza.yaml)** e incollalo in **Impostazioni → Automazioni e scene → Progetti → Importa progetto**.

> **Da testare prima della condivisione su TikTok.** Utilizza solo apparecchi che supportano l'accensione automatica senza sorveglianza e una presa adeguata alla potenza assorbita. La presenza dipende dall'aggiornamento del tracciamento; se risulta erroneamente `home`, la presa potrebbe accendersi anche senza nessuno in casa. L'automazione non spegne la presa.

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
