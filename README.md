<a href="https://www.tiktok.com/@luigi.regolo" title="Segui i tutorial Home Assistant su TikTok"><img src="assets/tiktok-segui.svg" alt="TikTok | Segui" width="116" height="22"></a>

# Automazioni pronte per Home Assistant

Una raccolta di automazioni pronte da importare in **Home Assistant**. Nessun codice YAML da copiare e nessuna installazione HACS richiesta.

## Come iniziare

1. **Scegli un'automazione** dal catalogo qui sotto.
2. **Premi "Importa in Home Assistant"** per aggiungerla alla tua installazione.
3. **Crea la tua automazione**, seleziona i dispositivi richiesti e salva.

Tutto direttamente dall'interfaccia di Home Assistant.

**Nota:** l'importazione aggiunge il progetto, ma non crea automaticamente un'automazione attiva. Prima di utilizzarla, configura i tuoi dispositivi e verifica che funzioni correttamente.

---

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

> **Nota:** La notifica dipende dalla disponibilità delle integrazioni e della connessione, e non sostituisce un sistema di protezione antiallagamento.

### 05 — Controllo automatico umidità

**Cosa fa:** se l'umidità supera **65% per 2 minuti** (valori modificabili), imposta il climatizzatore in modalità **dry** e invia una notifica allo smartphone. Non ci sono condizioni aggiuntive né spegnimento automatico.

**Requisiti:** sensore di umidità, entità climatizzatore compatibile con la modalità `dry` e smartphone con app ufficiale Home Assistant configurata.

**Messaggio precompilato:** «L’umidità è troppo alta e il climatizzatore è stato acceso in modalità deumidificazione.»

