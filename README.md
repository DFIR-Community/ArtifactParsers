# ArtifactParsers

A repo that aims to centralize a current, running list of relevant parsers/tools for known DFIR artifacts. 

## What makes this different from any other list of DFIR tools? 

Ideally, this will be maintained by the community as tools come and go from relevance. If a tool is listed below, then the community is vouching for it that it still works and is a good option to solve whatever problem you may be facing with a particular artifact.

## Commercial Tool Disclaimer

It's not that commercial tools aren't welcome in this list, but the table would become pretty bloated when you have 5+ tools duplicated in many cells. At the very minimum, this project aims to highlight single purpose tools made by the DFIR community members to allow for greater visibility at the options (often at no cost) for those who are looking to get problems solved in their everyday investigations.

Much love to the commercial vendors, their efforts, and their contributions to the community, but it would be ideal for anyone looking to learn more about the capabilities of a commercial tool to reach out to the vendor themselves, or visit their official website for more information.

## Analyzers vs Parsers

In the instance of Windows Event Logs, the Windows Registry, and possibly other artifacts, there is a distinct difference between a tool that analyzes an artifact and parses the artifact. Generally speaking, a tool that analyzes would do something similar to running YARA or SIGMA rules against a set of artifacts and provide meaningful output based on the rulesets used. A parser would provide raw output without any sort of predetermined rulesets or logic applied to the set of artifacts, leaving the analysis and interpretation to the end examiner. 

This is an important distinction to make with this project because, in the example of Windows Event Logs, it would be troublesome to lead an examiner looking for a tool to parse Windows Event Logs to think that a tool like Chainsaw, Hayabusa, or Zircolite will parse event logs when in reality they analyze the event logs using rulesets and logic created by threat researchers. Those tools do not PARSE the event logs like EvtxECmd, etc. 

## Contributing

Please contribute to this list if any artifacts and their corresponding tools are missing!

## Windows

