# ConfigTool - French (fr-FR) translation review

The complete translation, grouped by where the text appears in the tool. Edit the
**Translation** column directly, or put a replacement in **Your correction**, and
hand the file back. For anything with markup or long text, the spreadsheet next to
this file is easier to work in.

- Strings translated: **876** - the whole of the live user interface
- Strings still untranslated: **0**
- Rows carrying a question from me: **87**
- Generated from `translations/ConfigTool_fr_FR.ts`

This is a machine first pass awaiting a native French (France) speaker. This is deliberately metropolitan French and not Canadian: *courriel* usage, *téléverser*/*télécharger* and *ordinateur* follow French practice in France, and the typography is French - narrow non-breaking spaces before `?` `!` `:` `;` and French quotation marks.

Some strings are translated to themselves on purpose. Firmware fault codes (`CB`,
`OT`, `W1`, `P+`, `RAMP`...), baud rate values and Qt Designer object names
(`toolBar`, `MainWindow`) are identifiers rather than prose - translating them
would break the match against what the regulator actually sends.

A few strings carry HTML. Those rows show both columns as code, so the tags are
visible rather than rendered - they are part of the string and must survive
translation unchanged. `\n` marks a real line break, the same convention the
.tsv uses.

## About and licence dialogs (9)

| Original (English) | Translation (fr-FR) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `&3rd Party Licenses` | &amp;Licences tierces |  |  |
| `&About Qt` | À propos de &amp;Qt |  |  |
| `<h3>%1 - 3rd Party Licenses</h3>` | `<h3>%1 - Licences tierces</h3>` |  |  |
| `<h3>About %1</h3><p>%1</p><p>Version: %2</p><p>Build Date: %3</p><p>%4</p>` | `<h3>À propos de %1</h3><p>%1</p><p>Version : %2</p><p>Date de compilation : %3</p><p>%4</p>` |  |  |
| `<p>%1 uses multiple 3rd Party software mostly covered under the Qt distribution</p><p>However the following license(s) are not part of Qt.</p><hr style="width:50%;text-align:left;margin-left:0"><table border="1"><tr><th>Company</th><th>Product</th><th>License</th><th>Source Location</th><th>Patches</th></tr>` | `<p>%1 utilise plusieurs logiciels tiers, couverts pour la plupart par la distribution Qt</p><p>Les licences suivantes ne font toutefois pas partie de Qt.</p><hr style="width:50%;text-align:left;margin-left:0"><table border="1"><tr><th>Société</th><th>Produit</th><th>Licence</th><th>Emplacement des sources</th><th>Correctifs</th></tr>` | CHECK: only the text between tags is translated; the style/border attribute values (including the « 50% ») are copied verbatim and take no French spacing. |  |
| `<p>Is a tool to help configure %1's Voltage Regulators.</p><p>For more information, please visit <a href="%2">%3</a>.</p><p>For the default Advanced and Admin passwords, contact <a href="mailto:%4">%4</a>.</p><hr style="width:50%;text-align:left;margin-left:0"><p>%5</p>` | `<p>Outil d’aide à la configuration des régulateurs de tension de %1.</p><p>Pour plus d’informations, consultez <a href="%2">%3</a>.</p><p>Pour les mots de passe Avancé et Admin par défaut, contactez <a href="mailto:%4">%4</a>.</p><hr style="width:50%;text-align:left;margin-left:0"><p>%5</p>` |  |  |
| `3rd Party Licenses` | Licences tierces |  |  |
| `About %1` | À propos de %1 |  |  |
| `This tool supports the following LVR firmware versions:<br>LVR30 %1, LVR50 %2` | `Cet outil prend en charge les versions de micrologiciel LVR suivantes :<br>LVR30 %1, LVR50 %2` |  |  |

## Bluetooth - Available Regulators and pairing (48)

| Original (English) | Translation (fr-FR) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `%1 configured connection(s)` | %1 connexion(s) configurée(s) |  |  |
| `An error has occurred in the bluetooth system` | Une erreur s’est produite dans le système Bluetooth |  |  |
| `An unknown error has occurred.` | Une erreur inconnue s’est produite. |  |  |
| `Authorize Regulator` | Autoriser le régulateur |  |  |
| `Available Regulators` | Régulateurs disponibles |  |  |
| `Connecting to regulator '%1' timed out. Check your connection - the regulator may be out of range or turned off.` | La connexion au régulateur '%1' a expiré. Vérifiez la liaison - le régulateur est peut-être hors de portée ou éteint. |  |  |
| `Could not find a bluetooth adapter. ` | Impossible de trouver un adaptateur Bluetooth.  |  |  |
| `currently connected` | actuellement connecté |  |  |
| `Device discovery is not possible or implemented on the current platform.` | La détection des appareils est impossible ou n’est pas implémentée sur la plateforme actuelle. |  |  |
| `Device Name` | Nom de l’appareil |  |  |
| `Does the following PIN match the one shown on the device you are pairing?: %1` | Le code PIN suivant correspond-il à celui affiché sur l’appareil que vous appairez ? : %1 | CHECK: the English ends with the odd sequence « ?: » ; kept, as %1 is appended after it. |  |
| `Enter a PIN to pair with:` | Saisissez un code PIN pour l’appairage : |  |  |
| `Error in Bluetooth connection` | Erreur de connexion Bluetooth |  |  |
| `Error in pairing` | Erreur d’appairage | TERM: « appairage » is the usual fr-FR Bluetooth term (Windows fr uses « association », Apple « jumelage »). Confirm house choice. |  |
| `Finished` | Terminé |  |  |
| `Limit the list to shipped regulators, which are all named "PV...". Uncheck to also show bench and test units, which often are not. Non-regulators are never listed either way.` | Limite la liste aux régulateurs expédiés, dont le nom commence toujours par "PV...". Décochez la case pour afficher également les unités de banc d’essai et de test, qui souvent ne suivent pas cette règle. Les équipements qui ne sont pas des régulateurs ne sont jamais listés, dans un cas comme dans l’autre. | CHECK: "PV..." kept in ASCII double quotes — it is the device-name prefix the filter matches on, not prose. |  |
| `Missing permissions` | Autorisations manquantes |  |  |
| `No Bluetooth Adapter Found` | Aucun adaptateur Bluetooth trouvé |  |  |
| `One of the requested discovery methods is not supported by the current platform.` | L’une des méthodes de détection demandées n’est pas prise en charge par la plateforme actuelle. |  |  |
| `Pair Device` | Appairer l’appareil |  |  |
| `Pair Device?` | Appairer l’appareil ? |  |  |
| `Pair Regulator` | Appairer le régulateur |  |  |
| `paired` | appairé |  |  |
| `Paired?` | Appairé ? |  |  |
| `Permissions are needed to use Bluetooth. Please grant the permissions to this application in the system settings.` | Des autorisations sont nécessaires pour utiliser le Bluetooth. Veuillez les accorder à cette application dans les paramètres du système. |  |  |
| `Please enter this PIN on the device you are pairing with: %1` | Saisissez ce code PIN sur l’appareil que vous appairez : %1 |  |  |
| `PV Filter` | Filtre PV |  |  |
| `Re-Scan` | Relancer la recherche | LENGTH: « Re-Scan » (7 chars) becomes 22 on a toolbar-style button; « Relancer » alone if it clips. |  |
| `Remove %1 regulator(s)?` | Supprimer %1 régulateur(s) ? |  |  |
| `Remove Regulators` | Supprimer les régulateurs |  |  |
| `Remove the selected regulators from the list, delete their connections, and unpair them` | Supprime les régulateurs sélectionnés de la liste, efface leurs connexions et les désappaire |  |  |
| `Scanning for devices not previously paired.` | Recherche des appareils non encore appairés. |  |  |
| `Scanning for previously connected devices and devices not previously paired.` | Recherche des appareils précédemment connectés et des appareils non encore appairés. |  |  |
| `Scanning for previously connected devices.` | Recherche des appareils précédemment connectés. |  |  |
| `Scanning...` | Recherche en cours… |  |  |
| `Select Regulator` | Sélectionner un régulateur |  |  |
| `Select the Regulator to connect to.` | Sélectionnez le régulateur auquel vous souhaitez vous connecter. |  |  |
| `Service` | Service |  |  |
| `Stop Scanning` | Arrêter la recherche |  |  |
| `The Bluetooth adaptor is powered off, power it on before doing discovery.` | L’adaptateur Bluetooth est éteint ; activez-le avant de lancer la recherche d’appareils. |  |  |
| `The following error occurred connecting to regulator '%1': %2. Check your connection - the regulator may be out of range or turned off.` | L’erreur suivante s’est produite lors de la connexion au régulateur '%1' : %2. Vérifiez la liaison - le régulateur est peut-être hors de portée ou éteint. |  |  |
| `The location service is turned off.Usage of Bluetooth APIs is not possible when location service is turned off.` | Le service de localisation est désactivé. Les API Bluetooth ne peuvent pas être utilisées lorsque le service de localisation est désactivé. | CHECK: the English is missing a space after « off. » ; the French adds one. |  |
| `The operating system requests permissions which were not granted by the user.` | Le système d’exploitation demande des autorisations qui n’ont pas été accordées par l’utilisateur. |  |  |
| `The passed local adapter address does not match the physical adapter address of any local Bluetooth device.` | L’adresse d’adaptateur local indiquée ne correspond à l’adresse physique d’aucun périphérique Bluetooth local. |  |  |
| `This deletes their configured connections, removes them from the Available Regulators list, and unpairs them from this computer. Any open connections will be closed. This cannot be undone.` | Cette action supprime leurs connexions configurées, les retire de la liste des régulateurs disponibles et les désappaire de cet ordinateur. Toute connexion ouverte sera fermée. Cette action est irréversible. |  |  |
| `Unknown Error.` | Erreur inconnue. |  |  |
| `Unpair Regulator` | Désappairer le régulateur |  |  |
| `Writing or reading from the device resulted in an error.` | L’écriture ou la lecture sur l’appareil a provoqué une erreur. |  |  |

## Clock and time zone dialogs (13)

| Original (English) | Translation (fr-FR) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `...` | ... | CHECK: the « ... » browse-button label is left verbatim (Qt Designer widget text, not prose). |  |
| `...` | ... | CHECK: the « ... » browse-button label is left verbatim (Qt Designer widget text, not prose). |  |
| `Current Time` | Heure actuelle |  |  |
| `Custom Selected Time Zone` | Fuseau horaire personnalisé |  |  |
| `Custom Time` | Heure personnalisée |  |  |
| `Local Computer's Time Zone` | Fuseau horaire de l’ordinateur local |  |  |
| `Regulator's System Clock:` | Horloge système du régulateur : |  |  |
| `Regulator:` | Régulateur : |  |  |
| `Select Time Zone` | Sélectionner le fuseau horaire |  |  |
| `Select Time Zone` | Sélectionner le fuseau horaire |  |  |
| `Set Regulator System Clock` | Régler l’horloge système du régulateur |  |  |
| `Sync` | Synchroniser |  |  |
| `UTC` | UTC |  |  |

## Command names - transcript and queue status (65)

| Original (English) | Translation (fr-FR) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `    Command #: %1` |     Commande n° : %1 |  |  |
| `%1.` | %1. |  |  |
| `(Re)-initialize Control Board` | (Ré)initialiser la carte de commande |  |  |
| `, re-running command.` | , nouvelle exécution de la commande. |  |  |
| `. Removing from Queue.` | . Suppression de la file d’attente. |  |  |
| `Checking for Support of '%1'` | Vérification de la prise en charge de '%1' |  |  |
| `Clear Queue` | Vider la file d’attente |  |  |
| `cmd not supported` | cmd non prise en charge |  |  |
| `Command '%1' failed. Please disconnect and try again.  Consider rebooting the Regulator.` | La commande '%1' a échoué. Déconnectez-vous et réessayez.  Envisagez de redémarrer le régulateur. | TERM: « régulateur » = voltage regulator throughout (régulateur de tension). Confirm against French utility usage. |  |
| `Command '%1' failed. Removing from Queue.` | La commande '%1' a échoué. Suppression de la file d’attente. |  |  |
| `Command '%1' is not supported` | La commande '%1' n’est pas prise en charge |  |  |
| `Command '%2' timed out%1` | La commande '%2' a expiré%1 | CHECK: %1 is the sentence tail concatenated at runtime (rows 31/32) — it must read on from « a expiré ». |  |
| `Could not process results of command '%1'` | Impossible de traiter les résultats de la commande '%1' |  |  |
| `Custom Command` | Commande personnalisée |  |  |
| `Disable SDCard` | Désactiver la carte SD |  |  |
| `Download File` | Télécharger le fichier |  |  |
| `Enable Or Disable All Phases if there is a Failure in any Phase` | Activer ou désactiver toutes les phases en cas de défaillance d’une phase |  |  |
| `Enable Or Disable Regulator` | Activer ou désactiver le régulateur |  |  |
| `Enable SDCard` | Activer la carte SD |  |  |
| `Finished downloading data for command '%1'` | Téléchargement des données de la commande '%1' terminé |  |  |
| `Finished getting system info` | Récupération des informations système terminée |  |  |
| `Finished Getting System Info` | Récupération des informations système terminée |  |  |
| `Format SDCard` | Formater la carte SD |  |  |
| `Get Default Parameter File` | Obtenir le fichier de paramètres par défaut |  |  |
| `Get EEPROM Contents` | Obtenir le contenu de l’EEPROM |  |  |
| `Get File Sizes` | Obtenir les tailles des fichiers |  |  |
| `Get Parameter File` | Obtenir le fichier de paramètres |  |  |
| `Get Phase Firmware` | Obtenir le micrologiciel de phase |  |  |
| `Get Regulator Clock` | Obtenir l’horloge du régulateur |  |  |
| `Get Serial Num` | Obtenir le numéro de série |  |  |
| `Get Status` | Obtenir l’état |  |  |
| `Get System Firmware` | Obtenir le micrologiciel système |  |  |
| `Get System Firmware Date` | Obtenir la date du micrologiciel système |  |  |
| `Get System Gain` | Obtenir le gain du système |  |  |
| `Get UART Settings` | Obtenir les paramètres UART |  |  |
| `Get UART Settings via RB` | Obtenir les paramètres UART via RB |  |  |
| `Get UART Settings via RBAUD` | Obtenir les paramètres UART via RBAUD |  |  |
| `Get Voltage Calibration` | Obtenir l’étalonnage de tension |  |  |
| `Reboot Regulator` | Redémarrer le régulateur |  |  |
| `Regulator could not handle command '%1'` | Le régulateur n’a pas pu traiter la commande '%1' |  |  |
| `Reset Over Current Fault Lockout` | Réinitialiser le verrouillage sur défaut de surintensité | TERM: « verrouillage sur défaut de surintensité » for Over Current Fault Lockout. Confirm the protection vocabulary used by French utilities. |  |
| `Reset Regulator to Default Parameters` | Rétablir les paramètres par défaut du régulateur |  |  |
| `Restore Modem Power` | Rétablir l’alimentation du modem |  |  |
| `Send Ctrl-C` | Envoyer Ctrl-C |  |  |
| `Send Login` | Envoyer l’ouverture de session |  |  |
| `Send Logoff` | Envoyer la fermeture de session |  |  |
| `Send Password` | Envoyer le mot de passe |  |  |
| `Set Param File` | Définir le fichier de paramètres |  |  |
| `Set PIR Amperage` | Définir le courant PIR | CHECK: PIR (Power Interactive Regulation) kept as the firmware abbreviation, as in the English. |  |
| `Set PIR Delta Voltage` | Définir l’écart de tension PIR |  |  |
| `Set PIR Null Voltage` | Définir la tension nulle PIR |  |  |
| `Set PIR Time Constant` | Définir la constante de temps PIR |  |  |
| `Set Regulator Clock` | Régler l’horloge du régulateur |  |  |
| `Set Regulator Password` | Définir le mot de passe du régulateur |  |  |
| `Set Serial Number` | Définir le numéro de série |  |  |
| `Set System Gain` | Définir le gain du système |  |  |
| `Set Target Selection` | Définir la sélection de consigne |  |  |
| `Set Target Voltage` | Définir la tension de consigne |  |  |
| `Set UART 1 Baud Rate` | Définir le débit en bauds de l’UART 1 |  |  |
| `Set UART 1 FlowControl` | Définir le contrôle de flux de l’UART 1 |  |  |
| `Set UART 2 Baud Rate` | Définir le débit en bauds de l’UART 2 |  |  |
| `Set UART 2 FlowControl` | Définir le contrôle de flux de l’UART 2 |  |  |
| `Set Voltage Calibration` | Définir l’étalonnage de tension |  |  |
| `Size of Command Queue: %1` | Taille de la file d’attente des commandes : %1 |  |  |
| `Turn off Modem Power` | Couper l’alimentation du modem |  |  |

## Connected regulator window - menus, dialogs and messages (149)

| Original (English) | Translation (fr-FR) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `    Comm Port: %1` |     Port de communication : %1 |  |  |
| `    IP Address: %1\n    Domain Name: %2\n    Port: %3` |     Adresse IP : %1\n    Nom de domaine : %2\n    Port : %3 |  |  |
| ` - Regulator: %1` |  - Régulateur : %1 |  |  |
| ` - Transcript` |  - Journal de session |  |  |
| ` Reset Over Current Fault Lockout` |  Réinitialiser le verrouillage sur défaut de surintensité | CHECK: leading space is in the English source and is preserved. |  |
| `%1` | %1 |  |  |
| `&Disconnect` | Se &amp;déconnecter |  |  |
| `&Regulator` | &amp;Régulateur |  |  |
| `&Settings` | &amp;Paramètres |  |  |
| `<br/>Would you like to reconnect?` | `<br/>Souhaitez-vous vous reconnecter ?` |  |  |
| `'%1' is a name Windows reserves and cannot be used in a file name.` | '%1' est un nom réservé par Windows et ne peut pas être utilisé dans un nom de fichier. |  |  |
| `(Re-)Initialize Regulator Control Board` | (Ré)initialiser la carte de commande du régulateur |  |  |
| `(Re-)initialize the Control Board...` | (Ré)initialiser la carte de commande… | TERM: « carte de commande » for control board. Confirm against the hardware documentation. |  |
| `(Re-)initialize the control board...` | (Ré)initialiser la carte de commande… |  |  |
| `1=Fast` | 1=Rapide |  |  |
| `A timeout error occurred` | Une erreur de délai d’attente s’est produite |  |  |
| `About...` | À propos… |  |  |
| `Administration Mode` | Mode administration |  |  |
| `Administration Mode` | Mode administration |  |  |
| `Advanced Mode` | Mode avancé |  |  |
| `All Phases Disabled on Failure in Any Phase?` | Désactiver toutes les phases en cas de défaillance d’une phase ? |  |  |
| `An error occurred while attempting to open an already opened device by another process or a user not having enough permission and credentials to open.` | Une erreur s’est produite lors de la tentative d’ouverture d’un appareil déjà ouvert par un autre processus, ou par un utilisateur ne disposant pas des autorisations et des identifiants nécessaires. |  |  |
| `An error occurred while attempting to open an already opened device in this object.` | Une erreur s’est produite lors de la tentative d’ouverture d’un appareil déjà ouvert dans cet objet. |  |  |
| `An error occurred while attempting to open an non-existing device.` | Une erreur s’est produite lors de la tentative d’ouverture d’un appareil inexistant. |  |  |
| `An I/O error occurred when a resource becomes unavailable, e.g. when the device is unexpectedly removed from the system.` | Une erreur d’E/S s’est produite parce qu’une ressource est devenue indisponible, par exemple lorsque l’appareil est retiré du système de façon inattendue. |  |  |
| `An I/O error occurred while reading the data.` | Une erreur d’E/S s’est produite lors de la lecture des données. |  |  |
| `An I/O error occurred while writing the data.` | Une erreur d’E/S s’est produite lors de l’écriture des données. |  |  |
| `An unidentified error occurred.` | Une erreur non identifiée s’est produite. |  |  |
| `Are you sure you wish to continue?` | Voulez-vous vraiment continuer ? |  |  |
| `Automatically Refresh Status?` | Actualiser automatiquement l’état ? |  |  |
| `Available` | Disponible |  |  |
| `Available` | Disponible |  |  |
| `Available` | Disponible |  |  |
| `Bluetooth` | Bluetooth |  |  |
| `Bluetooth Regulator Unauthorized` | Régulateur Bluetooth non autorisé |  |  |
| `Bluetooth Regulator Unpaired` | Régulateur Bluetooth non appairé |  |  |
| `Can not set UART settings while connected via Ethernet` | Impossible de modifier les paramètres UART tant que la connexion se fait par Ethernet |  |  |
| `Change Time Zone...` | Changer de fuseau horaire… |  |  |
| `Clear Command Queue` | Vider la file d’attente des commandes |  |  |
| `Clear Transcript` | Effacer le journal de session | LENGTH: 16 chars becomes 28 on what is likely a toolbar button; « Effacer le journal » if it clips. |  |
| `Close Connection?` | Fermer la connexion ? |  |  |
| `COM Port` | Port COM |  |  |
| `Comm Port not Found` | Port de communication introuvable |  |  |
| `Command Queue Status` | État de la file d’attente des commandes |  |  |
| `Connect` | Se connecter |  |  |
| `Connection '%1' was lost or disconnected.` | La connexion '%1' a été perdue ou interrompue. |  |  |
| `Continue` | Continuer |  |  |
| `Continue` | Continuer |  |  |
| `Copy Transcript to Clipboard` | Copier le journal de session dans le presse-papiers |  |  |
| `Debug` | Débogage |  |  |
| `Debug Logging...` | Journalisation de débogage… |  |  |
| `Delete Data Logs...` | Supprimer les journaux de données… |  |  |
| `Delete Fault Log...` | Supprimer le journal des défauts… |  |  |
| `Disable Advanced Mode` | Désactiver le mode avancé |  |  |
| `Disable Regulator` | Désactiver le régulateur |  |  |
| `Disable SD Card` | Désactiver la carte SD |  |  |
| `Download from SD Card` | Télécharger depuis la carte SD |  |  |
| `Download from SD Card...` | Télécharger depuis la carte SD… |  |  |
| `Enable Advanced Mode` | Activer le mode avancé |  |  |
| `Enable Regulator` | Activer le régulateur |  |  |
| `Enable SD Card` | Activer la carte SD |  |  |
| `Enter New Regulator Password` | Saisir le nouveau mot de passe du régulateur |  |  |
| `Enter Regulator Password` | Saisir le mot de passe du régulateur |  |  |
| `Enter System Gain` | Saisir le gain du système |  |  |
| `Error` | Erreur |  |  |
| `Error Communicating with Regulator` | Erreur de communication avec le régulateur |  |  |
| `ERROR: %1` | ERREUR : %1 |  |  |
| `Fast Rate Data` | Données à cadence rapide |  |  |
| `Format SD Card...` | Formater la carte SD… |  |  |
| `Formatting erases the SD card and cannot be undone.` | Le formatage efface la carte SD et est irréversible. |  |  |
| `Help` | Aide |  |  |
| `Host '%1' was not found. Please check the host name and port settings.` | L’hôte '%1' est introuvable. Veuillez vérifier le nom d’hôte et les paramètres de port. |  |  |
| `Initialize System Information on Login?` | Initialiser les informations système à la connexion ? |  |  |
| `Medium Rate Data` | Données à cadence moyenne |  |  |
| `Name cannot be used` | Nom inutilisable |  |  |
| `Name for this regulator:\n\nThis name is stored by the Config Tool only. It is not written to the\nregulator and is not read back from it, and it is lost if the regulator\nis removed from the saved list.\n\nIt is used in the names of the files downloaded from this regulator, so\nit cannot contain characters that a file name cannot hold.` | Nom de ce régulateur :\n\nCe nom est conservé uniquement par le Config Tool. Il n’est pas écrit\ndans le régulateur ni relu depuis celui-ci, et il est perdu si le régulateur\nest retiré de la liste enregistrée.\n\nIl est utilisé dans les noms des fichiers téléchargés depuis ce régulateur, ;\nil ne peut donc pas contenir de caractères interdits dans un nom de fichier. |  |  |
| `Network not Reachable` | Réseau inaccessible |  |  |
| `No SD File Data` | Aucune donnée de fichier SD |  |  |
| `No SD file data available. Click on the green System Info arrows.` | Aucune donnée de fichier SD disponible. Cliquez sur les flèches vertes des informations système. |  |  |
| `Parameter File...` | Fichier de paramètres… |  |  |
| `Password Required` | Mot de passe requis |  |  |
| `Power cycle external modem at J2-2` | Couper et rétablir l’alimentation du modem externe sur J2-2 | LENGTH: French has no one-word equivalent of « power cycle » ; the string roughly doubles. « Redémarrer le modem externe sur J2-2 » is shorter but loses the power-cycle sense. |  |
| `Power Interactive Regulation Settings...` | Paramètres de régulation interactive de puissance… |  |  |
| `Quit` | Quitter |  |  |
| `Quit` | Quitter |  |  |
| `Reboot Regulator` | Redémarrer le régulateur |  |  |
| `Reboot Regulator...` | Redémarrer le régulateur… |  |  |
| `Reconnect` | Se reconnecter |  |  |
| `Refresh` | Actualiser |  |  |
| `Refresh All` | Tout actualiser |  |  |
| `Refresh Gain Values` | Actualiser les valeurs de gain |  |  |
| `Refresh Parameter File` | Actualiser le fichier de paramètres |  |  |
| `Refresh Regulator Clock` | Actualiser l’horloge du régulateur |  |  |
| `Refresh Regulator Information` | Actualiser les informations du régulateur |  |  |
| `Refresh SD Card Information` | Actualiser les informations de la carte SD |  |  |
| `Refresh UART Settings` | Actualiser les paramètres UART |  |  |
| `Refresh Voltage and Fault Status` | Actualiser l’état des tensions et des défauts |  |  |
| `Refresh Voltage Calibration Info` | Actualiser les informations d’étalonnage de tension |  |  |
| `Regulator` | Régulateur |  |  |
| `Regulator &Settings` | &amp;Paramètres du régulateur |  |  |
| `Regulator '%1' - %2` | Régulateur '%1' - %2 |  |  |
| `Regulator has logged off due to no command activity. Please reconnect and activate auto refresh.` | Le régulateur a fermé la session faute d’activité de commande. Reconnectez-vous, puis activez l’actualisation automatique. |  |  |
| `Regulator Logged Off` | Session fermée sur le régulateur |  |  |
| `Regulator:` | Régulateur : |  |  |
| `Remote` | Distant |  |  |
| `Reset Over Current Fault Lockout` | Réinitialiser le verrouillage sur défaut de surintensité | TERM: « verrouillage sur défaut de surintensité » for Over Current Fault Lockout. Confirm the protection vocabulary used by French utilities. |  |
| `Reset Regulator to Default Parameters` | Rétablir les paramètres par défaut du régulateur |  |  |
| `Reset Regulator to Default Parameters...` | Rétablir les paramètres par défaut du régulateur… |  |  |
| `Save Transcript...` | Enregistrer le journal de session… | LENGTH: grows to 34 chars; « Enregistrer le journal… » if the menu is narrow. |  |
| `SD Card` | Carte SD |  |  |
| `SD Card File Sizes` | Tailles des fichiers de la carte SD |  |  |
| `SD Card Has Error` | La carte SD présente une erreur |  |  |
| `SD Card is Disabled` | La carte SD est désactivée |  |  |
| `Session Timing Out` | Expiration de la session |  |  |
| `Set Regulator Name` | Définir le nom du régulateur |  |  |
| `Set Regulator Name...` | Définir le nom du régulateur… |  |  |
| `Set Regulator's Password...` | Définir le mot de passe du régulateur… |  |  |
| `Set Serial Number...` | Définir le numéro de série… |  |  |
| `Set System Clock...` | Régler l’horloge du système… |  |  |
| `Set System Gain...` | Définir le gain du système… |  |  |
| `Slow Rate Data` | Données à cadence lente |  |  |
| `Slow=9` | Lent=9 |  |  |
| `System Gain:` | Gain du système : |  |  |
| `System not initialized` | Système non initialisé |  |  |
| `The connection was refused by the regulator '%1'. Make sure the regulator is running and confirm the host name and port settings.` | La connexion a été refusée par le régulateur '%1'. Assurez-vous que le régulateur est en service, puis vérifiez le nom d’hôte et les paramètres de port. |  |  |
| `The following error occurred connecting to regulator '%1': %2.` | L’erreur suivante s’est produite lors de la connexion au régulateur '%1' : %2. |  |  |
| `The name cannot be empty.` | Le nom ne peut pas être vide. |  |  |
| `The name cannot contain %1, because it is used in the names of the files downloaded from this regulator.` | Le nom ne peut pas contenir %1, car il est utilisé dans les noms des fichiers téléchargés depuis ce régulateur. |  |  |
| `The name cannot contain control characters, because it is used in the names of the files downloaded from this regulator.` | Le nom ne peut pas contenir de caractères de contrôle, car il est utilisé dans les noms des fichiers téléchargés depuis ce régulateur. |  |  |
| `The name cannot end with a '.'` | Le nom ne peut pas se terminer par '.' |  |  |
| `The requested device operation is not supported or prohibited by the running operating system.` | L’opération demandée sur l’appareil n’est pas prise en charge ou est interdite par le système d’exploitation en cours d’exécution. |  |  |
| `This error occurs when an operation is executed that can only be successfully performed if the device is open.` | Cette erreur se produit lorsqu’une opération qui exige que l’appareil soit ouvert est exécutée. |  |  |
| `This session has been idle and is about to time out.\n\nThe regulator will be disconnected in %1 seconds unless you continue.` | Cette session est restée inactive et est sur le point d’expirer.\n\nLe régulateur sera déconnecté dans %1 secondes, sauf si vous poursuivez. |  |  |
| `Time Stamp Transcript?` | Horodater le journal de session ? |  |  |
| `toolBar` | toolBar |  |  |
| `Transcript` | Journal de session | TERM: « transcript » rendered as « journal de session » throughout (a literal « transcription » reads wrong for a scrolling command/response log). Confirm; it is used as a pane title, a menu and a toolbar button. |  |
| `UART Settings...` | Paramètres UART… |  |  |
| `USB` | USB |  |  |
| `View` | Affichage |  |  |
| `View EEPROM Contents...` | Afficher le contenu de l’EEPROM… |  |  |
| `View Regulator Information?` | Afficher les informations du régulateur ? |  |  |
| `View Regulator Status?` | Afficher l’état du régulateur ? |  |  |
| `View Transcript in Separate Window?` | Afficher le journal de session dans une fenêtre distincte ? | LENGTH: 34 chars becomes 58 for a checkable menu item. |  |
| `View Transcript?` | Afficher le journal de session ? |  |  |
| `Voltage Calibration Settings...` | Paramètres d’étalonnage de tension… |  |  |
| `Voltage Controller Settings...` | Paramètres du contrôleur de tension… | TERM: « contrôleur de tension » kept distinct from « régulateur » (the whole unit); the English distinguishes Voltage Controller from Regulator. Confirm. |  |
| `WARNING: %1` | AVERTISSEMENT : %1 | LENGTH: « WARNING » becomes « AVERTISSEMENT » on every warning line of the journal pane. |  |
| `Would you like to disconnect from '%1'` | Souhaitez-vous vous déconnecter de '%1' | CHECK: the English has no question mark; kept as-is, so no « ? » is added. |  |
| `Would you like to revert to Basic Mode?` | Souhaitez-vous revenir au mode de base ? |  |  |

## Connected window - status bar (10)

| Original (English) | Translation (fr-FR) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `Auto Refresh` | Actualisation auto | LENGTH: shortened deliberately — « Actualisation automatique » (25) is too long for a status-bar cell. |  |
| `Auto Refresh` | Actualisation auto | LENGTH: shortened deliberately — « Actualisation automatique » (25) is too long for a status-bar cell. |  |
| `Connection` | Connexion |  |  |
| `Connection` | Connexion |  |  |
| `Faults` | Défauts |  |  |
| `Faults` | Défauts |  |  |
| `Regulating` | Régulation |  |  |
| `Regulating` | Régulation |  |  |
| `Regulator` | Régulateur |  |  |
| `Regulator` | Régulateur |  |  |

## Connection editor dialog (22)

| Original (English) | Translation (fr-FR) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `...` | ... | CHECK: the « ... » browse-button label is left verbatim (Qt Designer widget text, not prose). |  |
| `000.000.000.000;_` | 000.000.000.000;_ | CHECK: Qt input mask, left verbatim — the « ;_ » is the mask’s blank-character syntax, not punctuation. |  |
| `A Bluetooth Device must be selected.` | Un appareil Bluetooth doit être sélectionné. |  |  |
| `Comm Port must be set.` | Le port de communication doit être renseigné. |  |  |
| `Comm Port:` | Port de communication : |  |  |
| `Direct Bluetooth Connection` | Connexion Bluetooth directe |  |  |
| `Edit/Create Regulator Connection` | Modifier/créer une connexion au régulateur |  |  |
| `Host Name` | Nom d’hôte |  |  |
| `Host Name:` | Nom d’hôte : |  |  |
| `Invalid IP Address: %1` | Adresse IP non valide : %1 |  |  |
| `Invalid Port: %1` | Port non valide : %1 |  |  |
| `IP Address` | Adresse IP |  |  |
| `IP Address or Hostname must be set.` | L’adresse IP ou le nom d’hôte doit être renseigné. |  |  |
| `IP Address:` | Adresse IP : |  |  |
| `Is USB/RS-232 Serial Port (Not Bluetoooth)?` | S’agit-il d’un port série USB/RS-232 (et non Bluetooth) ? | CHECK: the English misspells « Bluetoooth » ; corrected in the French. |  |
| `Please select a local or remote connection` | Veuillez sélectionner une connexion locale ou distante |  |  |
| `Port:` | Port : |  |  |
| `Regulator name must be set.` | Le nom du régulateur doit être renseigné. |  |  |
| `Regulator Name:` | Nom du régulateur : |  |  |
| `Selected Device:` | Appareil sélectionné : |  |  |
| `Serial Port Connection` | Connexion par port série |  |  |
| `TCP/IP Connection:` | Connexion TCP/IP : |  |  |

## Connection status and errors (19)

| Original (English) | Translation (fr-FR) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `%1 commands in a row went unanswered` | %1 commandes consécutives sont restées sans réponse |  |  |
| `115.2k` | 115.2k |  |  |
| `230.4k` | 230.4k |  |  |
| `38.4k` | 38.4k |  |  |
| `57.6k` | 57.6k |  |  |
| `Cannot log back in to the regulator. Status polling has stopped - please disconnect and reconnect.` | Impossible de se reconnecter au régulateur. L’interrogation de l’état est arrêtée - déconnectez-vous puis reconnectez-vous. |  |  |
| `Cannot make sense of the regulator's replies. Status polling has stopped - please disconnect and reconnect.` | Les réponses du régulateur sont incompréhensibles. L’interrogation de l’état est arrêtée - déconnectez-vous puis reconnectez-vous. |  |  |
| `Hardware Flow Control` | Contrôle de flux matériel |  |  |
| `No Flow Control` | Aucun contrôle de flux |  |  |
| `nothing has come back for %1 seconds` | aucune réponse depuis %1 secondes |  |  |
| `Paired` | Appairé |  |  |
| `Paired with Authorization` | Appairé avec autorisation |  |  |
| `Serial Port` | Port série |  |  |
| `Software Flow Control` | Contrôle de flux logiciel |  |  |
| `The connection to regulator '%1' has been lost - %2. Check the link and reconnect. If the regulator is still holding the previous session, reconnecting can take a few minutes.` | La connexion au régulateur '%1' a été perdue - %2. Vérifiez la liaison et reconnectez-vous. Si le régulateur conserve encore la session précédente, la reconnexion peut prendre quelques minutes. |  |  |
| `the login was not answered` | la connexion est restée sans réponse |  |  |
| `The regulator has stopped responding - %1 commands in a row went unanswered.` | Le régulateur ne répond plus - %1 commandes consécutives sont restées sans réponse. |  |  |
| `The regulator is responding again.` | Le régulateur répond à nouveau. |  |  |
| `Unpaired` | Non appairé |  |  |

## Debug logging dialog (13)

| Original (English) | Translation (fr-FR) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `<Filter>` | &lt;Filtre&gt; |  |  |
| `...` | ... | CHECK: the « ... » browse-button label is left verbatim (Qt Designer widget text, not prose). |  |
| `Append to Log File?` | Ajouter au fichier journal ? |  |  |
| `Check All` | Tout cocher |  |  |
| `Log File` | Fichier journal |  |  |
| `Log File:` | Fichier journal : |  |  |
| `Log Files (*.log);;All Files (*.*)` | Fichiers journaux (*.log);;Tous les fichiers (*.*) |  |  |
| `Logging Categories:` | Catégories de journalisation : |  |  |
| `Logging Category` | Catégorie de journalisation |  |  |
| `Select Logging Categories` | Sélectionner les catégories de journalisation |  |  |
| `Show Qt Categories?` | Afficher les catégories Qt ? |  |  |
| `Uncheck All` | Tout décocher |  |  |
| `Uncheck All Debug` | Décocher tout le débogage |  |  |

## EEPROM contents viewer (9)

| Original (English) | Translation (fr-FR) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `<ADDRESS>` | &lt;ADRESSE&gt; |  |  |
| `<VALUE>` | &lt;VALEUR&gt; |  |  |
| `0x00 0 ` | 0x00 0  |  |  |
| `0x00000000 ` | 0x00000000  |  |  |
| `Address:` | Adresse : |  |  |
| `EEPROM Contents` | Contenu de l’EEPROM |  |  |
| `EEPROM Contents:` | Contenu de l’EEPROM : |  |  |
| `EEPROM Contents: Loading...` | Contenu de l’EEPROM : chargement… |  |  |
| `Value:` | Valeur : |  |  |

## File download progress (20)

| Original (English) | Translation (fr-FR) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `%1 of %2%3 (%4%)` | %1 sur %2%3 (%4 %) |  |  |
| `%1%2` | %1%2 |  |  |
| `%1h %2m` | %1 h %2 min | CHECK: French abbreviates minutes as « min », not « m » ; rows 830-832 feed the « Il reste environ %1 » string (row 233). |  |
| `%1m %2s` | %1 min %2 s |  |  |
| `%1s` | %1 s |  |  |
| `0.%1 seconds` | 0,%1 seconde |  |  |
| `Abort Download` | Interrompre le téléchargement | LENGTH: « Abort Download » (14) becomes 29 on a dialog button; « Interrompre » alone if it clips. |  |
| `About %1 remaining` | Il reste environ %1 | AGREEMENT: %1 is a duration built from rows 45-51 (« 2 heures et 3 minutes », « 1 seconde »). « Il reste environ %1 » is used instead of « Environ %1 restant(e)(s) » so no agreement has to be resolved. |  |
| `Could not open file` | Impossible d’ouvrir le fichier |  |  |
| `Could not open file '%1' for write.  Please check Permissions` | Impossible d’ouvrir le fichier '%1' en écriture.  Veuillez vérifier les autorisations |  |  |
| `Downloading File` | Téléchargement du fichier |  |  |
| `Downloading File '%1'` | Téléchargement du fichier '%1' |  |  |
| `Downloading file '%1'` | Téléchargement du fichier '%1' |  |  |
| `Error downloading file` | Erreur lors du téléchargement du fichier |  |  |
| `Finishing up...` | Finalisation… |  |  |
| `less than a second` | moins d’une seconde |  |  |
| `Please Select Download Directory` | Sélectionnez le dossier de téléchargement |  |  |
| `Seconds Remaining until Timeout:` | Secondes restantes avant expiration : |  |  |
| `Seconds Remaining until Timeout: %1 seconds` | Secondes restantes avant expiration : %1 secondes |  |  |
| `Timeout while downloading` | Délai dépassé pendant le téléchargement |  |  |

## Main window - menus, toolbar and buttons (23)

| Original (English) | Translation (fr-FR) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `  #  ` |   #   |  |  |
| `&About` | À &amp;propos |  |  |
| `&Connect` | Se &amp;connecter |  |  |
| `&Disconnect from Selected Regulator` | Se &amp;déconnecter du régulateur sélectionné |  |  |
| `&Exit` | &amp;Quitter |  |  |
| `&File` | &amp;Fichier |  |  |
| `&Help` | &amp;Aide |  |  |
| `&Regulator` | &amp;Régulateur |  |  |
| `...` | ... | CHECK: the « ... » browse-button label is left verbatim (Qt Designer widget text, not prose). |  |
| `Add a new Regulator` | Ajouter un régulateur |  |  |
| `Connect to Selected Regulator` | Se connecter au régulateur sélectionné |  |  |
| `Debug Logging...` | Journalisation de débogage… |  |  |
| `Disconnect from Selected Regulator` | Se déconnecter du régulateur sélectionné |  |  |
| `Edit Selected Regulator` | Modifier le régulateur sélectionné |  |  |
| `Enable &Advanced Mode...` | Activer le mode &amp;avancé… |  |  |
| `Enable &Basic Mode` | Activer le mode de &amp;base |  |  |
| `MainWindow` | MainWindow |  |  |
| `Regulator Name Filter` | Filtre sur le nom du régulateur |  |  |
| `Regulators:` | Régulateurs : |  |  |
| `Remove Selected Regulator` | Supprimer le régulateur sélectionné |  |  |
| `Settings` | Paramètres |  |  |
| `Settings...` | Paramètres… |  |  |
| `toolBar` | toolBar |  |  |

## Main window - regulator table column headers (10)

| Original (English) | Translation (fr-FR) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `   #   ` |    #    |  |  |
| `Color` | Couleur |  |  |
| `Connection Status` | État de la connexion |  |  |
| `Connection Type` | Type de connexion |  |  |
| `Last Connection` | Dernière connexion |  |  |
| `Not Connected` | Non connecté |  |  |
| `Port or IPAddress` | Port ou adresse IP |  |  |
| `Regulating Status` | État de régulation |  |  |
| `Regulator Name` | Nom du régulateur |  |  |
| `Regulator Status` | État du régulateur |  |  |

## Numeric entry dialogs (6)

| Original (English) | Translation (fr-FR) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `Enter Integer` | Saisir un nombre entier |  |  |
| `Enter Integer` | Saisir un nombre entier |  |  |
| `Integer` | Nombre entier |  |  |
| `Integer` | Nombre entier |  |  |
| `Max` | Max |  |  |
| `Min` | Min |  |  |

## Other (QObject) (3)

| Original (English) | Translation (fr-FR) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `%1 - ` | %1 -  |  |  |
| `Cmd: %1 - Error Count: %2` | Cmd : %1 - Nombre d’erreurs : %2 |  |  |
| `Warning - Consecutive command ran too quickly '%1'` | Avertissement - commande consécutive exécutée trop rapidement '%1' |  |  |

## Parameter file editor (59)

| Original (English) | Translation (fr-FR) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `+ or - followed by 2 digits` | + ou - suivi de 2 chiffres |  |  |
| `...` | ... | CHECK: the « ... » browse-button label is left verbatim (Qt Designer widget text, not prose). |  |
| `0 or 1` | 0 ou 1 |  |  |
| `1 digit` | 1 chiffre |  |  |
| `2 digits` | 2 chiffres |  |  |
| `3 digits` | 3 chiffres |  |  |
| `4 digits` | 4 chiffres |  |  |
| `Active Voltage Target` | Consigne de tension active |  |  |
| `All Disabled on Any Fault` | Toutes désactivées en cas de défaut |  |  |
| `Amperage Rating LSB` | Courant nominal LSB |  |  |
| `Amperage Rating MSB` | Courant nominal MSB |  |  |
| `B or + or - followed by 2 digits` | B ou + ou - suivi de 2 chiffres |  |  |
| `Current Data` | Données actuelles |  |  |
| `Description` | Description |  |  |
| `Edit Parameter File` | Modifier le fichier de paramètres |  |  |
| `End Position` | Position de fin |  |  |
| `Error Message:` | Message d’erreur : |  |  |
| `Expected Data` | Données attendues |  |  |
| `Externally Controlled Select (1 or 2)` | Sélection commandée en externe (1 ou 2) |  |  |
| `File '%1' content was not 57 characters` | Le contenu du fichier '%1' ne comportait pas 57 caractères |  |  |
| `File '%1' Could not be Opened.` | Impossible d’ouvrir le fichier '%1'. |  |  |
| `Frequency` | Fréquence |  |  |
| `Ignored 21 bytes` | 21 octets ignorés |  |  |
| `Ignored 3 bytes` | 3 octets ignorés |  |  |
| `Ignored 4 bytes` | 4 octets ignorés |  |  |
| `Invalid character/text at position %1. Expected '%2', Got '%3'` | Caractère ou texte non valide à la position %1. Attendu '%2', obtenu '%3' |  |  |
| `Invalid Parameter File` | Fichier de paramètres non valide |  |  |
| `Open Parameter File` | Ouvrir le fichier de paramètres |  |  |
| `Over Current Fault Count Limit` | Limite du nombre de défauts de surintensité | LENGTH: 30 chars becomes 43 in a parameter-table description column. |  |
| `Over Voltage Limit` | Limite de surtension |  |  |
| `Over Voltage Protection Limit` | Limite de protection contre les surtensions | LENGTH: 29 chars becomes 43 in a status-tree label column. |  |
| `P followed by any 1 byte` | P suivi de n’importe quel octet |  |  |
| `Parameter File` | Fichier de paramètres |  |  |
| `Parameter File:` | Fichier de paramètres : |  |  |
| `Phase Voltage Offset` | Décalage de tension de phase |  |  |
| `Power Interactive Regulation` | Régulation interactive de puissance |  |  |
| `Power Interactive Regulation Delta Voltage` | Écart de tension de la régulation interactive de puissance | LENGTH: nearly doubles (42 to 58) in a table column. |  |
| `Power Interactive Regulation NULL Voltage` | Tension nulle de la régulation interactive de puissance | CHECK: « NULL » is written in capitals in the English and may be a literal parameter name rather than the adjective; translated as « nulle » here, following pt-PT. |  |
| `Power Interactive Regulation Time Constant` | Constante de temps de la régulation interactive de puissance | LENGTH: 42 chars becomes 60 in a table column. |  |
| `Prefix` | Préfixe |  |  |
| `Ramp Rate` | Vitesse de rampe | TERM: « Ramp Rate » as « vitesse de rampe ». « Gradient » is the other candidate; confirm the regulator’s own French wording. |  |
| `Ramp to Vin` | Rampe vers Vin |  |  |
| `Raw Data` | Données brutes |  |  |
| `Reset To Current` | Rétablir l’actuel |  |  |
| `Reset to Current Parameter File` | Rétablir le fichier de paramètres actuel |  |  |
| `Reset to Default` | Rétablir par défaut | CHECK: deliberately not « Rétablir le défaut » — in this application « défaut » means fault, and the short button sits next to fault-related controls. |  |
| `Reset to Default Parameter File` | Rétablir le fichier de paramètres par défaut |  |  |
| `Save Parameter File` | Enregistrer le fichier de paramètres |  |  |
| `Select Parameter File` | Sélectionner un fichier de paramètres |  |  |
| `SPARE` | SPARE |  |  |
| `Start Position` | Position de début |  |  |
| `System Gain` | Gain du système |  |  |
| `Target Voltage 1` | Tension de consigne 1 | TERM: « Target Voltage » rendered as « tension de consigne », matching « consigne » chosen for Set point at row 54. « Tension cible » is the literal alternative if the reviewer prefers it. |  |
| `Target Voltage 2` | Tension de consigne 2 |  |  |
| `Text Files (*.txt);;All Files (*.*)` | Fichiers texte (*.txt);;Tous les fichiers (*.*) | CHECK: Qt file-filter syntax — the « ;; » separator and the (*.txt)/(*.*) patterns are code and take no French spacing. |  |
| `Under Voltage Limit` | Limite de sous-tension |  |  |
| `Voltage Regulation Disabled` | Régulation de tension désactivée |  |  |
| `Voltage Setpoint 1` | Consigne de tension 1 |  |  |
| `Voltage Setpoint 2` | Consigne de tension 2 |  |  |

## Password and credential prompts (17)

| Original (English) | Translation (fr-FR) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `...` | ... | CHECK: the « ... » browse-button label is left verbatim (Qt Designer widget text, not prose). |  |
| `...` | ... | CHECK: the « ... » browse-button label is left verbatim (Qt Designer widget text, not prose). |  |
| `Access to %1 requires the correct password to be entered.` | L’accès à %1 nécessite la saisie du mot de passe correct. |  |  |
| `Confirm Password:` | Confirmer le mot de passe : |  |  |
| `Confirmation password does not match` | Le mot de passe de confirmation ne correspond pas |  |  |
| `Current password is not correct` | Le mot de passe actuel est incorrect |  |  |
| `Current Password:` | Mot de passe actuel : |  |  |
| `Enter Credentials` | Saisir les identifiants |  |  |
| `Enter Password` | Saisir le mot de passe |  |  |
| `Enter Password:` | Saisir le mot de passe : |  |  |
| `Incorrect Password` | Mot de passe incorrect |  |  |
| `Incorrect password entered, Access to %1 denied.` | Mot de passe incorrect ; l’accès à %1 est refusé. |  |  |
| `New password does not satisfy length criteria` | Le nouveau mot de passe ne respecte pas le critère de longueur |  |  |
| `Password Required` | Mot de passe requis |  |  |
| `Password Required for %1` | Mot de passe requis pour %1 |  |  |
| `Password:` | Mot de passe : |  |  |
| `Username:` | Nom d’utilisateur : |  |  |

## Regulator Information panel (18)

| Original (English) | Translation (fr-FR) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| ` - Not Connected` |  - non connecté |  |  |
| `<Unknown>` | &lt;Inconnu&gt; |  |  |
| `...` | ... | CHECK: the « ... » browse-button label is left verbatim (Qt Designer widget text, not prose). |  |
| `Connected Via:` | Connecté via : |  |  |
| `GroupBox` | GroupBox |  |  |
| `Invalid Serial Number` | Numéro de série non valide |  |  |
| `Name:` | Nom : |  |  |
| `Phase Firmware Version:` | Version du micrologiciel de phase : |  |  |
| `Product:` | Produit : |  |  |
| `Regulating Status:` | État de régulation : |  |  |
| `Regulator Information` | Informations du régulateur |  |  |
| `Regulator Information:` | Informations du régulateur : |  |  |
| `Regulator's System Clock:` | Horloge système du régulateur : |  |  |
| `Serial Number (12 Characters):` | Numéro de série (12 caractères) : |  |  |
| `Serial Number:` | Numéro de série : |  |  |
| `Set Serial Number` | Définir le numéro de série |  |  |
| `System Firmware Version and Compilation Date:` | Version du micrologiciel système et date de compilation : | LENGTH: 45 chars becomes 56 on a form label; « Micrologiciel système et date de compilation : » if it crowds the field. |  |
| `The serial number must have 12 characters` | Le numéro de série doit comporter 12 caractères |  |  |

## Regulator status and messages (21)

| Original (English) | Translation (fr-FR) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `    File #: %1` |     Fichier n° : %1 | CHECK: « # » rendered as « n° » ; the four leading spaces of the English source are preserved. |  |
| ` - Regulator clock off by %1` |  - horloge du régulateur décalée de %1 |  |  |
| ` - Running Command` |  - exécution d’une commande |  |  |
| ` and ` |  et  |  |  |
| `%1 Hour` | %1 heure |  |  |
| `%1 Hours` | %1 heures |  |  |
| `%1 Minute` | %1 minute |  |  |
| `%1 Minutes` | %1 minutes |  |  |
| `%1 Second` | %1 seconde |  |  |
| `%1 Seconds` | %1 secondes |  |  |
| `Enabled` | Activé |  |  |
| `Firmware must be updated to support Voltage Calibration` | Le micrologiciel doit être mis à jour pour prendre en charge l’étalonnage de tension |  |  |
| `Firmware must be upgraded to V17 or later to support Voltage Calibration` | Le micrologiciel doit être mis à niveau vers la V17 ou une version ultérieure pour prendre en charge l’étalonnage de tension | TERM: « étalonnage de tension » for Voltage Calibration (vs « calibrage »). Confirm the term used on the instrument itself. |  |
| `Number of SD Card files: %1` | Nombre de fichiers sur la carte SD : %1 |  |  |
| `Regulation Information:` | Informations de régulation : |  |  |
| `Regulator Will Reboot` | Le régulateur va redémarrer |  |  |
| `Target Voltage 1` | Tension de consigne 1 | TERM: « Target Voltage » rendered as « tension de consigne », matching « consigne » chosen for Set point at row 54. « Tension cible » is the literal alternative if the reviewer prefers it. |  |
| `Target Voltage 2` | Tension de consigne 2 |  |  |
| `This command will force the regulator to reboot. After it reboots and the green LED on the regulator comes on, you will need to reconnect.` | Cette commande force le redémarrage du régulateur. Une fois le redémarrage effectué et la LED verte du régulateur allumée, vous devrez vous reconnecter. |  |  |
| `Unknown` | Inconnu |  |  |
| `Voltage Control must be set to either Set point 1 or 2` | Le contrôle de tension doit être réglé sur la consigne 1 ou 2 | TERM: « consigne » for set point, the usual French regulation term. Confirm against the regulator’s own French panel wording. |  |

## Regulator status trees (59)

| Original (English) | Translation (fr-FR) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `Active Voltage Target` | Consigne de tension active |  |  |
| `ADC Cal Error` | Erreur d’étalonnage ADC |  |  |
| `All Phases Disabled on Failure in Any Phase` | Toutes les phases désactivées en cas de défaillance d’une phase | LENGTH: 43 chars becomes 63 in a status-tree label column. |  |
| `Amperage Rating (A)` | Courant nominal (A) |  |  |
| `Baud Rate` | Débit en bauds |  |  |
| `Connection:` | Connexion : |  |  |
| `Current (A)` | Courant (A) |  |  |
| `Delta Voltage (V)` | Écart de tension (V) |  |  |
| `Fault Code` | Code de défaut |  |  |
| `Flow Control` | Contrôle de flux |  |  |
| `Flux Sensor` | Capteur de flux |  |  |
| `Form` | Form |  |  |
| `Form` | Form |  |  |
| `Frequency` | Fréquence |  |  |
| `No` | Non |  |  |
| `Null Voltage (V)` | Tension nulle (V) |  |  |
| `Over Current Fault Count` | Nombre de défauts de surintensité |  |  |
| `Over Current Fault Count` | Nombre de défauts de surintensité |  |  |
| `Over Current Fault in Reset Delay` | Défaut de surintensité en délai de réarmement | AMBIGUOUS: read as « the over-current fault is within its reset delay » (waiting to be re-armed), not « a fault occurred during the reset delay ». Confirm with the firmware behaviour. |  |
| `Over Current Fault Limit` | Limite de défauts de surintensité |  |  |
| `Over Temperature` | Température excessive |  |  |
| `Over Voltage Limit` | Limite de surtension |  |  |
| `Over Voltage Protection Limit` | Limite de protection contre les surtensions | LENGTH: 29 chars becomes 43 in a status-tree label column. |  |
| `Phase %1` | Phase %1 |  |  |
| `Phase Lock Loop not Locked` | Boucle à verrouillage de phase non verrouillée | LENGTH: 26 chars becomes 46 in a fault tree; « PLL non verrouillée » is the short form if it clips. |  |
| `Power Interactive Regulation Status` | État de la régulation interactive de puissance |  |  |
| `Power Interactive Regulation Status` | État de la régulation interactive de puissance |  |  |
| `Ramp Rate` | Vitesse de rampe | TERM: « Ramp Rate » as « vitesse de rampe ». « Gradient » is the other candidate; confirm the regulator’s own French wording. |  |
| `Reaction Time (s)` | Temps de réaction (s) |  |  |
| `Regulating Status` | État de régulation |  |  |
| `Regulating:` | Régulation : |  |  |
| `Regulator at Maximum Boost or Buck` | Régulateur au maximum d’élévation ou d’abaissement | TERM: boost/buck rendered as élévation/abaissement (survolteur/dévolteur is the other French pair). Confirm which the utility audience uses. |  |
| `Regulator Faults:` | Défauts du régulateur : |  |  |
| `Regulator Ramping` | Régulateur en rampe |  |  |
| `Regulator:` | Régulateur : |  |  |
| `SCR or Gate Drive Faults` | Défauts du SCR ou de la commande de gâchette |  |  |
| `SD Card Status` | État de la carte SD |  |  |
| `Settings` | Paramètres |  |  |
| `Settings` | Paramètres |  |  |
| `Status:` | État : |  |  |
| `System Gain` | Gain du système |  |  |
| `Target Voltage 1` | Tension de consigne 1 | TERM: « Target Voltage » rendered as « tension de consigne », matching « consigne » chosen for Set point at row 54. « Tension cible » is the literal alternative if the reviewer prefers it. |  |
| `Target Voltage 2` | Tension de consigne 2 |  |  |
| `Temp Sensor or Fan` | Capteur de température ou ventilateur |  |  |
| `Temperature (°C)` | Température (°C) |  |  |
| `UART 1` | UART 1 |  |  |
| `UART 1` | UART 1 |  |  |
| `UART 1` | UART 1 |  |  |
| `UART 2` | UART 2 |  |  |
| `UART 2` | UART 2 |  |  |
| `UART 2` | UART 2 |  |  |
| `Under Voltage Limit` | Limite de sous-tension |  |  |
| `VCC or Fuse` | VCC ou fusible |  |  |
| `Vin/Vout out of limit` | Vin/Vout hors limites |  |  |
| `Voltage Calibration Offset` | Décalage d’étalonnage de tension |  |  |
| `Voltage In (V)` | Tension d’entrée (V) |  |  |
| `Voltage Out (V)` | Tension de sortie (V) |  |  |
| `Voltage Regulation Disabled` | Régulation de tension désactivée |  |  |
| `Yes` | Oui |  |  |

## SD card download dialog (36)

| Original (English) | Translation (fr-FR) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `...` | ... | CHECK: the « ... » browse-button label is left verbatim (Qt Designer widget text, not prose). |  |
| `2 Days Ago` | Il y a 2 jours |  |  |
| `3 Days Ago` | Il y a 3 jours |  |  |
| `4 Days Ago` | Il y a 4 jours |  |  |
| `5 Days Ago` | Il y a 5 jours |  |  |
| `6 Days Ago` | Il y a 6 jours |  |  |
| `7 Days Ago` | Il y a 7 jours |  |  |
| `A file is still downloading. Cancel it in the progress window before closing this one.` | Un fichier est encore en cours de téléchargement. Interrompez-le dans la fenêtre de progression avant de fermer celle-ci. |  |  |
| `April` | Avril |  |  |
| `August` | Août |  |  |
| `Command` | Commande |  |  |
| `Data will not be recorded or updated during file downloads` | Aucune donnée ne sera enregistrée ni actualisée pendant le téléchargement des fichiers |  |  |
| `December` | Décembre |  |  |
| `Download in progress` | Téléchargement en cours |  |  |
| `Download not started` | Téléchargement non démarré |  |  |
| `Fault Log` | Journal des défauts |  |  |
| `February` | Février |  |  |
| `File Name` | Nom du fichier |  |  |
| `January` | Janvier | CHECK: French month names are normally lower case; capitalised here because they stand alone as list/group labels alongside « Aujourd’hui », « Hier ». Lower-case them if they appear mid-sentence. |  |
| `July` | Juillet |  |  |
| `June` | Juin |  |  |
| `March` | Mars |  |  |
| `May` | Mai |  |  |
| `Modification Date` | Date de modification |  |  |
| `Name` | Nom |  |  |
| `November` | Novembre |  |  |
| `October` | Octobre |  |  |
| `SD Card Files` | Fichiers de la carte SD |  |  |
| `Select` | Sélectionner |  |  |
| `September` | Septembre |  |  |
| `Size (Bytes)` | Taille (octets) |  |  |
| `The regulator is still busy with the previous transfer. Please try again in a moment.` | Le régulateur est encore occupé par le transfert précédent. Veuillez réessayer dans un instant. |  |  |
| `This Month` | Ce mois-ci |  |  |
| `Today` | Aujourd’hui |  |  |
| `Waiting for regulator...` | Attente du régulateur… |  |  |
| `Yesterday` | Hier |  |  |

## Settings dialog (68)

| Original (English) | Translation (fr-FR) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `      This setting is also the time between consecutive commands.` |       Ce paramètre correspond aussi au délai entre deux commandes consécutives. | CHECK: the six leading spaces are in the English source and are preserved (the line is indented under the field above). |  |
| ` Amps` |  ampères |  |  |
| ` s` |  s |  |  |
| ` Seconds` |  secondes |  |  |
| ` Volts` |  volts |  |  |
| `<the system Downloads folder>` | &lt;le dossier Téléchargements du système&gt; |  |  |
| `+` | + |  |  |
| `-` | - |  |  |
| `1` | 1 |  |  |
| `Advanced user password:` | Mot de passe utilisateur avancé : |  |  |
| `Amperage Rating:` | Courant nominal : |  |  |
| `As Needed` | Selon les besoins |  |  |
| `Asked for when the tool starts, and by Settings > Enable Advanced Mode. Takes effect immediately.` | Demandé au démarrage de l’outil et par Paramètres &gt; Activer le mode avancé. Prend effet immédiatement. |  |  |
| `Automatically Refresh Status?` | Actualiser automatiquement l’état ? |  |  |
| `Change Advanced User Password` | Modifier le mot de passe utilisateur avancé |  |  |
| `Change Advanced User Password...` | Modifier le mot de passe utilisateur avancé… |  |  |
| `Choose the language the tool is displayed in. The change takes effect immediately; any regulator windows that are already open keep their current language until they are reopened.` | Choisissez la langue d’affichage de l’outil. Le changement prend effet immédiatement ; les fenêtres de régulateur déjà ouvertes conservent leur langue actuelle jusqu’à leur réouverture. |  |  |
| `Command Timeout:` | Délai d’expiration des commandes : | LENGTH: 16 chars becomes 34 on a settings-form label. |  |
| `Default Regulator Settings` | Paramètres par défaut du régulateur |  |  |
| `Default Time Zone` | Fuseau horaire par défaut |  |  |
| `Default View Settings` | Paramètres d’affichage par défaut |  |  |
| `Download Timeout:` | Délai d’expiration des téléchargements : | LENGTH: 17 chars becomes 40 on a settings-form label. |  |
| `Downloads` | Téléchargements |  |  |
| `External Voltage Setpoint Select (1 or 2)` | Sélection externe de la consigne de tension (1 ou 2) |  |  |
| `Fast` | Rapide |  |  |
| `Fast:` | Rapide : |  |  |
| `Folder for Downloaded Files` | Dossier des fichiers téléchargés |  |  |
| `Language` | Langue |  |  |
| `Medium` | Moyen |  |  |
| `Medium:` | Moyen : |  |  |
| `NULL Voltage at Zero kW:` | Tension nulle à zéro kW : |  |  |
| `Power Interactive Regulation` | Régulation interactive de puissance |  |  |
| `Power Interactive Regulation Settings` | Paramètres de régulation interactive de puissance |  |  |
| `Ramp to Vin` | Rampe vers Vin |  |  |
| `Refresh for Regulator Clock Time` | Actualisation de l’heure du régulateur |  |  |
| `Refresh for Regulator Faults and Voltages:` | Actualisation des défauts et des tensions du régulateur : | LENGTH: 42 chars becomes 56 on a settings-form label. |  |
| `Refresh for SD Card Files:` | Actualisation des fichiers de la carte SD : |  |  |
| `Refresh for Voltage Calibration Status:` | Actualisation de l’état d’étalonnage de tension : |  |  |
| `Refresh Gain Values:` | Actualisation des valeurs de gain : |  |  |
| `Refresh Rate Parameter File Information:` | Fréquence d’actualisation des informations du fichier de paramètres : | LENGTH: 40 chars becomes 68; consider « Actualisation du fichier de paramètres : » if the label column is fixed. |  |
| `Refresh Settings` | Paramètres d’actualisation |  |  |
| `Refresh Times:` | Intervalles d’actualisation : |  |  |
| `Refresh UART Settings:` | Actualisation des paramètres UART : |  |  |
| `Regulator Setting Defaults` | Valeurs par défaut des paramètres du régulateur | LENGTH: 26 chars becomes 47 as a group-box title. |  |
| `Regulator:` | Régulateur : |  |  |
| `Require Password to Enter Advanced Mode?` | Exiger un mot de passe pour passer en mode avancé ? |  |  |
| `Save downloaded files to:` | Enregistrer les fichiers téléchargés dans : |  |  |
| `Security` | Sécurité |  |  |
| `Settings` | Paramètres |  |  |
| `Setup UARTs` | Configurer les UART |  |  |
| `Show password` | Afficher le mot de passe |  |  |
| `Slow` | Lent |  |  |
| `Slow:` | Lent : |  |  |
| `Start in Advanced Mode?` | Démarrer en mode avancé ? |  |  |
| `The Advanced user password has been changed.` | Le mot de passe utilisateur avancé a été modifié. |  |  |
| `Time Constant:` | Constante de temps : |  |  |
| `Timeout Settings` | Paramètres de délai d’expiration |  |  |
| `Timestamp Transcript?` | Horodater le journal de session ? |  |  |
| `Update Settings For All Regulators?` | Appliquer les paramètres à tous les régulateurs ? |  |  |
| `View Regulator Information?` | Afficher les informations du régulateur ? |  |  |
| `View Regulator Status?` | Afficher l’état du régulateur ? |  |  |
| `View Transcript in Sepeate Window?` | Afficher le journal de session dans une fenêtre distincte ? | CHECK: the English misspells « Sepeate » (separate); corrected in the French. |  |
| `View Transcript?` | Afficher le journal de session ? |  |  |
| `Voltage Control Settings` | Paramètres de contrôle de tension |  |  |
| `Voltage Delta:` | Écart de tension : |  |  |
| `Voltage Setpoint 1:` | Consigne de tension 1 : |  |  |
| `Voltage Setpoint 2:` | Consigne de tension 2 : |  |  |
| `±` | ± |  |  |

## Status and fault values - tables, trees and panels (128)

| Original (English) | Translation (fr-FR) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `(in multiphase models only) Indicates one of the phases has an open fuse or there is no VCC power. NOTE - a single phase model could not be communicating.` | (sur les modèles multiphasés uniquement) Indique que l’une des phases a un fusible ouvert ou qu’il n’y a pas d’alimentation VCC. REMARQUE - un modèle monophasé pourrait, lui, ne plus communiquer du tout. |  |  |
| `7A` | 7A |  |  |
| `9A` | 9A |  |  |
| `Active` | Actif |  |  |
| `B2` | B2 |  |  |
| `B8` | B8 |  |  |
| `BA` | BA |  |  |
| `Bound` | Lié |  |  |
| `CA` | CA |  |  |
| `CB` | CB |  |  |
| `Closing` | Fermeture en cours |  |  |
| `Command Transmission Error` | Erreur de transmission de commande |  |  |
| `Communication Error` | Erreur de communication |  |  |
| `Confirming Connection` | Confirmation de la connexion |  |  |
| `Connected` | Connecté |  |  |
| `Connecting` | Connexion en cours |  |  |
| `Data File downloaded - not implemented` | Fichier de données téléchargé - non implémenté |  |  |
| `DC` | DC |  |  |
| `Disabled` | Désactivé |  |  |
| `Disabled by Current >1.5X current rating - resets 15min after return to rated current` | Désactivé par un courant supérieur à 1,5× le courant nominal - réarmement 15 min après le retour au courant nominal | LENGTH: 84 chars becomes 115 in a fault-table cell. |  |
| `Disabled by Over Current` | Désactivé par surintensité |  |  |
| `Disabled by Over Temperature` | Désactivé par température excessive |  |  |
| `Disabled by switch (3 phase only)` | Désactivé par interrupteur (triphasé uniquement) |  |  |
| `Disabled by User` | Désactivé par l’utilisateur |  |  |
| `Disabled by User command` | Désactivé par commande de l’utilisateur |  |  |
| `Disabled by Voltage Issue` | Désactivé pour problème de tension |  |  |
| `Disconnected` | Déconnecté |  |  |
| `DS` | DS |  |  |
| `DU` | DU |  |  |
| `EA` | EA |  |  |
| `Enabled by User command - i.e. regulating` | Activé par commande de l’utilisateur, c’est-à-dire en régulation |  |  |
| `Error Processing Voltage and Fault Status` | Erreur lors du traitement de l’état des tensions et des défauts |  |  |
| `EU` | EU |  |  |
| `F4` | F4 |  |  |
| `F5` | F5 |  |  |
| `FA` | FA |  |  |
| `Failed` | Défaillant | AMBIGUOUS: « Failed » as a component state (paired with « Missing » at row 632), so « Défaillant », not « Échec » as in a failed operation. |  |
| `Failed or Missing` | Défaillant ou absent |  |  |
| `Fan Fault Cleared` | Défaut de ventilateur résolu |  |  |
| `Fault` | Défaut |  |  |
| `FB` | FB |  |  |
| `FC` | FC |  |  |
| `FD` | FD |  |  |
| `FE` | FE |  |  |
| `FLUX` | FLUX |  |  |
| `Flux Sensor Error  If sustained, it writes to F/L once per hour (this will increase the number of Over Current Faults from transformer saturations)` | Erreur du capteur de flux.  Si elle persiste, elle est inscrite dans F/L une fois par heure (ce qui augmentera le nombre de défauts de surintensité dus aux saturations du transformateur) | CHECK: F/L left as the firmware identifier (fault log). The double space after the first sentence is in the English source and is preserved. |  |
| `Getting System Info` | Récupération des informations système |  |  |
| `Host Found` | Hôte trouvé |  |  |
| `Host Lookup` | Recherche de l’hôte |  |  |
| `Indicates a fault caused by a SCR gate drive error` | Indique un défaut provoqué par une erreur de commande de gâchette SCR |  |  |
| `Indicates a flux sensor malfunction which could cause the transformer to saturate` | Indique un dysfonctionnement du capteur de flux susceptible de provoquer la saturation du transformateur |  |  |
| `Indicates an A to D calibration error during bootup or Voltage sensing error` | Indique une erreur d’étalonnage du convertisseur A/N au démarrage ou une erreur de mesure de tension | CHECK: « A to D » rendered as « A/N » (analogique-numérique), the usual French abbreviation. « A/D » is also seen in French datasheets — confirm which the manuals use. |  |
| `Indicates Flux Sensor faults (>12 per 1/2 Second Interval)` | Indique des défauts du capteur de flux (plus de 12 par intervalle d’une demi-seconde) |  |  |
| `Indicates full PWM in boost mode (i.e. limiting the ability to hold the setpoint)` | Indique une PWM au maximum en mode élévateur (ce qui limite la capacité à tenir la consigne) |  |  |
| `Indicates full PWM in buck mode (i.e. limiting the ability to hold the setpoint)` | Indique une PWM au maximum en mode abaisseur (ce qui limite la capacité à tenir la consigne) |  |  |
| `Indicates SCR or Gate Drive Faults (>12 per 1/2 Second Interval)` | Indique des défauts du SCR ou de la commande de gâchette (plus de 12 par intervalle d’une demi-seconde) |  |  |
| `Indicates the converter board is temporally in a over temperature state which will reset` | Indique que la carte du convertisseur est temporairement en état de température excessive, état qui se réarmera |  |  |
| `Indicates the Over Current Fault has cleared and returned to regulation` | Indique que le défaut de surintensité a été résolu et que la régulation a repris |  |  |
| `Indicates the regulator is in a state of maximum Boost or Buck` | Indique que le régulateur est au maximum d’élévation ou d’abaissement |  |  |
| `Indicates the regulator is in an over current fault reset delay` | Indique que le régulateur est dans un délai de réarmement sur défaut de surintensité |  |  |
| `Indicates there are no hardware faults and the regulator is not disabled i.e. regulating` | Indique qu’il n’y a aucun défaut matériel et que le régulateur n’est pas désactivé, c’est-à-dire qu’il régule |  |  |
| `Indicates there are no hardware faults but the regulator is disabled for various reasons indicated in the Aux Status string. The cause could be it was disabled by the user, or as the result of a fault condition which may clear and return to regulation, or it is in a timer mode where regulation is temporally disabled.` | Indique qu’il n’y a aucun défaut matériel, mais que le régulateur est désactivé pour diverses raisons indiquées dans la chaîne d’état auxiliaire. La cause peut être une désactivation par l’utilisateur, une condition de défaut susceptible de disparaître avec retour à la régulation, ou un mode temporisé dans lequel la régulation est temporairement désactivée. | CHECK: the English writes « temporally » where it means « temporarily » (also at row 712); translated as « temporairement ». |  |
| `Indicates Vin or Vout is out of range, either because of high or low line voltage, or possibly a voltage sensing circuit error.` | Indique que Vin ou Vout est hors plage, en raison d’une tension de ligne haute ou basse, ou éventuellement d’une erreur du circuit de mesure de tension. |  |  |
| `Input Power Loss` | Perte d’alimentation d’entrée |  |  |
| `Listening` | En écoute |  |  |
| `Locked` | Verrouillé |  |  |
| `Logged In/Connected` | Session ouverte/connecté |  |  |
| `Logging In` | Ouverture de session |  |  |
| `Logging Out Phase 1` | Fermeture de session (phase 1) |  |  |
| `Logging Out Phase 2` | Fermeture de session (phase 2) |  |  |
| `MAX_BOOSTORBUCK` | MAX_BOOSTORBUCK |  |  |
| `Missing` | Absent |  |  |
| `Missing Zero Crossing` | Passage par zéro manquant |  |  |
| `MS` | MS |  |  |
| `ND` | ND |  |  |
| `Not Disabled by switch - i.e. regulating` | Non désactivé par interrupteur, c’est-à-dire en régulation |  |  |
| `O0` | O0 |  |  |
| `O1` | O1 |  |  |
| `OC` | OC |  |  |
| `OT` | OT |  |  |
| `Over Current Fault Count O,1...9 then 10,11, 12...` | Nombre de défauts de surintensité 0,1...9 puis 10,11, 12... | CHECK: the English writes the letter O for the digit 0 (« O,1...9 ») ; corrected to 0 here, as pt-PT did. |  |
| `Over Current Fault reset maximum count reached (per PRM file) must be reset manually` | Nombre maximal de réarmements sur défaut de surintensité atteint (selon le fichier PRM) - réarmement manuel nécessaire | LENGTH: 83 chars becomes 118 in a fault-table cell. |  |
| `Over Temperature fault - converter is disabled until it cools` | Défaut de température excessive - le convertisseur reste désactivé jusqu’à refroidissement | LENGTH: 60 chars becomes 89 in a fault-table cell. |  |
| `P+` | P+ |  |  |
| `P-` | P- |  |  |
| `PL` | PL |  |  |
| `PLL_NL` | PLL_NL |  |  |
| `PN` | PN |  |  |
| `PR` | PR |  |  |
| `Processor Reset by user command` | Processeur réinitialisé par une commande de l’utilisateur |  |  |
| `PWM is no longer railed, and has dropped below 95% of maximum` | La PWM n’est plus en butée et est descendue en dessous de 95 % du maximum | TERM: « railed » rendered as « en butée » (PWM saturated at its limit). Confirm. |  |
| `RAMP` | RAMP |  |  |
| `Ramping` | En rampe |  |  |
| `Real Time Clock time after Change` | Heure de l’horloge temps réel après modification |  |  |
| `Real Time Clock time before Change` | Heure de l’horloge temps réel avant modification |  |  |
| `Rebooting` | Redémarrage en cours |  |  |
| `Regulating` | En régulation |  |  |
| `Regulator is ramping to the active set point` | Le régulateur monte en rampe vers la consigne active |  |  |
| `Restoring Session` | Restauration de la session |  |  |
| `SCR_GATE` | SCR_GATE |  |  |
| `SD Card data logging was stopped by user command (disabled)` | La journalisation des données sur la carte SD a été arrêtée par une commande de l’utilisateur (désactivée) |  |  |
| `SE` | SE |  |  |
| `Service Lookup` | Recherche de service |  |  |
| `TEMP` | TEMP |  |  |
| `Temp sensor open` | Capteur de température en circuit ouvert |  |  |
| `Temp Sensor or Fan Fault` | Défaut du capteur de température ou du ventilateur |  |  |
| `Temp sensor shorted` | Capteur de température en court-circuit |  |  |
| `The PLL is currently not locked` | La PLL n’est actuellement pas verrouillée |  |  |
| `Transformer Saturation` | Saturation du transformateur |  |  |
| `TS` | TS |  |  |
| `Unknown` | Inconnu |  |  |
| `VC` | VC |  |  |
| `Vin or Vout is out of range as defined in PRM file - fault resets automatically with a 10V asymmetrical hysteresis (check fault log Vin column to determine over or under) ` | Vin ou Vout est hors de la plage définie dans le fichier PRM - le défaut se réarme automatiquement avec une hystérésis asymétrique de 10 V (consultez la colonne Vin du journal des défauts pour savoir s’il s’agit d’un dépassement par excès ou par défaut)  | LENGTH: 170 chars becomes 250 in a fault-table cell. Trailing space of the English source preserved. |  |
| `VO` | VO |  |  |
| `Voltage Calibration error on boot up. After bootup, it permanently disables the regulator` | Erreur d’étalonnage de tension au démarrage. Après le démarrage, elle désactive définitivement le régulateur |  |  |
| `W1` | W1 |  |  |
| `W2` | W2 |  |  |
| `W3` | W3 |  |  |
| `W4` | W4 |  |  |
| `W5` | W5 |  |  |
| `W6` | W6 |  |  |
| `Watchdog tripped - DSPIC failure to respond` | Watchdog déclenché - le DSPIC n’a pas répondu |  |  |
| `Watchdog tripped - Failed wellness test (Vout != Setpoint and no faults)` | Watchdog déclenché - échec du test de bon fonctionnement (Vout différent de la consigne et aucun défaut) |  |  |
| `Watchdog tripped - Main uP loop timed out OR H/W watchdog timed out` | Watchdog déclenché - délai dépassé dans la boucle principale du microprocesseur OU dans le watchdog matériel |  |  |
| `Watchdog tripped - Phase Parameter file checksum mismatch` | Watchdog déclenché - somme de contrôle du fichier de paramètres de phase non concordante |  |  |
| `Watchdog tripped - Phase Status or data checksum mismatch  ` | Watchdog déclenché - somme de contrôle de l’état ou des données de phase non concordante   |  |  |
| `Watchdog tripped - SPI buss to phase failure ` | Watchdog déclenché - défaillance du bus SPI vers la phase  | TERM: « watchdog » kept rather than « chien de garde » — the anglicism is standard in French embedded/utility engineering and the code W1…W6 sits beside it. Confirm. (The English misspells « buss » ; trailing space preserved.) |  |
| `ZX` | ZX |  |  |

## Transcript pane and window (18)

| Original (English) | Translation (fr-FR) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| ` Send Command ` |  Envoyer la commande  | CHECK: leading and trailing spaces are in the English source and are preserved (button padding). |  |
| ` Send CTRL-C ` |  Envoyer CTRL-C  |  |  |
| `%1:     Sent: %2` | %1: Envoyé : %2 |  |  |
| `%1: %2` | %1: %2 |  |  |
| `%1: <font color="orange">WARNING: %2</font>` | `%1: <font color="orange">AVERTISSEMENT : %2</font>` | LENGTH: « WARNING » becomes « AVERTISSEMENT » on every warning line of the journal. |  |
| `%1: <font color="red">ERROR: %2</font>` | `%1: <font color="red">ERREUR : %2</font>` |  |  |
| `%1: Received:   %2` | %1:   Reçu : %2 | CHECK: the English pads « Received: » / « Sent: » to line the %2 column up. « Reçu » / « Envoyé » are re-padded here so the two lines still align; adjust if the pane is not monospaced. |  |
| `Clear Transcript` | Effacer le journal de session | LENGTH: 16 chars becomes 28 on what is likely a toolbar button; « Effacer le journal » if it clips. |  |
| `Command To Send` | Commande à envoyer |  |  |
| `Copy Transcript to Clipboard` | Copier le journal de session dans le presse-papiers |  |  |
| `Could not open '%1' for writing, please check permissions\n%2` | Impossible d’ouvrir '%1' en écriture ; veuillez vérifier les autorisations\n%2 |  |  |
| `Could not Open File` | Impossible d’ouvrir le fichier |  |  |
| `Error` | Erreur |  |  |
| `Save Transcript` | Enregistrer le journal de session |  |  |
| `Save Transcript...` | Enregistrer le journal de session… | LENGTH: grows to 34 chars; « Enregistrer le journal… » if the menu is narrow. |  |
| `Select All` | Tout sélectionner |  |  |
| `Text Files (*.txt);;All Files (*.*)` | Fichiers texte (*.txt);;Tous les fichiers (*.*) | CHECK: Qt file-filter syntax — the « ;; » separator and the (*.txt)/(*.*) patterns are code and take no French spacing. |  |
| `Transcript` | Journal de session | TERM: « transcript » rendered as « journal de session » throughout (a literal « transcription » reads wrong for a scrolling command/response log). Confirm; it is used as a pane title, a menu and a toolbar button. |  |

## UART settings dialog (16)

| Original (English) | Translation (fr-FR) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `115.2k` | 115.2k |  |  |
| `230.4k` | 230.4k |  |  |
| `38.4k` | 38.4k |  |  |
| `57.6k` | 57.6k |  |  |
| `Baud Rate` | Débit en bauds |  |  |
| `Baud rate and Flow control must be set` | Le débit en bauds et le contrôle de flux doivent être définis |  |  |
| `Baud rate must be set` | Le débit en bauds doit être défini |  |  |
| `Flow Control` | Contrôle de flux |  |  |
| `Flow control must be set` | Le contrôle de flux doit être défini |  |  |
| `Hardware Control` | Contrôle matériel |  |  |
| `None` | Aucun |  |  |
| `Setup UARTs` | Configurer les UART |  |  |
| `Software Control` | Contrôle logiciel |  |  |
| `TextLabel` | TextLabel |  |  |
| `UART 1 settings can not be modified` | Les paramètres de l’UART 1 ne peuvent pas être modifiés |  |  |
| `WARNING: DO NOT CHANGE if UART2 is used with an Ethernet adapter.` | AVERTISSEMENT : NE PAS MODIFIER si l’UART2 est utilisée avec un adaptateur Ethernet. |  |  |

## User guide windows (7)

| Original (English) | Translation (fr-FR) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `Advanced User Guide` | Guide de l’utilisateur (avancé) |  |  |
| `Basic User Guide` | Guide de l’utilisateur (base) |  |  |
| `Bluetooth Pairing` | Appairage Bluetooth |  |  |
| `Bluetooth Pairing (Windows 11)` | Appairage Bluetooth (Windows 11) |  |  |
| `Close` | Fermer |  |  |
| `Fit to window` | Ajuster à la fenêtre |  |  |
| `The guide could not be loaded: %1` | Le guide n’a pas pu être chargé : %1 |  |  |

## Voltage calibration dialog (10)

| Original (English) | Translation (fr-FR) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| ` Volts` |  volts |  |  |
| `A Voltage Difference of '%1' is invalid, range is -9.9V to +9.9V` | Un écart de tension de '%1' n’est pas valide ; la plage va de -9,9 V à +9,9 V | CHECK: the range literal is re-punctuated for French (decimal comma, non-breaking space before the unit). Confirm the app does not parse this text back. |  |
| `Can not calibrate voltage` | Impossible d’étalonner la tension |  |  |
| `Externally Measured Output Voltage:` | Tension de sortie mesurée en externe : |  |  |
| `Regulator Target %1 Output Voltage:` | Tension de sortie de consigne %1 du régulateur : |  |  |
| `Regulator Target Output Voltage:` | Tension de sortie de consigne du régulateur : | LENGTH: 32 chars becomes 45 on a dialog label. |  |
| `Voltage Calibration` | Étalonnage de tension |  |  |
| `Voltage Calibration:` | Étalonnage de tension : |  |  |
| `Voltage Difference is too High` | L’écart de tension est trop élevé |  |  |
| `Volts` | Volts |  |  |
