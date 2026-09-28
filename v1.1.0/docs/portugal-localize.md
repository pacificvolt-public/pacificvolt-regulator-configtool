# ConfigTool - European Portuguese (pt-PT) translation review

The complete translation, grouped by where the text appears in the tool. Edit the
**Translation** column directly, or put a replacement in **Your correction**, and
hand the file back. For anything with markup or long text, the spreadsheet next to
this file is easier to work in.

- Strings translated: **876** - the whole of the live user interface
- Strings still untranslated: **0**
- Rows carrying a question from me: **71**
- Generated from `translations/ConfigTool_pt_PT.ts`

This is a machine first pass awaiting a native European Portuguese speaker. It is deliberately pt-PT and not Brazilian: *ficheiro* not *arquivo*, *palavra-passe* not *senha*, *transferir* not *baixar*, *ligacao* not *conexao*, *porta serie* not *porta serial*, *sobreintensidade* not *sobrecorrente*.

Some strings are translated to themselves on purpose. Firmware fault codes (`CB`,
`OT`, `W1`, `P+`, `RAMP`...), baud rate values and Qt Designer object names
(`toolBar`, `MainWindow`) are identifiers rather than prose - translating them
would break the match against what the regulator actually sends.

A few strings carry HTML. Those rows show both columns as code, so the tags are
visible rather than rendered - they are part of the string and must survive
translation unchanged. `\n` marks a real line break, the same convention the
.tsv uses.

## About and licence dialogs (9)

