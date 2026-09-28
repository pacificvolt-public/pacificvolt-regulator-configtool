# ConfigTool - Spanish (es-ES) translation review

The complete translation, grouped by where the text appears in the tool. Edit the
**Translation** column directly, or put a replacement in **Your correction**, and
hand the file back. For anything with markup or long text, the spreadsheet next to
this file is easier to work in.

- Strings translated: **876** - the whole of the live user interface
- Strings still untranslated: **0**
- Rows carrying a question from me: **75**
- Generated from `translations/ConfigTool_es_ES.ts`

This is a machine first pass awaiting a native European Spanish speaker. This is deliberately es-ES and not Latin American: *contraseña* not *clave*, *tensión* not *voltaje*, *ordenador* where a computer is meant, and *pulsar* rather than *cliquear*.

Some strings are translated to themselves on purpose. Firmware fault codes (`CB`,
`OT`, `W1`, `P+`, `RAMP`...), baud rate values and Qt Designer object names
(`toolBar`, `MainWindow`) are identifiers rather than prose - translating them
would break the match against what the regulator actually sends.

A few strings carry HTML, shown here as literal text rather than rendered. `\n`
marks a real line break, the same convention the .tsv uses.

## About and licence dialogs (9)

| Original (English) | Translation (es-ES) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `&3rd Party Licenses` | &amp;Licencias de terceros |  |  |
| `&About Qt` | Acerca de &amp;Qt |  |  |
| `<h3>%1 - 3rd Party Licenses</h3>` | &lt;h3&gt;%1 - Licencias de terceros&lt;/h3&gt; |  |  |
| `<h3>About %1</h3><p>%1</p><p>Version: %2</p><p>Build Date: %3</p><p>%4</p>` | &lt;h3&gt;Acerca de %1&lt;/h3&gt;&lt;p&gt;%1&lt;/p&gt;&lt;p&gt;Versión: %2&lt;/p&gt;&lt;p&gt;Fecha de compilación: %3&lt;/p&gt;&lt;p&gt;%4&lt;/p&gt; |  |  |
| `<p>%1 uses multiple 3rd Party software mostly covered under the Qt distribution</p><p>However the following license(s) are not part of Qt.</p><hr style="width:50%;text-align:left;margin-left:0"><table border="1"><tr><th>Company</th><th>Product</th><th>License</th><th>Source Location</th><th>Patches</th></tr>` | &lt;p&gt;%1 utiliza software de terceros, en su mayoría cubierto por la distribución de Qt&lt;/p&gt;&lt;p&gt;No obstante, las licencias siguientes no forman parte de Qt.&lt;/p&gt;&lt;hr style="width:50%;text-align:left;margin-left:0"&gt;&lt;table border="1"&gt;&lt;tr&gt;&lt;th&gt;Empresa&lt;/th&gt;&lt;th&gt;Producto&lt;/th&gt;&lt;th&gt;Licencia&lt;/th&gt;&lt;th&gt;Ubicación del código fuente&lt;/th&gt;&lt;th&gt;Parches&lt;/th&gt;&lt;/tr&gt; | LENGTH: «Ubicación del código fuente» is a wide table heading (13 -&gt; 27 characters); «Origen» is the fallback if the licence table is cramped. |  |
| `<p>Is a tool to help configure %1's Voltage Regulators.</p><p>For more information, please visit <a href="%2">%3</a>.</p><p>For the default Advanced and Admin passwords, contact <a href="mailto:%4">%4</a>.</p><hr style="width:50%;text-align:left;margin-left:0"><p>%5</p>` | &lt;p&gt;Es una herramienta que ayuda a configurar los reguladores de tensión de %1.&lt;/p&gt;&lt;p&gt;Para más información, visitar &lt;a href="%2"&gt;%3&lt;/a&gt;.&lt;/p&gt;&lt;p&gt;Para las contraseñas predeterminadas de Avanzado y Admin, escribir a &lt;a href="mailto:%4"&gt;%4&lt;/a&gt;.&lt;/p&gt;&lt;hr style="width:50%;text-align:left;margin-left:0"&gt;&lt;p&gt;%5&lt;/p&gt; |  |  |
| `3rd Party Licenses` | Licencias de terceros |  |  |
| `About %1` | Acerca de %1 |  |  |
| `This tool supports the following LVR firmware versions:<br>LVR30 %1, LVR50 %2` | Esta herramienta admite las siguientes versiones de firmware LVR:&lt;br&gt;LVR30 %1, LVR50 %2 |  |  |

## Bluetooth - Available Regulators and pairing (48)

| Original (English) | Translation (es-ES) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `%1 configured connection(s)` | %1 conexión(es) configurada(s) | AGREEMENT: the English '(s)' plural hack is mirrored with «conexión(es) configurada(s)». Qt plural forms (%n) would be the clean fix, but that is a source change. |  |
| `An error has occurred in the bluetooth system` | Se ha producido un error en el sistema Bluetooth |  |  |
| `An unknown error has occurred.` | Se ha producido un error desconocido. |  |  |
| `Authorize Regulator` | Autorizar regulador |  |  |
| `Available Regulators` | Reguladores disponibles |  |  |
| `Connecting to regulator '%1' timed out. Check your connection - the regulator may be out of range or turned off.` | Se ha agotado el tiempo de espera al conectar con el regulador '%1'. Compruebe la conexión - el regulador puede estar fuera de alcance o apagado. |  |  |
| `Could not find a bluetooth adapter. ` | No se ha podido encontrar un adaptador Bluetooth.  |  |  |
| `currently connected` | conectado actualmente |  |  |
| `Device discovery is not possible or implemented on the current platform.` | La detección de dispositivos no es posible ni está implementada en esta plataforma. |  |  |
| `Device Name` | Nombre del dispositivo |  |  |
| `Does the following PIN match the one shown on the device you are pairing?: %1` | ¿Coincide el siguiente PIN con el que se muestra en el dispositivo que se está emparejando?: %1 | CHECK: the source's odd '?:' sequence before the placeholder is kept as-is; Spanish adds the required opening ¿. |  |
| `Enter a PIN to pair with:` | Introducir un PIN para emparejar: |  |  |
| `Error in Bluetooth connection` | Error en la conexión Bluetooth |  |  |
| `Error in pairing` | Error de emparejamiento |  |  |
| `Finished` | Finalizado |  |  |
| `Limit the list to shipped regulators, which are all named "PV...". Uncheck to also show bench and test units, which often are not. Non-regulators are never listed either way.` | Limita la lista a los reguladores expedidos, cuyo nombre empieza siempre por "PV...". Desmarcar la casilla para mostrar también las unidades de banco de pruebas y de ensayo, que a menudo no lo cumplen. Los equipos que no son reguladores no se muestran en ningún caso. |  |  |
| `Missing permissions` | Faltan permisos |  |  |
| `No Bluetooth Adapter Found` | No se ha encontrado ningún adaptador Bluetooth |  |  |
| `One of the requested discovery methods is not supported by the current platform.` | Esta plataforma no admite uno de los métodos de detección solicitados. |  |  |
| `Pair Device` | Emparejar dispositivo |  |  |
| `Pair Device?` | ¿Emparejar dispositivo? |  |  |
| `Pair Regulator` | Emparejar regulador |  |  |
| `paired` | emparejado |  |  |
| `Paired?` | ¿Emparejado? |  |  |
| `Permissions are needed to use Bluetooth. Please grant the permissions to this application in the system settings.` | Se necesitan permisos para utilizar Bluetooth. Conceder los permisos a esta aplicación en la configuración del sistema. |  |  |
| `Please enter this PIN on the device you are pairing with: %1` | Introducir este PIN en el dispositivo con el que se está emparejando: %1 |  |  |
| `PV Filter` | Filtro PV |  |  |
| `Re-Scan` | Buscar de nuevo |  |  |
| `Remove %1 regulator(s)?` | ¿Quitar %1 regulador(es)? |  |  |
| `Remove Regulators` | Quitar reguladores | CHECK: «quitar» is used for removing an entry from a list and «eliminar» for deleting data; held consistently across the file. |  |
| `Remove the selected regulators from the list, delete their connections, and unpair them` | Quita de la lista los reguladores seleccionados, elimina sus conexiones y los desempareja |  |  |
| `Scanning for devices not previously paired.` | Buscando dispositivos aún no emparejados. |  |  |
| `Scanning for previously connected devices and devices not previously paired.` | Buscando dispositivos ya conectados anteriormente y dispositivos aún no emparejados. |  |  |
| `Scanning for previously connected devices.` | Buscando dispositivos ya conectados anteriormente. |  |  |
| `Scanning...` | Buscando... |  |  |
| `Select Regulator` | Seleccionar regulador |  |  |
| `Select the Regulator to connect to.` | Seleccionar el regulador al que se desea conectar. |  |  |
| `Service` | Servicio |  |  |
| `Stop Scanning` | Detener la búsqueda |  |  |
| `The Bluetooth adaptor is powered off, power it on before doing discovery.` | El adaptador Bluetooth está apagado; es necesario encenderlo antes de buscar dispositivos. |  |  |
| `The following error occurred connecting to regulator '%1': %2. Check your connection - the regulator may be out of range or turned off.` | Se ha producido el siguiente error al conectar con el regulador '%1': %2. Compruebe la conexión - el regulador puede estar fuera de alcance o apagado. |  |  |
| `The location service is turned off.Usage of Bluetooth APIs is not possible when location service is turned off.` | El servicio de ubicación está desactivado. No se pueden utilizar las API de Bluetooth con el servicio de ubicación desactivado. | CHECK: the English is missing the space after the first full stop ('off.Usage'); a space has been added in Spanish. |  |
| `The operating system requests permissions which were not granted by the user.` | El sistema operativo solicita permisos que el usuario no ha concedido. |  |  |
| `The passed local adapter address does not match the physical adapter address of any local Bluetooth device.` | La dirección de adaptador local indicada no coincide con la dirección física de ningún dispositivo Bluetooth local. |  |  |
| `This deletes their configured connections, removes them from the Available Regulators list, and unpairs them from this computer. Any open connections will be closed. This cannot be undone.` | Esto elimina sus conexiones configuradas, los quita de la lista Reguladores disponibles y los desempareja de este ordenador. Las conexiones abiertas se cerrarán. Esta acción no se puede deshacer. |  |  |
| `Unknown Error.` | Error desconocido. |  |  |
| `Unpair Regulator` | Desemparejar regulador |  |  |
| `Writing or reading from the device resulted in an error.` | La escritura o la lectura en el dispositivo ha producido un error. |  |  |

## Clock and time zone dialogs (13)