| DFIR Artifact                        | CLI Tool(s)                                                                                                                                                                                                                                                           | GUI Tool(s)                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| $I30                                 | [go-ntfs](https://github.com/Velocidex/go-ntfs)<br>[Index2Csv](https://github.com/jschicht/Indx2Csv)<br>[IndexCarver](https://github.com/jschicht/IndxCarver)<br>[MFTECmd](https://ericzimmerman.github.io/#!index.md)                                                |                                                                                                                                                                                                                                                                                                                                             |
| $J                                   | [dfir_ntfs](https://github.com/msuhanov/dfir_ntfs)<br>[ExtractUsnJrnl](https://github.com/jschicht/ExtractUsnJrnl)<br>[go-ntfs](https://github.com/Velocidex/go-ntfs)<br>[MFTECmd](https://ericzimmerman.github.io/#!index.md)                                        | [NTFS Log Tracker](https://sites.google.com/site/forensicnote/ntfs-log-tracker)                                                                                                                                                                                                                                                             |
| $LogFile                             | [dfir_ntfs](https://github.com/msuhanov/dfir_ntfs)<br>[go-ntfs](https://github.com/Velocidex/go-ntfs)<br>[LogFileParser](https://github.com/jschicht/LogFileParser)<br>[RcrdCarver](https://github.com/jschicht/RcrdCarver)                                           | [NTFS Log Tracker](https://sites.google.com/site/forensicnote/ntfs-log-tracker)                                                                                                                                                                                                                                                             |
| $MFT                                 | [dfir_ntfs](https://github.com/msuhanov/dfir_ntfs)<br>[Mft2Csv](https://github.com/jschicht/Mft2Csv)<br>[MftCarver](https://github.com/jschicht/MftCarver)<br>[MFTECmd](https://ericzimmerman.github.io/#!index.md)<br>[MftRcrd](https://github.com/jschicht/MftRcrd) | [MFT_Browser](https://github.com/kacos2000/MFT_Browser)<br>[MFTExplorer](https://ericzimmerman.github.io/#!index.md)<br>[NTFS Log Tracker](https://sites.google.com/site/forensicnote/ntfs-log-tracker)                                                                                                                                     |
| $SDS                                 | [MFTECmd](https://ericzimmerman.github.io/#!index.md)<br>[Secure2Csv](https://github.com/jschicht/Secure2Csv)                                                                                                                                                         |                                                                                                                                                                                                                                                                                                                                             |
| Amcache                              | [AmcacheParser](https://ericzimmerman.github.io/#!index.md)                                                                                                                                                                                                           | [Registry Explorer](https://ericzimmerman.github.io/#!index.md)                                                                                                                                                                                                                                                                             |
| AppCompatCache (ShimCache)           | [AppCompatCacheParser](https://ericzimmerman.github.io/#!index.md)                                                                                                                                                                                                    | [Registry Explorer](https://ericzimmerman.github.io/#!index.md)                                                                                                                                                                                                                                                                             |
| AppCompatCache PCA (Windows 11 only) | [PCAParser](https://github.com/AndrewRathbun/PCAParser)                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                                                                             |
| Browsing History                     | [BrowsingHistoryView](https://www.nirsoft.net/utils/browsing_history_view.html)<br>[Hindsight](https://github.com/obsidianforensics/hindsight) - Chromium only<br>[SQLECmd](https://ericzimmerman.github.io/#!index.md) - SQLite only                                 | [BrowsingHistoryView](https://www.nirsoft.net/utils/browsing_history_view.html)<br>[Browser History Viewer](https://www.foxtonforensics.com/browser-history-viewer/)                                                                                                                                                                        |
| CSV Files                            |                                                                                                                                                                                                                                                                       | [Modern CSV](https://www.moderncsv.com/)<br>[Timeline Explorer](https://ericzimmerman.github.io/#!index.md)                                                                                                                                                                                                                                 |
| Email (MBOX)                         | [mbox-web-viewer](https://github.com/PHMRanger/mbox-web-viewer)                                                                                                                                                                                                       | [mboxviewer](https://github.com/eneam/mboxviewer)                                                                                                                                                                                                                                                                                           |
| Email (OST/PST)                      | [XstReader](https://github.com/iluvadev/XstReader)                                                                                                                                                                                                                    | [XstReader](https://github.com/iluvadev/XstReader)                                                                                                                                                                                                                                                                                          |
| ESE Databases (General)              | [WindowsEDB-to-CSV](https://github.com/kacos2000/WinEDB)                                                                                                                                                                                                              | [ESEDatabaseView](https://www.nirsoft.net/utils/ese_database_view.html)<br>[WinEDB](https://github.com/kacos2000/WinEDB)                                                                                                                                                                                                                    |
| ETL Files                            | [ETLParser](https://github.com/forensiclunch/ETLParser)                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                                                                             |
| Event Logs (.evtx) - Analyzers       | [Chainsaw](https://github.com/WithSecureLabs/chainsaw)<br>[EvtxHussar](https://github.com/yarox24/EvtxHussar)<br>[Hayabusa](https://github.com/Yamato-Security/hayabusa)<br>[Zircolite](https://github.com/wagga40/Zircolite)                                         |                                                                                                                                                                                                                                                                                                                                             |
| Event Logs (.evtx) - Parsers         | [Events-Ripper](https://github.com/keydet89/Events-Ripper)<br>[EvtxECmd](https://ericzimmerman.github.io/#!index.md)                                                                                                                                                  | [Event Log Explorer](https://www.eventlogxp.com/)<br>[Event Log Observer](https://lizard-labs.com/event_log_observer.aspx)<br>[Evtx_Log_Browser](https://github.com/kacos2000/Evtx_Log_Browser)<br>[FullEventLogView](https://www.nirsoft.net/utils/full_event_log_view.html)<br>[LogViewPlus](https://www.logviewplus.com/log-viewer.html) |
| IIS Logs                             | [IISGeoLocate](https://ericzimmerman.github.io/#!index.md)                                                                                                                                                                                                            | [LogViewPlus](https://www.logviewplus.com/log-viewer.html)                                                                                                                                                                                                                                                                                  |
| Image Mounting                       | [Arsenal Image Mounter](https://arsenalrecon.com/downloads)                                                                                                                                                                                                           | [Arsenal Image Mounter](https://arsenalrecon.com/downloads)                                                                                                                                                                                                                                                                                 |
| IP Address GeoLocation               | [Abeebus](https://github.com/13Cubed/Abeebus)                                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                                                             |
| JumpLists                            | [JLECmd](https://ericzimmerman.github.io/#!index.md)                                                                                                                                                                                                                  | [Jumplist-Browser](https://github.com/kacos2000/Jumplist-Browser)<br>[JumpList Explorer](https://ericzimmerman.github.io/#!index.md)                                                                                                                                                                                                        |
| LevelDB                              | [LevelDBDumper](https://github.com/mdawsonuk/LevelDBDumper)                                                                                                                                                                                                           | [LevelDB Recon](https://arsenalrecon.com/downloads)                                                                                                                                                                                                                                                                                         |
| LNK Files                            | [LECmd](https://ericzimmerman.github.io/#!index.md)                                                                                                                                                                                                                   | [Jumplist-Browser](https://github.com/kacos2000/Jumplist-Browser)                                                                                                                                                                                                                                                                           |
| MalwareBytes Logs                    | [MBAMServiceLogParser.ps1](https://github.com/AndrewRathbun/DFIRPowerShellScripts/blob/main/MBAMServiceLogParser.ps1)                                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                             |
| NetWire Logs                         | [NetWireLogDecoder](https://github.com/ArsenalRecon/NetWireLogDecoder)                                                                                                                                                                                                |                                                                                                                                                                                                                                                                                                                                             |
| OneDrive                             | [OneDrive .ODL Parser](https://github.com/ydkhatri/OneDrive)<br>[OneDriveExplorer](https://github.com/Beercow/OneDriveExplorer)                                                                                                                                       | [OneDriveExplorer](https://github.com/Beercow/OneDriveExplorer)                                                                                                                                                                                                                                                                             |
| Prefetch                             | [PECmd](https://ericzimmerman.github.io/#!index.md)                                                                                                                                                                                                                   | [Prefetch-Browser](https://github.com/kacos2000/Prefetch-Browser)<br>[WinPrefetchView](https://www.nirsoft.net/utils/win_prefetch_view.html)                                                                                                                                                                                                |
| RAM (Memory)                         | [Volatility](https://www.volatilityfoundation.org/releases)                                                                                                                                                                                                           | [MemProcFS](https://github.com/ufrisk/MemProcFS)<br>[Volatility Workbench](https://www.osforensics.com/tools/volatility-workbench.html)                                                                                                                                                                                                     |
| RDP Bitmap Cache                     | [BMC-Tools](https://github.com/dingtoffee/bmc-tools)                                                                                                                                                                                                                  |                                                                                                                                                                                                                                                                                                                                             |
| Recycle Bin                          | [RBCmd](https://ericzimmerman.github.io/#!index.md)                                                                                                                                                                                                                   |                                                                                                                                                                                                                                                                                                                                             |
| RecentFileCache                      | [RecentFileCacheParser](https://ericzimmerman.github.io/#!index.md)                                                                                                                                                                                                   |                                                                                                                                                                                                                                                                                                                                             |
| Registry - Analyzers                 | [reg_hunter](https://github.com/theflakes/reg_hunter)                                                                                                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                             |
| Registry - Comparison Tools          |                                                                                                                                                                                                                                                                       | [RegistryChangesView](https://www.nirsoft.net/utils/registry_changes_view.html)<br>[RegShot-Advanced](https://github.com/skydive241/Regshot-Advanced)                                                                                                                                                                                       |
| Registry - Parsers                   | [jarp](https://github.com/ydkhatri/jarp)<br>[RECmd](https://ericzimmerman.github.io/#!index.md)<br>[Registry Recon](https://arsenalrecon.com/downloads)<br>[RegRipper](https://github.com/keydet89/RegRipper3.0)<br>[yarp](https://github.com/msuhanov/yarp)          | [Registry Explorer](https://ericzimmerman.github.io/#!index.md)                                                                                                                                                                                                                                                                             |
| Shellbags                            | [SBECmd](https://ericzimmerman.github.io/#!index.md)                                                                                                                                                                                                                  | [Shellbags Explorer](https://ericzimmerman.github.io/#!index.md)                                                                                                                                                                                                                                                                            |
| Shim Databases                       |                                                                                                                                                                                                                                                                       | [SDB Explorer](https://ericzimmerman.github.io/#!index.md)                                                                                                                                                                                                                                                                                  |
| SQLite Databases                     | [SQLECmd](https://ericzimmerman.github.io/#!index.md)                                                                                                                                                                                                                 | [DB Browser for SQLite](https://sqlitebrowser.org/)<br>[Navicat for SQLite](https://navicat.com/en/products/navicat-for-sqlite)<br>[SQLiteStudio](https://sqlitestudio.pl/)                                                                                                                                                                 |
| SRUM Database (ESE)                  | [SrumECmd](https://ericzimmerman.github.io/#!index.md)<br>[srum-dump](https://github.com/MarkBaggett/srum-dump)                                                                                                                                                       |                                                                                                                                                                                                                                                                                                                                             |
| SUM Database (ESE)                   | [SumECmd](https://ericzimmerman.github.io/#!index.md)                                                                                                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                             |
| Symantec AV Logs                     | [SEParser](https://github.com/Beercow/SEPparser)                                                                                                                                                                                                                      | [SEParser](https://github.com/Beercow/SEPparser)                                                                                                                                                                                                                                                                                            |
| Thumbcache                           | [Thumbcache Viewer (CMD)](https://github.com/thumbcacheviewer/thumbcacheviewer/releases/tag/v1.0.2.0)                                                                                                                                                                 | [Thumbcache Viewer](https://github.com/thumbcacheviewer/thumbcacheviewer)                                                                                                                                                                                                                                                                   |
| Volume Shadow Copies                 | [VSCMount](https://ericzimmerman.github.io/#!index.md)                                                                                                                                                                                                                | [ShadowExplorer](https://shadowexplorer.com/)                                                                                                                                                                                                                                                                                               |
| Windows Timeline                     | [WxTCmd](https://ericzimmerman.github.io/#!index.md)<br>[Windows Timeline PowerShell Scripts](https://github.com/kacos2000/WindowsTimeline)                                                                                                                           | [Clippy.exe](https://github.com/kacos2000/WindowsTimeline/releases)<br>[WindowsTimeline.exe](https://github.com/kacos2000/WindowsTimeline/releases)                                                                                                                                                                                         |
| WBEM (WMI)                           | [flare-wmi](https://github.com/mandiant/flare-wmi)<br>[PyWMIPersistenceFinder](https://github.com/davidpany/WMI_Forensics)<br>[WMIParserStr](https://github.com/AndrewRathbun/WMIParserStr)<br>[WMI-Parser](https://github.com/AndrewRathbun/WMI-Parser)              | [WMI-Explorer](https://github.com/AndrewRathbun/WMI-Explorer)                                                                                                                                                                                                                                                                               |
| Windows Defender Logs                | [DHParser](https://github.com/jklepsercyber/defender-detectionhistory-parser)                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                                                             |
| Windows Search Index Database        | [SIDR](https://github.com/strozfriedberg/sidr)<br>[WinEDB](https://github.com/kacos2000/WinEDB)                                                                                                                                                                       | [WinSearchDBAnalyzer](https://github.com/AndrewRathbun/WinSearchDBAnalyzer)<br>[WinEDB](https://github.com/kacos2000/WinEDB)                                                                                                                                                                                                                |

## Android

| DFIR Artifact     | CLI Tool(s)                                   | GUI Tools(s)                                  |
|-------------------|-----------------------------------------------|-----------------------------------------------|
| Android Artifacts | [ALEAPP](https://github.com/abrignoni/ALEAPP) | [ALEAPP](https://github.com/abrignoni/ALEAPP) |

## iOS

| DFIR Artifact     | CLI Tool(s)                                   | GUI Tools(s)                                  |
|-------------------|-----------------------------------------------|-----------------------------------------------|
| iOS Artifacts | [iLEAPP](https://github.com/abrignoni/iLEAPP) | [iLEAPP](https://github.com/abrignoni/iLEAPP) |

## macOS

| DFIR Artifact   | CLI Tool(s)                                    | GUI Tools(s) |
|-----------------|------------------------------------------------|--------------|
| macOS Artifacts | [mac_apt](https://github.com/ydkhatri/mac_apt) |              |