| Original (English) | Translation (pt-PT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `&3rd Party Licenses` | &amp;Licenças de terceiros |  |  |
| `&About Qt` | Acerca do &amp;Qt |  |  |
| `<h3>%1 - 3rd Party Licenses</h3>` | `<h3>%1 - Licenças de terceiros</h3>` |  |  |
| `<h3>About %1</h3><p>%1</p><p>Version: %2</p><p>Build Date: %3</p><p>%4</p>` | `<h3>Acerca de %1</h3><p>%1</p><p>Versão: %2</p><p>Data de compilação: %3</p><p>%4</p>` |  |  |
| `<p>%1 uses multiple 3rd Party software mostly covered under the Qt distribution</p><p>However the following license(s) are not part of Qt.</p><hr style="width:50%;text-align:left;margin-left:0"><table border="1"><tr><th>Company</th><th>Product</th><th>License</th><th>Source Location</th><th>Patches</th></tr>` | `<p>O %1 utiliza vário software de terceiros, na sua maioria abrangido pela distribuição Qt</p><p>No entanto, as licenças seguintes não fazem parte do Qt.</p><hr style="width:50%;text-align:left;margin-left:0"><table border="1"><tr><th>Empresa</th><th>Produto</th><th>Licença</th><th>Localização da fonte</th><th>Correções</th></tr>` |  |  |
| `<p>Is a tool to help configure %1's Voltage Regulators.</p><p>For more information, please visit <a href="%2">%3</a>.</p><p>For the default Advanced and Admin passwords, contact <a href="mailto:%4">%4</a>.</p><hr style="width:50%;text-align:left;margin-left:0"><p>%5</p>` | `<p>É uma ferramenta para ajudar a configurar os reguladores de tensão da %1.</p><p>Para mais informações, visite <a href="%2">%3</a>.</p><p>Para as palavras-passe predefinidas de Avançado e Administrador, contacte <a href="mailto:%4">%4</a>.</p><hr style="width:50%;text-align:left;margin-left:0"><p>%5</p>` |  |  |
| `3rd Party Licenses` | Licenças de terceiros |  |  |
| `About %1` | Acerca de %1 |  |  |
| `This tool supports the following LVR firmware versions:<br>LVR30 %1, LVR50 %2` | `Esta ferramenta suporta as seguintes versões de firmware LVR:<br>LVR30 %1, LVR50 %2` |  |  |

## Bluetooth - Available Regulators and pairing (48)

| Original (English) | Translation (pt-PT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `%1 configured connection(s)` | %1 ligação(ões) configurada(s) |  |  |
| `An error has occurred in the bluetooth system` | Ocorreu um erro no sistema Bluetooth |  |  |
| `An unknown error has occurred.` | Ocorreu um erro desconhecido. |  |  |
| `Authorize Regulator` | Autorizar regulador |  |  |
| `Available Regulators` | Reguladores disponíveis |  |  |
| `Connecting to regulator '%1' timed out. Check your connection - the regulator may be out of range or turned off.` | A ligação ao regulador '%1' excedeu o tempo limite. Verifique a ligação - o regulador pode estar fora de alcance ou desligado. |  |  |
| `Could not find a bluetooth adapter. ` | Não foi possível encontrar um adaptador Bluetooth.  |  |  |
| `currently connected` | atualmente ligado |  |  |
| `Device discovery is not possible or implemented on the current platform.` | A deteção de dispositivos não é possível nem está implementada nesta plataforma. |  |  |
| `Device Name` | Nome do dispositivo |  |  |
| `Does the following PIN match the one shown on the device you are pairing?: %1` | O PIN seguinte corresponde ao mostrado no dispositivo que está a emparelhar?: %1 |  |  |
| `Enter a PIN to pair with:` | Introduza um PIN para emparelhar: |  |  |
| `Error in Bluetooth connection` | Erro na ligação Bluetooth |  |  |
| `Error in pairing` | Erro no emparelhamento |  |  |
| `Finished` | Concluído |  |  |
| `Limit the list to shipped regulators, which are all named "PV...". Uncheck to also show bench and test units, which often are not. Non-regulators are never listed either way.` | Limita a lista aos reguladores expedidos, cujo nome começa sempre por "PV...". Desmarque para mostrar também unidades de bancada e de ensaio, que muitas vezes não seguem essa regra. Os equipamentos que não são reguladores nunca são listados. | LENGTH: a long tooltip that grows in Portuguese. Worth hovering it once to confirm it wraps rather than running off screen. |  |
| `Missing permissions` | Permissões em falta |  |  |
| `No Bluetooth Adapter Found` | Nenhum adaptador Bluetooth encontrado |  |  |
| `One of the requested discovery methods is not supported by the current platform.` | Um dos métodos de deteção pedidos não é suportado por esta plataforma. |  |  |
| `Pair Device` | Emparelhar dispositivo |  |  |
| `Pair Device?` | Emparelhar dispositivo? |  |  |
| `Pair Regulator` | Emparelhar regulador | "Emparelhar"/"Desemparelhar" for pair/unpair - the terms Windows itself uses in pt-PT, so they should be familiar. |  |
| `paired` | emparelhado |  |  |
| `Paired?` | Emparelhado? |  |  |
| `Permissions are needed to use Bluetooth. Please grant the permissions to this application in the system settings.` | São necessárias permissões para utilizar o Bluetooth. Conceda as permissões a esta aplicação nas definições do sistema. |  |  |
| `Please enter this PIN on the device you are pairing with: %1` | Introduza este PIN no dispositivo com que está a emparelhar: %1 |  |  |
| `PV Filter` | Filtro PV |  |  |
| `Re-Scan` | Procurar novamente |  |  |
| `Remove %1 regulator(s)?` | Remover %1 regulador(es)? |  |  |
| `Remove Regulators` | Remover reguladores |  |  |
| `Remove the selected regulators from the list, delete their connections, and unpair them` | Remove os reguladores selecionados da lista, elimina as respetivas ligações e desemparelha-os |  |  |
| `Scanning for devices not previously paired.` | A procurar dispositivos ainda não emparelhados. |  |  |
| `Scanning for previously connected devices and devices not previously paired.` | A procurar dispositivos anteriormente ligados e dispositivos ainda não emparelhados. |  |  |
| `Scanning for previously connected devices.` | A procurar dispositivos anteriormente ligados. |  |  |
| `Scanning...` | A procurar... |  |  |
| `Select Regulator` | Selecionar regulador |  |  |
| `Select the Regulator to connect to.` | Selecione o regulador ao qual se pretende ligar. |  |  |
| `Service` | Serviço |  |  |
| `Stop Scanning` | Parar a procura |  |  |
| `The Bluetooth adaptor is powered off, power it on before doing discovery.` | O adaptador Bluetooth está desligado; ligue-o antes de procurar dispositivos. |  |  |
| `The following error occurred connecting to regulator '%1': %2. Check your connection - the regulator may be out of range or turned off.` | Ocorreu o seguinte erro ao ligar ao regulador '%1': %2. Verifique a ligação - o regulador pode estar fora de alcance ou desligado. |  |  |
| `The location service is turned off.Usage of Bluetooth APIs is not possible when location service is turned off.` | O serviço de localização está desligado. Não é possível utilizar as APIs Bluetooth com o serviço de localização desligado. | NOTE: the English source is missing a space after the first full stop. The Portuguese adds one. |  |
| `The operating system requests permissions which were not granted by the user.` | O sistema operativo pede permissões que não foram concedidas pelo utilizador. |  |  |
| `The passed local adapter address does not match the physical adapter address of any local Bluetooth device.` | O endereço de adaptador local indicado não corresponde ao endereço físico de nenhum dispositivo Bluetooth local. |  |  |
| `This deletes their configured connections, removes them from the Available Regulators list, and unpairs them from this computer. Any open connections will be closed. This cannot be undone.` | Isto elimina as respetivas ligações configuradas, remove-os da lista Reguladores disponíveis e desemparelha-os deste computador. As ligações abertas serão fechadas. Esta ação não pode ser anulada. | Destructive-action warning, so the wording matters more than most. Worth reading carefully. |  |
| `Unknown Error.` | Erro desconhecido. |  |  |
| `Unpair Regulator` | Desemparelhar regulador |  |  |
| `Writing or reading from the device resulted in an error.` | A escrita ou leitura no dispositivo originou um erro. |  |  |

## Clock and time zone dialogs (13)

| Original (English) | Translation (pt-PT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `...` | ... |  |  |
| `...` | ... |  |  |
| `Current Time` | Hora atual |  |  |
| `Custom Selected Time Zone` | Fuso horário personalizado |  |  |
| `Custom Time` | Hora personalizada |  |  |
| `Local Computer's Time Zone` | Fuso horário do computador local |  |  |
| `Regulator's System Clock:` | Relógio do sistema do regulador: |  |  |
| `Regulator:` | Regulador: |  |  |
| `Select Time Zone` | Selecionar o fuso horário |  |  |
| `Select Time Zone` | Selecionar o fuso horário |  |  |
| `Set Regulator System Clock` | Acertar o relógio do sistema do regulador |  |  |
| `Sync` | Sincronizar |  |  |
| `UTC` | UTC |  |  |

## Command names - transcript and queue status (65)

| Original (English) | Translation (pt-PT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `    Command #: %1` |     Comando n.º: %1 |  |  |
| `%1.` | %1. |  |  |
| `(Re)-initialize Control Board` | (Re)inicializar a placa de controlo |  |  |
| `, re-running command.` | , a executar novamente o comando. |  |  |
| `. Removing from Queue.` | . A remover da fila. |  |  |
| `Checking for Support of '%1'` | A verificar o suporte de '%1' |  |  |
| `Clear Queue` | Limpar a fila |  |  |
| `cmd not supported` | comando não suportado |  |  |
| `Command '%1' failed. Please disconnect and try again.  Consider rebooting the Regulator.` | O comando '%1' falhou. Desligue-se e tente novamente. Considere reiniciar o regulador. |  |  |
| `Command '%1' failed. Removing from Queue.` | O comando '%1' falhou. A remover da fila. |  |  |
| `Command '%1' is not supported` | O comando '%1' não é suportado |  |  |
| `Command '%2' timed out%1` | O comando '%2' excedeu o tempo limite%1 |  |  |
| `Could not process results of command '%1'` | Não foi possível processar os resultados do comando '%1' |  |  |
| `Custom Command` | Comando personalizado |  |  |
| `Disable SDCard` | Desativar cartão SD |  |  |
| `Download File` | Transferir ficheiro | "Transferir" used for download throughout, which is the pt-PT convention. Brazilian text would use "baixar". |  |
| `Enable Or Disable All Phases if there is a Failure in any Phase` | Ativar ou desativar todas as fases em caso de falha em qualquer fase |  |  |
| `Enable Or Disable Regulator` | Ativar ou desativar o regulador |  |  |
| `Enable SDCard` | Ativar cartão SD |  |  |
| `Finished downloading data for command '%1'` | Transferência dos dados do comando '%1' concluída |  |  |
| `Finished getting system info` | Obtenção da informação do sistema concluída |  |  |
| `Finished Getting System Info` | Obtenção da informação do sistema concluída |  |  |
| `Format SDCard` | Formatar cartão SD |  |  |
| `Get Default Parameter File` | Obter ficheiro de parâmetros predefinido |  |  |
| `Get EEPROM Contents` | Obter o conteúdo da EEPROM |  |  |
| `Get File Sizes` | Obter tamanhos dos ficheiros |  |  |
| `Get Parameter File` | Obter ficheiro de parâmetros |  |  |
| `Get Phase Firmware` | Obter firmware de fase |  |  |
| `Get Regulator Clock` | Obter relógio do regulador |  |  |
| `Get Serial Num` | Obter número de série |  |  |
| `Get Status` | Obter estado |  |  |
| `Get System Firmware` | Obter firmware do sistema |  |  |
| `Get System Firmware Date` | Obter data do firmware do sistema |  |  |
| `Get System Gain` | Obter o ganho do sistema |  |  |
| `Get UART Settings` | Obter definições UART |  |  |
| `Get UART Settings via RB` | Obter definições UART através de RB |  |  |
| `Get UART Settings via RBAUD` | Obter definições UART através de RBAUD |  |  |
| `Get Voltage Calibration` | Obter calibração de tensão |  |  |
| `Reboot Regulator` | Reiniciar o regulador |  |  |
| `Regulator could not handle command '%1'` | O regulador não conseguiu processar o comando '%1' |  |  |
| `Reset Over Current Fault Lockout` | Repor o bloqueio por avaria de sobreintensidade |  |  |
| `Reset Regulator to Default Parameters` | Repor os parâmetros predefinidos do regulador |  |  |
| `Restore Modem Power` | Restaurar a alimentação do modem |  |  |
| `Send Ctrl-C` | Enviar Ctrl-C |  |  |
| `Send Login` | Enviar início de sessão |  |  |
| `Send Logoff` | Enviar fim de sessão |  |  |
| `Send Password` | Enviar palavra-passe | "Palavra-passe" used throughout for password, which is pt-PT. Brazilian would be "senha". |  |
| `Set Param File` | Definir o ficheiro de parâmetros |  |  |
| `Set PIR Amperage` | Definir a corrente PIR |  |  |
| `Set PIR Delta Voltage` | Definir a variação de tensão PIR |  |  |
| `Set PIR Null Voltage` | Definir a tensão nula PIR |  |  |
| `Set PIR Time Constant` | Definir a constante de tempo PIR |  |  |
| `Set Regulator Clock` | Acertar o relógio do regulador |  |  |
| `Set Regulator Password` | Definir a palavra-passe do regulador |  |  |
| `Set Serial Number` | Definir o número de série | Dialog title in sentence case, following pt-PT convention rather than mirroring English Title Case. |  |
| `Set System Gain` | Definir o ganho do sistema |  |  |
| `Set Target Selection` | Definir a seleção de alvo |  |  |
| `Set Target Voltage` | Definir a tensão alvo |  |  |
| `Set UART 1 Baud Rate` | Definir a velocidade da UART 1 |  |  |
| `Set UART 1 FlowControl` | Definir o controlo de fluxo da UART 1 |  |  |
| `Set UART 2 Baud Rate` | Definir a velocidade da UART 2 |  |  |
| `Set UART 2 FlowControl` | Definir o controlo de fluxo da UART 2 |  |  |
| `Set Voltage Calibration` | Definir a calibração de tensão |  |  |
| `Size of Command Queue: %1` | Dimensão da fila de comandos: %1 |  |  |
| `Turn off Modem Power` | Desligar a alimentação do modem |  |  |

## Connected regulator window - menus, dialogs and messages (149)

| Original (English) | Translation (pt-PT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `    Comm Port: %1` |     Porta de comunicação: %1 |  |  |
| `    IP Address: %1\n    Domain Name: %2\n    Port: %3` |     Endereço IP: %1\n    Nome de domínio: %2\n    Porta: %3 | Multi-line block with deliberate leading indentation, preserved so the fields still line up. |  |
| ` - Regulator: %1` |  - Regulador: %1 |  |  |
| ` - Transcript` |  - Transcrição |  |  |
| ` Reset Over Current Fault Lockout` |  Repor o bloqueio por avaria de sobreintensidade |  |  |
| `%1` | %1 |  |  |
| `&Disconnect` | &amp;Desligar | Mnemonic D kept - "Desligar" also starts with D. Convenient coincidence rather than design. |  |
| `&Regulator` | &amp;Regulador | Mnemonic R kept, since "Regulador" also starts with R. No collision in the connected window menu bar. |  |
| `&Settings` | &amp;Definições | Mnemonic D on "Definicoes". Distinct from the other menu bar entries. |  |
| `<br/>Would you like to reconnect?` | `<br/>Pretende voltar a ligar-se?` |  |  |
| `'%1' is a name Windows reserves and cannot be used in a file name.` | '%1' é um nome reservado pelo Windows e não pode ser utilizado num nome de ficheiro. |  |  |
| `(Re-)Initialize Regulator Control Board` | (Re)inicializar a placa de controlo do regulador |  |  |
| `(Re-)initialize the Control Board...` | (Re)inicializar a placa de controlo... |  |  |
| `(Re-)initialize the control board...` | (Re)inicializar a placa de controlo... |  |  |
| `1=Fast` | 1=Rápido |  |  |
| `A timeout error occurred` | Ocorreu um erro de tempo limite |  |  |
| `About...` | Acerca de... |  |  |
| `Administration Mode` | Modo de administração |  |  |
| `Administration Mode` | Modo de administração |  |  |
| `Advanced Mode` | Modo avançado |  |  |
| `All Phases Disabled on Failure in Any Phase?` | Desativar todas as fases em caso de falha em qualquer fase? |  |  |
| `An error occurred while attempting to open an already opened device by another process or a user not having enough permission and credentials to open.` | Ocorreu um erro ao tentar abrir um dispositivo já aberto por outro processo, ou por um utilizador sem permissões e credenciais suficientes. |  |  |
| `An error occurred while attempting to open an already opened device in this object.` | Ocorreu um erro ao tentar abrir um dispositivo já aberto neste objeto. |  |  |
| `An error occurred while attempting to open an non-existing device.` | Ocorreu um erro ao tentar abrir um dispositivo inexistente. |  |  |
| `An I/O error occurred when a resource becomes unavailable, e.g. when the device is unexpectedly removed from the system.` | Ocorreu um erro de E/S por indisponibilidade de um recurso, por exemplo quando o dispositivo é removido inesperadamente do sistema. |  |  |
| `An I/O error occurred while reading the data.` | Ocorreu um erro de E/S ao ler os dados. |  |  |
| `An I/O error occurred while writing the data.` | Ocorreu um erro de E/S ao escrever os dados. |  |  |
| `An unidentified error occurred.` | Ocorreu um erro não identificado. |  |  |
| `Are you sure you wish to continue?` | Tem a certeza de que pretende continuar? |  |  |
| `Automatically Refresh Status?` | Atualizar o estado automaticamente? |  |  |
| `Available` | Disponível |  |  |
| `Available` | Disponível |  |  |
| `Available` | Disponível |  |  |
| `Bluetooth` | Bluetooth |  |  |
| `Bluetooth Regulator Unauthorized` | Regulador Bluetooth não autorizado |  |  |
| `Bluetooth Regulator Unpaired` | Regulador Bluetooth não emparelhado |  |  |
| `Can not set UART settings while connected via Ethernet` | Não é possível definir as definições UART enquanto estiver ligado por Ethernet |  |  |
| `Change Time Zone...` | Alterar o fuso horário... |  |  |
| `Clear Command Queue` | Limpar a fila de comandos |  |  |
| `Clear Transcript` | Limpar a transcrição |  |  |
| `Close Connection?` | Fechar a ligação? |  |  |
| `COM Port` | Porta COM |  |  |
| `Comm Port not Found` | Porta de comunicação não encontrada |  |  |
| `Command Queue Status` | Estado da fila de comandos |  |  |
| `Connect` | Ligar |  |  |
| `Connection '%1' was lost or disconnected.` | A ligação '%1' foi perdida ou terminada. |  |  |
| `Continue` | Continuar |  |  |
| `Continue` | Continuar |  |  |
| `Copy Transcript to Clipboard` | Copiar a transcrição para a área de transferência |  |  |
| `Debug` | Depuração |  |  |
| `Debug Logging...` | Registo de depuração... |  |  |
| `Delete Data Logs...` | Eliminar os registos de dados... |  |  |
| `Delete Fault Log...` | Eliminar o registo de avarias... |  |  |
| `Disable Advanced Mode` | Desativar o modo avançado |  |  |
| `Disable Regulator` | Desativar o regulador |  |  |
| `Disable SD Card` | Desativar o cartão SD |  |  |
| `Download from SD Card` | Transferir do cartão SD |  |  |
| `Download from SD Card...` | Transferir do cartão SD... |  |  |
| `Enable Advanced Mode` | Ativar o modo avançado |  |  |
| `Enable Regulator` | Ativar o regulador |  |  |
| `Enable SD Card` | Ativar o cartão SD |  |  |
| `Enter New Regulator Password` | Introduza a nova palavra-passe do regulador |  |  |
| `Enter Regulator Password` | Introduza a palavra-passe do regulador |  |  |
| `Enter System Gain` | Introduza o ganho do sistema |  |  |
| `Error` | Erro |  |  |
| `Error Communicating with Regulator` | Erro de comunicação com o regulador |  |  |
| `ERROR: %1` | ERRO: %1 |  |  |
| `Fast Rate Data` | Dados de taxa rápida |  |  |
| `Format SD Card...` | Formatar o cartão SD... |  |  |
| `Formatting erases the SD card and cannot be undone.` | A formatação apaga o cartão SD e não pode ser anulada. |  |  |
| `Help` | Ajuda |  |  |
| `Host '%1' was not found. Please check the host name and port settings.` | O anfitrião '%1' não foi encontrado. Verifique o nome do anfitrião e as definições de porta. |  |  |
| `Initialize System Information on Login?` | Inicializar a informação do sistema ao iniciar sessão? |  |  |
| `Medium Rate Data` | Dados de taxa média |  |  |
| `Name cannot be used` | O nome não pode ser utilizado |  |  |
| `Name for this regulator:\n\nThis name is stored by the Config Tool only. It is not written to the\nregulator and is not read back from it, and it is lost if the regulator\nis removed from the saved list.\n\nIt is used in the names of the files downloaded from this regulator, so\nit cannot contain characters that a file name cannot hold.` | Nome para este regulador:\n\nEste nome é guardado apenas pelo Config Tool. Não é escrito no\nregulador nem é lido a partir dele, e é perdido se o regulador\nfor removido da lista guardada.\n\nÉ utilizado nos nomes dos ficheiros transferidos deste regulador, pelo\nque não pode conter caracteres que um nome de ficheiro não permite. |  |  |
| `Network not Reachable` | Rede inacessível |  |  |
| `No SD File Data` | Sem dados de ficheiros do cartão SD |  |  |
| `No SD file data available. Click on the green System Info arrows.` | Não há dados de ficheiros do cartão SD. Clique nas setas verdes de informação do sistema. |  |  |
| `Parameter File...` | Ficheiro de parâmetros... |  |  |
| `Password Required` | Palavra-passe necessária |  |  |
| `Power cycle external modem at J2-2` | Reiniciar a alimentação do modem externo em J2-2 |  |  |
| `Power Interactive Regulation Settings...` | Definições da regulação interativa de potência... |  |  |
| `Quit` | Sair |  |  |
| `Quit` | Sair |  |  |
| `Reboot Regulator` | Reiniciar o regulador |  |  |
| `Reboot Regulator...` | Reiniciar o regulador... |  |  |
| `Reconnect` | Voltar a ligar |  |  |
| `Refresh` | Atualizar |  |  |
| `Refresh All` | Atualizar tudo |  |  |
| `Refresh Gain Values` | Atualizar os valores de ganho |  |  |
| `Refresh Parameter File` | Atualizar o ficheiro de parâmetros |  |  |
| `Refresh Regulator Clock` | Atualizar o relógio do regulador |  |  |
| `Refresh Regulator Information` | Atualizar a informação do regulador |  |  |
| `Refresh SD Card Information` | Atualizar a informação do cartão SD |  |  |
| `Refresh UART Settings` | Atualizar as definições UART |  |  |
| `Refresh Voltage and Fault Status` | Atualizar o estado de tensão e avarias |  |  |
| `Refresh Voltage Calibration Info` | Atualizar a informação de calibração de tensão |  |  |
| `Regulator` | Regulador |  |  |
| `Regulator &Settings` | &amp;Definições do regulador |  |  |
| `Regulator '%1' - %2` | Regulador '%1' - %2 |  |  |
| `Regulator has logged off due to no command activity. Please reconnect and activate auto refresh.` | O regulador terminou a sessão por falta de atividade de comandos. Volte a ligar-se e ative a atualização automática. | Wording supplied by you in English. The Portuguese follows it closely - check it carries the same instruction to reconnect AND turn auto refresh on. |  |
| `Regulator Logged Off` | Sessão terminada no regulador |  |  |
| `Regulator:` | Regulador: |  |  |
| `Remote` | Remoto |  |  |
| `Reset Over Current Fault Lockout` | Repor o bloqueio por avaria de sobreintensidade |  |  |
| `Reset Regulator to Default Parameters` | Repor os parâmetros predefinidos do regulador |  |  |
| `Reset Regulator to Default Parameters...` | Repor os parâmetros predefinidos do regulador... |  |  |
| `Save Transcript...` | Guardar a transcrição... |  |  |
| `SD Card` | Cartão SD |  |  |
| `SD Card File Sizes` | Tamanhos dos ficheiros do cartão SD |  |  |
| `SD Card Has Error` | O cartão SD tem um erro |  |  |
| `SD Card is Disabled` | O cartão SD está desativado |  |  |
| `Session Timing Out` | A sessão está a expirar |  |  |
| `Set Regulator Name` | Definir o nome do regulador |  |  |
| `Set Regulator Name...` | Definir o nome do regulador... |  |  |
| `Set Regulator's Password...` | Definir a palavra-passe do regulador... |  |  |
| `Set Serial Number...` | Definir o número de série... |  |  |
| `Set System Clock...` | Acertar o relógio do sistema... |  |  |
| `Set System Gain...` | Definir o ganho do sistema... |  |  |
| `Slow Rate Data` | Dados de taxa lenta |  |  |
| `Slow=9` | Lento=9 |  |  |
| `System Gain:` | Ganho do sistema: |  |  |
| `System not initialized` | Sistema não inicializado |  |  |
| `The connection was refused by the regulator '%1'. Make sure the regulator is running and confirm the host name and port settings.` | A ligação foi recusada pelo regulador '%1'. Certifique-se de que o regulador está em funcionamento e confirme o nome do anfitrião e as definições de porta. |  |  |
| `The following error occurred connecting to regulator '%1': %2.` | Ocorreu o seguinte erro ao ligar ao regulador '%1': %2. |  |  |
| `The name cannot be empty.` | O nome não pode estar vazio. |  |  |
| `The name cannot contain %1, because it is used in the names of the files downloaded from this regulator.` | O nome não pode conter %1, porque é utilizado nos nomes dos ficheiros transferidos deste regulador. |  |  |
| `The name cannot contain control characters, because it is used in the names of the files downloaded from this regulator.` | O nome não pode conter caracteres de controlo, porque é utilizado nos nomes dos ficheiros transferidos deste regulador. |  |  |
| `The name cannot end with a '.'` | O nome não pode terminar com '.' |  |  |
| `The requested device operation is not supported or prohibited by the running operating system.` | A operação pedida no dispositivo não é suportada ou é proibida pelo sistema operativo em execução. |  |  |
| `This error occurs when an operation is executed that can only be successfully performed if the device is open.` | Este erro ocorre quando é executada uma operação que só pode ser concluída com o dispositivo aberto. |  |  |
| `This session has been idle and is about to time out.\n\nThe regulator will be disconnected in %1 seconds unless you continue.` | Esta sessão esteve inativa e está prestes a expirar.\n\nO regulador será desligado dentro de %1 segundos, a não ser que continue. | Multi-line string. The blank line between the two sentences is preserved. |  |
| `Time Stamp Transcript?` | Marcar a transcrição com a hora? |  |  |
| `toolBar` | toolBar | Qt Designer object name that leaks into the translation file. Left as-is deliberately; translating it would have no effect and could confuse. |  |
| `Transcript` | Transcrição |  |  |
| `UART Settings...` | Definições UART... |  |  |
| `USB` | USB |  |  |
| `View` | Ver |  |  |
| `View EEPROM Contents...` | Ver o conteúdo da EEPROM... |  |  |
| `View Regulator Information?` | Ver a informação do regulador? |  |  |
| `View Regulator Status?` | Ver o estado do regulador? |  |  |
| `View Transcript in Separate Window?` | Ver a transcrição numa janela separada? |  |  |
| `View Transcript?` | Ver a transcrição? |  |  |
| `Voltage Calibration Settings...` | Definições de calibração de tensão... |  |  |
| `Voltage Controller Settings...` | Definições do controlador de tensão... |  |  |
| `WARNING: %1` | AVISO: %1 |  |  |
| `Would you like to disconnect from '%1'` | Pretende desligar-se de '%1' |  |  |
| `Would you like to revert to Basic Mode?` | Pretende voltar ao modo básico? |  |  |

## Connected window - status bar (10)

| Original (English) | Translation (pt-PT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `Auto Refresh` | Atualização automática |  |  |
| `Auto Refresh` | Atualização automática |  |  |
| `Connection` | Ligação |  |  |
| `Connection` | Ligação |  |  |
| `Faults` | Avarias |  |  |
| `Faults` | Avarias |  |  |
| `Regulating` | Em regulação | Appears in three separate places and is translated identically in all three. Intentional, and worth keeping in step. |  |
| `Regulating` | Em regulação | Appears in three separate places and is translated identically in all three. Intentional, and worth keeping in step. |  |
| `Regulator` | Regulador |  |  |
| `Regulator` | Regulador |  |  |

## Connection editor dialog (22)

| Original (English) | Translation (pt-PT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `...` | ... |  |  |
| `000.000.000.000;_` | 000.000.000.000;_ |  |  |
| `A Bluetooth Device must be selected.` | É necessário selecionar um dispositivo Bluetooth. |  |  |
| `Comm Port must be set.` | É necessário indicar a porta de comunicação. |  |  |
| `Comm Port:` | Porta de comunicação: |  |  |
| `Direct Bluetooth Connection` | Ligação Bluetooth direta |  |  |
| `Edit/Create Regulator Connection` | Editar/criar ligação ao regulador |  |  |
| `Host Name` | Nome do anfitrião |  |  |
| `Host Name:` | Nome do anfitrião: |  |  |
| `Invalid IP Address: %1` | Endereço IP inválido: %1 |  |  |
| `Invalid Port: %1` | Porta inválida: %1 |  |  |
| `IP Address` | Endereço IP |  |  |
| `IP Address or Hostname must be set.` | É necessário indicar o endereço IP ou o nome do anfitrião. |  |  |
| `IP Address:` | Endereço IP: |  |  |
| `Is USB/RS-232 Serial Port (Not Bluetoooth)?` | É uma porta série USB/RS-232 (não Bluetooth)? | NOTE: "Bluetoooth" is misspelled in the English source. The Portuguese spells it correctly. Worth fixing the original so the two match. |  |
| `Please select a local or remote connection` | Selecione uma ligação local ou remota |  |  |
| `Port:` | Porta: |  |  |
| `Regulator name must be set.` | É necessário indicar o nome do regulador. |  |  |
| `Regulator Name:` | Nome do regulador: |  |  |
| `Selected Device:` | Dispositivo selecionado: |  |  |
| `Serial Port Connection` | Ligação por porta série |  |  |
| `TCP/IP Connection:` | Ligação TCP/IP: |  |  |

## Connection status and errors (19)

| Original (English) | Translation (pt-PT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `%1 commands in a row went unanswered` | %1 comandos consecutivos ficaram sem resposta |  |  |
| `115.2k` | 115.2k |  |  |
| `230.4k` | 230.4k |  |  |
| `38.4k` | 38.4k |  |  |
| `57.6k` | 57.6k | Baud rate value, left unchanged. Note the decimal point is correct here even though Portuguese uses a comma, because it is a protocol value rather than a number for reading. |  |
| `Cannot log back in to the regulator. Status polling has stopped - please disconnect and reconnect.` | Não foi possível voltar a iniciar sessão no regulador. A consulta do estado foi interrompida - desligue-se e volte a ligar-se. |  |  |
| `Cannot make sense of the regulator's replies. Status polling has stopped - please disconnect and reconnect.` | Não é possível interpretar as respostas do regulador. A consulta do estado foi interrompida - desligue-se e volte a ligar-se. |  |  |
| `Hardware Flow Control` | Controlo de fluxo por hardware |  |  |
| `No Flow Control` | Sem controlo de fluxo |  |  |
| `nothing has come back for %1 seconds` | não há resposta há %1 segundos |  |  |
| `Paired` | Emparelhado |  |  |
| `Paired with Authorization` | Emparelhado com autorização |  |  |
| `Serial Port` | Porta série | Uses "Porta serie", the pt-PT form, rather than the Brazilian "porta serial". |  |
| `Software Flow Control` | Controlo de fluxo por software |  |  |
| `The connection to regulator '%1' has been lost - %2. Check the link and reconnect. If the regulator is still holding the previous session, reconnecting can take a few minutes.` | A ligação ao regulador '%1' foi perdida - %2. Verifique a ligação e volte a ligar-se. Se o regulador ainda mantiver a sessão anterior, voltar a ligar-se pode levar alguns minutos. |  |  |
| `the login was not answered` | o início de sessão não obteve resposta |  |  |
| `The regulator has stopped responding - %1 commands in a row went unanswered.` | O regulador deixou de responder - %1 comandos consecutivos ficaram sem resposta. |  |  |
| `The regulator is responding again.` | O regulador voltou a responder. |  |  |
| `Unpaired` | Não emparelhado |  |  |

## Debug logging dialog (13)

| Original (English) | Translation (pt-PT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `<Filter>` | &lt;Filtro&gt; |  |  |
| `...` | ... |  |  |
| `Append to Log File?` | Acrescentar ao ficheiro de registo? |  |  |
| `Check All` | Selecionar tudo |  |  |
| `Log File` | Ficheiro de registo |  |  |
| `Log File:` | Ficheiro de registo: |  |  |
| `Log Files (*.log);;All Files (*.*)` | Ficheiros de registo (*.log);;Todos os ficheiros (*.*) |  |  |
| `Logging Categories:` | Categorias de registo: |  |  |
| `Logging Category` | Categoria de registo |  |  |
| `Select Logging Categories` | Selecionar as categorias de registo |  |  |
| `Show Qt Categories?` | Mostrar as categorias Qt? |  |  |
| `Uncheck All` | Desmarcar tudo |  |  |
| `Uncheck All Debug` | Desmarcar toda a depuração |  |  |

## EEPROM contents viewer (9)

| Original (English) | Translation (pt-PT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `<ADDRESS>` | &lt;ENDEREÇO&gt; |  |  |
| `<VALUE>` | &lt;VALOR&gt; |  |  |
| `0x00 0 ` | 0x00 0  |  |  |
| `0x00000000 ` | 0x00000000  |  |  |
| `Address:` | Endereço: |  |  |
| `EEPROM Contents` | Conteúdo da EEPROM |  |  |
| `EEPROM Contents:` | Conteúdo da EEPROM: |  |  |
| `EEPROM Contents: Loading...` | Conteúdo da EEPROM: a carregar... |  |  |
| `Value:` | Valor: |  |  |

## File download progress (20)

| Original (English) | Translation (pt-PT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `%1 of %2%3 (%4%)` | %1 de %2%3 (%4%) |  |  |
| `%1%2` | %1%2 |  |  |
| `%1h %2m` | %1 h %2 m |  |  |
| `%1m %2s` | %1 m %2 s |  |  |
| `%1s` | %1 s | Rendered "%1 s" with a space before the unit, per SI convention, where the English has none. Confirm that is wanted rather than matching the English exactly. |  |
| `0.%1 seconds` | 0,%1 segundos |  |  |
| `Abort Download` | Cancelar a transferência |  |  |
| `About %1 remaining` | Cerca de %1 restantes |  |  |
| `Could not open file` | Não foi possível abrir o ficheiro |  |  |
| `Could not open file '%1' for write.  Please check Permissions` | Não foi possível abrir o ficheiro '%1' para escrita. Verifique as permissões |  |  |
| `Downloading File` | A transferir ficheiro |  |  |
| `Downloading File '%1'` | A transferir o ficheiro '%1' |  |  |
| `Downloading file '%1'` | A transferir o ficheiro '%1' |  |  |
| `Error downloading file` | Erro ao transferir o ficheiro |  |  |
| `Finishing up...` | A concluir... |  |  |
| `less than a second` | menos de um segundo |  |  |
| `Please Select Download Directory` | Selecione a pasta de transferências |  |  |
| `Seconds Remaining until Timeout:` | Segundos até ao tempo limite: |  |  |
| `Seconds Remaining until Timeout: %1 seconds` | Segundos até ao tempo limite: %1 segundos |  |  |
| `Timeout while downloading` | Tempo limite excedido durante a transferência |  |  |

## Main window - menus, toolbar and buttons (23)

| Original (English) | Translation (pt-PT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `  #  ` |   #   |  |  |
| `&About` | &amp;Acerca de | Mnemonic A. Shares the letter with "modo avancado", but that sits in the Regulator menu, so there is no collision. Qt only needs uniqueness within one menu. |  |
| `&Connect` | &amp;Ligar |  |  |
| `&Disconnect from Selected Regulator` | &amp;Desligar do regulador selecionado |  |  |
| `&Exit` | &amp;Sair | ACCELERATOR MOVED: E to S, since Sair has no E. No collision within the File menu. |  |
| `&File` | &amp;Ficheiro |  |  |
| `&Help` | A&amp;juda | ACCELERATOR MOVED: Ajuda has no H, so the mnemonic moved to j. No collision. Confirm the underline lands acceptably. |  |
| `&Regulator` | &amp;Regulador | Mnemonic R kept, since "Regulador" also starts with R. No collision in the connected window menu bar. |  |
| `...` | ... |  |  |
| `Add a new Regulator` | Adicionar um novo regulador |  |  |
| `Connect to Selected Regulator` | Ligar ao regulador selecionado |  |  |
| `Debug Logging...` | Registo de depuração... |  |  |
| `Disconnect from Selected Regulator` | Desligar do regulador selecionado |  |  |
| `Edit Selected Regulator` | Editar o regulador selecionado |  |  |
| `Enable &Advanced Mode...` | Ativar o modo &amp;avançado... |  |  |
| `Enable &Basic Mode` | Ativar o modo &amp;básico |  |  |
| `MainWindow` | MainWindow | As with toolBar - a Designer object name, not user-visible text. Left unchanged. |  |
| `Regulator Name Filter` | Filtro por nome de regulador |  |  |
| `Regulators:` | Reguladores: |  |  |
| `Remove Selected Regulator` | Remover o regulador selecionado |  |  |
| `Settings` | Definições |  |  |
| `Settings...` | Definições... |  |  |
| `toolBar` | toolBar | Qt Designer object name that leaks into the translation file. Left as-is deliberately; translating it would have no effect and could confuse. |  |

## Main window - regulator table column headers (10)

| Original (English) | Translation (pt-PT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `   #   ` |    #    |  |  |
| `Color` | Cor |  |  |
| `Connection Status` | Estado da ligação |  |  |
| `Connection Type` | Tipo de ligação |  |  |
| `Last Connection` | Última ligação |  |  |
| `Not Connected` | Não ligado |  |  |
| `Port or IPAddress` | Porta ou endereço IP |  |  |
| `Regulating Status` | Estado de regulação |  |  |
| `Regulator Name` | Nome do regulador | CAPITALISATION: English uses Title Case for headers, the Portuguese uses sentence case. Correct pt-PT convention, applied consistently. Confirm it is the house rule. |  |
| `Regulator Status` | Estado do regulador |  |  |

## Numeric entry dialogs (6)

| Original (English) | Translation (pt-PT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `Enter Integer` | Introduza um número inteiro | "Numero inteiro" is correct but wordy for a dialog title. If space is tight, just "Inteiro" may do. |  |
| `Enter Integer` | Introduza um número inteiro | "Numero inteiro" is correct but wordy for a dialog title. If space is tight, just "Inteiro" may do. |  |
| `Integer` | Número inteiro |  |  |
| `Integer` | Número inteiro |  |  |
| `Max` | Máx |  |  |
| `Min` | Mín | Abbreviated to "Min" with an accent. Confirm it fits the slider label without clipping. |  |

## Other (QObject) (3)

| Original (English) | Translation (pt-PT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `%1 - ` | %1 -  |  |  |
| `Cmd: %1 - Error Count: %2` | Comando: %1 - Número de erros: %2 |  |  |
| `Warning - Consecutive command ran too quickly '%1'` | Aviso - comando consecutivo executado demasiado depressa '%1' |  |  |

## Parameter file editor (59)

| Original (English) | Translation (pt-PT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `+ or - followed by 2 digits` | + ou - seguido de 2 dígitos |  |  |
| `...` | ... |  |  |
| `0 or 1` | 0 ou 1 |  |  |
| `1 digit` | 1 dígito |  |  |
| `2 digits` | 2 dígitos |  |  |
| `3 digits` | 3 dígitos |  |  |
| `4 digits` | 4 dígitos |  |  |
| `Active Voltage Target` | Tensão alvo ativa |  |  |
| `All Disabled on Any Fault` | Todas desativadas em qualquer avaria |  |  |
| `Amperage Rating LSB` | Corrente nominal LSB |  |  |
| `Amperage Rating MSB` | Corrente nominal MSB |  |  |
| `B or + or - followed by 2 digits` | B ou + ou - seguido de 2 dígitos |  |  |
| `Current Data` | Dados atuais |  |  |
| `Description` | Descrição |  |  |
| `Edit Parameter File` | Editar o ficheiro de parâmetros |  |  |
| `End Position` | Posição final |  |  |
| `Error Message:` | Mensagem de erro: |  |  |
| `Expected Data` | Dados esperados |  |  |
| `Externally Controlled Select (1 or 2)` | Seleção controlada externamente (1 ou 2) |  |  |
| `File '%1' content was not 57 characters` | O conteúdo do ficheiro '%1' não tinha 57 caracteres |  |  |
| `File '%1' Could not be Opened.` | Não foi possível abrir o ficheiro '%1'. |  |  |
| `Frequency` | Frequência |  |  |
| `Ignored 21 bytes` | 21 bytes ignorados |  |  |
| `Ignored 3 bytes` | 3 bytes ignorados |  |  |
| `Ignored 4 bytes` | 4 bytes ignorados |  |  |
| `Invalid character/text at position %1. Expected '%2', Got '%3'` | Carácter ou texto inválido na posição %1. Esperado '%2', obtido '%3' |  |  |
| `Invalid Parameter File` | Ficheiro de parâmetros inválido |  |  |
| `Open Parameter File` | Abrir o ficheiro de parâmetros |  |  |
| `Over Current Fault Count Limit` | Limite da contagem de avarias por sobreintensidade |  |  |
| `Over Voltage Limit` | Limite de sobretensão |  |  |
| `Over Voltage Protection Limit` | Limite de proteção contra sobretensão |  |  |
| `P followed by any 1 byte` | P seguido de qualquer 1 byte |  |  |
| `Parameter File` | Ficheiro de parâmetros |  |  |
| `Parameter File:` | Ficheiro de parâmetros: |  |  |
| `Phase Voltage Offset` | Desvio de tensão de fase |  |  |
| `Power Interactive Regulation` | Regulação interativa de potência |  |  |
| `Power Interactive Regulation Delta Voltage` | Variação de tensão da regulação interativa de potência |  |  |
| `Power Interactive Regulation NULL Voltage` | Tensão nula da regulação interativa de potência |  |  |
| `Power Interactive Regulation Time Constant` | Constante de tempo da regulação interativa de potência |  |  |
| `Prefix` | Prefixo |  |  |
| `Ramp Rate` | Velocidade de rampa | "Velocidade de rampa" - consistent with "Em rampa" for Ramping. Confirm both against field usage together. |  |
| `Ramp to Vin` | Rampa até Vin |  |  |
| `Raw Data` | Dados em bruto |  |  |
| `Reset To Current` | Repor o atual |  |  |
| `Reset to Current Parameter File` | Repor o ficheiro de parâmetros atual |  |  |
| `Reset to Default` | Repor o predefinido |  |  |
| `Reset to Default Parameter File` | Repor o ficheiro de parâmetros predefinido |  |  |
| `Save Parameter File` | Guardar o ficheiro de parâmetros |  |  |
| `Select Parameter File` | Selecionar o ficheiro de parâmetros |  |  |
| `SPARE` | SPARE | Left untranslated. It appears to be a placeholder field name in the parameter file rather than a word shown to an operator - confirm. |  |
| `Start Position` | Posição inicial |  |  |
| `System Gain` | Ganho do sistema |  |  |
| `Target Voltage 1` | Tensão alvo 1 |  |  |
| `Target Voltage 2` | Tensão alvo 2 |  |  |
| `Text Files (*.txt);;All Files (*.*)` | Ficheiros de texto (*.txt);;Todos os ficheiros (*.*) |  |  |
| `Under Voltage Limit` | Limite de subtensão |  |  |
| `Voltage Regulation Disabled` | Regulação de tensão desativada |  |  |
| `Voltage Setpoint 1` | Valor de tensão definido 1 |  |  |
| `Voltage Setpoint 2` | Valor de tensão definido 2 |  |  |

## Password and credential prompts (17)

| Original (English) | Translation (pt-PT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `...` | ... |  |  |
| `...` | ... |  |  |
| `Access to %1 requires the correct password to be entered.` | O acesso a %1 exige a introdução da palavra-passe correta. |  |  |
| `Confirm Password:` | Confirme a palavra-passe: |  |  |
| `Confirmation password does not match` | A palavra-passe de confirmação não coincide |  |  |
| `Current password is not correct` | A palavra-passe atual não está correta |  |  |
| `Current Password:` | Palavra-passe atual: |  |  |
| `Enter Credentials` | Introduza as credenciais |  |  |
| `Enter Password` | Introduza a palavra-passe |  |  |
| `Enter Password:` | Introduza a palavra-passe: |  |  |
| `Incorrect Password` | Palavra-passe incorreta |  |  |
| `Incorrect password entered, Access to %1 denied.` | Palavra-passe incorreta; acesso a %1 negado. |  |  |
| `New password does not satisfy length criteria` | A nova palavra-passe não cumpre o critério de comprimento |  |  |
| `Password Required` | Palavra-passe necessária |  |  |
| `Password Required for %1` | Palavra-passe necessária para %1 |  |  |
| `Password:` | Palavra-passe: |  |  |
| `Username:` | Nome de utilizador: |  |  |

## Regulator Information panel (18)

| Original (English) | Translation (pt-PT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| ` - Not Connected` |  - Não ligado |  |  |
| `<Unknown>` | &lt;Desconhecido&gt; | Angle brackets are UI decoration and have been preserved. Confirm that reads as a placeholder rather than a broken tag. |  |
| `...` | ... |  |  |
| `Connected Via:` | Ligado via: | "Ligado via:" is compact and fits the column. "Ligado atraves de:" is more formal but longer. Flagged in case house style prefers it. |  |
| `GroupBox` | GroupBox | Designer object name, not user-visible. Left unchanged. |  |
| `Invalid Serial Number` | Número de série inválido |  |  |
| `Name:` | Nome: |  |  |
| `Phase Firmware Version:` | Versão do firmware de fase: | "firmware" deliberately left in English, which is normal practice. Confirm that is wanted throughout. |  |
| `Product:` | Produto: |  |  |
| `Regulating Status:` | Estado de regulação: |  |  |
| `Regulator Information` | Informação do regulador |  |  |
| `Regulator Information:` | Informação do regulador: |  |  |
| `Regulator's System Clock:` | Relógio do sistema do regulador: |  |  |
| `Serial Number (12 Characters):` | Número de série (12 caracteres): | The 12 is a firmware limit, not a translation choice. If that limit changes, both languages change. |  |
| `Serial Number:` | Número de série: |  |  |
| `Set Serial Number` | Definir número de série | Dialog title in sentence case, following pt-PT convention rather than mirroring English Title Case. |  |
| `System Firmware Version and Compilation Date:` | Versão do firmware do sistema e data de compilação: | LAYOUT RISK: the Portuguese runs about 20 percent longer and this is already the widest label in the panel. Worth checking it does not push the field off the edge. |  |
| `The serial number must have 12 characters` | O número de série tem de ter 12 caracteres | Same fixed 12 as the prompt above. Keep the two in step. |  |

## Regulator status and messages (21)

| Original (English) | Translation (pt-PT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `    File #: %1` |     Ficheiro n.º: %1 |  |  |
| ` - Regulator clock off by %1` |  - Relógio do regulador desfasado em %1 |  |  |
| ` - Running Command` |  - a executar comando |  |  |
| ` and ` |  e  |  |  |
| `%1 Hour` | %1 hora |  |  |
| `%1 Hours` | %1 horas |  |  |
| `%1 Minute` | %1 minuto |  |  |
| `%1 Minutes` | %1 minutos |  |  |
| `%1 Second` | %1 segundo |  |  |
| `%1 Seconds` | %1 segundos |  |  |
| `Enabled` | Ativado |  |  |
| `Firmware must be updated to support Voltage Calibration` | O firmware tem de ser atualizado para suportar a calibração de tensão |  |  |
| `Firmware must be upgraded to V17 or later to support Voltage Calibration` | O firmware tem de ser atualizado para a V17 ou posterior para suportar a calibração de tensão |  |  |
| `Number of SD Card files: %1` | Número de ficheiros no cartão SD: %1 |  |  |
| `Regulation Information:` | Informação de regulação: |  |  |
| `Regulator Will Reboot` | O regulador vai reiniciar |  |  |
| `Target Voltage 1` | Tensão alvo 1 |  |  |
| `Target Voltage 2` | Tensão alvo 2 |  |  |
| `This command will force the regulator to reboot. After it reboots and the green LED on the regulator comes on, you will need to reconnect.` | Este comando obriga o regulador a reiniciar. Depois de reiniciar e de o LED verde do regulador acender, terá de voltar a ligar-se. |  |  |
| `Unknown` | Desconhecido | Used both as a status value and as a placeholder. Confirm one word works for both, since it must agree with a masculine noun (estado, regulador). |  |
| `Voltage Control must be set to either Set point 1 or 2` | O controlo de tensão tem de estar definido no valor 1 ou 2 |  |  |

## Regulator status trees (59)

| Original (English) | Translation (pt-PT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `Active Voltage Target` | Tensão alvo ativa |  |  |
| `ADC Cal Error` | Erro de calibração do ADC |  |  |
| `All Phases Disabled on Failure in Any Phase` | Todas as fases desativadas em caso de falha em qualquer fase |  |  |
| `Amperage Rating (A)` | Corrente nominal (A) |  |  |
| `Baud Rate` | Velocidade de transmissão | TERMINOLOGY: rendered "Velocidade de transmissao". Some pt-PT technical writing keeps "Baud rate" untranslated. Decide once and apply to the UART screens. |  |
| `Connection:` | Ligação: |  |  |
| `Current (A)` | Corrente (A) |  |  |
| `Delta Voltage (V)` | Variação de tensão (V) |  |  |
| `Fault Code` | Código de avaria |  |  |
| `Flow Control` | Controlo de fluxo |  |  |
| `Flux Sensor` | Sensor de fluxo |  |  |
| `Form` | Form | Designer object name, not user-visible. Left unchanged. |  |
| `Form` | Form | Designer object name, not user-visible. Left unchanged. |  |
| `Frequency` | Frequência |  |  |
| `No` | Não |  |  |
| `Null Voltage (V)` | Tensão nula (V) |  |  |
| `Over Current Fault Count` | Contagem de avarias por sobreintensidade |  |  |
| `Over Current Fault Count` | Contagem de avarias por sobreintensidade |  |  |
| `Over Current Fault in Reset Delay` | Avaria por sobreintensidade em atraso de reposição |  |  |
| `Over Current Fault Limit` | Limite de avarias por sobreintensidade |  |  |
| `Over Temperature` | Temperatura excessiva |  |  |
| `Over Voltage Limit` | Limite de sobretensão |  |  |
| `Over Voltage Protection Limit` | Limite de proteção contra sobretensão |  |  |
| `Phase %1` | Fase %1 |  |  |
| `Phase Lock Loop not Locked` | PLL não sincronizado |  |  |
| `Power Interactive Regulation Status` | Estado da regulação interativa de potência |  |  |
| `Power Interactive Regulation Status` | Estado da regulação interativa de potência |  |  |
| `Ramp Rate` | Velocidade de rampa | "Velocidade de rampa" - consistent with "Em rampa" for Ramping. Confirm both against field usage together. |  |
| `Reaction Time (s)` | Tempo de reação (s) |  |  |
| `Regulating Status` | Estado de regulação |  |  |
| `Regulating:` | Regulação: |  |  |
| `Regulator at Maximum Boost or Buck` | Regulador no máximo de elevação ou redução |  |  |
| `Regulator Faults:` | Avarias do regulador: |  |  |
| `Regulator Ramping` | Regulador em rampa |  |  |
| `Regulator:` | Regulador: |  |  |
| `SCR or Gate Drive Faults` | Avarias do SCR ou do comando de porta |  |  |
| `SD Card Status` | Estado do cartão SD |  |  |
| `Settings` | Definições |  |  |
| `Settings` | Definições |  |  |
| `Status:` | Estado: |  |  |
| `System Gain` | Ganho do sistema |  |  |
| `Target Voltage 1` | Tensão alvo 1 |  |  |
| `Target Voltage 2` | Tensão alvo 2 |  |  |
| `Temp Sensor or Fan` | Sensor de temperatura ou ventoinha |  |  |
| `Temperature (°C)` | Temperatura (°C) | Degree symbol preserved. Confirm it renders correctly in the status tree with the bundled condensed font. |  |
| `UART 1` | UART 1 |  |  |
| `UART 1` | UART 1 |  |  |
| `UART 1` | UART 1 |  |  |
| `UART 2` | UART 2 |  |  |
| `UART 2` | UART 2 |  |  |
| `UART 2` | UART 2 |  |  |
| `Under Voltage Limit` | Limite de subtensão |  |  |
| `VCC or Fuse` | VCC ou fusível |  |  |
| `Vin/Vout out of limit` | Vin/Vout fora do limite |  |  |
| `Voltage Calibration Offset` | Desvio de calibração de tensão |  |  |
| `Voltage In (V)` | Tensão de entrada (V) |  |  |
| `Voltage Out (V)` | Tensão de saída (V) |  |  |
| `Voltage Regulation Disabled` | Regulação de tensão desativada |  |  |
| `Yes` | Sim |  |  |

## SD card download dialog (36)

| Original (English) | Translation (pt-PT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `...` | ... |  |  |
| `2 Days Ago` | Há 2 dias |  |  |
| `3 Days Ago` | Há 3 dias |  |  |
| `4 Days Ago` | Há 4 dias |  |  |
| `5 Days Ago` | Há 5 dias |  |  |
| `6 Days Ago` | Há 6 dias |  |  |
| `7 Days Ago` | Há 7 dias |  |  |
| `A file is still downloading. Cancel it in the progress window before closing this one.` | Ainda está a ser transferido um ficheiro. Cancele-o na janela de progresso antes de fechar esta. |  |  |
| `April` | Abril |  |  |
| `August` | Agosto |  |  |
| `Command` | Comando |  |  |
| `Data will not be recorded or updated during file downloads` | Os dados não serão registados nem atualizados durante a transferência de ficheiros |  |  |
| `December` | Dezembro |  |  |
| `Download in progress` | Transferência em curso |  |  |
| `Download not started` | A transferência não foi iniciada |  |  |
| `Fault Log` | Registo de avarias |  |  |
| `February` | Fevereiro |  |  |
| `File Name` | Nome do ficheiro |  |  |
| `January` | Janeiro |  |  |
| `July` | Julho |  |  |
| `June` | Junho |  |  |
| `March` | Março |  |  |
| `May` | Maio |  |  |
| `Modification Date` | Data de modificação |  |  |
| `Name` | Nome |  |  |
| `November` | Novembro |  |  |
| `October` | Outubro |  |  |
| `SD Card Files` | Ficheiros do cartão SD |  |  |
| `Select` | Selecionar |  |  |
| `September` | Setembro |  |  |
| `Size (Bytes)` | Tamanho (bytes) |  |  |
| `The regulator is still busy with the previous transfer. Please try again in a moment.` | O regulador ainda está ocupado com a transferência anterior. Tente novamente dentro de instantes. |  |  |
| `This Month` | Este mês |  |  |
| `Today` | Hoje |  |  |
| `Waiting for regulator...` | À espera do regulador... |  |  |
| `Yesterday` | Ontem |  |  |

## Settings dialog (68)

| Original (English) | Translation (pt-PT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `      This setting is also the time between consecutive commands.` |       Esta definição é também o intervalo entre comandos consecutivos. |  |  |
| ` Amps` |  Amperes |  |  |
| ` s` |  s |  |  |
| ` Seconds` |  Segundos |  |  |
| ` Volts` |  Volts |  |  |
| `<the system Downloads folder>` | &lt;a pasta Transferências do sistema&gt; |  |  |
| `+` | + |  |  |
| `-` | - |  |  |
| `1` | 1 |  |  |
| `Advanced user password:` | Palavra-passe de utilizador avançado: |  |  |
| `Amperage Rating:` | Corrente nominal: |  |  |
| `As Needed` | Conforme necessário |  |  |
| `Asked for when the tool starts, and by Settings > Enable Advanced Mode. Takes effect immediately.` | Pedida ao iniciar a ferramenta e em Definições &gt; Ativar o modo avançado. Tem efeito imediato. |  |  |
| `Automatically Refresh Status?` | Atualizar o estado automaticamente? |  |  |
| `Change Advanced User Password` | Alterar a palavra-passe de utilizador avançado |  |  |
| `Change Advanced User Password...` | Alterar a palavra-passe de utilizador avançado... |  |  |
| `Choose the language the tool is displayed in. The change takes effect immediately; any regulator windows that are already open keep their current language until they are reopened.` | Escolha o idioma em que a ferramenta é apresentada. A alteração tem efeito imediato; as janelas de regulador já abertas mantêm o idioma atual até serem reabertas. |  |  |
| `Command Timeout:` | Tempo limite de comando: |  |  |
| `Default Regulator Settings` | Predefinições do regulador |  |  |
| `Default Time Zone` | Fuso horário predefinido |  |  |
| `Default View Settings` | Predefinições de visualização |  |  |
| `Download Timeout:` | Tempo limite de transferência: |  |  |
| `Downloads` | Transferências |  |  |
| `External Voltage Setpoint Select (1 or 2)` | Seleção externa do valor de tensão (1 ou 2) |  |  |
| `Fast` | Rápido |  |  |
| `Fast:` | Rápido: |  |  |
| `Folder for Downloaded Files` | Pasta para os ficheiros transferidos |  |  |
| `Language` | Idioma |  |  |
| `Medium` | Médio |  |  |
| `Medium:` | Médio: |  |  |
| `NULL Voltage at Zero kW:` | Tensão nula a zero kW: |  |  |
| `Power Interactive Regulation` | Regulação interativa de potência |  |  |
| `Power Interactive Regulation Settings` | Definições da regulação interativa de potência |  |  |
| `Ramp to Vin` | Rampa até Vin |  |  |
| `Refresh for Regulator Clock Time` | Atualização da hora do relógio do regulador |  |  |
| `Refresh for Regulator Faults and Voltages:` | Atualização das avarias e tensões do regulador: |  |  |
| `Refresh for SD Card Files:` | Atualização dos ficheiros do cartão SD: |  |  |
| `Refresh for Voltage Calibration Status:` | Atualização do estado de calibração de tensão: |  |  |
| `Refresh Gain Values:` | Atualização dos valores de ganho: |  |  |
| `Refresh Rate Parameter File Information:` | Frequência de atualização da informação do ficheiro de parâmetros: |  |  |
| `Refresh Settings` | Definições de atualização |  |  |
| `Refresh Times:` | Intervalos de atualização: |  |  |
| `Refresh UART Settings:` | Atualização das definições UART: |  |  |
| `Regulator Setting Defaults` | Predefinições do regulador |  |  |
| `Regulator:` | Regulador: |  |  |
| `Require Password to Enter Advanced Mode?` | Exigir palavra-passe para entrar em modo avançado? |  |  |
| `Save downloaded files to:` | Guardar os ficheiros transferidos em: |  |  |
| `Security` | Segurança |  |  |
| `Settings` | Definições |  |  |
| `Setup UARTs` | Configurar UARTs |  |  |
| `Show password` | Mostrar a palavra-passe |  |  |
| `Slow` | Lento |  |  |
| `Slow:` | Lento: |  |  |
| `Start in Advanced Mode?` | Iniciar em modo avançado? |  |  |
| `The Advanced user password has been changed.` | A palavra-passe de utilizador avançado foi alterada. |  |  |
| `Time Constant:` | Constante de tempo: |  |  |
| `Timeout Settings` | Definições de tempo limite |  |  |
| `Timestamp Transcript?` | Marcar a transcrição com a hora? |  |  |
| `Update Settings For All Regulators?` | Aplicar as definições a todos os reguladores? |  |  |
| `View Regulator Information?` | Ver a informação do regulador? |  |  |
| `View Regulator Status?` | Ver o estado do regulador? |  |  |
| `View Transcript in Sepeate Window?` | Ver a transcrição numa janela separada? | NOTE: "Sepeate" is misspelled in the English source. The Portuguese is correct. Worth fixing the original - and note the correctly spelled variant exists separately in the connected window. |  |
| `View Transcript?` | Ver a transcrição? |  |  |
| `Voltage Control Settings` | Definições de controlo de tensão |  |  |
| `Voltage Delta:` | Variação de tensão: |  |  |
| `Voltage Setpoint 1:` | Valor de tensão definido 1: |  |  |
| `Voltage Setpoint 2:` | Valor de tensão definido 2: |  |  |
| `±` | ± |  |  |

## Status and fault values - tables, trees and panels (128)

| Original (English) | Translation (pt-PT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `(in multiphase models only) Indicates one of the phases has an open fuse or there is no VCC power. NOTE - a single phase model could not be communicating.` | (apenas em modelos multifásicos) Indica que uma das fases tem um fusível aberto ou que não há alimentação VCC. NOTA - um modelo monofásico poderá estar sem comunicação. |  |  |
| `7A` | 7A |  |  |
| `9A` | 9A |  |  |
| `Active` | Ativo |  |  |
| `B2` | B2 |  |  |
| `B8` | B8 |  |  |
| `BA` | BA |  |  |
| `Bound` | Vinculado | Low-level socket state. "Vinculado" is literal; "Associado" is more idiomatic for sockets. Also worth asking whether a user ever sees this state. |  |
| `CA` | CA |  |  |
| `CB` | CB | PROTOCOL CODE: this and the other two-character codes (OT, W1, P+, ZX, RAMP, FLUX...) are firmware identifiers shown verbatim in the fault log. Deliberately translated to themselves - translating them would break the match against regulator output. |  |
| `Closing` | A fechar | Low-level socket state, probably never shown to an installer. |  |
| `Command Transmission Error` | Erro de transmissão de comando |  |  |
| `Communication Error` | Erro de comunicação |  |  |
| `Confirming Connection` | A confirmar ligação |  |  |
| `Connected` | Ligado |  |  |
| `Connecting` | A ligar |  |  |
| `Data File downloaded - not implemented` | Ficheiro de dados transferido - não implementado |  |  |
| `DC` | DC |  |  |
| `Disabled` | Desativado |  |  |
| `Disabled by Current >1.5X current rating - resets 15min after return to rated current` | Desativado por corrente superior a 1,5x a corrente nominal - reposição 15 min após o regresso à corrente nominal | DECIMAL COMMA: written "1,5x" using the Portuguese decimal separator. Check this against how the app formats numbers elsewhere, so the text and the data agree. |  |
| `Disabled by Over Current` | Desativado por sobreintensidade | Uses the IEC term "sobreintensidade" rather than the Brazilian "sobrecorrente". Confirm that matches what your installers say. |  |
| `Disabled by Over Temperature` | Desativado por sobreaquecimento | PRECISION: "sobreaquecimento" means overheating. If the trip is a temperature threshold rather than overheating as such, "sobretemperatura" is more exact. |  |
| `Disabled by switch (3 phase only)` | Desativado por interruptor (apenas trifásico) |  |  |
| `Disabled by User` | Desativado pelo utilizador | One of the states the enable/disable confirmation polls exist to surface, so this text is user-facing and worth getting exactly right. |  |
| `Disabled by User command` | Desativado por comando do utilizador |  |  |
| `Disabled by Voltage Issue` | Desativado por problema de tensão |  |  |
| `Disconnected` | Desligado |  |  |
| `DS` | DS |  |  |
| `DU` | DU |  |  |
| `EA` | EA |  |  |
| `Enabled by User command - i.e. regulating` | Ativado por comando do utilizador - ou seja, em regulação |  |  |
| `Error Processing Voltage and Fault Status` | Erro ao processar o estado de tensão e avarias | Long error string. Confirm it fits wherever it is shown without truncation. |  |
| `EU` | EU |  |  |
| `F4` | F4 |  |  |
| `F5` | F5 |  |  |
| `FA` | FA |  |  |
| `Failed` | Falhou |  |  |
| `Failed or Missing` | Falhou ou ausente | GRAMMAR: mixes a verb (Falhou) with an adjective (ausente). "Falhou ou nao encontrado" may read better. Must also agree with the subject, SD card being masculine (cartao). |  |
| `Fan Fault Cleared` | Avaria da ventoinha resolvida |  |  |
| `Fault` | Avaria | Chose "Avaria" (equipment breakdown) over "Falha" (failure). Right for hardware, but confirm against the rest of your field vocabulary. |  |
| `FB` | FB |  |  |
| `FC` | FC |  |  |
| `FD` | FD |  |  |
| `FE` | FE |  |  |
| `FLUX` | FLUX |  |  |
| `Flux Sensor Error  If sustained, it writes to F/L once per hour (this will increase the number of Over Current Faults from transformer saturations)` | Erro do sensor de fluxo. Se persistir, é registado no F/L uma vez por hora (o que aumentará o número de avarias por sobreintensidade devidas a saturação do transformador) |  |  |
| `Getting System Info` | A obter informação do sistema |  |  |
| `Host Found` | Anfitrião encontrado |  |  |
| `Host Lookup` | A procurar anfitrião | TERMINOLOGY: "anfitriao" is the correct pt-PT word for host, but technical users often expect the English "host". Which does your audience use? |  |
| `Indicates a fault caused by a SCR gate drive error` | Indica uma avaria provocada por um erro de comando de porta do SCR |  |  |
| `Indicates a flux sensor malfunction which could cause the transformer to saturate` | Indica uma avaria do sensor de fluxo que poderá levar à saturação do transformador |  |  |
| `Indicates an A to D calibration error during bootup or Voltage sensing error` | Indica um erro de calibração do conversor A/D durante o arranque ou um erro de medição de tensão |  |  |
| `Indicates Flux Sensor faults (>12 per 1/2 Second Interval)` | Indica avarias do sensor de fluxo (mais de 12 por intervalo de meio segundo) |  |  |
| `Indicates full PWM in boost mode (i.e. limiting the ability to hold the setpoint)` | Indica PWM no máximo em modo elevador (limitando a capacidade de manter o valor definido) | BOOST/BUCK: rendered "elevador" and "redutor". These are the standard pt-PT power-electronics terms, but confirm your installers use them rather than the English. |  |
| `Indicates full PWM in buck mode (i.e. limiting the ability to hold the setpoint)` | Indica PWM no máximo em modo redutor (limitando a capacidade de manter o valor definido) |  |  |
| `Indicates SCR or Gate Drive Faults (>12 per 1/2 Second Interval)` | Indica avarias do SCR ou do comando de porta (mais de 12 por intervalo de meio segundo) |  |  |
| `Indicates the converter board is temporally in a over temperature state which will reset` | Indica que a placa do conversor está temporariamente em estado de temperatura excessiva, que será reposto |  |  |
| `Indicates the Over Current Fault has cleared and returned to regulation` | Indica que a avaria por sobreintensidade foi resolvida e que a regulação foi retomada |  |  |
| `Indicates the regulator is in a state of maximum Boost or Buck` | Indica que o regulador está no máximo de elevação ou de redução |  |  |
| `Indicates the regulator is in an over current fault reset delay` | Indica que o regulador está num atraso de reposição de avaria por sobreintensidade |  |  |
| `Indicates there are no hardware faults and the regulator is not disabled i.e. regulating` | Indica que não existem avarias de hardware e que o regulador não está desativado, ou seja, está em regulação |  |  |
| `Indicates there are no hardware faults but the regulator is disabled for various reasons indicated in the Aux Status string. The cause could be it was disabled by the user, or as the result of a fault condition which may clear and return to regulation, or it is in a timer mode where regulation is temporally disabled.` | Indica que não existem avarias de hardware, mas que o regulador está desativado por motivos indicados na cadeia de estado auxiliar. A causa pode ser a desativação pelo utilizador, uma condição de avaria que poderá ser resolvida com regresso à regulação, ou um modo temporizado em que a regulação está temporariamente desativada. |  |  |
| `Indicates Vin or Vout is out of range, either because of high or low line voltage, or possibly a voltage sensing circuit error.` | Indica que Vin ou Vout está fora do intervalo, por tensão de linha alta ou baixa, ou eventualmente por erro do circuito de medição de tensão. |  |  |
| `Input Power Loss` | Perda de alimentação de entrada |  |  |
| `Listening` | Em escuta | Low-level socket state, probably never shown to an installer. Flagged so effort is not spent perfecting it. |  |
| `Locked` | Bloqueado | Confirm this means latched off after an over-current event. If so, "Em bloqueio" may read better than "Bloqueado", which suggests a locked door. |  |
| `Logged In/Connected` | Sessão iniciada/Ligado | Slash construction carried straight over. Confirm it reads naturally rather than as two truncated words. |  |
| `Logging In` | A iniciar sessão |  |  |
| `Logging Out Phase 1` | A terminar sessão (fase 1) |  |  |
| `Logging Out Phase 2` | A terminar sessão (fase 2) |  |  |
| `MAX_BOOSTORBUCK` | MAX_BOOSTORBUCK |  |  |
| `Missing` | Ausente |  |  |
| `Missing Zero Crossing` | Passagem por zero em falta |  |  |
| `MS` | MS |  |  |
| `ND` | ND |  |  |
| `Not Disabled by switch - i.e. regulating` | Não desativado por interruptor - ou seja, em regulação |  |  |
| `O0` | O0 |  |  |
| `O1` | O1 |  |  |
| `OC` | OC |  |  |
| `OT` | OT |  |  |
| `Over Current Fault Count O,1...9 then 10,11, 12...` | Contagem de avarias por sobreintensidade 0,1...9 e depois 10,11,12... |  |  |
| `Over Current Fault reset maximum count reached (per PRM file) must be reset manually` | Atingido o número máximo de reposições de avaria por sobreintensidade (conforme o ficheiro PRM) - é necessária reposição manual |  |  |
| `Over Temperature fault - converter is disabled until it cools` | Avaria por temperatura excessiva - o conversor fica desativado até arrefecer |  |  |
| `P+` | P+ |  |  |
| `P-` | P- |  |  |
| `PL` | PL |  |  |
| `PLL_NL` | PLL_NL |  |  |
| `PN` | PN |  |  |
| `PR` | PR |  |  |
| `Processor Reset by user command` | Processador reposto por comando do utilizador |  |  |
| `PWM is no longer railed, and has dropped below 95% of maximum` | O PWM deixou de estar no limite e desceu abaixo de 95% do máximo |  |  |
| `RAMP` | RAMP |  |  |
| `Ramping` | Em rampa | FIELD TERM: "Em rampa" is literal. Is there a term Portuguese installers actually use for a regulator ramping to target? |  |
| `Real Time Clock time after Change` | Hora do relógio de tempo real após a alteração |  |  |
| `Real Time Clock time before Change` | Hora do relógio de tempo real antes da alteração |  |  |
| `Rebooting` | A reiniciar |  |  |
| `Regulating` | Em regulação | Appears in three separate places and is translated identically in all three. Intentional, and worth keeping in step. |  |
| `Regulator is ramping to the active set point` | O regulador está a subir em rampa para o valor definido ativo |  |  |
| `Restoring Session` | A restaurar a sessão |  |  |
| `SCR_GATE` | SCR_GATE |  |  |
| `SD Card data logging was stopped by user command (disabled)` | O registo de dados no cartão SD foi parado por comando do utilizador (desativado) |  |  |
| `SE` | SE |  |  |
| `Service Lookup` | A procurar serviço |  |  |
| `TEMP` | TEMP |  |  |
| `Temp sensor open` | Sensor de temperatura em circuito aberto |  |  |
| `Temp Sensor or Fan Fault` | Avaria do sensor de temperatura ou da ventoinha |  |  |
| `Temp sensor shorted` | Sensor de temperatura em curto-circuito |  |  |
| `The PLL is currently not locked` | O PLL não está sincronizado |  |  |
| `Transformer Saturation` | Saturação do transformador |  |  |
| `TS` | TS |  |  |
| `Unknown` | Desconhecido | Used both as a status value and as a placeholder. Confirm one word works for both, since it must agree with a masculine noun (estado, regulador). |  |
| `VC` | VC |  |  |
| `Vin or Vout is out of range as defined in PRM file - fault resets automatically with a 10V asymmetrical hysteresis (check fault log Vin column to determine over or under) ` | Vin ou Vout fora do intervalo definido no ficheiro PRM - a avaria repõe-se automaticamente com uma histerese assimétrica de 10 V (consulte a coluna Vin do registo de avarias para determinar se é por excesso ou por defeito) |  |  |
| `VO` | VO |  |  |
| `Voltage Calibration error on boot up. After bootup, it permanently disables the regulator` | Erro de calibração de tensão no arranque. Após o arranque, desativa permanentemente o regulador |  |  |
| `W1` | W1 |  |  |
| `W2` | W2 |  |  |
| `W3` | W3 |  |  |
| `W4` | W4 |  |  |
| `W5` | W5 |  |  |
| `W6` | W6 |  |  |
| `Watchdog tripped - DSPIC failure to respond` | Watchdog disparado - o DSPIC não respondeu | "Watchdog" left in English throughout, as is normal in Portuguese engineering text. Confirm. |  |
| `Watchdog tripped - Failed wellness test (Vout != Setpoint and no faults)` | Watchdog disparado - teste de integridade falhado (Vout diferente do valor definido e sem avarias) |  |  |
| `Watchdog tripped - Main uP loop timed out OR H/W watchdog timed out` | Watchdog disparado - tempo esgotado no ciclo principal do microprocessador ou no watchdog de hardware |  |  |
| `Watchdog tripped - Phase Parameter file checksum mismatch` | Watchdog disparado - checksum do ficheiro de parâmetros de fase não corresponde |  |  |
| `Watchdog tripped - Phase Status or data checksum mismatch  ` | Watchdog disparado - checksum do estado ou dos dados de fase não corresponde |  |  |
| `Watchdog tripped - SPI buss to phase failure ` | Watchdog disparado - falha do barramento SPI para a fase |  |  |
| `ZX` | ZX |  |  |

## Transcript pane and window (18)

| Original (English) | Translation (pt-PT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| ` Send Command ` |  Enviar comando  |  |  |
| ` Send CTRL-C ` |  Enviar CTRL-C  |  |  |
| `%1:     Sent: %2` | %1:     Enviado: %2 |  |  |
| `%1: %2` | %1: %2 |  |  |
| `%1: <font color="orange">WARNING: %2</font>` | `%1: <font color="orange">AVISO: %2</font>` |  |  |
| `%1: <font color="red">ERROR: %2</font>` | `%1: <font color="red">ERRO: %2</font>` |  |  |
| `%1: Received:   %2` | %1: Recebido:   %2 |  |  |
| `Clear Transcript` | Limpar a transcrição |  |  |
| `Command To Send` | Comando a enviar |  |  |
| `Copy Transcript to Clipboard` | Copiar a transcrição para a área de transferência |  |  |
| `Could not open '%1' for writing, please check permissions\n%2` | Não foi possível abrir '%1' para escrita; verifique as permissões\n%2 | Multi-line string, with %2 carrying the underlying system error on its own line. |  |
| `Could not Open File` | Não foi possível abrir o ficheiro |  |  |
| `Error` | Erro |  |  |
| `Save Transcript` | Guardar a transcrição |  |  |
| `Save Transcript...` | Guardar a transcrição... |  |  |
| `Select All` | Selecionar tudo |  |  |
| `Text Files (*.txt);;All Files (*.*)` | Ficheiros de texto (*.txt);;Todos os ficheiros (*.*) |  |  |
| `Transcript` | Transcrição |  |  |

## UART settings dialog (16)

| Original (English) | Translation (pt-PT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `115.2k` | 115.2k |  |  |
| `230.4k` | 230.4k |  |  |
| `38.4k` | 38.4k |  |  |
| `57.6k` | 57.6k | Baud rate value, left unchanged. Note the decimal point is correct here even though Portuguese uses a comma, because it is a protocol value rather than a number for reading. |  |
| `Baud Rate` | Velocidade de transmissão | TERMINOLOGY: rendered "Velocidade de transmissao". Some pt-PT technical writing keeps "Baud rate" untranslated. Decide once and apply to the UART screens. |  |
| `Baud rate and Flow control must be set` | É necessário definir a velocidade de transmissão e o controlo de fluxo |  |  |
| `Baud rate must be set` | É necessário definir a velocidade de transmissão |  |  |
| `Flow Control` | Controlo de fluxo |  |  |
| `Flow control must be set` | É necessário definir o controlo de fluxo |  |  |
| `Hardware Control` | Controlo por hardware |  |  |
| `None` | Nenhum |  |  |
| `Setup UARTs` | Configurar UARTs |  |  |
| `Software Control` | Controlo por software |  |  |
| `TextLabel` | TextLabel | Designer placeholder text, not user-visible. Left unchanged. |  |
| `UART 1 settings can not be modified` | As definições da UART 1 não podem ser alteradas |  |  |
| `WARNING: DO NOT CHANGE if UART2 is used with an Ethernet adapter.` | AVISO: NÃO ALTERE se a UART2 for utilizada com um adaptador Ethernet. |  |  |

## User guide windows (7)

| Original (English) | Translation (pt-PT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| `Advanced User Guide` | Guia do utilizador (avançado) |  |  |
| `Basic User Guide` | Guia do utilizador (básico) |  |  |
| `Bluetooth Pairing` | Emparelhamento Bluetooth |  |  |
| `Bluetooth Pairing (Windows 11)` | Emparelhamento Bluetooth (Windows 11) |  |  |
| `Close` | Fechar |  |  |
| `Fit to window` | Ajustar à janela |  |  |
| `The guide could not be loaded: %1` | Não foi possível carregar o guia: %1 |  |  |

## Voltage calibration dialog (10)

| Original (English) | Translation (pt-PT) | Questions / concerns | Your correction |
| --- | --- | --- | --- |
| ` Volts` |  Volts |  |  |
| `A Voltage Difference of '%1' is invalid, range is -9.9V to +9.9V` | Uma diferença de tensão de '%1' é inválida; o intervalo é de -9,9 V a +9,9 V | DECIMAL COMMA: the literal range is written "-9,9 V a +9,9 V" but %1 is formatted by the code, which may still produce a decimal point. Worth checking the two match on screen. |  |
| `Can not calibrate voltage` | Não é possível calibrar a tensão |  |  |
| `Externally Measured Output Voltage:` | Tensão de saída medida externamente: |  |  |
| `Regulator Target %1 Output Voltage:` | Tensão de saída alvo %1 do regulador: |  |  |
| `Regulator Target Output Voltage:` | Tensão de saída alvo do regulador: |  |  |
| `Voltage Calibration` | Calibração de tensão |  |  |
| `Voltage Calibration:` | Calibração de tensão: |  |  |
| `Voltage Difference is too High` | A diferença de tensão é demasiado elevada |  |  |
| `Volts` | Volts |  |  |