| Original (English) | Translation (es-ES) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `...` | ... |  |  |
| `...` | ... |  |  |
| `Current Time` | Hora actual |  |  |
| `Custom Selected Time Zone` | Zona horaria personalizada |  |  |
| `Custom Time` | Hora personalizada |  |  |
| `Local Computer's Time Zone` | Zona horaria de este ordenador | CHECK: «ordenador», the es-ES word for computer - never «computadora». |  |
| `Regulator's System Clock:` | Reloj del sistema del regulador: |  |  |
| `Regulator:` | Regulador: |  |  |
| `Select Time Zone` | Seleccionar la zona horaria |  |  |
| `Select Time Zone` | Seleccionar la zona horaria |  |  |
| `Set Regulator System Clock` | Ajustar el reloj del sistema del regulador |  |  |
| `Sync` | Sincronizar | LENGTH: 4 -&gt; 11 characters on a small push button next to the clock field. |  |
| `UTC` | UTC |  |  |

## Command names - transcript and queue status (65)

| Original (English) | Translation (es-ES) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `    Command #: %1` |     Comando n.º: %1 |  |  |
| `%1.` | %1. |  |  |
| `(Re)-initialize Control Board` | (Re)inicializar la placa de control |  |  |
| `, re-running command.` | , se volverá a ejecutar el comando. |  |  |
| `. Removing from Queue.` | . Se eliminará de la cola. |  |  |
| `Checking for Support of '%1'` | Comprobando la compatibilidad con '%1' |  |  |
| `Clear Queue` | Vaciar la cola |  |  |
| `cmd not supported` | comando no admitido | CHECK: lowercase kept - this fragment is concatenated into a longer transcript line. |  |
| `Command '%1' failed. Please disconnect and try again.  Consider rebooting the Regulator.` | El comando '%1' ha fallado. Desconectar y volver a intentarlo.  Se recomienda reiniciar el regulador. |  |  |
| `Command '%1' failed. Removing from Queue.` | El comando '%1' ha fallado. Se eliminará de la cola. |  |  |
| `Command '%1' is not supported` | No se admite el comando '%1' |  |  |
| `Command '%2' timed out%1` | Se ha agotado el tiempo de espera del comando '%2'%1 | CHECK: %1 is a sentence-final fragment (', re-running command.' / '. Removing from Queue.'), so the Spanish must end exactly at the placeholder. |  |
| `Could not process results of command '%1'` | No se han podido procesar los resultados del comando '%1' |  |  |
| `Custom Command` | Comando personalizado |  |  |
| `Disable SDCard` | Desactivar la tarjeta SD |  |  |
| `Download File` | Descargar archivo |  |  |
| `Enable Or Disable All Phases if there is a Failure in any Phase` | Activar o desactivar todas las fases si falla cualquiera de ellas |  |  |
| `Enable Or Disable Regulator` | Activar o desactivar el regulador |  |  |
| `Enable SDCard` | Activar la tarjeta SD |  |  |
| `Finished downloading data for command '%1'` | Descarga de los datos del comando '%1' finalizada |  |  |
| `Finished getting system info` | Obtención de la información del sistema finalizada |  |  |
| `Finished Getting System Info` | Obtención de la información del sistema finalizada |  |  |
| `Format SDCard` | Formatear la tarjeta SD |  |  |
| `Get Default Parameter File` | Obtener archivo de parámetros predeterminado |  |  |
| `Get EEPROM Contents` | Obtener el contenido de la EEPROM |  |  |
| `Get File Sizes` | Obtener tamaños de archivo |  |  |
| `Get Parameter File` | Obtener archivo de parámetros |  |  |
| `Get Phase Firmware` | Obtener firmware de fase |  |  |
| `Get Regulator Clock` | Obtener reloj del regulador |  |  |
| `Get Serial Num` | Obtener número de serie |  |  |
| `Get Status` | Obtener estado |  |  |
| `Get System Firmware` | Obtener firmware del sistema |  |  |
| `Get System Firmware Date` | Obtener fecha del firmware del sistema |  |  |
| `Get System Gain` | Obtener la ganancia del sistema |  |  |
| `Get UART Settings` | Obtener configuración de UART |  |  |
| `Get UART Settings via RB` | Obtener configuración de UART mediante RB | CHECK: 'RB' and 'RBAUD' are firmware command names and are left untranslated. |  |
| `Get UART Settings via RBAUD` | Obtener configuración de UART mediante RBAUD |  |  |
| `Get Voltage Calibration` | Obtener calibración de tensión |  |  |
| `Reboot Regulator` | Reiniciar el regulador |  |  |
| `Regulator could not handle command '%1'` | El regulador no ha podido procesar el comando '%1' |  |  |
| `Reset Over Current Fault Lockout` | Restablecer el bloqueo por fallo de sobreintensidad | TERM: two decisions fixed here for the whole file. fault -&gt; «fallo» (not «falta», which in Spanish utility practice means a network short-circuit fault, whereas these are device diagnostic conditions). over current -&gt; «sobreintensidad», the Spanish power-industry term, never the calque «sobrecorriente». |  |
| `Reset Regulator to Default Parameters` | Restablecer los parámetros predeterminados del regulador |  |  |
| `Restore Modem Power` | Restaurar la alimentación del módem |  |  |
| `Send Ctrl-C` | Enviar Ctrl-C |  |  |
| `Send Login` | Enviar inicio de sesión |  |  |
| `Send Logoff` | Enviar cierre de sesión |  |  |
| `Send Password` | Enviar contraseña |  |  |
| `Set Param File` | Establecer el archivo de parámetros |  |  |
| `Set PIR Amperage` | Establecer la corriente PIR | CHECK: PIR (Power Interactive Regulation) is kept as the English initialism in these command names, as the firmware uses it; the expanded form «regulación interactiva de potencia» is used where the UI spells it out. |  |
| `Set PIR Delta Voltage` | Establecer la tensión delta PIR |  |  |
| `Set PIR Null Voltage` | Establecer la tensión nula PIR |  |  |
| `Set PIR Time Constant` | Establecer la constante de tiempo PIR |  |  |
| `Set Regulator Clock` | Ajustar el reloj del regulador |  |  |
| `Set Regulator Password` | Establecer la contraseña del regulador |  |  |
| `Set Serial Number` | Establecer el número de serie |  |  |
| `Set System Gain` | Establecer la ganancia del sistema |  |  |
| `Set Target Selection` | Establecer la selección de objetivo |  |  |
| `Set Target Voltage` | Establecer la tensión objetivo |  |  |
| `Set UART 1 Baud Rate` | Establecer la velocidad en baudios de la UART 1 | LENGTH: 20 -&gt; 46 characters. These command names are listed in the transcript and the command-queue pane; if that column is fixed-width, «Velocidad UART 1» is the fallback. |  |
| `Set UART 1 FlowControl` | Establecer el control de flujo de la UART 1 |  |  |
| `Set UART 2 Baud Rate` | Establecer la velocidad en baudios de la UART 2 |  |  |
| `Set UART 2 FlowControl` | Establecer el control de flujo de la UART 2 |  |  |
| `Set Voltage Calibration` | Establecer la calibración de tensión |  |  |
| `Size of Command Queue: %1` | Tamaño de la cola de comandos: %1 |  |  |
| `Turn off Modem Power` | Apagar la alimentación del módem |  |  |

## Connected regulator window - menus, dialogs and messages (149)

