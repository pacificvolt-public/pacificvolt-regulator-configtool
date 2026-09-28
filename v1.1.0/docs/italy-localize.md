# ConfigTool - Italian (it-IT) translation review

The complete translation, grouped by where the text appears in the tool. Edit the
**Translation** column directly, or put a replacement in **Your correction**, and
hand the file back. For anything with markup or long text, the spreadsheet next to
this file is easier to work in.

- Strings translated: **876** - the whole of the live user interface
- Strings still untranslated: **0**
- Rows carrying a question from me: **72**
- Generated from `translations/ConfigTool_it_IT.ts`

This is a machine first pass awaiting a native Italian speaker. Italian technical usage keeps a number of English terms untranslated - *firmware*, *download*, *reset*, *log* - and the first pass follows that rather than forcing a calque. Where it chose one way over the other the row carries a note.

Some strings are translated to themselves on purpose. Firmware fault codes (`CB`,
`OT`, `W1`, `P+`, `RAMP`...), baud rate values and Qt Designer object names
(`toolBar`, `MainWindow`) are identifiers rather than prose - translating them
would break the match against what the regulator actually sends.

A few strings carry HTML, shown here as literal text rather than rendered. `\n`
marks a real line break, the same convention the .tsv uses.

## About and licence dialogs (9)

