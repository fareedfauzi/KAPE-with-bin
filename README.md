# KAPE-with-bin
KAPE files with required binaries for "Module options" to accelerate live response and artifact parsing activities.

## Update
```
27-12-23:
  1. Fix PowerShell_DLL_List script
  2. Add binaries of Live Response in ./bin folder
  3. Generate specific live response command for future usage (see below).
    - Exclude CrowdResponse, TDSSKiller, McAfeeStinger because of unmaintain project and its binary not available anymore
    - Exclude log4j, KernelDump, ParseScheduledTasks (Takes time parsing)
  4. Generate offline artifact parsing
```

## Live response command
You might want to disable Loki
```
.\kape.exe --msource E:\ --mdest D:\KAPE_cases\%m --mflush --module Thor-Lite_LiveResponse,PowerShell_Get-InjectedThread,PowerShell_Get-NetworkConnection,PowerShell_Netscan,PowerShell_Signed,SIDR_WindowsIndexSearchParser,WIFIPassView,MagnetForensics_EDD,Nirsoft_BluetoothView,Nirsoft_LastActivityView,Nirsoft_OpenedFilesView,NirSoft_USBDeview,NirSoft_VideoCacheView,NirSoft_WebBrowserPassView,Nirsoft_WhatInStartup,Nirsoft_WifiHistoryView,Nirsoft_WirelessKeyView,SysInternals_Autoruns,SysInternals_Handle,SysInternals_PsFile,SysInternals_PsInfo,SysInternals_PsList,SysInternals_PsLoggedOn,SysInternals_PsService,SysInternals_PsTree,SysInternals_Tcpvcon,Powrshell_LiveResponse_SystemInfo,PowerShell_Arp_Cache_Extraction,PowerShell_Bitlocker_Key_Extraction,PowerShell_Bitlocker_Status,PowerShell_Defender_Exclusions,PowerShell_DLL_List,PowerShell_Dns_Cache,PowerShell_Local_Group_List,PowerShell_LocalAdmin,PowerShell_NamedPipes,PowerShell_NetUserAdministrators,PowerShell_Network_Configuration,PowerShell_Network_Connections_Status,PowerShell_Network_Share,PowerShell_Process_Cmdline,PowerShell_ProcessList_CimInstance,PowerShell_ProcessList_WMI,PowerShell_Services_List,PowerShell_SMBMapping,PowerShell_SMBOpenFile,PowerShell_SMBSession,PowerShell_Startup_Commands,PowerShell_User_List,PowerShell_WMIRepositoryAuditing,Windows_ARPCache,Windows_DNSCache,Windows_GpResult,Windows_IPConfig,Windows_MsInfo,Windows_nbtstat_NetBIOSCache,Windows_nbtstat_NetBIOSSessions,Windows_Net_Accounts,Windows_Net_File,Windows_Net_LocalGroup,Windows_Net_Session,Windows_Net_Share,Windows_Net_Start,Windows_Net_Use,Windows_Net_User,Windows_netsh_portproxy,Windows_NetStat,Windows_qwinsta_RDPSessions,Windows_RoutingTable,Windows_schtasks,Windows_SystemInfo,Reghunter --gui

.\kape.exe --msource E:\ --mdest D:\KAPE_cases --module Thor-Lite_Upgrade,Thor-Lite_LiveResponse --gui

.\kape.exe --msource E:\ --mdest D:\KAPE_cases --module Loki_LiveResponse --gui
```

## Offline artifact parsing
```
.\kape.exe --msource E:\ --mdest D:\KAPE_cases\%m --module Loki_Scan,DensityScout,BackstageParser,BitsParser,CCMRUAFinder_RecentlyUsedApps,Chainsaw,DeepblueCLI,DHParser,EvtxHussar,hasherezade_HollowsHunter,INDXRipper,LevelDBDumper,OneDriveExplorer,PowerShell_Get-ChainsawSigmaRules,TeamsParser,ThumbCacheViewer,WMI-Parser,Zircolite_Scan,Zircolite_Update,LogParser_ApacheAccessLogs,LogParser_DetailedNetworkShareAccess,LogParser_LogonLogoffEvents,LogParser_RDPUsageEvents,LogParser_SMBServerAnonymousLogons,Nirsoft_AlternateStreamView,NirSoft_BrowsingHistoryView,NirSoft_FullEventLogView_AllEventLogs,NirSoft_FullEventLogView_Application,NirSoft_FullEventLogView_PowerShell-Operational,NirSoft_FullEventLogView_PrintService-Operational,NirSoft_FullEventLogView_ScheduledTasks,NirSoft_FullEventLogView_Security,NirSoft_FullEventLogView_System,NirSoft_TurnedOnTimesView,NirSoft_WebBrowserDownloads,Nirsoft_WinLogonView,SysInternals_SigCheck,TZWorks_CAFAE_Registry_System,Events-Ripper,Hayabusa,LogParser,MFTECmd,NTFSLogTracker,RECmd_AllBatchFiles,Reghunter,RegRipper,AmcacheParser,AppCompatCacheParser,EvtxECmd,EvtxECmd_RDP,iisGeoLocate,JLECmd,LECmd,PECmd,RBCmd,RecentFileCacheParser,SBECmd,SQLECmd,SQLECmd_Hunt,SrumECmd,SumECmd,WxTCmd,Sync_EvtxECmd,Sync_KAPE,Sync_RECmd,Sync_SQLECmd,Windows_ManageBDE_BitLockerKeys,Windows_ManageBDE_BitLockerStatus --gui
```

## Scanning command
```
.\kape.exe --msource E:\ --mdest D:\KAPE_cases --module Thor-Lite_Upgrade,Thor-Lite_Scan --gui
.\kape.exe --msource E:\ --mdest D:\KAPE_cases --module Loki_Scan --gui
```