| Original (English) | Translation (es-ES) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `    Comm Port: %1` |     Puerto de comunicaciones: %1 |  |  |
| `    IP Address: %1\n    Domain Name: %2\n    Port: %3` |     Dirección IP: %1\n    Nombre de dominio: %2\n    Puerto: %3 |  |  |
| ` - Regulator: %1` |  - Regulador: %1 |  |  |
| ` - Transcript` |  - Transcripción |  |  |
| ` Reset Over Current Fault Lockout` |  Restablecer el bloqueo por fallo de sobreintensidad |  |  |
| `%1` | %1 |  |  |
| `&Disconnect` | &amp;Desconectar |  |  |
| `&Regulator` | &amp;Regulador |  |  |
| `&Settings` | &amp;Configuración |  |  |
| `<br/>Would you like to reconnect?` | &lt;br/&gt;¿Desea volver a conectarse? |  |  |
| `'%1' is a name Windows reserves and cannot be used in a file name.` | '%1' es un nombre reservado por Windows y no se puede usar en un nombre de archivo. |  |  |
| `(Re-)Initialize Regulator Control Board` | (Re)inicializar la placa de control del regulador |  |  |
| `(Re-)initialize the Control Board...` | (Re)inicializar la placa de control... |  |  |
| `(Re-)initialize the control board...` | (Re)inicializar la placa de control... |  |  |
| `1=Fast` | 1=Rápido |  |  |
| `A timeout error occurred` | Se ha producido un error de tiempo de espera |  |  |
| `About...` | Acerca de... |  |  |
| `Administration Mode` | Modo de administración |  |  |
| `Administration Mode` | Modo de administración |  |  |
| `Advanced Mode` | Modo avanzado |  |  |
| `All Phases Disabled on Failure in Any Phase?` | ¿Desactivar todas las fases si falla cualquiera de ellas? |  |  |
| `An error occurred while attempting to open an already opened device by another process or a user not having enough permission and credentials to open.` | Se ha producido un error al intentar abrir un dispositivo que ya está abierto por otro proceso, o por un usuario sin permisos ni credenciales suficientes. |  |  |
| `An error occurred while attempting to open an already opened device in this object.` | Se ha producido un error al intentar abrir un dispositivo que este objeto ya tiene abierto. |  |  |
| `An error occurred while attempting to open an non-existing device.` | Se ha producido un error al intentar abrir un dispositivo inexistente. |  |  |
| `An I/O error occurred when a resource becomes unavailable, e.g. when the device is unexpectedly removed from the system.` | Se ha producido un error de E/S por falta de disponibilidad de un recurso, por ejemplo al retirarse el dispositivo del sistema de forma inesperada. |  |  |
| `An I/O error occurred while reading the data.` | Se ha producido un error de E/S al leer los datos. |  |  |
| `An I/O error occurred while writing the data.` | Se ha producido un error de E/S al escribir los datos. |  |  |
| `An unidentified error occurred.` | Se ha producido un error no identificado. |  |  |
| `Are you sure you wish to continue?` | ¿Está seguro de que desea continuar? |  |  |
| `Automatically Refresh Status?` | ¿Actualizar el estado automáticamente? |  |  |
| `Available` | Disponible |  |  |
| `Available` | Disponible |  |  |
| `Available` | Disponible |  |  |
| `Bluetooth` | Bluetooth |  |  |
| `Bluetooth Regulator Unauthorized` | Regulador Bluetooth no autorizado |  |  |
| `Bluetooth Regulator Unpaired` | Regulador Bluetooth no emparejado |  |  |
| `Can not set UART settings while connected via Ethernet` | No se puede cambiar la configuración de UART mientras haya una conexión por Ethernet |  |  |
| `Change Time Zone...` | Cambiar la zona horaria... |  |  |
| `Clear Command Queue` | Vaciar la cola de comandos |  |  |
| `Clear Transcript` | Borrar la transcripción |  |  |
| `Close Connection?` | ¿Cerrar la conexión? |  |  |
| `COM Port` | Puerto COM |  |  |
| `Comm Port not Found` | Puerto de comunicaciones no encontrado |  |  |
| `Command Queue Status` | Estado de la cola de comandos |  |  |
| `Connect` | Conectar |  |  |
| `Connection '%1' was lost or disconnected.` | Se ha perdido o se ha cerrado la conexión '%1'. |  |  |
| `Continue` | Continuar |  |  |
| `Continue` | Continuar |  |  |
| `Copy Transcript to Clipboard` | Copiar la transcripción al portapapeles |  |  |
| `Debug` | Depuración |  |  |
| `Debug Logging...` | Registro de depuración... |  |  |
| `Delete Data Logs...` | Eliminar los registros de datos... |  |  |
| `Delete Fault Log...` | Eliminar el registro de fallos... |  |  |
| `Disable Advanced Mode` | Desactivar el modo avanzado |  |  |
| `Disable Regulator` | Desactivar el regulador |  |  |
| `Disable SD Card` | Desactivar la tarjeta SD |  |  |
| `Download from SD Card` | Descargar de la tarjeta SD |  |  |
| `Download from SD Card...` | Descargar de la tarjeta SD... |  |  |
| `Enable Advanced Mode` | Activar el modo avanzado |  |  |
| `Enable Regulator` | Activar el regulador |  |  |
| `Enable SD Card` | Activar la tarjeta SD |  |  |
| `Enter New Regulator Password` | Introducir la nueva contraseña del regulador |  |  |
| `Enter Regulator Password` | Introducir la contraseña del regulador |  |  |
| `Enter System Gain` | Introducir la ganancia del sistema |  |  |
| `Error` | Error |  |  |
| `Error Communicating with Regulator` | Error de comunicación con el regulador |  |  |
| `ERROR: %1` | ERROR: %1 |  |  |
| `Fast Rate Data` | Datos de tasa rápida |  |  |
| `Format SD Card...` | Formatear la tarjeta SD... |  |  |
| `Formatting erases the SD card and cannot be undone.` | El formateo borra la tarjeta SD y no se puede deshacer. |  |  |
| `Help` | Ayuda |  |  |
| `Host '%1' was not found. Please check the host name and port settings.` | No se ha encontrado el host '%1'. Comprobar el nombre de host y la configuración del puerto. |  |  |
| `Initialize System Information on Login?` | ¿Inicializar la información del sistema al iniciar sesión? |  |  |
| `Medium Rate Data` | Datos de tasa media |  |  |
| `Name cannot be used` | No se puede usar el nombre |  |  |
| `Name for this regulator:\n\nThis name is stored by the Config Tool only. It is not written to the\nregulator and is not read back from it, and it is lost if the regulator\nis removed from the saved list.\n\nIt is used in the names of the files downloaded from this regulator, so\nit cannot contain characters that a file name cannot hold.` | Nombre de este regulador:\n\nEste nombre lo guarda únicamente el Config Tool. No se escribe en el\nregulador ni se lee de él, y se pierde si el regulador\nse elimina de la lista guardada.\n\nSe utiliza en los nombres de los archivos descargados de este regulador, por\nlo que no puede contener caracteres que un nombre de archivo no admita. |  |  |
| `Network not Reachable` | Red no accesible |  |  |
| `No SD File Data` | Sin datos de archivos de la tarjeta SD |  |  |
| `No SD file data available. Click on the green System Info arrows.` | No hay datos de archivos de la tarjeta SD. Haga clic en las flechas verdes de información del sistema. |  |  |
| `Parameter File...` | Archivo de parámetros... |  |  |
| `Password Required` | Contraseña necesaria |  |  |
| `Power cycle external modem at J2-2` | Apagar y encender el módem externo en J2-2 | CHECK: «power cycle» rendered as «apagar y encender»; there is no single-word Spanish equivalent, so this menu entry is noticeably longer than the English. |  |
| `Power Interactive Regulation Settings...` | Configuración de la regulación interactiva de potencia... |  |  |
| `Quit` | Salir |  |  |
| `Quit` | Salir |  |  |
| `Reboot Regulator` | Reiniciar el regulador |  |  |
| `Reboot Regulator...` | Reiniciar el regulador... |  |  |
| `Reconnect` | Volver a conectar |  |  |
| `Refresh` | Actualizar |  |  |
| `Refresh All` | Actualizar todo |  |  |
| `Refresh Gain Values` | Actualizar los valores de ganancia |  |  |
| `Refresh Parameter File` | Actualizar el archivo de parámetros |  |  |
| `Refresh Regulator Clock` | Actualizar el reloj del regulador |  |  |
| `Refresh Regulator Information` | Actualizar la información del regulador |  |  |
| `Refresh SD Card Information` | Actualizar la información de la tarjeta SD |  |  |
| `Refresh UART Settings` | Actualizar la configuración de UART |  |  |
| `Refresh Voltage and Fault Status` | Actualizar el estado de tensión y de fallos |  |  |
| `Refresh Voltage Calibration Info` | Actualizar la información de calibración de tensión |  |  |
| `Regulator` | Regulador |  |  |
| `Regulator &Settings` | Configuración del &amp;regulador | CHECK: mnemonic moved off the first word so it does not collide with the «&amp;Configuración» menu title in the same window. |  |
| `Regulator '%1' - %2` | Regulador '%1' - %2 |  |  |
| `Regulator has logged off due to no command activity. Please reconnect and activate auto refresh.` | El regulador ha cerrado la sesión por falta de actividad de comandos. Volver a conectarse y activar la actualización automática. |  |  |
| `Regulator Logged Off` | Sesión cerrada en el regulador |  |  |
| `Regulator:` | Regulador: |  |  |
| `Remote` | Remoto |  |  |
| `Reset Over Current Fault Lockout` | Restablecer el bloqueo por fallo de sobreintensidad | TERM: two decisions fixed here for the whole file. fault -&gt; «fallo» (not «falta», which in Spanish utility practice means a network short-circuit fault, whereas these are device diagnostic conditions). over current -&gt; «sobreintensidad», the Spanish power-industry term, never the calque «sobrecorriente». |  |
| `Reset Regulator to Default Parameters` | Restablecer los parámetros predeterminados del regulador |  |  |
| `Reset Regulator to Default Parameters...` | Restablecer los parámetros predeterminados del regulador... |  |  |
| `Save Transcript...` | Guardar la transcripción... |  |  |
| `SD Card` | Tarjeta SD |  |  |
| `SD Card File Sizes` | Tamaños de los archivos de la tarjeta SD |  |  |
| `SD Card Has Error` | La tarjeta SD tiene un error |  |  |
| `SD Card is Disabled` | La tarjeta SD está desactivada |  |  |
| `Session Timing Out` | La sesión está a punto de expirar |  |  |
| `Set Regulator Name` | Establecer el nombre del regulador |  |  |
| `Set Regulator Name...` | Establecer el nombre del regulador... |  |  |
| `Set Regulator's Password...` | Establecer la contraseña del regulador... |  |  |
| `Set Serial Number...` | Establecer el número de serie... |  |  |
| `Set System Clock...` | Ajustar el reloj del sistema... | CHECK: «set» is rendered «establecer» for values and «ajustar» for clocks throughout. |  |
| `Set System Gain...` | Establecer la ganancia del sistema... |  |  |
| `Slow Rate Data` | Datos de tasa lenta |  |  |
| `Slow=9` | Lento=9 |  |  |
| `System Gain:` | Ganancia del sistema: |  |  |
| `System not initialized` | Sistema no inicializado |  |  |
| `The connection was refused by the regulator '%1'. Make sure the regulator is running and confirm the host name and port settings.` | El regulador '%1' ha rechazado la conexión. Asegurarse de que el regulador está en funcionamiento y confirmar el nombre de host y la configuración del puerto. |  |  |
| `The following error occurred connecting to regulator '%1': %2.` | Se ha producido el siguiente error al conectar con el regulador '%1': %2. |  |  |
| `The name cannot be empty.` | El nombre no puede estar vacío. |  |  |
| `The name cannot contain %1, because it is used in the names of the files downloaded from this regulator.` | El nombre no puede contener %1, porque se utiliza en los nombres de los archivos descargados de este regulador. |  |  |
| `The name cannot contain control characters, because it is used in the names of the files downloaded from this regulator.` | El nombre no puede contener caracteres de control, porque se utiliza en los nombres de los archivos descargados de este regulador. |  |  |
| `The name cannot end with a '.'` | El nombre no puede terminar con '.' |  |  |
| `The requested device operation is not supported or prohibited by the running operating system.` | El sistema operativo en ejecución no admite o prohíbe la operación solicitada en el dispositivo. |  |  |
| `This error occurs when an operation is executed that can only be successfully performed if the device is open.` | Este error se produce al ejecutar una operación que solo puede completarse correctamente con el dispositivo abierto. |  |  |
| `This session has been idle and is about to time out.\n\nThe regulator will be disconnected in %1 seconds unless you continue.` | Esta sesión ha estado inactiva y está a punto de expirar.\n\nEl regulador se desconectará dentro de %1 segundos si no se continúa. |  |  |
| `Time Stamp Transcript?` | ¿Marcar la transcripción con la hora? |  |  |
| `toolBar` | toolBar |  |  |
| `Transcript` | Transcripción |  |  |
| `UART Settings...` | Configuración de UART... |  |  |
| `USB` | USB |  |  |
| `View` | Ver |  |  |
| `View EEPROM Contents...` | Ver el contenido de la EEPROM... |  |  |
| `View Regulator Information?` | ¿Ver la información del regulador? |  |  |
| `View Regulator Status?` | ¿Ver el estado del regulador? |  |  |
| `View Transcript in Separate Window?` | ¿Ver la transcripción en una ventana aparte? |  |  |
| `View Transcript?` | ¿Ver la transcripción? |  |  |
| `Voltage Calibration Settings...` | Configuración de la calibración de tensión... |  |  |
| `Voltage Controller Settings...` | Configuración del controlador de tensión... |  |  |
| `WARNING: %1` | AVISO: %1 |  |  |
| `Would you like to disconnect from '%1'` | ¿Desea desconectarse de '%1'? | CHECK: the English has no closing question mark. Spanish needs the pair ¿ ... ?, so a closing '?' has been added; if the app appends anything after this string the punctuation will need revisiting. |  |
| `Would you like to revert to Basic Mode?` | ¿Desea volver al modo básico? |  |  |

## Connected window - status bar (10)