| Original (English) | Translation (it-IT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `&3rd Party Licenses` | &amp;Licenze di terze parti |  |  |
| `&About Qt` | Informazioni su &amp;Qt |  |  |
| `<h3>%1 - 3rd Party Licenses</h3>` | &lt;h3&gt;%1 - Licenze di terze parti&lt;/h3&gt; |  |  |
| `<h3>About %1</h3><p>%1</p><p>Version: %2</p><p>Build Date: %3</p><p>%4</p>` | &lt;h3&gt;Informazioni su %1&lt;/h3&gt;&lt;p&gt;%1&lt;/p&gt;&lt;p&gt;Versione: %2&lt;/p&gt;&lt;p&gt;Data di compilazione: %3&lt;/p&gt;&lt;p&gt;%4&lt;/p&gt; |  |  |
| `<p>%1 uses multiple 3rd Party software mostly covered under the Qt distribution</p><p>However the following license(s) are not part of Qt.</p><hr style="width:50%;text-align:left;margin-left:0"><table border="1"><tr><th>Company</th><th>Product</th><th>License</th><th>Source Location</th><th>Patches</th></tr>` | &lt;p&gt;%1 utilizza diversi software di terze parti, per la maggior parte coperti dalla distribuzione Qt&lt;/p&gt;&lt;p&gt;Tuttavia le licenze seguenti non fanno parte di Qt.&lt;/p&gt;&lt;hr style="width:50%;text-align:left;margin-left:0"&gt;&lt;table border="1"&gt;&lt;tr&gt;&lt;th&gt;Azienda&lt;/th&gt;&lt;th&gt;Prodotto&lt;/th&gt;&lt;th&gt;Licenza&lt;/th&gt;&lt;th&gt;Posizione dei sorgenti&lt;/th&gt;&lt;th&gt;Patch&lt;/th&gt;&lt;/tr&gt; | LENGTH: the five table headers land in a narrow HTML table; "Posizione dei sorgenti" is the one most likely to wrap. |  |
| `<p>Is a tool to help configure %1's Voltage Regulators.</p><p>For more information, please visit <a href="%2">%3</a>.</p><p>For the default Advanced and Admin passwords, contact <a href="mailto:%4">%4</a>.</p><hr style="width:50%;text-align:left;margin-left:0"><p>%5</p>` | &lt;p&gt;È uno strumento per la configurazione dei regolatori di tensione di %1.&lt;/p&gt;&lt;p&gt;Per maggiori informazioni, visitare &lt;a href="%2"&gt;%3&lt;/a&gt;.&lt;/p&gt;&lt;p&gt;Per le password predefinite Avanzato e Admin, contattare &lt;a href="mailto:%4"&gt;%4&lt;/a&gt;.&lt;/p&gt;&lt;hr style="width:50%;text-align:left;margin-left:0"&gt;&lt;p&gt;%5&lt;/p&gt; |  |  |
| `3rd Party Licenses` | Licenze di terze parti |  |  |
| `About %1` | Informazioni su %1 |  |  |
| `This tool supports the following LVR firmware versions:<br>LVR30 %1, LVR50 %2` | Questo strumento supporta le seguenti versioni del firmware LVR:&lt;br&gt;LVR30 %1, LVR50 %2 |  |  |

## Bluetooth - Available Regulators and pairing (48)

| Original (English) | Translation (it-IT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `%1 configured connection(s)` | %1 connessione/i configurata/e | CHECK: Italian has no neat "(s)" form. I used the slash convention; if the reviewer prefers, "Connessioni configurate: %1" avoids the problem entirely but changes the phrase shape. |  |
| `An error has occurred in the bluetooth system` | Si è verificato un errore nel sistema Bluetooth |  |  |
| `An unknown error has occurred.` | Si è verificato un errore sconosciuto. |  |  |
| `Authorize Regulator` | Autorizza regolatore |  |  |
| `Available Regulators` | Regolatori disponibili |  |  |
| `Connecting to regulator '%1' timed out. Check your connection - the regulator may be out of range or turned off.` | Timeout della connessione al regolatore '%1'. Controllare il collegamento - il regolatore potrebbe essere fuori portata o spento. |  |  |
| `Could not find a bluetooth adapter. ` | Impossibile trovare un adattatore Bluetooth.  | CHECK: trailing space kept - this string is concatenated with a following one at runtime. |  |
| `currently connected` | attualmente connesso |  |  |
| `Device discovery is not possible or implemented on the current platform.` | La ricerca dei dispositivi non è possibile o non è implementata su questa piattaforma. |  |  |
| `Device Name` | Nome dispositivo |  |  |
| `Does the following PIN match the one shown on the device you are pairing?: %1` | Il PIN seguente corrisponde a quello mostrato sul dispositivo che si sta associando?: %1 |  |  |
| `Enter a PIN to pair with:` | Immettere un PIN per l'associazione: |  |  |
| `Error in Bluetooth connection` | Errore nella connessione Bluetooth |  |  |
| `Error in pairing` | Errore di associazione | TERM: pairing = "associazione" (the Windows Italian form, used consistently here); Android Italian says "accoppiamento". Please confirm which one Italian field engineers expect on a Bluetooth dialog. |  |
| `Finished` | Completata | GENDER: agrees with "la ricerca" (the Bluetooth scan), which is what this status reports. If the string is ever reused for something masculine it would need "Completato". |  |
| `Limit the list to shipped regulators, which are all named "PV...". Uncheck to also show bench and test units, which often are not. Non-regulators are never listed either way.` | Limita l'elenco ai regolatori spediti, il cui nome inizia sempre con "PV...". Deselezionare per mostrare anche le unità da banco e di prova, che spesso non seguono questa regola. Le apparecchiature che non sono regolatori non vengono mai elencate. | LENGTH: long tooltip, roughly 15% longer than the English. Worth hovering once to check it wraps instead of running off the screen. |  |
| `Missing permissions` | Autorizzazioni mancanti |  |  |
| `No Bluetooth Adapter Found` | Nessun adattatore Bluetooth trovato |  |  |
| `One of the requested discovery methods is not supported by the current platform.` | Uno dei metodi di ricerca richiesti non è supportato da questa piattaforma. |  |  |
| `Pair Device` | Associa dispositivo |  |  |
| `Pair Device?` | Associare il dispositivo? |  |  |
| `Pair Regulator` | Associa regolatore |  |  |
| `paired` | associato |  |  |
| `Paired?` | Associato? |  |  |
| `Permissions are needed to use Bluetooth. Please grant the permissions to this application in the system settings.` | Per utilizzare il Bluetooth sono necessarie alcune autorizzazioni. Concedere le autorizzazioni a questa applicazione nelle impostazioni di sistema. |  |  |
| `Please enter this PIN on the device you are pairing with: %1` | Immettere questo PIN sul dispositivo che si sta associando: %1 |  |  |
| `PV Filter` | Filtro PV |  |  |
| `Re-Scan` | Cerca di nuovo |  |  |
| `Remove %1 regulator(s)?` | Rimuovere %1 regolatore/i? | CHECK: same "(s)" problem as the previous row - slash convention used for consistency. |  |
| `Remove Regulators` | Rimuovi regolatori |  |  |
| `Remove the selected regulators from the list, delete their connections, and unpair them` | Rimuove i regolatori selezionati dall'elenco, ne elimina le connessioni e ne annulla l'associazione | LENGTH: tooltip on a toolbar button; noticeably longer than the English. |  |
| `Scanning for devices not previously paired.` | Ricerca di dispositivi non ancora associati. |  |  |
| `Scanning for previously connected devices and devices not previously paired.` | Ricerca di dispositivi già connessi in precedenza e di dispositivi non ancora associati. |  |  |
| `Scanning for previously connected devices.` | Ricerca di dispositivi già connessi in precedenza. |  |  |
| `Scanning...` | Ricerca in corso... |  |  |
| `Select Regulator` | Seleziona regolatore |  |  |
| `Select the Regulator to connect to.` | Selezionare il regolatore a cui connettersi. |  |  |
| `Service` | Servizio |  |  |
| `Stop Scanning` | Interrompi la ricerca |  |  |
| `The Bluetooth adaptor is powered off, power it on before doing discovery.` | L'adattatore Bluetooth è spento: accenderlo prima di avviare la ricerca. |  |  |
| `The following error occurred connecting to regulator '%1': %2. Check your connection - the regulator may be out of range or turned off.` | Si è verificato il seguente errore durante la connessione al regolatore '%1': %2. Controllare il collegamento - il regolatore potrebbe essere fuori portata o spento. |  |  |
| `The location service is turned off.Usage of Bluetooth APIs is not possible when location service is turned off.` | Il servizio di localizzazione è disattivato. Non è possibile utilizzare le API Bluetooth quando il servizio di localizzazione è disattivato. | CHECK: the English is missing the space after "turned off." - I have restored it in Italian. |  |
| `The operating system requests permissions which were not granted by the user.` | Il sistema operativo richiede autorizzazioni che non sono state concesse dall'utente. |  |  |
| `The passed local adapter address does not match the physical adapter address of any local Bluetooth device.` | L'indirizzo dell'adattatore locale indicato non corrisponde all'indirizzo fisico di alcun dispositivo Bluetooth locale. |  |  |
| `This deletes their configured connections, removes them from the Available Regulators list, and unpairs them from this computer. Any open connections will be closed. This cannot be undone.` | Questa operazione elimina le connessioni configurate dei regolatori, li rimuove dall'elenco Regolatori disponibili e ne annulla l'associazione con questo computer. Le connessioni aperte verranno chiuse. L'operazione non può essere annullata. |  |  |
| `Unknown Error.` | Errore sconosciuto. |  |  |
| `Unpair Regulator` | Annulla associazione regolatore | LENGTH: doubles the English on what looks like a narrow button. "Dissocia regolatore" is a shorter fallback if it clips. |  |
| `Writing or reading from the device resulted in an error.` | La scrittura o la lettura sul dispositivo ha generato un errore. |  |  |

## Clock and time zone dialogs (13)

| Original (English) | Translation (it-IT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `...` | ... |  |  |
| `...` | ... |  |  |
| `Current Time` | Ora corrente |  |  |
| `Custom Selected Time Zone` | Fuso orario personalizzato |  |  |
| `Custom Time` | Ora personalizzata |  |  |
| `Local Computer's Time Zone` | Fuso orario del computer locale |  |  |
| `Regulator's System Clock:` | Orologio di sistema del regolatore: |  |  |
| `Regulator:` | Regolatore: |  |  |
| `Select Time Zone` | Seleziona fuso orario |  |  |
| `Select Time Zone` | Seleziona fuso orario |  |  |
| `Set Regulator System Clock` | Imposta l'orologio di sistema del regolatore |  |  |
| `Sync` | Sincronizza |  |  |
| `UTC` | UTC |  |  |

## Command names - transcript and queue status (65)

| Original (English) | Translation (it-IT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `    Command #: %1` |     Comando n.: %1 |  |  |
| `%1.` | %1. |  |  |
| `(Re)-initialize Control Board` | (Re)inizializza la scheda di controllo |  |  |
| `, re-running command.` | , nuova esecuzione del comando. |  |  |
| `. Removing from Queue.` | . Rimozione dalla coda. |  |  |
| `Checking for Support of '%1'` | Verifica del supporto di '%1' in corso |  |  |
| `Clear Queue` | Svuota la coda |  |  |
| `cmd not supported` | comando non supportato |  |  |
| `Command '%1' failed. Please disconnect and try again.  Consider rebooting the Regulator.` | Il comando '%1' non è riuscito. Disconnettersi e riprovare. Valutare il riavvio del regolatore. |  |  |
| `Command '%1' failed. Removing from Queue.` | Il comando '%1' non è riuscito. Rimozione dalla coda. |  |  |
| `Command '%1' is not supported` | Il comando '%1' non è supportato |  |  |
| `Command '%2' timed out%1` | Timeout del comando '%2'%1 | CHECK: %1 is the sentence tail supplied by the next two rows (", nuova esecuzione del comando." / ". Rimozione dalla coda."), so it must stay at the end. |  |
| `Could not process results of command '%1'` | Impossibile elaborare i risultati del comando '%1' |  |  |
| `Custom Command` | Comando personalizzato |  |  |
| `Disable SDCard` | Disabilita la scheda SD |  |  |
| `Download File` | Scarica il file |  |  |
| `Enable Or Disable All Phases if there is a Failure in any Phase` | Abilita o disabilita tutte le fasi in caso di guasto in una fase qualsiasi | LENGTH: about 30% longer than the English in the command-queue list. |  |
| `Enable Or Disable Regulator` | Abilita o disabilita il regolatore |  |  |
| `Enable SDCard` | Abilita la scheda SD |  |  |
| `Finished downloading data for command '%1'` | Download dei dati per il comando '%1' completato |  |  |
| `Finished getting system info` | Recupero delle informazioni di sistema completato |  |  |
| `Finished Getting System Info` | Recupero delle informazioni di sistema completato |  |  |
| `Format SDCard` | Formatta la scheda SD |  |  |
| `Get Default Parameter File` | Leggi il file dei parametri predefinito |  |  |
| `Get EEPROM Contents` | Leggi il contenuto della EEPROM |  |  |
| `Get File Sizes` | Leggi le dimensioni dei file | CHECK: the Get.../Set... command family is rendered "Leggi..."/"Imposta...", the natural Italian pair for reading and writing device parameters. |  |
| `Get Parameter File` | Leggi il file dei parametri |  |  |
| `Get Phase Firmware` | Leggi il firmware di fase |  |  |
| `Get Regulator Clock` | Leggi l'orologio del regolatore |  |  |
| `Get Serial Num` | Leggi il numero di serie |  |  |
| `Get Status` | Leggi lo stato |  |  |
| `Get System Firmware` | Leggi il firmware di sistema |  |  |
| `Get System Firmware Date` | Leggi la data del firmware di sistema |  |  |
| `Get System Gain` | Leggi il guadagno di sistema |  |  |
| `Get UART Settings` | Leggi le impostazioni UART |  |  |
| `Get UART Settings via RB` | Leggi le impostazioni UART tramite RB |  |  |
| `Get UART Settings via RBAUD` | Leggi le impostazioni UART tramite RBAUD |  |  |
| `Get Voltage Calibration` | Leggi la calibrazione della tensione |  |  |
| `Reboot Regulator` | Riavvia il regolatore |  |  |
| `Regulator could not handle command '%1'` | Il regolatore non è riuscito a gestire il comando '%1' |  |  |
| `Reset Over Current Fault Lockout` | Azzera il blocco per guasto di sovracorrente | TERM: "reset" here means clearing a latched lockout, so "azzera"; where "reset" means restoring a saved state I used "ripristina". Please confirm the split reads right. |  |
| `Reset Regulator to Default Parameters` | Ripristina i parametri predefiniti del regolatore |  |  |
| `Restore Modem Power` | Ripristina l'alimentazione del modem |  |  |
| `Send Ctrl-C` | Invia Ctrl-C |  |  |
| `Send Login` | Invia login | TERM: "login"/"logoff" kept in English here because these rows name the literal protocol commands sent to the regulator. Elsewhere the connection states are translated ("Accesso in corso", "Disconnessione"). |  |
| `Send Logoff` | Invia logoff |  |  |
| `Send Password` | Invia password |  |  |
| `Set Param File` | Imposta il file dei parametri |  |  |
| `Set PIR Amperage` | Imposta la corrente PIR |  |  |
| `Set PIR Delta Voltage` | Imposta il delta di tensione PIR |  |  |
| `Set PIR Null Voltage` | Imposta la tensione nulla PIR |  |  |
| `Set PIR Time Constant` | Imposta la costante di tempo PIR |  |  |
| `Set Regulator Clock` | Imposta l'orologio del regolatore |  |  |
| `Set Regulator Password` | Imposta la password del regolatore |  |  |
| `Set Serial Number` | Imposta il numero di serie |  |  |
| `Set System Gain` | Imposta il guadagno di sistema |  |  |
| `Set Target Selection` | Imposta la selezione del target |  |  |
| `Set Target Voltage` | Imposta la tensione target |  |  |
| `Set UART 1 Baud Rate` | Imposta il baud rate della UART 1 |  |  |
| `Set UART 1 FlowControl` | Imposta il controllo di flusso della UART 1 |  |  |
| `Set UART 2 Baud Rate` | Imposta il baud rate della UART 2 |  |  |
| `Set UART 2 FlowControl` | Imposta il controllo di flusso della UART 2 |  |  |
| `Set Voltage Calibration` | Imposta la calibrazione della tensione |  |  |
| `Size of Command Queue: %1` | Dimensione della coda comandi: %1 |  |  |
| `Turn off Modem Power` | Spegni l'alimentazione del modem |  |  |

## Connected regulator window - menus, dialogs and messages (149)

| Original (English) | Translation (it-IT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `    Comm Port: %1` |     Porta di comunicazione: %1 |  |  |
| `    IP Address: %1\n    Domain Name: %2\n    Port: %3` |     Indirizzo IP: %1\n    Nome di dominio: %2\n    Porta: %3 |  |  |
| ` - Regulator: %1` |  - Regolatore: %1 |  |  |
| ` - Transcript` |  - Trascrizione |  |  |
| ` Reset Over Current Fault Lockout` |  Azzera il blocco per guasto di sovracorrente | LENGTH: leading space suggests a toolbar button; this is about 60% longer than the English. "Azzera blocco sovracorrente" is a shorter fallback. |  |
| `%1` | %1 |  |  |
| `&Disconnect` | &amp;Disconnetti |  |  |
| `&Regulator` | &amp;Regolatore |  |  |
| `&Settings` | &amp;Impostazioni |  |  |
| `<br/>Would you like to reconnect?` | &lt;br/&gt;Riconnettersi? |  |  |
| `'%1' is a name Windows reserves and cannot be used in a file name.` | '%1' è un nome riservato da Windows e non può essere usato in un nome di file. |  |  |
| `(Re-)Initialize Regulator Control Board` | (Re)inizializza la scheda di controllo del regolatore |  |  |
| `(Re-)initialize the Control Board...` | (Re)inizializza la scheda di controllo... |  |  |
| `(Re-)initialize the control board...` | (Re)inizializza la scheda di controllo... |  |  |
| `1=Fast` | 1=Rapido |  |  |
| `A timeout error occurred` | Si è verificato un errore di timeout |  |  |
| `About...` | Informazioni... |  |  |
| `Administration Mode` | Modalità di amministrazione |  |  |
| `Administration Mode` | Modalità di amministrazione |  |  |
| `Advanced Mode` | Modalità avanzata |  |  |
| `All Phases Disabled on Failure in Any Phase?` | Disabilitare tutte le fasi in caso di guasto in una fase qualsiasi? | LENGTH: checkbox label, about 40% longer than the English. |  |
| `An error occurred while attempting to open an already opened device by another process or a user not having enough permission and credentials to open.` | Si è verificato un errore durante il tentativo di apertura di un dispositivo già aperto da un altro processo o da un utente privo di autorizzazioni e credenziali sufficienti. |  |  |
| `An error occurred while attempting to open an already opened device in this object.` | Si è verificato un errore durante il tentativo di apertura di un dispositivo già aperto in questo oggetto. |  |  |
| `An error occurred while attempting to open an non-existing device.` | Si è verificato un errore durante il tentativo di apertura di un dispositivo inesistente. |  |  |
| `An I/O error occurred when a resource becomes unavailable, e.g. when the device is unexpectedly removed from the system.` | Si è verificato un errore di I/O per indisponibilità di una risorsa, ad esempio quando il dispositivo viene rimosso inaspettatamente dal sistema. |  |  |
| `An I/O error occurred while reading the data.` | Si è verificato un errore di I/O durante la lettura dei dati. |  |  |
| `An I/O error occurred while writing the data.` | Si è verificato un errore di I/O durante la scrittura dei dati. |  |  |
| `An unidentified error occurred.` | Si è verificato un errore non identificato. |  |  |
| `Are you sure you wish to continue?` | Continuare? |  |  |
| `Automatically Refresh Status?` | Aggiornare automaticamente lo stato? |  |  |
| `Available` | Disponibile |  |  |
| `Available` | Disponibile |  |  |
| `Available` | Disponibile |  |  |
| `Bluetooth` | Bluetooth |  |  |
| `Bluetooth Regulator Unauthorized` | Regolatore Bluetooth non autorizzato |  |  |
| `Bluetooth Regulator Unpaired` | Regolatore Bluetooth non associato |  |  |
| `Can not set UART settings while connected via Ethernet` | Impossibile modificare le impostazioni UART durante una connessione Ethernet |  |  |
| `Change Time Zone...` | Cambia fuso orario... |  |  |
| `Clear Command Queue` | Svuota la coda comandi |  |  |
| `Clear Transcript` | Cancella la trascrizione |  |  |
| `Close Connection?` | Chiudere la connessione? |  |  |
| `COM Port` | Porta COM |  |  |
| `Comm Port not Found` | Porta di comunicazione non trovata |  |  |
| `Command Queue Status` | Stato della coda comandi |  |  |
| `Connect` | Connetti |  |  |
| `Connection '%1' was lost or disconnected.` | La connessione '%1' è stata persa o interrotta. |  |  |
| `Continue` | Continua |  |  |
| `Continue` | Continua |  |  |
| `Copy Transcript to Clipboard` | Copia la trascrizione negli appunti |  |  |
| `Debug` | Debug |  |  |
| `Debug Logging...` | Log di debug... |  |  |
| `Delete Data Logs...` | Elimina i log dei dati... |  |  |
| `Delete Fault Log...` | Elimina il log dei guasti... |  |  |
| `Disable Advanced Mode` | Disabilita la modalità avanzata |  |  |
| `Disable Regulator` | Disabilita il regolatore |  |  |
| `Disable SD Card` | Disabilita la scheda SD |  |  |
| `Download from SD Card` | Scarica dalla scheda SD |  |  |
| `Download from SD Card...` | Scarica dalla scheda SD... |  |  |
| `Enable Advanced Mode` | Abilita la modalità avanzata |  |  |
| `Enable Regulator` | Abilita il regolatore |  |  |
| `Enable SD Card` | Abilita la scheda SD |  |  |
| `Enter New Regulator Password` | Immettere la nuova password del regolatore |  |  |
| `Enter Regulator Password` | Immettere la password del regolatore |  |  |
| `Enter System Gain` | Immettere il guadagno di sistema |  |  |
| `Error` | Errore |  |  |
| `Error Communicating with Regulator` | Errore di comunicazione con il regolatore |  |  |
| `ERROR: %1` | ERRORE: %1 |  |  |
| `Fast Rate Data` | Dati a frequenza rapida |  |  |
| `Format SD Card...` | Formatta la scheda SD... |  |  |
| `Formatting erases the SD card and cannot be undone.` | La formattazione cancella la scheda SD e non può essere annullata. |  |  |
| `Help` | Aiuto |  |  |
| `Host '%1' was not found. Please check the host name and port settings.` | Host '%1' non trovato. Verificare il nome host e le impostazioni della porta. |  |  |
| `Initialize System Information on Login?` | Inizializzare le informazioni di sistema all'accesso? |  |  |
| `Medium Rate Data` | Dati a frequenza media |  |  |
| `Name cannot be used` | Nome non utilizzabile |  |  |
| `Name for this regulator:\n\nThis name is stored by the Config Tool only. It is not written to the\nregulator and is not read back from it, and it is lost if the regulator\nis removed from the saved list.\n\nIt is used in the names of the files downloaded from this regulator, so\nit cannot contain characters that a file name cannot hold.` | Nome di questo regolatore:\n\nQuesto nome viene memorizzato solo dal Config Tool. Non viene scritto nel\nregolatore né riletto da esso e viene perso se il regolatore\nviene rimosso dall'elenco salvato.\n\nViene usato nei nomi dei file scaricati da questo regolatore, quindi\nnon può contenere caratteri non ammessi in un nome di file. |  |  |
| `Network not Reachable` | Rete non raggiungibile |  |  |
| `No SD File Data` | Nessun dato sui file della scheda SD |  |  |
| `No SD file data available. Click on the green System Info arrows.` | Nessun dato sui file della scheda SD disponibile. Fare clic sulle frecce verdi delle informazioni di sistema. |  |  |
| `Parameter File...` | File dei parametri... |  |  |
| `Password Required` | Password richiesta |  |  |
| `Power cycle external modem at J2-2` | Spegni e riaccendi il modem esterno su J2-2 | CHECK: "power cycle" has no one-word Italian verb; I used "spegni e riaccendi". "Riavvia l'alimentazione del modem esterno su J2-2" is the alternative. |  |
| `Power Interactive Regulation Settings...` | Impostazioni della regolazione interattiva di potenza... | LENGTH: long menu item; roughly 40% longer than the English. |  |
| `Quit` | Esci |  |  |
| `Quit` | Esci |  |  |
| `Reboot Regulator` | Riavvia il regolatore |  |  |
| `Reboot Regulator...` | Riavvia il regolatore... |  |  |
| `Reconnect` | Riconnetti |  |  |
| `Refresh` | Aggiorna |  |  |
| `Refresh All` | Aggiorna tutto |  |  |
| `Refresh Gain Values` | Aggiorna i valori di guadagno |  |  |
| `Refresh Parameter File` | Aggiorna il file dei parametri |  |  |
| `Refresh Regulator Clock` | Aggiorna l'orologio del regolatore |  |  |
| `Refresh Regulator Information` | Aggiorna le informazioni sul regolatore |  |  |
| `Refresh SD Card Information` | Aggiorna le informazioni sulla scheda SD |  |  |
| `Refresh UART Settings` | Aggiorna le impostazioni UART |  |  |
| `Refresh Voltage and Fault Status` | Aggiorna lo stato di tensione e guasti |  |  |
| `Refresh Voltage Calibration Info` | Aggiorna le info di calibrazione della tensione |  |  |
| `Regulator` | Regolatore |  |  |
| `Regulator &Settings` | &amp;Impostazioni regolatore |  |  |
| `Regulator '%1' - %2` | Regolatore '%1' - %2 |  |  |
| `Regulator has logged off due to no command activity. Please reconnect and activate auto refresh.` | Il regolatore ha chiuso la sessione per assenza di attività di comando. Riconnettersi e attivare l'aggiornamento automatico. |  |  |
| `Regulator Logged Off` | Sessione chiusa sul regolatore |  |  |
| `Regulator:` | Regolatore: |  |  |
| `Remote` | Remoto |  |  |
| `Reset Over Current Fault Lockout` | Azzera il blocco per guasto di sovracorrente | TERM: "reset" here means clearing a latched lockout, so "azzera"; where "reset" means restoring a saved state I used "ripristina". Please confirm the split reads right. |  |
| `Reset Regulator to Default Parameters` | Ripristina i parametri predefiniti del regolatore |  |  |
| `Reset Regulator to Default Parameters...` | Ripristina i parametri predefiniti del regolatore... |  |  |
| `Save Transcript...` | Salva la trascrizione... |  |  |
| `SD Card` | Scheda SD |  |  |
| `SD Card File Sizes` | Dimensioni dei file della scheda SD |  |  |
| `SD Card Has Error` | La scheda SD presenta un errore |  |  |
| `SD Card is Disabled` | La scheda SD è disabilitata |  |  |
| `Session Timing Out` | Sessione in scadenza |  |  |
| `Set Regulator Name` | Imposta il nome del regolatore |  |  |
| `Set Regulator Name...` | Imposta il nome del regolatore... |  |  |
| `Set Regulator's Password...` | Imposta la password del regolatore... |  |  |
| `Set Serial Number...` | Imposta il numero di serie... |  |  |
| `Set System Clock...` | Imposta l'orologio di sistema... |  |  |
| `Set System Gain...` | Imposta il guadagno di sistema... |  |  |
| `Slow Rate Data` | Dati a frequenza lenta |  |  |
| `Slow=9` | Lento=9 |  |  |
| `System Gain:` | Guadagno di sistema: |  |  |
| `System not initialized` | Sistema non inizializzato |  |  |
| `The connection was refused by the regulator '%1'. Make sure the regulator is running and confirm the host name and port settings.` | La connessione è stata rifiutata dal regolatore '%1'. Assicurarsi che il regolatore sia in funzione e verificare il nome host e le impostazioni della porta. |  |  |
| `The following error occurred connecting to regulator '%1': %2.` | Si è verificato il seguente errore durante la connessione al regolatore '%1': %2. |  |  |
| `The name cannot be empty.` | Il nome non può essere vuoto. |  |  |
| `The name cannot contain %1, because it is used in the names of the files downloaded from this regulator.` | Il nome non può contenere %1, perché viene usato nei nomi dei file scaricati da questo regolatore. |  |  |
| `The name cannot contain control characters, because it is used in the names of the files downloaded from this regulator.` | Il nome non può contenere caratteri di controllo, perché viene usato nei nomi dei file scaricati da questo regolatore. |  |  |
| `The name cannot end with a '.'` | Il nome non può terminare con '.' |  |  |
| `The requested device operation is not supported or prohibited by the running operating system.` | L'operazione richiesta sul dispositivo non è supportata o è vietata dal sistema operativo in esecuzione. |  |  |
| `This error occurs when an operation is executed that can only be successfully performed if the device is open.` | Questo errore si verifica quando viene eseguita un'operazione che può essere completata solo con il dispositivo aperto. |  |  |
| `This session has been idle and is about to time out.\n\nThe regulator will be disconnected in %1 seconds unless you continue.` | La sessione è rimasta inattiva e sta per scadere.\n\nIl regolatore verrà disconnesso tra %1 secondi se non si continua. |  |  |
| `Time Stamp Transcript?` | Marcare la trascrizione con l'orario? |  |  |
| `toolBar` | toolBar |  |  |
| `Transcript` | Trascrizione |  |  |
| `UART Settings...` | Impostazioni UART... |  |  |
| `USB` | USB |  |  |
| `View` | Visualizza |  |  |
| `View EEPROM Contents...` | Visualizza il contenuto della EEPROM... |  |  |
| `View Regulator Information?` | Visualizzare le informazioni sul regolatore? |  |  |
| `View Regulator Status?` | Visualizzare lo stato del regolatore? |  |  |
| `View Transcript in Separate Window?` | Visualizzare la trascrizione in una finestra separata? |  |  |
| `View Transcript?` | Visualizzare la trascrizione? |  |  |
| `Voltage Calibration Settings...` | Impostazioni di calibrazione della tensione... |  |  |
| `Voltage Controller Settings...` | Impostazioni del controllore di tensione... | TERM: "controller" rendered "controllore" to keep it distinct from "regolatore" (the unit itself). Confirm this is what Italian utility engineers say. |  |
| `WARNING: %1` | AVVISO: %1 |  |  |
| `Would you like to disconnect from '%1'` | Disconnettersi da '%1' |  |  |
| `Would you like to revert to Basic Mode?` | Tornare alla modalità base? |  |  |

## Connected window - status bar (10)

| Original (English) | Translation (it-IT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `Auto Refresh` | Aggiornamento automatico |  |  |
| `Auto Refresh` | Aggiornamento automatico |  |  |
| `Connection` | Connessione |  |  |
| `Connection` | Connessione |  |  |
| `Faults` | Guasti |  |  |
| `Faults` | Guasti |  |  |
| `Regulating` | In regolazione |  |  |
| `Regulating` | In regolazione |  |  |
| `Regulator` | Regolatore |  |  |
| `Regulator` | Regolatore |  |  |

## Connection editor dialog (22)

| Original (English) | Translation (it-IT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `...` | ... |  |  |
| `000.000.000.000;_` | 000.000.000.000;_ |  |  |
| `A Bluetooth Device must be selected.` | È necessario selezionare un dispositivo Bluetooth. |  |  |
| `Comm Port must be set.` | È necessario impostare la porta di comunicazione. |  |  |
| `Comm Port:` | Porta di comunicazione: |  |  |
| `Direct Bluetooth Connection` | Connessione Bluetooth diretta |  |  |
| `Edit/Create Regulator Connection` | Modifica/crea connessione al regolatore |  |  |
| `Host Name` | Nome host |  |  |
| `Host Name:` | Nome host: |  |  |
| `Invalid IP Address: %1` | Indirizzo IP non valido: %1 |  |  |
| `Invalid Port: %1` | Porta non valida: %1 |  |  |
| `IP Address` | Indirizzo IP |  |  |
| `IP Address or Hostname must be set.` | È necessario impostare l'indirizzo IP o il nome host. |  |  |
| `IP Address:` | Indirizzo IP: |  |  |
| `Is USB/RS-232 Serial Port (Not Bluetoooth)?` | È una porta seriale USB/RS-232 (non Bluetooth)? | CHECK: the English misspells "Bluetoooth"; corrected in the Italian. |  |
| `Please select a local or remote connection` | Selezionare una connessione locale o remota |  |  |
| `Port:` | Porta: |  |  |
| `Regulator name must be set.` | È necessario impostare il nome del regolatore. |  |  |
| `Regulator Name:` | Nome del regolatore: |  |  |
| `Selected Device:` | Dispositivo selezionato: |  |  |
| `Serial Port Connection` | Connessione tramite porta seriale |  |  |
| `TCP/IP Connection:` | Connessione TCP/IP: |  |  |

## Connection status and errors (19)

| Original (English) | Translation (it-IT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `%1 commands in a row went unanswered` | %1 comandi consecutivi non hanno ricevuto risposta |  |  |
| `115.2k` | 115.2k |  |  |
| `230.4k` | 230.4k |  |  |
| `38.4k` | 38.4k |  |  |
| `57.6k` | 57.6k |  |  |
| `Cannot log back in to the regulator. Status polling has stopped - please disconnect and reconnect.` | Impossibile accedere di nuovo al regolatore. Il polling dello stato è stato interrotto - disconnettersi e riconnettersi. |  |  |
| `Cannot make sense of the regulator's replies. Status polling has stopped - please disconnect and reconnect.` | Non è possibile interpretare le risposte del regolatore. Il polling dello stato è stato interrotto - disconnettersi e riconnettersi. |  |  |
| `Hardware Flow Control` | Controllo di flusso hardware |  |  |
| `No Flow Control` | Nessun controllo di flusso |  |  |
| `nothing has come back for %1 seconds` | nessuna risposta da %1 secondi |  |  |
| `Paired` | Associato |  |  |
| `Paired with Authorization` | Associato con autorizzazione |  |  |
| `Serial Port` | Porta seriale |  |  |
| `Software Flow Control` | Controllo di flusso software |  |  |
| `The connection to regulator '%1' has been lost - %2. Check the link and reconnect. If the regulator is still holding the previous session, reconnecting can take a few minutes.` | La connessione al regolatore '%1' è stata persa - %2. Controllare il collegamento e riconnettersi. Se il regolatore mantiene ancora la sessione precedente, la riconnessione può richiedere alcuni minuti. |  |  |
| `the login was not answered` | l'accesso non ha ricevuto risposta |  |  |
| `The regulator has stopped responding - %1 commands in a row went unanswered.` | Il regolatore ha smesso di rispondere - %1 comandi consecutivi non hanno ricevuto risposta. |  |  |
| `The regulator is responding again.` | Il regolatore risponde di nuovo. |  |  |
| `Unpaired` | Non associato |  |  |

## Debug logging dialog (13)

| Original (English) | Translation (it-IT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `<Filter>` | &lt;Filtro&gt; |  |  |
| `...` | ... |  |  |
| `Append to Log File?` | Aggiungere in coda al file di log? |  |  |
| `Check All` | Seleziona tutto |  |  |
| `Log File` | File di log |  |  |
| `Log File:` | File di log: |  |  |
| `Log Files (*.log);;All Files (*.*)` | File di log (*.log);;Tutti i file (*.*) |  |  |
| `Logging Categories:` | Categorie di log: |  |  |
| `Logging Category` | Categoria di log |  |  |
| `Select Logging Categories` | Seleziona le categorie di log |  |  |
| `Show Qt Categories?` | Mostrare le categorie Qt? |  |  |
| `Uncheck All` | Deseleziona tutto |  |  |
| `Uncheck All Debug` | Deseleziona tutti i debug |  |  |

## EEPROM contents viewer (9)

| Original (English) | Translation (it-IT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `<ADDRESS>` | &lt;INDIRIZZO&gt; |  |  |
| `<VALUE>` | &lt;VALORE&gt; |  |  |
| `0x00 0 ` | 0x00 0  |  |  |
| `0x00000000 ` | 0x00000000  |  |  |
| `Address:` | Indirizzo: |  |  |
| `EEPROM Contents` | Contenuto della EEPROM |  |  |
| `EEPROM Contents:` | Contenuto della EEPROM: |  |  |
| `EEPROM Contents: Loading...` | Contenuto della EEPROM: caricamento in corso... |  |  |
| `Value:` | Valore: |  |  |

## File download progress (20)

| Original (English) | Translation (it-IT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `%1 of %2%3 (%4%)` | %1 di %2%3 (%4%) |  |  |
| `%1%2` | %1%2 |  |  |
| `%1h %2m` | %1 h %2 min |  |  |
| `%1m %2s` | %1 min %2 s | CHECK: "min" is the Italian abbreviation for minutes; "m" alone reads as metres. A space before each unit, per SI and Italian convention. |  |
| `%1s` | %1 s |  |  |
| `0.%1 seconds` | 0,%1 secondi |  |  |
| `Abort Download` | Interrompi il download |  |  |
| `About %1 remaining` | Tempo rimanente: circa %1 | AGREEMENT: the English "About %1 remaining" needs an adjective agreeing with %1, which is a runtime duration string ("meno di un secondo", "5 min 3 s"). I restructured to "Tempo rimanente: circa %1" so nothing has to agree. |  |
| `Could not open file` | Impossibile aprire il file |  |  |
| `Could not open file '%1' for write.  Please check Permissions` | Impossibile aprire il file '%1' in scrittura. Verificare le autorizzazioni |  |  |
| `Downloading File` | Download del file in corso |  |  |
| `Downloading File '%1'` | Download del file '%1' in corso |  |  |
| `Downloading file '%1'` | Download del file '%1' in corso |  |  |
| `Error downloading file` | Errore durante il download del file |  |  |
| `Finishing up...` | Completamento in corso... |  |  |
| `less than a second` | meno di un secondo |  |  |
| `Please Select Download Directory` | Selezionare la cartella di download |  |  |
| `Seconds Remaining until Timeout:` | Secondi rimanenti al timeout: |  |  |
| `Seconds Remaining until Timeout: %1 seconds` | Secondi rimanenti al timeout: %1 secondi |  |  |
| `Timeout while downloading` | Timeout durante il download |  |  |

## Main window - menus, toolbar and buttons (23)

| Original (English) | Translation (it-IT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `  #  ` |   #   |  |  |
| `&About` | &amp;Informazioni | CHECK: "About" as a bare menu item is "Informazioni" in Italian; the "su" only appears when a product name follows ("Informazioni su %1", two rows of which are translated that way). |  |
| `&Connect` | &amp;Connetti |  |  |
| `&Disconnect from Selected Regulator` | &amp;Disconnetti dal regolatore selezionato |  |  |
| `&Exit` | &amp;Esci |  |  |
| `&File` | &amp;File |  |  |
| `&Help` | &amp;Aiuto |  |  |
| `&Regulator` | &amp;Regolatore |  |  |
| `...` | ... |  |  |
| `Add a new Regulator` | Aggiungi un nuovo regolatore |  |  |
| `Connect to Selected Regulator` | Connetti al regolatore selezionato |  |  |
| `Debug Logging...` | Log di debug... |  |  |
| `Disconnect from Selected Regulator` | Disconnetti dal regolatore selezionato |  |  |
| `Edit Selected Regulator` | Modifica il regolatore selezionato |  |  |
| `Enable &Advanced Mode...` | Abilita la modalità &amp;avanzata... |  |  |
| `Enable &Basic Mode` | Abilita la modalità &amp;base |  |  |
| `MainWindow` | MainWindow |  |  |
| `Regulator Name Filter` | Filtro per nome regolatore |  |  |
| `Regulators:` | Regolatori: |  |  |
| `Remove Selected Regulator` | Rimuovi il regolatore selezionato |  |  |
| `Settings` | Impostazioni |  |  |
| `Settings...` | Impostazioni... |  |  |
| `toolBar` | toolBar |  |  |

## Main window - regulator table column headers (10)

| Original (English) | Translation (it-IT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `   #   ` |    #    |  |  |
| `Color` | Colore |  |  |
| `Connection Status` | Stato connessione |  |  |
| `Connection Type` | Tipo di connessione | LENGTH: table column header; "Tipo connessione" is a shorter fallback if the column is narrow. |  |
| `Last Connection` | Ultima connessione |  |  |
| `Not Connected` | Non connesso |  |  |
| `Port or IPAddress` | Porta o indirizzo IP |  |  |
| `Regulating Status` | Stato di regolazione |  |  |
| `Regulator Name` | Nome regolatore |  |  |
| `Regulator Status` | Stato regolatore |  |  |

## Numeric entry dialogs (6)

| Original (English) | Translation (it-IT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `Enter Integer` | Immettere un numero intero |  |  |
| `Enter Integer` | Immettere un numero intero |  |  |
| `Integer` | Numero intero |  |  |
| `Integer` | Numero intero |  |  |
| `Max` | Max |  |  |
| `Min` | Min |  |  |

## Other (QObject) (3)

| Original (English) | Translation (it-IT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `%1 - ` | %1 -  |  |  |
| `Cmd: %1 - Error Count: %2` | Comando: %1 - Numero di errori: %2 |  |  |
| `Warning - Consecutive command ran too quickly '%1'` | Avviso - comando consecutivo eseguito troppo rapidamente '%1' |  |  |

## Parameter file editor (59)

| Original (English) | Translation (it-IT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `+ or - followed by 2 digits` | + o - seguito da 2 cifre |  |  |
| `...` | ... |  |  |
| `0 or 1` | 0 o 1 |  |  |
| `1 digit` | 1 cifra |  |  |
| `2 digits` | 2 cifre |  |  |
| `3 digits` | 3 cifre |  |  |
| `4 digits` | 4 cifre |  |  |
| `Active Voltage Target` | Target di tensione attivo |  |  |
| `All Disabled on Any Fault` | Tutte disabilitate a qualsiasi guasto |  |  |
| `Amperage Rating LSB` | Corrente nominale LSB |  |  |
| `Amperage Rating MSB` | Corrente nominale MSB |  |  |
| `B or + or - followed by 2 digits` | B o + o - seguito da 2 cifre |  |  |
| `Current Data` | Dati correnti |  |  |
| `Description` | Descrizione |  |  |
| `Edit Parameter File` | Modifica il file dei parametri |  |  |
| `End Position` | Posizione finale |  |  |
| `Error Message:` | Messaggio di errore: |  |  |
| `Expected Data` | Dati attesi |  |  |
| `Externally Controlled Select (1 or 2)` | Selezione controllata esternamente (1 o 2) |  |  |
| `File '%1' content was not 57 characters` | Il contenuto del file '%1' non era di 57 caratteri |  |  |
| `File '%1' Could not be Opened.` | Impossibile aprire il file '%1'. |  |  |
| `Frequency` | Frequenza |  |  |
| `Ignored 21 bytes` | 21 byte ignorati |  |  |
| `Ignored 3 bytes` | 3 byte ignorati |  |  |
| `Ignored 4 bytes` | 4 byte ignorati |  |  |
| `Invalid character/text at position %1. Expected '%2', Got '%3'` | Carattere o testo non valido nella posizione %1. Atteso '%2', ricevuto '%3' |  |  |
| `Invalid Parameter File` | File dei parametri non valido |  |  |
| `Open Parameter File` | Apri il file dei parametri |  |  |
| `Over Current Fault Count Limit` | Limite del conteggio guasti di sovracorrente | LENGTH: nearly twice the English in a parameter-table cell. |  |
| `Over Voltage Limit` | Limite di sovratensione |  |  |
| `Over Voltage Protection Limit` | Limite di protezione da sovratensione | LENGTH: about 35% longer than the English in a tree label. |  |
| `P followed by any 1 byte` | P seguito da 1 byte qualsiasi |  |  |
| `Parameter File` | File dei parametri |  |  |
| `Parameter File:` | File dei parametri: |  |  |
| `Phase Voltage Offset` | Offset di tensione di fase |  |  |
| `Power Interactive Regulation` | Regolazione interattiva di potenza |  |  |
| `Power Interactive Regulation Delta Voltage` | Delta di tensione della regolazione interattiva di potenza | LENGTH: more than twice the English in a parameter-table cell. |  |
| `Power Interactive Regulation NULL Voltage` | Tensione nulla della regolazione interattiva di potenza | LENGTH: more than twice the English in a parameter-table cell. |  |
| `Power Interactive Regulation Time Constant` | Costante di tempo della regolazione interattiva di potenza | LENGTH: more than twice the English in a parameter-table cell. |  |
| `Prefix` | Prefisso |  |  |
| `Ramp Rate` | Velocità di rampa |  |  |
| `Ramp to Vin` | Rampa fino a Vin |  |  |
| `Raw Data` | Dati grezzi |  |  |
| `Reset To Current` | Ripristina corrente |  |  |
| `Reset to Current Parameter File` | Ripristina il file dei parametri corrente |  |  |
| `Reset to Default` | Ripristina predefinito |  |  |
| `Reset to Default Parameter File` | Ripristina il file dei parametri predefinito |  |  |
| `Save Parameter File` | Salva il file dei parametri |  |  |
| `Select Parameter File` | Seleziona il file dei parametri |  |  |
| `SPARE` | SPARE |  |  |
| `Start Position` | Posizione iniziale |  |  |
| `System Gain` | Guadagno di sistema |  |  |
| `Target Voltage 1` | Tensione target 1 | TERM: "target voltage" = "tensione target", deliberately kept distinct from "set point" (see the glossary); "tensione di riferimento" would collide with the set-point strings. |  |
| `Target Voltage 2` | Tensione target 2 |  |  |
| `Text Files (*.txt);;All Files (*.*)` | File di testo (*.txt);;Tutti i file (*.*) |  |  |
| `Under Voltage Limit` | Limite di sottotensione |  |  |
| `Voltage Regulation Disabled` | Regolazione di tensione disabilitata |  |  |
| `Voltage Setpoint 1` | Set point di tensione 1 |  |  |
| `Voltage Setpoint 2` | Set point di tensione 2 |  |  |

## Password and credential prompts (17)

| Original (English) | Translation (it-IT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `...` | ... |  |  |
| `...` | ... |  |  |
| `Access to %1 requires the correct password to be entered.` | Per accedere a %1 è necessario immettere la password corretta. | AGREEMENT: same "a %1" article problem as the row above. |  |
| `Confirm Password:` | Confermare la password: |  |  |
| `Confirmation password does not match` | La password di conferma non corrisponde |  |  |
| `Current password is not correct` | La password attuale non è corretta |  |  |
| `Current Password:` | Password attuale: |  |  |
| `Enter Credentials` | Immettere le credenziali |  |  |
| `Enter Password` | Immettere la password |  |  |
| `Enter Password:` | Immettere la password: |  |  |
| `Incorrect Password` | Password errata |  |  |
| `Incorrect password entered, Access to %1 denied.` | Password errata: accesso a %1 negato. | AGREEMENT: "a %1" may need to become "al/alla/all'..." depending on the feature name substituted at runtime. Left as the bare preposition; the reviewer may prefer restructuring to "Password errata: accesso negato (%1)." |  |
| `New password does not satisfy length criteria` | La nuova password non soddisfa il requisito di lunghezza |  |  |
| `Password Required` | Password richiesta |  |  |
| `Password Required for %1` | Password richiesta per %1 | AGREEMENT: %1 is the name of the protected feature, so no article is possible here; fine as it stands, but see the note two rows down. |  |
| `Password:` | Password: |  |  |
| `Username:` | Nome utente: |  |  |

## Regulator Information panel (18)

| Original (English) | Translation (it-IT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| ` - Not Connected` |  - Non connesso |  |  |
| `<Unknown>` | &lt;Sconosciuto&gt; |  |  |
| `...` | ... |  |  |
| `Connected Via:` | Connesso tramite: |  |  |
| `GroupBox` | GroupBox |  |  |
| `Invalid Serial Number` | Numero di serie non valido |  |  |
| `Name:` | Nome: |  |  |
| `Phase Firmware Version:` | Versione del firmware di fase: |  |  |
| `Product:` | Prodotto: |  |  |
| `Regulating Status:` | Stato di regolazione: |  |  |
| `Regulator Information` | Informazioni sul regolatore |  |  |
| `Regulator Information:` | Informazioni sul regolatore: |  |  |
| `Regulator's System Clock:` | Orologio di sistema del regolatore: |  |  |
| `Serial Number (12 Characters):` | Numero di serie (12 caratteri): |  |  |
| `Serial Number:` | Numero di serie: |  |  |
| `Set Serial Number` | Imposta il numero di serie |  |  |
| `System Firmware Version and Compilation Date:` | Versione del firmware di sistema e data di compilazione: | LENGTH: long field label; about 35% longer than the English. |  |
| `The serial number must have 12 characters` | Il numero di serie deve avere 12 caratteri |  |  |

## Regulator status and messages (21)

| Original (English) | Translation (it-IT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `    File #: %1` |     File n.: %1 | CHECK: "#" has no Italian equivalent; rendered "n.". The four leading spaces are kept because this line is indented under a heading at runtime. |  |
| ` - Regulator clock off by %1` |  - orologio del regolatore sfasato di %1 |  |  |
| ` - Running Command` |  - comando in esecuzione |  |  |
| ` and ` |  e  |  |  |
| `%1 Hour` | %1 ora |  |  |
| `%1 Hours` | %1 ore |  |  |
| `%1 Minute` | %1 minuto |  |  |
| `%1 Minutes` | %1 minuti |  |  |
| `%1 Second` | %1 secondo |  |  |
| `%1 Seconds` | %1 secondi |  |  |
| `Enabled` | Abilitato |  |  |
| `Firmware must be updated to support Voltage Calibration` | Per supportare la calibrazione della tensione è necessario aggiornare il firmware |  |  |
| `Firmware must be upgraded to V17 or later to support Voltage Calibration` | Per supportare la calibrazione della tensione è necessario aggiornare il firmware alla V17 o successiva |  |  |
| `Number of SD Card files: %1` | Numero di file sulla scheda SD: %1 |  |  |
| `Regulation Information:` | Informazioni di regolazione: |  |  |
| `Regulator Will Reboot` | Il regolatore verrà riavviato |  |  |
| `Target Voltage 1` | Tensione target 1 | TERM: "target voltage" = "tensione target", deliberately kept distinct from "set point" (see the glossary); "tensione di riferimento" would collide with the set-point strings. |  |
| `Target Voltage 2` | Tensione target 2 |  |  |
| `This command will force the regulator to reboot. After it reboots and the green LED on the regulator comes on, you will need to reconnect.` | Questo comando forza il riavvio del regolatore. Dopo il riavvio, quando il LED verde del regolatore si accende, sarà necessario riconnettersi. |  |  |
| `Unknown` | Sconosciuto |  |  |
| `Voltage Control must be set to either Set point 1 or 2` | Il controllo di tensione deve essere impostato su set point 1 o 2 | TERM: "set point" kept in English throughout - standard in Italian control/power engineering. The alternative is "valore di consegna"; please pick one. |  |

## Regulator status trees (59)

| Original (English) | Translation (it-IT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `Active Voltage Target` | Target di tensione attivo |  |  |
| `ADC Cal Error` | Errore di calibrazione ADC |  |  |
| `All Phases Disabled on Failure in Any Phase` | Tutte le fasi disabilitate in caso di guasto in una fase qualsiasi | LENGTH: about 45% longer than the English in a tree label. |  |
| `Amperage Rating (A)` | Corrente nominale (A) |  |  |
| `Baud Rate` | Baud rate | TERM: kept in English - what Italian engineers actually say for a serial line. "Velocità di trasmissione" is the fully Italian alternative but is much longer for a narrow column. |  |
| `Connection:` | Connessione: |  |  |
| `Current (A)` | Corrente (A) |  |  |
| `Delta Voltage (V)` | Delta di tensione (V) |  |  |
| `Fault Code` | Codice guasto |  |  |
| `Flow Control` | Controllo di flusso |  |  |
| `Flux Sensor` | Sensore di flusso |  |  |
| `Form` | Form |  |  |
| `Form` | Form |  |  |
| `Frequency` | Frequenza |  |  |
| `No` | No |  |  |
| `Null Voltage (V)` | Tensione nulla (V) |  |  |
| `Over Current Fault Count` | Conteggio guasti di sovracorrente |  |  |
| `Over Current Fault Count` | Conteggio guasti di sovracorrente |  |  |
| `Over Current Fault in Reset Delay` | Guasto di sovracorrente in ritardo di azzeramento | LENGTH: about 45% longer than the English in a tree label. |  |
| `Over Current Fault Limit` | Limite guasti di sovracorrente |  |  |
| `Over Temperature` | Sovratemperatura |  |  |
| `Over Voltage Limit` | Limite di sovratensione |  |  |
| `Over Voltage Protection Limit` | Limite di protezione da sovratensione | LENGTH: about 35% longer than the English in a tree label. |  |
| `Phase %1` | Fase %1 |  |  |
| `Phase Lock Loop not Locked` | PLL non agganciato | TERM: "locked" for a PLL is "agganciato" in Italian. The English label spells the acronym out; I used the acronym, which is what Italian engineers read. |  |
| `Power Interactive Regulation Status` | Stato della regolazione interattiva di potenza | LENGTH: about 35% longer than the English in a tree label. |  |
| `Power Interactive Regulation Status` | Stato della regolazione interattiva di potenza | LENGTH: about 35% longer than the English in a tree label. |  |
| `Ramp Rate` | Velocità di rampa |  |  |
| `Reaction Time (s)` | Tempo di reazione (s) |  |  |
| `Regulating Status` | Stato di regolazione |  |  |
| `Regulating:` | Regolazione: |  |  |
| `Regulator at Maximum Boost or Buck` | Regolatore al massimo boost o buck | TERM: "boost" and "buck" kept in English, as in Italian power electronics. If the house style prefers Italian, this becomes "al massimo di elevazione o riduzione" (and likewise in the four other boost/buck rows). |  |
| `Regulator Faults:` | Guasti del regolatore: |  |  |
| `Regulator Ramping` | Regolatore in rampa |  |  |
| `Regulator:` | Regolatore: |  |  |
| `SCR or Gate Drive Faults` | Guasti SCR o del pilotaggio di gate |  |  |
| `SD Card Status` | Stato della scheda SD |  |  |
| `Settings` | Impostazioni |  |  |
| `Settings` | Impostazioni |  |  |
| `Status:` | Stato: |  |  |
| `System Gain` | Guadagno di sistema |  |  |
| `Target Voltage 1` | Tensione target 1 | TERM: "target voltage" = "tensione target", deliberately kept distinct from "set point" (see the glossary); "tensione di riferimento" would collide with the set-point strings. |  |
| `Target Voltage 2` | Tensione target 2 |  |  |
| `Temp Sensor or Fan` | Sensore di temperatura o ventola |  |  |
| `Temperature (°C)` | Temperatura (°C) |  |  |
| `UART 1` | UART 1 |  |  |
| `UART 1` | UART 1 |  |  |
| `UART 1` | UART 1 |  |  |
| `UART 2` | UART 2 |  |  |
| `UART 2` | UART 2 |  |  |
| `UART 2` | UART 2 |  |  |
| `Under Voltage Limit` | Limite di sottotensione |  |  |
| `VCC or Fuse` | VCC o fusibile |  |  |
| `Vin/Vout out of limit` | Vin/Vout fuori limite |  |  |
| `Voltage Calibration Offset` | Offset di calibrazione della tensione |  |  |
| `Voltage In (V)` | Tensione di ingresso (V) |  |  |
| `Voltage Out (V)` | Tensione di uscita (V) |  |  |
| `Voltage Regulation Disabled` | Regolazione di tensione disabilitata |  |  |
| `Yes` | Sì |  |  |

## SD card download dialog (36)

| Original (English) | Translation (it-IT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `...` | ... |  |  |
| `2 Days Ago` | 2 giorni fa |  |  |
| `3 Days Ago` | 3 giorni fa |  |  |
| `4 Days Ago` | 4 giorni fa |  |  |
| `5 Days Ago` | 5 giorni fa |  |  |
| `6 Days Ago` | 6 giorni fa |  |  |
| `7 Days Ago` | 7 giorni fa |  |  |
| `A file is still downloading. Cancel it in the progress window before closing this one.` | È ancora in corso il download di un file. Interromperlo nella finestra di avanzamento prima di chiudere questa. |  |  |
| `April` | Aprile |  |  |
| `August` | Agosto |  |  |
| `Command` | Comando |  |  |
| `Data will not be recorded or updated during file downloads` | I dati non verranno registrati né aggiornati durante il download dei file |  |  |
| `December` | Dicembre |  |  |
| `Download in progress` | Download in corso |  |  |
| `Download not started` | Download non avviato |  |  |
| `Fault Log` | Log dei guasti |  |  |
| `February` | Febbraio |  |  |
| `File Name` | Nome del file |  |  |
| `January` | Gennaio | CHECK: Italian normally writes month names in lower case ("gennaio"). I capitalised them because they are standalone group headings in this list, alongside "Oggi" / "Ieri" / "Questo mese". Applies to all twelve rows. |  |
| `July` | Luglio |  |  |
| `June` | Giugno |  |  |
| `March` | Marzo |  |  |
| `May` | Maggio |  |  |
| `Modification Date` | Data di modifica |  |  |
| `Name` | Nome |  |  |
| `November` | Novembre |  |  |
| `October` | Ottobre |  |  |
| `SD Card Files` | File della scheda SD |  |  |
| `Select` | Seleziona |  |  |
| `September` | Settembre |  |  |
| `Size (Bytes)` | Dimensione (byte) |  |  |
| `The regulator is still busy with the previous transfer. Please try again in a moment.` | Il regolatore è ancora occupato con il trasferimento precedente. Riprovare tra un momento. |  |  |
| `This Month` | Questo mese |  |  |
| `Today` | Oggi |  |  |
| `Waiting for regulator...` | In attesa del regolatore... |  |  |
| `Yesterday` | Ieri |  |  |

## Settings dialog (68)

| Original (English) | Translation (it-IT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `      This setting is also the time between consecutive commands.` |       Questa impostazione è anche l'intervallo tra comandi consecutivi. | CHECK: the six leading spaces of the English are kept - they indent the note under the field above it. |  |
| ` Amps` |  Ampere | LENGTH: spin-box suffix. " A" is the compact alternative if the field is narrow. |  |
| ` s` |  s |  |  |
| ` Seconds` |  Secondi |  |  |
| ` Volts` |  Volt |  |  |
| `<the system Downloads folder>` | &lt;la cartella Download di sistema&gt; |  |  |
| `+` | + |  |  |
| `-` | - |  |  |
| `1` | 1 |  |  |
| `Advanced user password:` | Password dell'utente avanzato: |  |  |
| `Amperage Rating:` | Corrente nominale: |  |  |
| `As Needed` | Secondo necessità |  |  |
| `Asked for when the tool starts, and by Settings > Enable Advanced Mode. Takes effect immediately.` | Richiesta all'avvio dello strumento e da Impostazioni &gt; Abilita la modalità avanzata. Ha effetto immediato. |  |  |
| `Automatically Refresh Status?` | Aggiornare automaticamente lo stato? |  |  |
| `Change Advanced User Password` | Modifica la password dell'utente avanzato |  |  |
| `Change Advanced User Password...` | Modifica la password dell'utente avanzato... |  |  |
| `Choose the language the tool is displayed in. The change takes effect immediately; any regulator windows that are already open keep their current language until they are reopened.` | Scegliere la lingua in cui viene visualizzato lo strumento. La modifica ha effetto immediato; le finestre dei regolatori già aperte mantengono la lingua attuale fino alla riapertura. |  |  |
| `Command Timeout:` | Timeout comando: |  |  |
| `Default Regulator Settings` | Impostazioni predefinite del regolatore |  |  |
| `Default Time Zone` | Fuso orario predefinito |  |  |
| `Default View Settings` | Impostazioni di visualizzazione predefinite | LENGTH: tab or group title, roughly twice the English. |  |
| `Download Timeout:` | Timeout download: |  |  |
| `Downloads` | Download |  |  |
| `External Voltage Setpoint Select (1 or 2)` | Selezione esterna del set point di tensione (1 o 2) | LENGTH: about 35% longer than the English. |  |
| `Fast` | Rapido |  |  |
| `Fast:` | Rapido: |  |  |
| `Folder for Downloaded Files` | Cartella per i file scaricati |  |  |
| `Language` | Lingua |  |  |
| `Medium` | Medio |  |  |
| `Medium:` | Medio: |  |  |
| `NULL Voltage at Zero kW:` | Tensione nulla a zero kW: |  |  |
| `Power Interactive Regulation` | Regolazione interattiva di potenza |  |  |
| `Power Interactive Regulation Settings` | Impostazioni della regolazione interattiva di potenza | LENGTH: group-box title, about 45% longer than the English. |  |
| `Ramp to Vin` | Rampa fino a Vin |  |  |
| `Refresh for Regulator Clock Time` | Aggiornamento dell'ora dell'orologio del regolatore | LENGTH: about 45% longer than the English. |  |
| `Refresh for Regulator Faults and Voltages:` | Aggiornamento dei guasti e delle tensioni del regolatore: | LENGTH: about 40% longer than the English. |  |
| `Refresh for SD Card Files:` | Aggiornamento dei file della scheda SD: |  |  |
| `Refresh for Voltage Calibration Status:` | Aggiornamento dello stato di calibrazione della tensione: | LENGTH: about 45% longer than the English. |  |
| `Refresh Gain Values:` | Aggiornamento dei valori di guadagno: |  |  |
| `Refresh Rate Parameter File Information:` | Frequenza di aggiornamento delle informazioni del file dei parametri: | LENGTH: the longest label in this dialog; about 50% longer than the English. |  |
| `Refresh Settings` | Impostazioni di aggiornamento |  |  |
| `Refresh Times:` | Intervalli di aggiornamento: |  |  |
| `Refresh UART Settings:` | Aggiornamento delle impostazioni UART: |  |  |
| `Regulator Setting Defaults` | Valori predefiniti delle impostazioni del regolatore | LENGTH: group-box title, roughly twice the English. |  |
| `Regulator:` | Regolatore: |  |  |
| `Require Password to Enter Advanced Mode?` | Richiedere la password per accedere alla modalità avanzata? | LENGTH: checkbox label, about 40% longer than the English. |  |
| `Save downloaded files to:` | Salva i file scaricati in: |  |  |
| `Security` | Sicurezza |  |  |
| `Settings` | Impostazioni |  |  |
| `Setup UARTs` | Configura le UART |  |  |
| `Show password` | Mostra la password |  |  |
| `Slow` | Lento |  |  |
| `Slow:` | Lento: |  |  |
| `Start in Advanced Mode?` | Avviare in modalità avanzata? |  |  |
| `The Advanced user password has been changed.` | La password dell'utente avanzato è stata modificata. |  |  |
| `Time Constant:` | Costante di tempo: |  |  |
| `Timeout Settings` | Impostazioni di timeout |  |  |
| `Timestamp Transcript?` | Marcare la trascrizione con l'orario? |  |  |
| `Update Settings For All Regulators?` | Applicare le impostazioni a tutti i regolatori? |  |  |
| `View Regulator Information?` | Visualizzare le informazioni sul regolatore? |  |  |
| `View Regulator Status?` | Visualizzare lo stato del regolatore? |  |  |
| `View Transcript in Sepeate Window?` | Visualizzare la trascrizione in una finestra separata? | CHECK: the English misspells "Sepeate"; corrected in the Italian. |  |
| `View Transcript?` | Visualizzare la trascrizione? |  |  |
| `Voltage Control Settings` | Impostazioni di controllo della tensione |  |  |
| `Voltage Delta:` | Delta di tensione: |  |  |
| `Voltage Setpoint 1:` | Set point di tensione 1: |  |  |
| `Voltage Setpoint 2:` | Set point di tensione 2: |  |  |
| `±` | ± |  |  |

## Status and fault values - tables, trees and panels (128)

| Original (English) | Translation (it-IT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `(in multiphase models only) Indicates one of the phases has an open fuse or there is no VCC power. NOTE - a single phase model could not be communicating.` | (solo nei modelli multifase) Indica che una delle fasi ha un fusibile aperto o che manca l'alimentazione VCC. NOTA - un modello monofase potrebbe non essere in comunicazione. |  |  |
| `7A` | 7A |  |  |
| `9A` | 9A |  |  |
| `Active` | Attivo | GENDER: this row and the five that follow (Disabled / Failed / Missing / Locked / Failed or Missing) are status values shown for the SD card, which is feminine in Italian ("la scheda SD"). I used the masculine because the same values may be reused for other subjects; if they are only ever the SD card, they should read Attiva / Disabilitata / Guasta / Assente / Bloccata / Guasta o assente. |  |
| `B2` | B2 |  |  |
| `B8` | B8 |  |  |
| `BA` | BA |  |  |
| `Bound` | Vincolato | CHECK: this is the Qt socket state "Bound". "Vincolato" is the literal rendering; some Italian Qt material leaves "Bound" untranslated. Please pick. |  |
| `CA` | CA |  |  |
| `CB` | CB |  |  |
| `Closing` | Chiusura in corso |  |  |
| `Command Transmission Error` | Errore di trasmissione del comando |  |  |
| `Communication Error` | Errore di comunicazione |  |  |
| `Confirming Connection` | Conferma della connessione |  |  |
| `Connected` | Connesso |  |  |
| `Connecting` | Connessione in corso |  |  |
| `Data File downloaded - not implemented` | File di dati scaricato - non implementato |  |  |
| `DC` | DC |  |  |
| `Disabled` | Disabilitato |  |  |
| `Disabled by Current >1.5X current rating - resets 15min after return to rated current` | Disabilitato per corrente superiore a 1,5 volte la corrente nominale - si azzera 15 min dopo il ritorno alla corrente nominale |  |  |
| `Disabled by Over Current` | Disabilitato per sovracorrente |  |  |
| `Disabled by Over Temperature` | Disabilitato per sovratemperatura |  |  |
| `Disabled by switch (3 phase only)` | Disabilitato da interruttore (solo trifase) |  |  |
| `Disabled by User` | Disabilitato dall'utente |  |  |
| `Disabled by User command` | Disabilitato da comando utente |  |  |
| `Disabled by Voltage Issue` | Disabilitato per problema di tensione |  |  |
| `Disconnected` | Disconnesso |  |  |
| `DS` | DS |  |  |
| `DU` | DU |  |  |
| `EA` | EA |  |  |
| `Enabled by User command - i.e. regulating` | Abilitato da comando utente, ossia in regolazione |  |  |
| `Error Processing Voltage and Fault Status` | Errore durante l'elaborazione dello stato di tensione e guasti |  |  |
| `EU` | EU |  |  |
| `F4` | F4 |  |  |
| `F5` | F5 |  |  |
| `FA` | FA |  |  |
| `Failed` | Guasto |  |  |
| `Failed or Missing` | Guasto o assente |  |  |
| `Fan Fault Cleared` | Guasto della ventola rientrato |  |  |
| `Fault` | Guasto |  |  |
| `FB` | FB |  |  |
| `FC` | FC |  |  |
| `FD` | FD |  |  |
| `FE` | FE |  |  |
| `FLUX` | FLUX |  |  |
| `Flux Sensor Error  If sustained, it writes to F/L once per hour (this will increase the number of Over Current Faults from transformer saturations)` | Errore del sensore di flusso. Se persiste, viene registrato nel F/L una volta all'ora (questo aumenterà il numero di guasti di sovracorrente dovuti a saturazioni del trasformatore) | CHECK: "F/L" left as-is - read as the fault-log abbreviation the firmware uses, not as prose. |  |
| `Getting System Info` | Recupero informazioni di sistema |  |  |
| `Host Found` | Host trovato |  |  |
| `Host Lookup` | Ricerca dell'host |  |  |
| `Indicates a fault caused by a SCR gate drive error` | Indica un guasto provocato da un errore del pilotaggio del gate SCR |  |  |
| `Indicates a flux sensor malfunction which could cause the transformer to saturate` | Indica un malfunzionamento del sensore di flusso che potrebbe portare il trasformatore in saturazione |  |  |
| `Indicates an A to D calibration error during bootup or Voltage sensing error` | Indica un errore di calibrazione del convertitore A/D durante l'avvio o un errore di misura della tensione |  |  |
| `Indicates Flux Sensor faults (>12 per 1/2 Second Interval)` | Indica guasti del sensore di flusso (più di 12 per intervallo di mezzo secondo) |  |  |
| `Indicates full PWM in boost mode (i.e. limiting the ability to hold the setpoint)` | Indica PWM al massimo in modalità boost (limitando quindi la capacità di mantenere il set point) |  |  |
| `Indicates full PWM in buck mode (i.e. limiting the ability to hold the setpoint)` | Indica PWM al massimo in modalità buck (limitando quindi la capacità di mantenere il set point) |  |  |
| `Indicates SCR or Gate Drive Faults (>12 per 1/2 Second Interval)` | Indica guasti dell'SCR o del pilotaggio di gate (più di 12 per intervallo di mezzo secondo) |  |  |
| `Indicates the converter board is temporally in a over temperature state which will reset` | Indica che la scheda del convertitore si trova temporaneamente in stato di sovratemperatura, che rientrerà automaticamente |  |  |
| `Indicates the Over Current Fault has cleared and returned to regulation` | Indica che il guasto di sovracorrente è rientrato ed è ripresa la regolazione |  |  |
| `Indicates the regulator is in a state of maximum Boost or Buck` | Indica che il regolatore è al massimo boost o buck |  |  |
| `Indicates the regulator is in an over current fault reset delay` | Indica che il regolatore è in un ritardo di azzeramento del guasto di sovracorrente |  |  |
| `Indicates there are no hardware faults and the regulator is not disabled i.e. regulating` | Indica che non sono presenti guasti hardware e che il regolatore non è disabilitato, ossia sta regolando |  |  |
| `Indicates there are no hardware faults but the regulator is disabled for various reasons indicated in the Aux Status string. The cause could be it was disabled by the user, or as the result of a fault condition which may clear and return to regulation, or it is in a timer mode where regulation is temporally disabled.` | Indica che non sono presenti guasti hardware, ma che il regolatore è disabilitato per uno dei motivi riportati nella stringa di stato ausiliario. La causa può essere la disabilitazione da parte dell'utente, una condizione di guasto che può rientrare con ripresa della regolazione, oppure una modalità temporizzata in cui la regolazione è temporaneamente disabilitata. |  |  |
| `Indicates Vin or Vout is out of range, either because of high or low line voltage, or possibly a voltage sensing circuit error.` | Indica che Vin o Vout è fuori intervallo, per tensione di linea alta o bassa oppure, eventualmente, per un errore del circuito di misura della tensione. |  |  |
| `Input Power Loss` | Perdita di alimentazione in ingresso |  |  |
| `Listening` | In ascolto |  |  |
| `Locked` | Bloccato |  |  |
| `Logged In/Connected` | Accesso effettuato/Connesso |  |  |
| `Logging In` | Accesso in corso |  |  |
| `Logging Out Phase 1` | Disconnessione (fase 1) |  |  |
| `Logging Out Phase 2` | Disconnessione (fase 2) |  |  |
| `MAX_BOOSTORBUCK` | MAX_BOOSTORBUCK |  |  |
| `Missing` | Assente |  |  |
| `Missing Zero Crossing` | Passaggio per lo zero mancante |  |  |
| `MS` | MS |  |  |
| `ND` | ND |  |  |
| `Not Disabled by switch - i.e. regulating` | Non disabilitato da interruttore, ossia in regolazione |  |  |
| `O0` | O0 |  |  |
| `O1` | O1 |  |  |
| `OC` | OC |  |  |
| `OT` | OT |  |  |
| `Over Current Fault Count O,1...9 then 10,11, 12...` | Conteggio guasti di sovracorrente 0,1...9 poi 10,11,12... | CHECK: the English starts the sequence with the letter "O" rather than a zero; I assumed a typo and used 0. |  |
| `Over Current Fault reset maximum count reached (per PRM file) must be reset manually` | Raggiunto il numero massimo di azzeramenti del guasto di sovracorrente (secondo il file PRM): è necessario l'azzeramento manuale |  |  |
| `Over Temperature fault - converter is disabled until it cools` | Guasto di sovratemperatura - il convertitore resta disabilitato fino al raffreddamento |  |  |
| `P+` | P+ |  |  |
| `P-` | P- |  |  |
| `PL` | PL |  |  |
| `PLL_NL` | PLL_NL |  |  |
| `PN` | PN |  |  |
| `PR` | PR |  |  |
| `Processor Reset by user command` | Reset del processore da comando utente |  |  |
| `PWM is no longer railed, and has dropped below 95% of maximum` | Il PWM non è più al limite ed è sceso sotto il 95% del massimo | CHECK: "railed" rendered as "al limite" (saturated at the rail). Confirm the shop term. |  |
| `RAMP` | RAMP |  |  |
| `Ramping` | In rampa |  |  |
| `Real Time Clock time after Change` | Ora dell'orologio in tempo reale dopo la modifica |  |  |
| `Real Time Clock time before Change` | Ora dell'orologio in tempo reale prima della modifica |  |  |
| `Rebooting` | Riavvio in corso |  |  |
| `Regulating` | In regolazione |  |  |
| `Regulator is ramping to the active set point` | Il regolatore sta salendo in rampa verso il set point attivo |  |  |
| `Restoring Session` | Ripristino della sessione |  |  |
| `SCR_GATE` | SCR_GATE |  |  |
| `SD Card data logging was stopped by user command (disabled)` | La registrazione dei dati sulla scheda SD è stata interrotta da comando utente (disabilitata) |  |  |
| `SE` | SE |  |  |
| `Service Lookup` | Ricerca del servizio |  |  |
| `TEMP` | TEMP |  |  |
| `Temp sensor open` | Sensore di temperatura in circuito aperto |  |  |
| `Temp Sensor or Fan Fault` | Guasto del sensore di temperatura o della ventola |  |  |
| `Temp sensor shorted` | Sensore di temperatura in cortocircuito |  |  |
| `The PLL is currently not locked` | Il PLL non è attualmente agganciato |  |  |
| `Transformer Saturation` | Saturazione del trasformatore |  |  |
| `TS` | TS |  |  |
| `Unknown` | Sconosciuto |  |  |
| `VC` | VC |  |  |
| `Vin or Vout is out of range as defined in PRM file - fault resets automatically with a 10V asymmetrical hysteresis (check fault log Vin column to determine over or under) ` | Vin o Vout fuori dall'intervallo definito nel file PRM - il guasto si azzera automaticamente con un'isteresi asimmetrica di 10 V (controllare la colonna Vin del log dei guasti per determinare se è per eccesso o per difetto)  | CHECK: trailing space kept, as in the English. |  |
| `VO` | VO |  |  |
| `Voltage Calibration error on boot up. After bootup, it permanently disables the regulator` | Errore di calibrazione della tensione all'avvio. Dopo l'avvio, disabilita permanentemente il regolatore |  |  |
| `W1` | W1 |  |  |
| `W2` | W2 |  |  |
| `W3` | W3 |  |  |
| `W4` | W4 |  |  |
| `W5` | W5 |  |  |
| `W6` | W6 |  |  |
| `Watchdog tripped - DSPIC failure to respond` | Watchdog intervenuto - il DSPIC non ha risposto |  |  |
| `Watchdog tripped - Failed wellness test (Vout != Setpoint and no faults)` | Watchdog intervenuto - test di funzionalità non superato (Vout diverso dal set point e nessun guasto) |  |  |
| `Watchdog tripped - Main uP loop timed out OR H/W watchdog timed out` | Watchdog intervenuto - timeout del ciclo principale del microprocessore o timeout del watchdog hardware |  |  |
| `Watchdog tripped - Phase Parameter file checksum mismatch` | Watchdog intervenuto - checksum del file dei parametri di fase non corrispondente |  |  |
| `Watchdog tripped - Phase Status or data checksum mismatch  ` | Watchdog intervenuto - checksum dello stato o dei dati di fase non corrispondente   | CHECK: two trailing spaces kept, as in the English. |  |
| `Watchdog tripped - SPI buss to phase failure ` | Watchdog intervenuto - guasto del bus SPI verso la fase  | CHECK: trailing space kept, as in the English. |  |
| `ZX` | ZX |  |  |

## Transcript pane and window (18)

| Original (English) | Translation (it-IT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| ` Send Command ` |  Invia comando  |  |  |
| ` Send CTRL-C ` |  Invia CTRL-C  |  |  |
| `%1:     Sent: %2` | %1:     Inviato: %2 | CHECK: internal padding copied from the English unchanged; "Ricevuto:" and "Inviato:" are different lengths, so the two lines will not line up exactly. Adjust the spaces if the transcript is meant to be column-aligned. |  |
| `%1: %2` | %1: %2 |  |  |
| `%1: <font color="orange">WARNING: %2</font>` | %1: &lt;font color="orange"&gt;AVVISO: %2&lt;/font&gt; |  |  |
| `%1: <font color="red">ERROR: %2</font>` | %1: &lt;font color="red"&gt;ERRORE: %2&lt;/font&gt; |  |  |
| `%1: Received:   %2` | %1: Ricevuto:   %2 |  |  |
| `Clear Transcript` | Cancella la trascrizione |  |  |
| `Command To Send` | Comando da inviare |  |  |
| `Copy Transcript to Clipboard` | Copia la trascrizione negli appunti |  |  |
| `Could not open '%1' for writing, please check permissions\n%2` | Impossibile aprire '%1' in scrittura, verificare le autorizzazioni\n%2 |  |  |
| `Could not Open File` | Impossibile aprire il file |  |  |
| `Error` | Errore |  |  |
| `Save Transcript` | Salva la trascrizione |  |  |
| `Save Transcript...` | Salva la trascrizione... |  |  |
| `Select All` | Seleziona tutto |  |  |
| `Text Files (*.txt);;All Files (*.*)` | File di testo (*.txt);;Tutti i file (*.*) |  |  |
| `Transcript` | Trascrizione |  |  |

## UART settings dialog (16)

| Original (English) | Translation (it-IT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `115.2k` | 115.2k |  |  |
| `230.4k` | 230.4k |  |  |
| `38.4k` | 38.4k |  |  |
| `57.6k` | 57.6k |  |  |
| `Baud Rate` | Baud rate | TERM: kept in English - what Italian engineers actually say for a serial line. "Velocità di trasmissione" is the fully Italian alternative but is much longer for a narrow column. |  |
| `Baud rate and Flow control must be set` | È necessario impostare il baud rate e il controllo di flusso |  |  |
| `Baud rate must be set` | È necessario impostare il baud rate |  |  |
| `Flow Control` | Controllo di flusso |  |  |
| `Flow control must be set` | È necessario impostare il controllo di flusso |  |  |
| `Hardware Control` | Controllo hardware |  |  |
| `None` | Nessuno |  |  |
| `Setup UARTs` | Configura le UART |  |  |
| `Software Control` | Controllo software |  |  |
| `TextLabel` | TextLabel |  |  |
| `UART 1 settings can not be modified` | Le impostazioni della UART 1 non possono essere modificate |  |  |
| `WARNING: DO NOT CHANGE if UART2 is used with an Ethernet adapter.` | AVVISO: NON MODIFICARE se la UART2 è utilizzata con un adattatore Ethernet. |  |  |

## User guide windows (7)

| Original (English) | Translation (it-IT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `Advanced User Guide` | Guida utente (avanzata) |  |  |
| `Basic User Guide` | Guida utente (base) |  |  |
| `Bluetooth Pairing` | Associazione Bluetooth |  |  |
| `Bluetooth Pairing (Windows 11)` | Associazione Bluetooth (Windows 11) |  |  |
| `Close` | Chiudi |  |  |
| `Fit to window` | Adatta alla finestra |  |  |
| `The guide could not be loaded: %1` | Non è stato possibile caricare la guida: %1 |  |  |

## Voltage calibration dialog (10)

| Original (English) | Translation (it-IT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| ` Volts` |  Volt |  |  |
| `A Voltage Difference of '%1' is invalid, range is -9.9V to +9.9V` | Una differenza di tensione di '%1' non è valida: l'intervallo ammesso va da -9,9 V a +9,9 V | CHECK: decimal comma and a space before the unit, per Italian convention. |  |
| `Can not calibrate voltage` | Impossibile calibrare la tensione |  |  |
| `Externally Measured Output Voltage:` | Tensione di uscita misurata esternamente: |  |  |
| `Regulator Target %1 Output Voltage:` | Tensione di uscita target %1 del regolatore: |  |  |
| `Regulator Target Output Voltage:` | Tensione di uscita target del regolatore: |  |  |
| `Voltage Calibration` | Calibrazione della tensione |  |  |
| `Voltage Calibration:` | Calibrazione della tensione: |  |  |
| `Voltage Difference is too High` | La differenza di tensione è troppo elevata |  |  |
| `Volts` | Volt |  |  |