[![Importa in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fclima%2Fcontrollo_umidita_deumidificazione.yaml)

**[Importa direttamente in Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fclima%2Fcontrollo_umidita_deumidificazione.yaml)**

**Importazione alternativa:** copia il **[link GitHub dell'automazione](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/clima/controllo_umidita_deumidificazione.yaml)** e incollalo in **Impostazioni → Automazioni e scene → Progetti → Importa progetto**.

> **Nota:** La modalità `dry` non è supportata da tutti i climatizzatori e l'azione non imposta un livello di umidità né spegne il dispositivo automaticamente. Il trigger scatta solo al superamento della soglia; un riavvio di Home Assistant durante i 2 minuti azzera l'attesa. È opportuno testare la notifica e la modalità HVAC prima di abilitare la nuova automazione.

### 06 — Spegnimento automatico deumidificazione

**Cosa fa:** quando l'umidità scende **sotto il 61% per 2 minuti**, imposta la modalità HVAC del climatizzatore su **off** e invia una notifica allo smartphone. Soglia e durata sono modificabili. Non sono presenti condizioni aggiuntive.

**Requisiti:** sensore di umidità, climatizzatore compatibile e smartphone con app Home Assistant. **Importante:** `off` spegne l'intero climatizzatore, non soltanto la modalità deumidificazione.

**Messaggio precompilato:** «L’umidità è tornata nei valori ideali e il climatizzatore in modalità deumidificazione è stato spento»

[![Importa in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fclima%2Fspegnimento_automatico_deumidificazione.yaml)

**[Importa direttamente in Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fclima%2Fspegnimento_automatico_deumidificazione.yaml)**

**Importazione alternativa:** copia il **[link GitHub dell'automazione](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/clima/spegnimento_automatico_deumidificazione.yaml)** e incollalo in **Impostazioni → Automazioni e scene → Progetti → Importa progetto**.

> **Nota:** Questa automazione è complementare ad AUTO 05. Se usata con AUTO 05, seleziona lo stesso sensore e climatizzatore, e mantieni la soglia di spegnimento inferiore a quella di accensione. La notifica viene inviata dopo il comando, senza verifica dello stato effettivo del climatizzatore.

### 07 — Dashboard automatica in base al movimento

**Cosa fa:** quando un sensore rileva movimento per almeno **1 secondo**, imposta l'opzione scelta in un aiutante **input_select**. Una dashboard già configurata per leggere quel selettore può quindi mostrare l'ambiente corrispondente.

**Requisiti:** un sensore di movimento, un aiutante a tendina (`input_select`) con le opzioni desiderate e una dashboard già predisposta per reagire al suo valore. **Questo progetto non crea la dashboard e non cambia direttamente la pagina aperta nel browser.**

[![Importa in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fdashboard%2Fdashboard_automatica_movimento.yaml)

**[Importa direttamente in Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fdashboard%2Fdashboard_automatica_movimento.yaml)**

**Importazione alternativa:** copia il **[link GitHub dell'automazione](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/dashboard/dashboard_automatica_movimento.yaml)** e incollalo in **Impostazioni → Automazioni e scene → Progetti → Importa progetto**.

> **Nota:** Dopo l'importazione seleziona il sensore, l'aiutante e inserisci esattamente il testo di una delle opzioni esistenti. Per ogni ambiente si può creare una distinta automazione dal medesimo progetto. Il comportamento visivo dipende dalla dashboard configurata dall'utente.

### 08 — Accendi o spegni una presa con tag NFC

**Cosa fa:** quando viene scansionata l'etichetta NFC scelta, cambia lo stato della presa smart: se è accesa la spegne, se è spenta la accende. Nessuna condizione aggiuntiva.

**Requisiti:** un tag NFC configurato in Home Assistant, un dispositivo capace di effettuare la scansione (ad esempio l'app Companion) e una presa smart esposta come entità `switch`.

[![Importa in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fnfc%2Ftoggle_presa_con_tag.yaml)

**[Importa direttamente in Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fnfc%2Ftoggle_presa_con_tag.yaml)**

**Importazione alternativa:** copia il **[link GitHub dell'automazione](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/nfc/toggle_presa_con_tag.yaml)** e incollalo in **Impostazioni → Automazioni e scene → Progetti → Importa progetto**.

> **Nota:** Durante la creazione dell'automazione, nel campo **Scansione del tag NFC** scegli **Tag** e seleziona la tua etichetta; nel campo **Presa smart** scegli lo switch. Verifica che il carico elettrico sia compatibile con la presa. Il comando cambia l'alimentazione ma non garantisce l'avvio o l'arresto sicuro di un elettrodomestico. Evita il controllo di apparecchi ad alta potenza senza dispositivi adeguati.

### 09 — Accensione programmata macchina del caffè

**Cosa fa:** alle **07:00**, dal **lunedì al venerdì**, accende la presa smart della macchina del caffè **solo se la persona o il dispositivo scelto risulta a casa**. L'orario è modificabile. Non è previsto uno spegnimento automatico né l'avvio garantito della preparazione del caffè.

**Requisiti:** una presa smart con entità `switch`, una macchina del caffè compatibile con l'alimentazione programmata e un'entità `person` o `device_tracker` che rilevi lo stato `home`.

[![Importa in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fprese%2Faccensione_programmata_con_presenza.yaml)

**[Importa direttamente in Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fprese%2Faccensione_programmata_con_presenza.yaml)**

**Importazione alternativa:** copia il **[link GitHub dell'automazione](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/prese/accensione_programmata_con_presenza.yaml)** e incollalo in **Impostazioni → Automazioni e scene → Progetti → Importa progetto**.

> **Nota:** Utilizza solo apparecchi che supportano l'accensione automatica senza sorveglianza e una presa adeguata alla potenza assorbita. La presenza dipende dall'aggiornamento del tracciamento; se risulta erroneamente `home`, la presa potrebbe accendersi anche senza nessuno in casa. L'automazione non spegne la presa.

### 10 — Avviso spegnimento Home Assistant

**Cosa fa:** quando Home Assistant **inizia uno spegnimento o un riavvio**, prova a inviare una notifica allo smartphone scelto. Nessuna condizione aggiuntiva.

**Requisiti:** app ufficiale Home Assistant su smartphone, registrazione del dispositivo in Home Assistant e notifiche abilitate. Il dispositivo e il servizio di notifiche devono essere raggiungibili durante lo spegnimento.

**Titolo precompilato:** «Server di casa»

**Messaggio precompilato:** «Home Assistant si sta spegnendo»

[![Importa in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fsistema%2Favviso_spegnimento_home_assistant.yaml)

**[Importa direttamente in Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fsistema%2Favviso_spegnimento_home_assistant.yaml)**

**Importazione alternativa:** copia il **[link GitHub dell'automazione](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/sistema/avviso_spegnimento_home_assistant.yaml)** e incollalo in **Impostazioni → Automazioni e scene → Progetti → Importa progetto**.

> **Nota:** L'avviso è un tentativo di notifica, non una conferma della consegna. Lo spegnimento lascia un tempo limitato alle automazioni e il messaggio potrebbe non arrivare. Crash, blackout, perdita di rete e interruzioni improvvise non sono rilevabili in modo affidabile da Home Assistant mentre è offline. Per il controllo della disponibilità serve un monitoraggio esterno. Evita riavvii solo per provare il progetto: verifica l'invio durante una manutenzione programmata.

### 11 — Apertura programmata tapparella

**Cosa fa:** alle **07:00**, dal **lunedì al venerdì**, apre la tapparella selezionata. L'orario è modificabile. Nessuna condizione aggiuntiva.

**Requisiti:** una tapparella motorizzata configurata in Home Assistant come entità `cover`. Il dispositivo deve supportare il comando di apertura.

[![Importa in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Ftapparelle%2Fapertura_programmata_tapparella.yaml)

**[Importa direttamente in Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Ftapparelle%2Fapertura_programmata_tapparella.yaml)**

**Importazione alternativa:** copia il **[link GitHub dell'automazione](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/tapparelle/apertura_programmata_tapparella.yaml)** e incollalo in **Impostazioni → Automazioni e scene → Progetti → Importa progetto**.

> **Nota:** Si attiva anche nei giorni festivi che cadono tra lunedì e venerdì e indipendentemente dalla presenza di persone. Non rileva la sveglia effettiva, né chiude automaticamente la tapparella. Verifica il corretto funzionamento e la sicurezza del movimento prima di abilitarla.

### 12 — Sospendi riscaldamento con finestra aperta

**Cosa fa:** quando una finestra passa da **chiusa ad aperta**, applica al termostato la modalità preimpostata selezionata. Per replicare l'esempio originale, scegli **Protezione antigelo**, se supportata. Nessuna condizione aggiuntiva e nessun ripristino automatico alla chiusura.

**Requisiti:** sensore di apertura finestra e termostato Home Assistant con supporto alle modalità preimpostate. I preset disponibili dipendono dal dispositivo.

[![Importa in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Friscaldamento%2Friduzione_riscaldamento_finestra_aperta.yaml)

**[Importa direttamente in Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Friscaldamento%2Friduzione_riscaldamento_finestra_aperta.yaml)**

**Importazione alternativa:** copia il **[link GitHub dell'automazione](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/riscaldamento/riduzione_riscaldamento_finestra_aperta.yaml)** e incollalo in **Impostazioni → Automazioni e scene → Progetti → Importa progetto**.

> **Nota:** Dopo l'importazione scegli il sensore finestra e configura l'azione del termostato usando l'editor grafico, selezionando il preset effettivamente disponibile. "Protezione antigelo" non equivale necessariamente a spegnimento completo; la temperatura minima dipende dal termostato. Se il preset non è supportato, non usarlo. Alla richiusura della finestra il riscaldamento non viene ripristinato automaticamente.

### 13 — Ripristina riscaldamento alla chiusura della finestra

**Cosa fa:** quando una finestra passa da **aperta a chiusa** e rimane chiusa per **1 minuto**, imposta sul termostato il preset scelto dall'utente. Per replicare l'esempio, seleziona **Pianificazione** se supportato. Nessuna condizione aggiuntiva.

**Requisiti:** sensore finestra e termostato Home Assistant che supporti le modalità preimpostate. La modalità Pianificazione può avere un nome differente o non essere disponibile su altri termostati.

[![Importa in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Friscaldamento%2Fripristino_riscaldamento_finestra_chiusa.yaml)

**[Importa direttamente in Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Friscaldamento%2Fripristino_riscaldamento_finestra_chiusa.yaml)**

**Importazione alternativa:** copia il **[link GitHub dell'automazione](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/riscaldamento/ripristino_riscaldamento_finestra_chiusa.yaml)** e incollalo in **Impostazioni → Automazioni e scene → Progetti → Importa progetto**.

> **Nota:** Dopo l'importazione, seleziona il sensore e configura nell'editor l'azione del termostato con un preset realmente supportato. AUTO 13 è complementare ad AUTO 12: per utilizzarle insieme scegli lo stesso sensore e lo stesso termostato. Questa automazione applica un preset predefinito, **non** ripristina necessariamente lo stato precedente all'apertura. Il timer di un minuto riparte se la finestra si riapre.

### 14 — Avviso valvole riscaldamento attive

**Cosa fa:** quando una delle valvole termostatiche o dei termostati selezionati indica **riscaldamento attivo per almeno 5 secondi**, invia una notifica sullo smartphone. Nessuna condizione aggiuntiva.

**Requisiti:** almeno una valvola termostatica o un termostato con entità `climate` che esponga l'attributo `hvac_action` con valore `heating`, e uno smartphone con l'app ufficiale Home Assistant.

**Titolo precompilato:** «Riscaldamento acceso»

**Messaggio precompilato:** «Le valvole si sono attivate e il riscaldamento è partito»

[![Importa in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fclima%2Favviso_climatizzazione_attiva.yaml)

**[Importa direttamente in Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fclima%2Favviso_climatizzazione_attiva.yaml)**

**Importazione alternativa:** copia il **[link GitHub dell'automazione](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/clima/avviso_climatizzazione_attiva.yaml)** e incollalo in **Impostazioni → Automazioni e scene → Progetti → Importa progetto**.

> **Nota:** L'automazione controlla solo il riscaldamento (`hvac_action: heating`), non il raffreddamento o la deumidificazione. Alcune valvole non espongono `hvac_action` o non lo aggiornano in modo affidabile. La notifica conferma lo stato riportato dall'integrazione, non necessariamente l'effettiva apertura fisica della valvola.

### 15 — Avviso valvole riscaldamento spente

**Cosa fa:** quando una valvola termostatica o un termostato selezionato passa da **riscaldamento attivo** (`heating`) a **spento** (`off`) e rimane in questo stato per almeno **5 secondi**, invia una notifica allo smartphone. Nessuna condizione aggiuntiva.

**Requisiti:** almeno una valvola termostatica o un termostato con entità `climate` che esponga l'attributo `hvac_action` con valori `heating` e `off`, e uno smartphone con l'app ufficiale Home Assistant.

**Titolo precompilato:** «Riscaldamento»

**Messaggio precompilato:** «Le valvole hanno terminato il riscaldamento»

[![Importa in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fclima%2Favviso_riscaldamento_spento.yaml)

**[Importa direttamente in Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fclima%2Favviso_riscaldamento_spento.yaml)**

**Importazione alternativa:** copia il **[link GitHub dell'automazione](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/clima/avviso_riscaldamento_spento.yaml)** e incollalo in **Impostazioni → Automazioni e scene → Progetti → Importa progetto**.

> **Nota:** Alcuni dispositivi passano da `heating` a `idle` invece di `off`: in tal caso questa automazione non invia la notifica. Controlla gli stati effettivamente esposti dalla tua integrazione. La notifica riflette lo stato riportato da Home Assistant, non necessariamente la posizione fisica della valvola.

### 16 — Riduci riscaldamento quando sei fuori casa (lun–ven)

**Cosa fa:** quando la persona selezionata risulta **fuori casa per 5 minuti**, dal **lunedì al venerdì** tra le **00:00 e le 23:59**, applica ai termostati il preset configurato nell'editor. Nell'esempio viene usato **Fuori casa**. Nessun ripristino automatico al rientro.

**Requisiti:** un'entità `person` configurata e uno o più termostati che supportino le modalità preimpostate. Il nome del preset dipende dall'integrazione.

[![Importa in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Friscaldamento%2Friduci_riscaldamento_assenza_feriali.yaml)

**[Importa direttamente in Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Friscaldamento%2Friduci_riscaldamento_assenza_feriali.yaml)**

**Importazione alternativa:** copia il **[link GitHub dell'automazione](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/riscaldamento/riduci_riscaldamento_assenza_feriali.yaml)** e incollalo in **Impostazioni → Automazioni e scene → Progetti → Importa progetto**.

> **Nota:** Nella configurazione dell'automazione seleziona la persona e aggiungi l'azione per i termostati con il preset supportato. Il tracciamento GPS può generare falsi stati di assenza; il ritardo di 5 minuti non li elimina completamente. La condizione termina alle 23:59, come nell'esempio. Nessun intervento viene eseguito quando si torna a casa.

### 17 — Riattiva riscaldamento quando rientri a casa (lun–ven)

**Cosa fa:** quando la persona selezionata risulta **in casa per 15 secondi**, dal **lunedì al venerdì** tra le **00:00 e le 23:59**, imposta sui termostati il preset scelto nell'editor. Nell'esempio è **Pianificazione**. Nessuna ulteriore condizione.

**Requisiti:** un'entità `person` configurata e uno o più termostati compatibili con le modalità preimpostate. Il nome del preset dipende dall'integrazione.

[![Importa in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Friscaldamento%2Fripristina_riscaldamento_rientro_feriali.yaml)

**[Importa direttamente in Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Friscaldamento%2Fripristina_riscaldamento_rientro_feriali.yaml)**

**Importazione alternativa:** copia il **[link GitHub dell'automazione](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/riscaldamento/ripristina_riscaldamento_rientro_feriali.yaml)** e incollalo in **Impostazioni → Automazioni e scene → Progetti → Importa progetto**.

> **Nota:** Se usata insieme ad AUTO 16, seleziona la stessa entità persona e gli stessi termostati. La presenza GPS può generare falsi rilevamenti: 15 secondi non garantiscono che il rientro sia reale. La modalità Pianificazione deve essere supportata dal termostato. L'automazione applica un preset specifico, non recupera automaticamente quello precedente.

### 18 — Riduci riscaldamento fuori casa nel weekend

**Cosa fa:** quando esci di casa durante il weekend e risulti assente per almeno **2 minuti**, Home Assistant imposta automaticamente i termostati sulla modalità selezionata e invia una notifica allo smartphone.

**Requisiti:** un'entità persona configurata in Home Assistant, uno o più termostati compatibili con le modalità preimpostate e uno smartphone con l'app Home Assistant.

**Titolo precompilato:** «Riscaldamento sospeso»

**Messaggio precompilato:** «Il riscaldamento è stato fermato perché nel weekend non sei a casa»

[![Importa in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Friscaldamento%2Friduci_riscaldamento_assenza_weekend.yaml)

**[Importa direttamente in Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Friscaldamento%2Friduci_riscaldamento_assenza_weekend.yaml)**

**Importazione alternativa:** copia il **[link GitHub dell'automazione](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/riscaldamento/riduci_riscaldamento_assenza_weekend.yaml)** e incollalo in **Impostazioni → Automazioni e scene → Progetti → Importa progetto**.

> **Nota:** il rilevamento della presenza dipende dall'aggiornamento della posizione e può generare falsi rilevamenti. La modalità selezionata deve essere supportata dai termostati. L'automazione non ripristina automaticamente il riscaldamento quando rientri a casa.

### 19 — Ripristina programmazione riscaldamento nel weekend

**Cosa fa:** quando rientri a casa durante il weekend e risulti presente per almeno **5 minuti**, Home Assistant ripristina automaticamente la modalità **Pianificazione** sui termostati selezionati, riattivando la normale gestione programmata del riscaldamento.

**Requisiti:** un'entità persona configurata in Home Assistant e uno o più termostati compatibili con le modalità preimpostate.

[![Importa in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Friscaldamento%2Fripristina_riscaldamento_rientro_weekend.yaml)

**[Importa direttamente in Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Friscaldamento%2Fripristina_riscaldamento_rientro_weekend.yaml)**

**Importazione alternativa:** copia il **[link GitHub dell'automazione](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/riscaldamento/ripristina_riscaldamento_rientro_weekend.yaml)** e incollalo in **Impostazioni → Automazioni e scene → Progetti → Importa progetto**.

> **Nota:** il rilevamento della presenza dipende dagli aggiornamenti della posizione e può generare falsi rilevamenti. La modalità Pianificazione deve essere supportata dai termostati. L'automazione applica il preset selezionato, senza recuperare necessariamente la modalità precedentemente attiva.

### 20 — Apri Home Assistant su tablet con rilevamento presenza

**Cosa fa:** quando il sensore di presenza selezionato rileva occupazione per **1 secondo**, Home Assistant verifica che la persona o il dispositivo scelto risulti **in casa**. Se la condizione è soddisfatta, invia una notifica al tablet con messaggio **Apri** e titolo **Dashboard**.

**Funzionamento:**

1. Rileva la presenza tramite il sensore configurato.
2. Verifica che la persona o il dispositivo selezionato sia in casa.
3. Invia una notifica al tablet.

**Requisiti:** un sensore di presenza compatibile, una persona o un dispositivo tracciato come presente in casa e un tablet configurato per ricevere notifiche tramite Home Assistant.

**Titolo precompilato:** «Dashboard»

**Messaggio precompilato:** «Apri»

[![Importa in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fdashboard%2Fapri_home_assistant_tablet.yaml)

**[Importa direttamente in Home Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fluigi-regolo%2Fautomazioni-home-assistant%2Fblob%2Fmain%2Fautomations%2Fdashboard%2Fapri_home_assistant_tablet.yaml)**

**Importazione alternativa:** copia il **[link GitHub dell'automazione](https://github.com/luigi-regolo/automazioni-home-assistant/blob/main/automations/dashboard/apri_home_assistant_tablet.yaml)** e incollalo in **Impostazioni → Automazioni e scene → Progetti → Importa progetto**.

> **Nota:** questa automazione invia una notifica al tablet. L'apertura effettiva dell'app o della dashboard dipende dalla configurazione del tablet e dell'app Home Assistant sul dispositivo; la notifica da sola non garantisce l'apertura automatica.

## Aggiornamenti e sicurezza

- I file sono esempi generici: non contengono credenziali, indirizzi o ID delle entità di una casa reale.
- Le modifiche su GitHub non aggiornano automaticamente i progetti già importati. Usa **Reimporta progetto** solo dopo aver valutato eventuali incompatibilità.

## Licenza

[MIT](LICENSE)