| Original (English) | Translation (es-ES) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `Auto Refresh` | Actualización automática | LENGTH: 12 -&gt; 24 characters in a status-bar cell. «Auto. autom.» is not acceptable Spanish; if it clips, the field should be widened rather than abbreviated. |  |
| `Auto Refresh` | Actualización automática | LENGTH: 12 -&gt; 24 characters in a status-bar cell. «Auto. autom.» is not acceptable Spanish; if it clips, the field should be widened rather than abbreviated. |  |
| `Connection` | Conexión |  |  |
| `Connection` | Conexión |  |  |
| `Faults` | Fallos |  |  |
| `Faults` | Fallos |  |  |
| `Regulating` | En regulación |  |  |
| `Regulating` | En regulación |  |  |
| `Regulator` | Regulador |  |  |
| `Regulator` | Regulador |  |  |

## Connection editor dialog (22)

| Original (English) | Translation (es-ES) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `...` | ... |  |  |
| `000.000.000.000;_` | 000.000.000.000;_ |  |  |
| `A Bluetooth Device must be selected.` | Es necesario seleccionar un dispositivo Bluetooth. |  |  |
| `Comm Port must be set.` | Es necesario indicar el puerto de comunicaciones. |  |  |
| `Comm Port:` | Puerto de comunicaciones: | LENGTH: «Comm Port:» is 10 characters, this is 26, and it labels a narrow combo box in the connection editor. «Puerto COM:» is the short fallback. |  |
| `Direct Bluetooth Connection` | Conexión Bluetooth directa |  |  |
| `Edit/Create Regulator Connection` | Editar o crear una conexión de regulador |  |  |
| `Host Name` | Nombre de host |  |  |
| `Host Name:` | Nombre de host: |  |  |
| `Invalid IP Address: %1` | Dirección IP no válida: %1 |  |  |
| `Invalid Port: %1` | Puerto no válido: %1 |  |  |
| `IP Address` | Dirección IP |  |  |
| `IP Address or Hostname must be set.` | Es necesario indicar la dirección IP o el nombre de host. |  |  |
| `IP Address:` | Dirección IP: |  |  |
| `Is USB/RS-232 Serial Port (Not Bluetoooth)?` | ¿Es un puerto serie USB/RS-232 (no Bluetooth)? | CHECK: the English misspells it 'Bluetoooth'; the Spanish spells it correctly. |  |
| `Please select a local or remote connection` | Seleccionar una conexión local o remota |  |  |
| `Port:` | Puerto: |  |  |
| `Regulator name must be set.` | Es necesario indicar el nombre del regulador. |  |  |
| `Regulator Name:` | Nombre del regulador: |  |  |
| `Selected Device:` | Dispositivo seleccionado: |  |  |
| `Serial Port Connection` | Conexión por puerto serie |  |  |
| `TCP/IP Connection:` | Conexión TCP/IP: |  |  |

## Connection status and errors (19)

| Original (English) | Translation (es-ES) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `%1 commands in a row went unanswered` | %1 comandos consecutivos quedaron sin respuesta |  |  |
| `115.2k` | 115.2k |  |  |
| `230.4k` | 230.4k |  |  |
| `38.4k` | 38.4k |  |  |
| `57.6k` | 57.6k |  |  |
| `Cannot log back in to the regulator. Status polling has stopped - please disconnect and reconnect.` | No se ha podido volver a iniciar sesión en el regulador. La consulta del estado se ha detenido - desconéctese y vuelva a conectarse. |  |  |
| `Cannot make sense of the regulator's replies. Status polling has stopped - please disconnect and reconnect.` | No se pueden interpretar las respuestas del regulador. La consulta del estado se ha detenido - desconéctese y vuelva a conectarse. |  |  |
| `Hardware Flow Control` | Control de flujo por hardware |  |  |
| `No Flow Control` | Sin control de flujo |  |  |
| `nothing has come back for %1 seconds` | no se recibe nada desde hace %1 segundos |  |  |
| `Paired` | Emparejado |  |  |
| `Paired with Authorization` | Emparejado con autorización |  |  |
| `Serial Port` | Puerto serie |  |  |
| `Software Flow Control` | Control de flujo por software |  |  |
| `The connection to regulator '%1' has been lost - %2. Check the link and reconnect. If the regulator is still holding the previous session, reconnecting can take a few minutes.` | Se ha perdido la conexión con el regulador '%1' - %2. Compruebe el enlace y vuelva a conectarse. Si el regulador mantiene todavía la sesión anterior, volver a conectarse puede tardar unos minutos. |  |  |
| `the login was not answered` | el inicio de sesión no obtuvo respuesta |  |  |
| `The regulator has stopped responding - %1 commands in a row went unanswered.` | El regulador ha dejado de responder - %1 comandos consecutivos quedaron sin respuesta. |  |  |
| `The regulator is responding again.` | El regulador vuelve a responder. |  |  |
| `Unpaired` | No emparejado |  |  |

## Debug logging dialog (13)

| Original (English) | Translation (es-ES) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `<Filter>` | &lt;Filtro&gt; |  |  |
| `...` | ... |  |  |
| `Append to Log File?` | ¿Añadir al archivo de registro? |  |  |
| `Check All` | Marcar todo |  |  |
| `Log File` | Archivo de registro |  |  |
| `Log File:` | Archivo de registro: |  |  |
| `Log Files (*.log);;All Files (*.*)` | Archivos de registro (*.log);;Todos los archivos (*.*) |  |  |
| `Logging Categories:` | Categorías de registro: |  |  |
| `Logging Category` | Categoría de registro |  |  |
| `Select Logging Categories` | Seleccionar las categorías de registro |  |  |
| `Show Qt Categories?` | ¿Mostrar las categorías de Qt? |  |  |
| `Uncheck All` | Desmarcar todo |  |  |
| `Uncheck All Debug` | Desmarcar toda la depuración |  |  |

## EEPROM contents viewer (9)

| Original (English) | Translation (es-ES) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `<ADDRESS>` | &lt;DIRECCIÓN&gt; |  |  |
| `<VALUE>` | &lt;VALOR&gt; |  |  |
| `0x00 0 ` | 0x00 0  |  |  |
| `0x00000000 ` | 0x00000000  |  |  |
| `Address:` | Dirección: |  |  |
| `EEPROM Contents` | Contenido de la EEPROM |  |  |
| `EEPROM Contents:` | Contenido de la EEPROM: |  |  |
| `EEPROM Contents: Loading...` | Contenido de la EEPROM: cargando... |  |  |
| `Value:` | Valor: |  |  |

## File download progress (20)

| Original (English) | Translation (es-ES) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `%1 of %2%3 (%4%)` | %1 de %2%3 (%4%) | CHECK: the '%' straight after %4 is a literal percent sign, not a placeholder. No space inserted before it, matching normal Spanish software practice. |  |
| `%1%2` | %1%2 |  |  |
| `%1h %2m` | %1 h %2 min |  |  |
| `%1m %2s` | %1 min %2 s | CHECK: the minute symbol in Spanish is «min», not «m» (which is metres). |  |
| `%1s` | %1 s | CHECK: a space added between the number and the unit symbol, as Spanish typography requires. Same for the two duration strings that follow. |  |
| `0.%1 seconds` | 0,%1 segundos | CHECK: decimal separator changed from point to comma, as Spanish requires. |  |
| `Abort Download` | Cancelar la descarga |  |  |
| `About %1 remaining` | Tiempo restante aproximado: %1 | CHECK: restructured from 'About %1 remaining'. A literal Spanish rendering breaks because %1 can be «menos de un segundo», which does not sit after «aproximadamente». |  |
| `Could not open file` | No se ha podido abrir el archivo |  |  |
| `Could not open file '%1' for write.  Please check Permissions` | No se ha podido abrir el archivo '%1' para escritura.  Comprobar los permisos |  |  |
| `Downloading File` | Descargando archivo |  |  |
| `Downloading File '%1'` | Descargando el archivo '%1' |  |  |
| `Downloading file '%1'` | Descargando el archivo '%1' |  |  |
| `Error downloading file` | Error al descargar el archivo |  |  |
| `Finishing up...` | Finalizando... |  |  |
| `less than a second` | menos de un segundo |  |  |
| `Please Select Download Directory` | Seleccionar la carpeta de descarga |  |  |
| `Seconds Remaining until Timeout:` | Segundos restantes hasta el tiempo de espera: | LENGTH: 31 -&gt; 47 characters in a progress dialog label that sits next to a number. If it clips, «Segundos hasta el tiempo de espera:» is a safe shortening. |  |
| `Seconds Remaining until Timeout: %1 seconds` | Segundos restantes hasta el tiempo de espera: %1 segundos |  |  |
| `Timeout while downloading` | Tiempo de espera agotado durante la descarga |  |  |

## Main window - menus, toolbar and buttons (23)

| Original (English) | Translation (es-ES) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `  #  ` |   #   |  |  |
| `&About` | &amp;Acerca de |  |  |
| `&Connect` | &amp;Conectar |  |  |
| `&Disconnect from Selected Regulator` | &amp;Desconectar del regulador seleccionado |  |  |
| `&Exit` | &amp;Salir |  |  |
| `&File` | &amp;Archivo |  |  |
| `&Help` | A&amp;yuda | CHECK: mnemonic on the 'y' because «Archivo» already claims 'A' in the same menu bar. |  |
| `&Regulator` | &amp;Regulador |  |  |
| `...` | ... |  |  |
| `Add a new Regulator` | Añadir un regulador |  |  |
| `Connect to Selected Regulator` | Conectar con el regulador seleccionado |  |  |
| `Debug Logging...` | Registro de depuración... |  |  |
| `Disconnect from Selected Regulator` | Desconectar del regulador seleccionado |  |  |
| `Edit Selected Regulator` | Editar el regulador seleccionado |  |  |
| `Enable &Advanced Mode...` | Activar el modo &amp;avanzado... |  |  |
| `Enable &Basic Mode` | Activar el modo &amp;básico |  |  |
| `MainWindow` | MainWindow |  |  |
| `Regulator Name Filter` | Filtro por nombre de regulador |  |  |
| `Regulators:` | Reguladores: |  |  |
| `Remove Selected Regulator` | Quitar el regulador seleccionado |  |  |
| `Settings` | Configuración |  |  |
| `Settings...` | Configuración... |  |  |
| `toolBar` | toolBar |  |  |

## Main window - regulator table column headers (10)

| Original (English) | Translation (es-ES) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `   #   ` |    #    |  |  |
| `Color` | Color |  |  |
| `Connection Status` | Estado de la conexión |  |  |
| `Connection Type` | Tipo de conexión |  |  |
| `Last Connection` | Última conexión |  |  |
| `Not Connected` | No conectado |  |  |
| `Port or IPAddress` | Puerto o dirección IP |  |  |
| `Regulating Status` | Estado de regulación |  |  |
| `Regulator Name` | Nombre del regulador |  |  |
| `Regulator Status` | Estado del regulador |  |  |

## Numeric entry dialogs (6)

| Original (English) | Translation (es-ES) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `Enter Integer` | Introducir un número entero |  |  |
| `Enter Integer` | Introducir un número entero |  |  |
| `Integer` | Número entero |  |  |
| `Integer` | Número entero |  |  |
| `Max` | Máx |  |  |
| `Min` | Mín |  |  |

## Other (QObject) (3)

| Original (English) | Translation (es-ES) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `%1 - ` | %1 -  |  |  |
| `Cmd: %1 - Error Count: %2` | Comando: %1 - Número de errores: %2 |  |  |
| `Warning - Consecutive command ran too quickly '%1'` | Aviso: el comando consecutivo se ha ejecutado demasiado pronto '%1' | AMBIGUOUS: the English ('Consecutive command ran too quickly') is itself unclear - it appears to mean the command was sent before the inter-command delay had elapsed. Translated on that reading. |  |

## Parameter file editor (59)

| Original (English) | Translation (es-ES) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `+ or - followed by 2 digits` | + o - seguido de 2 dígitos |  |  |
| `...` | ... |  |  |
| `0 or 1` | 0 o 1 |  |  |
| `1 digit` | 1 dígito |  |  |
| `2 digits` | 2 dígitos |  |  |
| `3 digits` | 3 dígitos |  |  |
| `4 digits` | 4 dígitos |  |  |
| `Active Voltage Target` | Tensión objetivo activa |  |  |
| `All Disabled on Any Fault` | Todas desactivadas ante cualquier fallo | AGREEMENT: feminine plural «todas ... desactivadas» agrees with «las fases», which the longer form of this setting names. Correct only while the subject stays «fases». |  |
| `Amperage Rating LSB` | Corriente nominal LSB | CHECK: LSB/MSB kept as English abbreviations - they are how the byte layout is documented, not prose. |  |
| `Amperage Rating MSB` | Corriente nominal MSB |  |  |
| `B or + or - followed by 2 digits` | B, + o - seguido de 2 dígitos |  |  |
| `Current Data` | Datos actuales |  |  |
| `Description` | Descripción |  |  |
| `Edit Parameter File` | Editar el archivo de parámetros |  |  |
| `End Position` | Posición final |  |  |
| `Error Message:` | Mensaje de error: |  |  |
| `Expected Data` | Datos esperados |  |  |
| `Externally Controlled Select (1 or 2)` | Selección controlada externamente (1 o 2) |  |  |
| `File '%1' content was not 57 characters` | El contenido del archivo '%1' no tenía 57 caracteres |  |  |
| `File '%1' Could not be Opened.` | No se ha podido abrir el archivo '%1'. |  |  |
| `Frequency` | Frecuencia |  |  |
| `Ignored 21 bytes` | 21 bytes ignorados |  |  |
| `Ignored 3 bytes` | 3 bytes ignorados |  |  |
| `Ignored 4 bytes` | 4 bytes ignorados |  |  |
| `Invalid character/text at position %1. Expected '%2', Got '%3'` | Carácter o texto no válido en la posición %1. Se esperaba '%2' y se ha obtenido '%3' |  |  |
| `Invalid Parameter File` | Archivo de parámetros no válido |  |  |
| `Open Parameter File` | Abrir el archivo de parámetros |  |  |
| `Over Current Fault Count Limit` | Límite del recuento de fallos por sobreintensidad | LENGTH: 30 -&gt; 48 characters in the parameter-file table's Description column. «Límite de fallos por sobreintensidad» is the fallback if it clips. |  |
| `Over Voltage Limit` | Límite de sobretensión |  |  |
| `Over Voltage Protection Limit` | Límite de protección contra sobretensión |  |  |
| `P followed by any 1 byte` | P seguido de 1 byte cualquiera |  |  |
| `Parameter File` | Archivo de parámetros |  |  |
| `Parameter File:` | Archivo de parámetros: |  |  |
| `Phase Voltage Offset` | Desviación de tensión de fase | TERM: «offset» -&gt; «desviación», used consistently (also in «Voltage Calibration Offset»). Spanish engineers often keep the English «offset»; confirm house preference. |  |
| `Power Interactive Regulation` | Regulación interactiva de potencia |  |  |
| `Power Interactive Regulation Delta Voltage` | Tensión delta de la regulación interactiva de potencia | TERM+LENGTH: «delta voltage» -&gt; «tensión delta» (held for the tree label, the settings field and the PIR command). 42 -&gt; 53 characters in a table column. |  |
| `Power Interactive Regulation NULL Voltage` | Tensión nula de la regulación interactiva de potencia | LENGTH: 41 -&gt; 52 characters in the parameter-file Description column. |  |
| `Power Interactive Regulation Time Constant` | Constante de tiempo de la regulación interactiva de potencia | LENGTH: 42 -&gt; 60 characters in the parameter-file Description column. |  |
| `Prefix` | Prefijo |  |  |
| `Ramp Rate` | Velocidad de rampa |  |  |
| `Ramp to Vin` | Rampa hasta Vin |  |  |
| `Raw Data` | Datos en bruto |  |  |
| `Reset To Current` | Restablecer el actual | AGREEMENT: elliptical button label. Masculine «el actual» agrees with «archivo (de parámetros)», which is what it restores; it would be wrong if the button were ever reused for a feminine object. |  |
| `Reset to Current Parameter File` | Restablecer el archivo de parámetros actual |  |  |
| `Reset to Default` | Restablecer el predeterminado | AGREEMENT: same ellipsis as «Reset To Current» - masculine, agreeing with «archivo». |  |
| `Reset to Default Parameter File` | Restablecer el archivo de parámetros predeterminado |  |  |
| `Save Parameter File` | Guardar el archivo de parámetros |  |  |
| `Select Parameter File` | Seleccionar el archivo de parámetros |  |  |
| `SPARE` | SPARE |  |  |
| `Start Position` | Posición inicial |  |  |
| `System Gain` | Ganancia del sistema |  |  |
| `Target Voltage 1` | Tensión objetivo 1 |  |  |
| `Target Voltage 2` | Tensión objetivo 2 |  |  |
| `Text Files (*.txt);;All Files (*.*)` | Archivos de texto (*.txt);;Todos los archivos (*.*) |  |  |
| `Under Voltage Limit` | Límite de subtensión |  |  |
| `Voltage Regulation Disabled` | Regulación de tensión desactivada |  |  |
| `Voltage Setpoint 1` | Consigna de tensión 1 |  |  |
| `Voltage Setpoint 2` | Consigna de tensión 2 |  |  |

## Password and credential prompts (17)

| Original (English) | Translation (es-ES) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `...` | ... |  |  |
| `...` | ... |  |  |
| `Access to %1 requires the correct password to be entered.` | El acceso a %1 requiere introducir la contraseña correcta. |  |  |
| `Confirm Password:` | Confirmar la contraseña: |  |  |
| `Confirmation password does not match` | La contraseña de confirmación no coincide |  |  |
| `Current password is not correct` | La contraseña actual no es correcta |  |  |
| `Current Password:` | Contraseña actual: |  |  |
| `Enter Credentials` | Introducir las credenciales |  |  |
| `Enter Password` | Introducir la contraseña |  |  |
| `Enter Password:` | Introducir la contraseña: |  |  |
| `Incorrect Password` | Contraseña incorrecta |  |  |
| `Incorrect password entered, Access to %1 denied.` | Contraseña incorrecta; se deniega el acceso a %1. |  |  |
| `New password does not satisfy length criteria` | La nueva contraseña no cumple el requisito de longitud |  |  |
| `Password Required` | Contraseña necesaria |  |  |
| `Password Required for %1` | Contraseña necesaria para %1 |  |  |
| `Password:` | Contraseña: |  |  |
| `Username:` | Nombre de usuario: |  |  |

## Regulator Information panel (18)

| Original (English) | Translation (es-ES) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| ` - Not Connected` |  - No conectado |  |  |
| `<Unknown>` | &lt;Desconocido&gt; |  |  |
| `...` | ... |  |  |
| `Connected Via:` | Conectado mediante: |  |  |
| `GroupBox` | GroupBox |  |  |
| `Invalid Serial Number` | Número de serie no válido | CHECK: «no válido» is the es-ES convention for 'invalid'; «inválido» is avoided throughout. |  |
| `Name:` | Nombre: |  |  |
| `Phase Firmware Version:` | Versión del firmware de fase: |  |  |
| `Product:` | Producto: |  |  |
| `Regulating Status:` | Estado de regulación: |  |  |
| `Regulator Information` | Información del regulador |  |  |
| `Regulator Information:` | Información del regulador: |  |  |
| `Regulator's System Clock:` | Reloj del sistema del regulador: |  |  |
| `Serial Number (12 Characters):` | Número de serie (12 caracteres): |  |  |
| `Serial Number:` | Número de serie: |  |  |
| `Set Serial Number` | Establecer el número de serie |  |  |
| `System Firmware Version and Compilation Date:` | Versión del firmware del sistema y fecha de compilación: |  |  |
| `The serial number must have 12 characters` | El número de serie debe tener 12 caracteres |  |  |

## Regulator status and messages (21)

| Original (English) | Translation (es-ES) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `    File #: %1` |     Archivo n.º: %1 | CHECK: '#' rendered as «n.º», the Spanish ordinal abbreviation. The four leading spaces are preserved. |  |
| ` - Regulator clock off by %1` |  - reloj del regulador desfasado en %1 |  |  |
| ` - Running Command` |  - ejecutando comando |  |  |
| ` and ` |  y  | CHECK: joins duration fragments ('1 hora y 2 minutos'). Spanish «y» becomes «e» before a word starting with i-/hi-, but no duration unit does, so «y» is always safe here. |  |
| `%1 Hour` | %1 hora |  |  |
| `%1 Hours` | %1 horas |  |  |
| `%1 Minute` | %1 minuto |  |  |
| `%1 Minutes` | %1 minutos |  |  |
| `%1 Second` | %1 segundo |  |  |
| `%1 Seconds` | %1 segundos |  |  |
| `Enabled` | Activado |  |  |
| `Firmware must be updated to support Voltage Calibration` | Es necesario actualizar el firmware para admitir la calibración de tensión |  |  |
| `Firmware must be upgraded to V17 or later to support Voltage Calibration` | Es necesario actualizar el firmware a la versión V17 o posterior para admitir la calibración de tensión |  |  |
| `Number of SD Card files: %1` | Número de archivos en la tarjeta SD: %1 |  |  |
| `Regulation Information:` | Información de regulación: |  |  |
| `Regulator Will Reboot` | El regulador se reiniciará |  |  |
| `Target Voltage 1` | Tensión objetivo 1 |  |  |
| `Target Voltage 2` | Tensión objetivo 2 |  |  |
| `This command will force the regulator to reboot. After it reboots and the green LED on the regulator comes on, you will need to reconnect.` | Este comando obliga al regulador a reiniciarse. Cuando se haya reiniciado y se encienda el LED verde del regulador, será necesario volver a conectarse. |  |  |
| `Unknown` | Desconocido | AGREEMENT: this single string is returned by the regulator-status, regulating-status AND SD-card-status converters in Core/Enums.cpp. Masculine is right for the first two; the SD-card row would want «Desconocida». Unresolvable without splitting the source string. |  |
| `Voltage Control must be set to either Set point 1 or 2` | El control de tensión debe estar ajustado a la consigna 1 o a la 2 | TERM: setpoint -&gt; «consigna», the standard Spanish control-engineering term. Confirm that utility engineers here do not simply say «punto de consigna» or keep «setpoint». |  |

## Regulator status trees (59)

| Original (English) | Translation (es-ES) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `Active Voltage Target` | Tensión objetivo activa |  |  |
| `ADC Cal Error` | Error de calibración del ADC |  |  |
| `All Phases Disabled on Failure in Any Phase` | Todas las fases desactivadas si falla cualquiera de ellas | LENGTH: 42 -&gt; 57 characters in a status-tree label column. |  |
| `Amperage Rating (A)` | Corriente nominal (A) |  |  |
| `Baud Rate` | Velocidad en baudios | LENGTH: 9 -&gt; 20 characters. It labels a narrow combo box in the UART dialog and a tree column; «Baudios» alone is the fallback. |  |
| `Connection:` | Conexión: |  |  |
| `Current (A)` | Corriente (A) |  |  |
| `Delta Voltage (V)` | Tensión delta (V) |  |  |
| `Fault Code` | Código de fallo |  |  |
| `Flow Control` | Control de flujo |  |  |
| `Flux Sensor` | Sensor de flujo |  |  |
| `Form` | Form |  |  |
| `Form` | Form |  |  |
| `Frequency` | Frecuencia |  |  |
| `No` | No |  |  |
| `Null Voltage (V)` | Tensión nula (V) |  |  |
| `Over Current Fault Count` | Recuento de fallos por sobreintensidad | LENGTH: 24 -&gt; 38 characters in a status-tree label column. |  |
| `Over Current Fault Count` | Recuento de fallos por sobreintensidad | LENGTH: 24 -&gt; 38 characters in a status-tree label column. |  |
| `Over Current Fault in Reset Delay` | Fallo por sobreintensidad en retardo de restablecimiento | LENGTH: 33 -&gt; 56 characters in a status-tree label column. |  |
| `Over Current Fault Limit` | Límite de fallos por sobreintensidad |  |  |
| `Over Temperature` | Sobretemperatura |  |  |
| `Over Voltage Limit` | Límite de sobretensión |  |  |
| `Over Voltage Protection Limit` | Límite de protección contra sobretensión |  |  |
| `Phase %1` | Fase %1 |  |  |
| `Phase Lock Loop not Locked` | PLL no enganchado | TERM: «phase lock loop» -&gt; PLL, «not locked» -&gt; «no enganchado» (bucle de enganche de fase). Spelling out «Bucle de enganche de fase no enganchado» would be both redundant and far too long for the tree. |  |
| `Power Interactive Regulation Status` | Estado de la regulación interactiva de potencia |  |  |
| `Power Interactive Regulation Status` | Estado de la regulación interactiva de potencia |  |  |
| `Ramp Rate` | Velocidad de rampa |  |  |
| `Reaction Time (s)` | Tiempo de reacción (s) |  |  |
| `Regulating Status` | Estado de regulación |  |  |
| `Regulating:` | Regulación: |  |  |
| `Regulator at Maximum Boost or Buck` | Regulador en elevación o reducción máxima | TERM: boost/buck -&gt; «elevación»/«reducción». Spanish power-electronics practice often keeps «boost»/«buck» untranslated; confirm house preference, as this decision recurs in several strings. |  |
| `Regulator Faults:` | Fallos del regulador: |  |  |
| `Regulator Ramping` | Regulador en rampa |  |  |
| `Regulator:` | Regulador: |  |  |
| `SCR or Gate Drive Faults` | Fallos del SCR o de la excitación de puerta |  |  |
| `SD Card Status` | Estado de la tarjeta SD |  |  |
| `Settings` | Configuración |  |  |
| `Settings` | Configuración |  |  |
| `Status:` | Estado: |  |  |
| `System Gain` | Ganancia del sistema |  |  |
| `Target Voltage 1` | Tensión objetivo 1 |  |  |
| `Target Voltage 2` | Tensión objetivo 2 |  |  |
| `Temp Sensor or Fan` | Sensor de temperatura o ventilador |  |  |
| `Temperature (°C)` | Temperatura (°C) |  |  |
| `UART 1` | UART 1 |  |  |
| `UART 1` | UART 1 |  |  |
| `UART 1` | UART 1 |  |  |
| `UART 2` | UART 2 |  |  |
| `UART 2` | UART 2 |  |  |
| `UART 2` | UART 2 |  |  |
| `Under Voltage Limit` | Límite de subtensión |  |  |
| `VCC or Fuse` | VCC o fusible |  |  |
| `Vin/Vout out of limit` | Vin/Vout fuera de límite |  |  |
| `Voltage Calibration Offset` | Desviación de calibración de tensión |  |  |
| `Voltage In (V)` | Tensión de entrada (V) |  |  |
| `Voltage Out (V)` | Tensión de salida (V) |  |  |
| `Voltage Regulation Disabled` | Regulación de tensión desactivada |  |  |
| `Yes` | Sí |  |  |

## SD card download dialog (36)

| Original (English) | Translation (es-ES) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `...` | ... |  |  |
| `2 Days Ago` | Hace 2 días |  |  |
| `3 Days Ago` | Hace 3 días |  |  |
| `4 Days Ago` | Hace 4 días |  |  |
| `5 Days Ago` | Hace 5 días |  |  |
| `6 Days Ago` | Hace 6 días |  |  |
| `7 Days Ago` | Hace 7 días |  |  |
| `A file is still downloading. Cancel it in the progress window before closing this one.` | Todavía se está descargando un archivo. Cancélelo en la ventana de progreso antes de cerrar esta. |  |  |
| `April` | Abril |  |  |
| `August` | Agosto |  |  |
| `Command` | Comando |  |  |
| `Data will not be recorded or updated during file downloads` | Los datos no se registrarán ni se actualizarán durante la descarga de archivos |  |  |
| `December` | Diciembre |  |  |
| `Download in progress` | Descarga en curso |  |  |
| `Download not started` | La descarga no se ha iniciado |  |  |
| `Fault Log` | Registro de fallos |  |  |
| `February` | Febrero |  |  |
| `File Name` | Nombre del archivo |  |  |
| `January` | Enero | CHECK: Spanish month names are normally lowercase, but these are standalone group headings in a tree, so sentence case gives them an initial capital. Applies to all twelve. |  |
| `July` | Julio |  |  |
| `June` | Junio |  |  |
| `March` | Marzo |  |  |
| `May` | Mayo |  |  |
| `Modification Date` | Fecha de modificación |  |  |
| `Name` | Nombre |  |  |
| `November` | Noviembre |  |  |
| `October` | Octubre |  |  |
| `SD Card Files` | Archivos de la tarjeta SD |  |  |
| `Select` | Seleccionar |  |  |
| `September` | Septiembre |  |  |
| `Size (Bytes)` | Tamaño (bytes) |  |  |
| `The regulator is still busy with the previous transfer. Please try again in a moment.` | El regulador todavía está ocupado con la transferencia anterior. Vuelva a intentarlo en un momento. |  |  |
| `This Month` | Este mes |  |  |
| `Today` | Hoy |  |  |
| `Waiting for regulator...` | Esperando al regulador... |  |  |
| `Yesterday` | Ayer |  |  |

## Settings dialog (68)

| Original (English) | Translation (es-ES) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `      This setting is also the time between consecutive commands.` |       Este ajuste es también el tiempo entre comandos consecutivos. | CHECK: the six leading spaces are the source's own indentation and have been preserved. |  |
| ` Amps` |  amperios |  |  |
| ` s` |  s |  |  |
| ` Seconds` |  segundos |  |  |
| ` Volts` |  voltios |  |  |
| `<the system Downloads folder>` | &lt;la carpeta Descargas del sistema&gt; |  |  |
| `+` | + |  |  |
| `-` | - |  |  |
| `1` | 1 |  |  |
| `Advanced user password:` | Contraseña de usuario avanzado: |  |  |
| `Amperage Rating:` | Corriente nominal: |  |  |
| `As Needed` | Cuando sea necesario |  |  |
| `Asked for when the tool starts, and by Settings > Enable Advanced Mode. Takes effect immediately.` | Se solicita al iniciar la herramienta y en Configuración &gt; Activar el modo avanzado. Se aplica de inmediato. |  |  |
| `Automatically Refresh Status?` | ¿Actualizar el estado automáticamente? |  |  |
| `Change Advanced User Password` | Cambiar la contraseña de usuario avanzado |  |  |
| `Change Advanced User Password...` | Cambiar la contraseña de usuario avanzado... |  |  |
| `Choose the language the tool is displayed in. The change takes effect immediately; any regulator windows that are already open keep their current language until they are reopened.` | Elija el idioma en el que se muestra la herramienta. El cambio se aplica de inmediato; las ventanas de regulador ya abiertas mantienen su idioma actual hasta que se vuelvan a abrir. |  |  |
| `Command Timeout:` | Tiempo de espera de comando: |  |  |
| `Default Regulator Settings` | Configuración predeterminada del regulador |  |  |
| `Default Time Zone` | Zona horaria predeterminada |  |  |
| `Default View Settings` | Configuración de visualización predeterminada |  |  |
| `Download Timeout:` | Tiempo de espera de descarga: |  |  |
| `Downloads` | Descargas |  |  |
| `External Voltage Setpoint Select (1 or 2)` | Selección externa de la consigna de tensión (1 o 2) |  |  |
| `Fast` | Rápido |  |  |
| `Fast:` | Rápido: |  |  |
| `Folder for Downloaded Files` | Carpeta para los archivos descargados |  |  |
| `Language` | Idioma |  |  |
| `Medium` | Medio |  |  |
| `Medium:` | Medio: |  |  |
| `NULL Voltage at Zero kW:` | Tensión nula a cero kW: |  |  |
| `Power Interactive Regulation` | Regulación interactiva de potencia |  |  |
| `Power Interactive Regulation Settings` | Configuración de la regulación interactiva de potencia |  |  |
| `Ramp to Vin` | Rampa hasta Vin |  |  |
| `Refresh for Regulator Clock Time` | Actualización de la hora del reloj del regulador |  |  |
| `Refresh for Regulator Faults and Voltages:` | Actualización de los fallos y las tensiones del regulador: |  |  |
| `Refresh for SD Card Files:` | Actualización de los archivos de la tarjeta SD: |  |  |
| `Refresh for Voltage Calibration Status:` | Actualización del estado de calibración de tensión: |  |  |
| `Refresh Gain Values:` | Actualización de los valores de ganancia: |  |  |
| `Refresh Rate Parameter File Information:` | Frecuencia de actualización de la información del archivo de parámetros: | LENGTH: 40 -&gt; 71 characters on a settings-dialog label. «Actualización del archivo de parámetros:» is the safe shortening if the column is fixed. |  |
| `Refresh Settings` | Configuración de actualización |  |  |
| `Refresh Times:` | Intervalos de actualización: |  |  |
| `Refresh UART Settings:` | Actualización de la configuración de UART: |  |  |
| `Regulator Setting Defaults` | Valores predeterminados del regulador |  |  |
| `Regulator:` | Regulador: |  |  |
| `Require Password to Enter Advanced Mode?` | ¿Exigir contraseña para entrar en el modo avanzado? |  |  |
| `Save downloaded files to:` | Guardar los archivos descargados en: |  |  |
| `Security` | Seguridad |  |  |
| `Settings` | Configuración |  |  |
| `Setup UARTs` | Configurar las UART |  |  |
| `Show password` | Mostrar la contraseña |  |  |
| `Slow` | Lento |  |  |
| `Slow:` | Lento: |  |  |
| `Start in Advanced Mode?` | ¿Iniciar en modo avanzado? |  |  |
| `The Advanced user password has been changed.` | Se ha cambiado la contraseña de usuario avanzado. |  |  |
| `Time Constant:` | Constante de tiempo: |  |  |
| `Timeout Settings` | Configuración de tiempos de espera |  |  |
| `Timestamp Transcript?` | ¿Marcar la transcripción con la hora? |  |  |
| `Update Settings For All Regulators?` | ¿Aplicar la configuración a todos los reguladores? |  |  |
| `View Regulator Information?` | ¿Ver la información del regulador? |  |  |
| `View Regulator Status?` | ¿Ver el estado del regulador? |  |  |
| `View Transcript in Sepeate Window?` | ¿Ver la transcripción en una ventana aparte? | CHECK: the English misspells 'Separate' as 'Sepeate'; the Spanish is spelled correctly. Note this is a second, separately-keyed copy of the same label in NUi::CConnectedRegulator. |  |
| `View Transcript?` | ¿Ver la transcripción? |  |  |
| `Voltage Control Settings` | Configuración del control de tensión |  |  |
| `Voltage Delta:` | Tensión delta: |  |  |
| `Voltage Setpoint 1:` | Consigna de tensión 1: |  |  |
| `Voltage Setpoint 2:` | Consigna de tensión 2: |  |  |
| `±` | ± |  |  |

## Status and fault values - tables, trees and panels (128)

| Original (English) | Translation (es-ES) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `(in multiphase models only) Indicates one of the phases has an open fuse or there is no VCC power. NOTE - a single phase model could not be communicating.` | (solo en modelos multifásicos) Indica que una de las fases tiene un fusible abierto o que no hay alimentación VCC. NOTA: en un modelo monofásico podría tratarse de una falta de comunicación. | AMBIGUOUS: the English note ('a single phase model could not be communicating') is a fragment. Read as 'on a single-phase model this may simply mean it is not communicating'. Worth confirming against the firmware documentation. |  |
| `7A` | 7A |  |  |
| `9A` | 9A |  |  |
| `Active` | Activa | AGREEMENT: verified in Core/Enums.cpp - this and the next five values are the SD-card status enum only, so they take feminine agreement with «la tarjeta SD». (The pt-PT reference used masculine here.) |  |
| `B2` | B2 |  |  |
| `B8` | B8 |  |  |
| `BA` | BA |  |  |
| `Bound` | Vinculado | TERM: Qt socket state 'Bound'. «Vinculado» is the usual Spanish rendering of a bound socket; «Enlazado» is the alternative. |  |
| `CA` | CA |  |  |
| `CB` | CB |  |  |
| `Closing` | Cerrando |  |  |
| `Command Transmission Error` | Error de transmisión de comando |  |  |
| `Communication Error` | Error de comunicación |  |  |
| `Confirming Connection` | Confirmando la conexión |  |  |
| `Connected` | Conectado |  |  |
| `Connecting` | Conectando |  |  |
| `Data File downloaded - not implemented` | Archivo de datos descargado; no implementado |  |  |
| `DC` | DC |  |  |
| `Disabled` | Desactivada |  |  |
| `Disabled by Current >1.5X current rating - resets 15min after return to rated current` | Desactivado por corriente superior a 1,5 veces la corriente nominal; se restablece 15 min después de volver a la corriente nominal | CHECK: '1.5X' rendered as «1,5 veces» - decimal comma, and the multiplication 'X' spelled out because «1,5X» is not read as a multiplier in Spanish. |  |
| `Disabled by Over Current` | Desactivado por sobreintensidad |  |  |
| `Disabled by Over Temperature` | Desactivado por sobretemperatura |  |  |
| `Disabled by switch (3 phase only)` | Desactivado por el interruptor (solo en trifásico) |  |  |
| `Disabled by User` | Desactivado por el usuario |  |  |
| `Disabled by User command` | Desactivado por un comando del usuario |  |  |
| `Disabled by Voltage Issue` | Desactivado por un problema de tensión |  |  |
| `Disconnected` | Desconectado |  |  |
| `DS` | DS |  |  |
| `DU` | DU |  |  |
| `EA` | EA |  |  |
| `Enabled by User command - i.e. regulating` | Activado por un comando del usuario, es decir, en regulación |  |  |
| `Error Processing Voltage and Fault Status` | Error al procesar el estado de tensión y de fallos |  |  |
| `EU` | EU |  |  |
| `F4` | F4 |  |  |
| `F5` | F5 |  |  |
| `FA` | FA |  |  |
| `Failed` | Con fallo | CHECK: «Con fallo» rather than «Fallida» - it reads better as a status value and keeps the wording parallel with «Con fallo o ausente». |  |
| `Failed or Missing` | Con fallo o ausente |  |  |
| `Fan Fault Cleared` | Fallo del ventilador resuelto |  |  |
| `Fault` | Fallo |  |  |
| `FB` | FB |  |  |
| `FC` | FC |  |  |
| `FD` | FD |  |  |
| `FE` | FE |  |  |
| `FLUX` | FLUX |  |  |
| `Flux Sensor Error  If sustained, it writes to F/L once per hour (this will increase the number of Over Current Faults from transformer saturations)` | Error del sensor de flujo. Si persiste, se escribe en el F/L una vez por hora (esto aumentará el número de fallos por sobreintensidad debidos a saturaciones del transformador) | CHECK: the English separates the two sentences with a double space and no full stop; a full stop has been added. 'F/L' (fault log) is left as the abbreviation the firmware documentation uses. |  |
| `Getting System Info` | Obteniendo la información del sistema |  |  |
| `Host Found` | Host encontrado |  |  |
| `Host Lookup` | Buscando host |  |  |
| `Indicates a fault caused by a SCR gate drive error` | Indica un fallo provocado por un error de excitación de puerta del SCR |  |  |
| `Indicates a flux sensor malfunction which could cause the transformer to saturate` | Indica un fallo del sensor de flujo que podría provocar la saturación del transformador |  |  |
| `Indicates an A to D calibration error during bootup or Voltage sensing error` | Indica un error de calibración del conversor A/D durante el arranque o un error de medición de tensión |  |  |
| `Indicates Flux Sensor faults (>12 per 1/2 Second Interval)` | Indica fallos del sensor de flujo (más de 12 por intervalo de medio segundo) |  |  |
| `Indicates full PWM in boost mode (i.e. limiting the ability to hold the setpoint)` | Indica PWM al máximo en modo elevador (lo que limita la capacidad de mantener la consigna) |  |  |
| `Indicates full PWM in buck mode (i.e. limiting the ability to hold the setpoint)` | Indica PWM al máximo en modo reductor (lo que limita la capacidad de mantener la consigna) |  |  |
| `Indicates SCR or Gate Drive Faults (>12 per 1/2 Second Interval)` | Indica fallos del SCR o de la excitación de puerta (más de 12 por intervalo de medio segundo) |  |  |
| `Indicates the converter board is temporally in a over temperature state which will reset` | Indica que la placa del convertidor se encuentra temporalmente en estado de sobretemperatura, que se restablecerá | CHECK: 'temporally' again read as 'temporarily'. |  |
| `Indicates the Over Current Fault has cleared and returned to regulation` | Indica que el fallo por sobreintensidad se ha resuelto y se ha vuelto a la regulación |  |  |
| `Indicates the regulator is in a state of maximum Boost or Buck` | Indica que el regulador está en estado de elevación o reducción máxima |  |  |
| `Indicates the regulator is in an over current fault reset delay` | Indica que el regulador está en un retardo de restablecimiento de fallo por sobreintensidad |  |  |
| `Indicates there are no hardware faults and the regulator is not disabled i.e. regulating` | Indica que no hay fallos de hardware y que el regulador no está desactivado, es decir, está en regulación |  |  |
| `Indicates there are no hardware faults but the regulator is disabled for various reasons indicated in the Aux Status string. The cause could be it was disabled by the user, or as the result of a fault condition which may clear and return to regulation, or it is in a timer mode where regulation is temporally disabled.` | Indica que no hay fallos de hardware, pero que el regulador está desactivado por diversos motivos que se indican en la cadena de estado auxiliar. La causa puede ser que lo haya desactivado el usuario, una condición de fallo que puede resolverse y volver a la regulación, o que esté en un modo temporizado en el que la regulación está temporalmente desactivada. | CHECK: the English writes 'temporally' where it means 'temporarily'; translated as «temporalmente» (the intended sense). |  |
| `Indicates Vin or Vout is out of range, either because of high or low line voltage, or possibly a voltage sensing circuit error.` | Indica que Vin o Vout está fuera del intervalo, ya sea por una tensión de línea alta o baja, o posiblemente por un error del circuito de medición de tensión. |  |  |
| `Input Power Loss` | Pérdida de alimentación de entrada |  |  |
| `Listening` | A la escucha |  |  |
| `Locked` | Bloqueada |  |  |
| `Logged In/Connected` | Sesión iniciada/Conectado |  |  |
| `Logging In` | Iniciando sesión |  |  |
| `Logging Out Phase 1` | Cerrando sesión (fase 1) |  |  |
| `Logging Out Phase 2` | Cerrando sesión (fase 2) |  |  |
| `MAX_BOOSTORBUCK` | MAX_BOOSTORBUCK |  |  |
| `Missing` | Ausente |  |  |
| `Missing Zero Crossing` | Falta el paso por cero |  |  |
| `MS` | MS |  |  |
| `ND` | ND |  |  |
| `Not Disabled by switch - i.e. regulating` | No desactivado por el interruptor, es decir, en regulación |  |  |
| `O0` | O0 |  |  |
| `O1` | O1 |  |  |
| `OC` | OC |  |  |
| `OT` | OT |  |  |
| `Over Current Fault Count O,1...9 then 10,11, 12...` | Recuento de fallos por sobreintensidad 0,1...9 y después 10,11,12... | CHECK: the English starts the sequence with the letter 'O' ('O,1...9') where it plainly means the digit zero; the Spanish uses 0. Same normalisation the pt-PT reviewer made. |  |
| `Over Current Fault reset maximum count reached (per PRM file) must be reset manually` | Se ha alcanzado el número máximo de restablecimientos del fallo por sobreintensidad (según el archivo PRM); es necesario restablecerlo manualmente |  |  |
| `Over Temperature fault - converter is disabled until it cools` | Fallo por sobretemperatura; el convertidor queda desactivado hasta que se enfríe |  |  |
| `P+` | P+ |  |  |
| `P-` | P- |  |  |
| `PL` | PL |  |  |
| `PLL_NL` | PLL_NL |  |  |
| `PN` | PN |  |  |
| `PR` | PR |  |  |
| `Processor Reset by user command` | Procesador restablecido por un comando del usuario |  |  |
| `PWM is no longer railed, and has dropped below 95% of maximum` | El PWM ha dejado de estar saturado y ha bajado por debajo del 95% del máximo | TERM: 'railed' -&gt; «saturado». No space before the percent sign, matching normal Spanish software practice (RAE would prefer «95 %»). |  |
| `RAMP` | RAMP |  |  |
| `Ramping` | En rampa |  |  |
| `Real Time Clock time after Change` | Hora del reloj de tiempo real después del cambio |  |  |
| `Real Time Clock time before Change` | Hora del reloj de tiempo real antes del cambio |  |  |
| `Rebooting` | Reiniciando |  |  |
| `Regulating` | En regulación |  |  |
| `Regulator is ramping to the active set point` | El regulador está en rampa hacia la consigna activa | CHECK: 'ramping to' left directionless in Spanish («en rampa hacia»); the regulator can ramp up or down, so «subiendo en rampa» would be wrong half the time. |  |
| `Restoring Session` | Restaurando la sesión |  |  |
| `SCR_GATE` | SCR_GATE |  |  |
| `SD Card data logging was stopped by user command (disabled)` | El registro de datos en la tarjeta SD se ha detenido por un comando del usuario (desactivado) |  |  |
| `SE` | SE |  |  |
| `Service Lookup` | Buscando servicio |  |  |
| `TEMP` | TEMP |  |  |
| `Temp sensor open` | Sensor de temperatura en circuito abierto |  |  |
| `Temp Sensor or Fan Fault` | Fallo del sensor de temperatura o del ventilador |  |  |
| `Temp sensor shorted` | Sensor de temperatura en cortocircuito |  |  |
| `The PLL is currently not locked` | El PLL no está enganchado actualmente |  |  |
| `Transformer Saturation` | Saturación del transformador |  |  |
| `TS` | TS |  |  |
| `Unknown` | Desconocido | AGREEMENT: this single string is returned by the regulator-status, regulating-status AND SD-card-status converters in Core/Enums.cpp. Masculine is right for the first two; the SD-card row would want «Desconocida». Unresolvable without splitting the source string. |  |
| `VC` | VC |  |  |
| `Vin or Vout is out of range as defined in PRM file - fault resets automatically with a 10V asymmetrical hysteresis (check fault log Vin column to determine over or under) ` | Vin o Vout está fuera del intervalo definido en el archivo PRM; el fallo se restablece automáticamente con una histéresis asimétrica de 10 V (consultar la columna Vin del registro de fallos para determinar si es por exceso o por defecto)  | CHECK: the source's trailing space is preserved. |  |
| `VO` | VO |  |  |
| `Voltage Calibration error on boot up. After bootup, it permanently disables the regulator` | Error de calibración de tensión durante el arranque. Tras el arranque, desactiva permanentemente el regulador |  |  |
| `W1` | W1 |  |  |
| `W2` | W2 |  |  |
| `W3` | W3 |  |  |
| `W4` | W4 |  |  |
| `W5` | W5 |  |  |
| `W6` | W6 |  |  |
| `Watchdog tripped - DSPIC failure to respond` | Watchdog disparado; el DSPIC no ha respondido |  |  |
| `Watchdog tripped - Failed wellness test (Vout != Setpoint and no faults)` | Watchdog disparado; prueba de integridad fallida (Vout distinto de la consigna y sin fallos) |  |  |
| `Watchdog tripped - Main uP loop timed out OR H/W watchdog timed out` | Watchdog disparado; se ha agotado el tiempo del bucle principal del microprocesador o del watchdog de hardware |  |  |
| `Watchdog tripped - Phase Parameter file checksum mismatch` | Watchdog disparado; discrepancia en la suma de comprobación del archivo de parámetros de fase |  |  |
| `Watchdog tripped - Phase Status or data checksum mismatch  ` | Watchdog disparado; discrepancia en la suma de comprobación del estado o de los datos de fase   | CHECK: the source's two trailing spaces are preserved. |  |
| `Watchdog tripped - SPI buss to phase failure ` | Watchdog disparado; fallo del bus SPI hacia la fase  | CHECK: the English misspells 'bus' as 'buss'; the trailing space is preserved. |  |
| `ZX` | ZX |  |  |

## Transcript pane and window (18)

| Original (English) | Translation (es-ES) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| ` Send Command ` |  Enviar comando  |  |  |
| ` Send CTRL-C ` |  Enviar CTRL-C  |  |  |
| `%1:     Sent: %2` | %1:     Enviado: %2 | CHECK: the source pads 'Sent' with spaces so it lines up under 'Received'. «Recibido»/«Enviado» differ in length, so the padding no longer aligns; the reviewer may want to re-space both lines together. |  |
| `%1: %2` | %1: %2 |  |  |
| `%1: <font color="orange">WARNING: %2</font>` | %1: &lt;font color="orange"&gt;AVISO: %2&lt;/font&gt; |  |  |
| `%1: <font color="red">ERROR: %2</font>` | %1: &lt;font color="red"&gt;ERROR: %2&lt;/font&gt; |  |  |
| `%1: Received:   %2` | %1: Recibido:   %2 |  |  |
| `Clear Transcript` | Borrar la transcripción |  |  |
| `Command To Send` | Comando a enviar |  |  |
| `Copy Transcript to Clipboard` | Copiar la transcripción al portapapeles |  |  |
| `Could not open '%1' for writing, please check permissions\n%2` | No se ha podido abrir '%1' para escritura; comprobar los permisos\n%2 |  |  |
| `Could not Open File` | No se ha podido abrir el archivo |  |  |
| `Error` | Error |  |  |
| `Save Transcript` | Guardar la transcripción |  |  |
| `Save Transcript...` | Guardar la transcripción... |  |  |
| `Select All` | Seleccionar todo |  |  |
| `Text Files (*.txt);;All Files (*.*)` | Archivos de texto (*.txt);;Todos los archivos (*.*) |  |  |
| `Transcript` | Transcripción |  |  |

## UART settings dialog (16)

| Original (English) | Translation (es-ES) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `115.2k` | 115.2k |  |  |
| `230.4k` | 230.4k |  |  |
| `38.4k` | 38.4k |  |  |
| `57.6k` | 57.6k |  |  |
| `Baud Rate` | Velocidad en baudios | LENGTH: 9 -&gt; 20 characters. It labels a narrow combo box in the UART dialog and a tree column; «Baudios» alone is the fallback. |  |
| `Baud rate and Flow control must be set` | Es necesario definir la velocidad en baudios y el control de flujo |  |  |
| `Baud rate must be set` | Es necesario definir la velocidad en baudios |  |  |
| `Flow Control` | Control de flujo |  |  |
| `Flow control must be set` | Es necesario definir el control de flujo |  |  |
| `Hardware Control` | Control por hardware |  |  |
| `None` | Ninguno | AGREEMENT: masculine, agreeing with «control (de flujo)», the field this combo box fills. |  |
| `Setup UARTs` | Configurar las UART |  |  |
| `Software Control` | Control por software |  |  |
| `TextLabel` | TextLabel |  |  |
| `UART 1 settings can not be modified` | La configuración de la UART 1 no se puede modificar |  |  |
| `WARNING: DO NOT CHANGE if UART2 is used with an Ethernet adapter.` | AVISO: NO MODIFICAR si la UART2 se utiliza con un adaptador Ethernet. |  |  |

## User guide windows (7)

| Original (English) | Translation (es-ES) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `Advanced User Guide` | Guía del usuario (avanzado) |  |  |
| `Basic User Guide` | Guía del usuario (básico) |  |  |
| `Bluetooth Pairing` | Emparejamiento Bluetooth |  |  |
| `Bluetooth Pairing (Windows 11)` | Emparejamiento Bluetooth (Windows 11) |  |  |
| `Close` | Cerrar |  |  |
| `Fit to window` | Ajustar a la ventana |  |  |
| `The guide could not be loaded: %1` | No se ha podido cargar la guía: %1 |  |  |

## Voltage calibration dialog (10)

| Original (English) | Translation (es-ES) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| ` Volts` |  voltios |  |  |
| `A Voltage Difference of '%1' is invalid, range is -9.9V to +9.9V` | Una diferencia de tensión de '%1' no es válida; el intervalo es de -9,9 V a +9,9 V | CHECK: decimal points changed to commas and a space inserted before the unit symbol, as Spanish requires. |  |
| `Can not calibrate voltage` | No se puede calibrar la tensión |  |  |
| `Externally Measured Output Voltage:` | Tensión de salida medida externamente: |  |  |
| `Regulator Target %1 Output Voltage:` | Tensión de salida objetivo %1 del regulador: | AGREEMENT: %1 is the setpoint number (1 or 2), so the surrounding words stay invariable. Confirm it is never filled with a word. |  |
| `Regulator Target Output Voltage:` | Tensión de salida objetivo del regulador: |  |  |
| `Voltage Calibration` | Calibración de tensión |  |  |
| `Voltage Calibration:` | Calibración de tensión: |  |  |
| `Voltage Difference is too High` | La diferencia de tensión es demasiado alta |  |  |
| `Volts` | Voltios |  |  |
