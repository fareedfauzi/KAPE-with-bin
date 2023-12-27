# KAPE-with-bin
KAPE files with required binaries for "Module options" to accelerate live response and artifact parsing activities.

## Update
```
27-12-23:
  1. Fix PowerShell_DLL_List script
  2. Add binaries of Live Response in ./bin folder
  3. Create specific live response command for future usage (see below).
    - Exclude CrowdResponse, TDSSKiller, McAfeeStinger because of unmaintain project and its binary not available anymore
    - Exclude log4j, KernelDump, ParseScheduledTasks (Takes time parsing)
```

## Live response command
You might want to disable Loki
```
.\kape.exe --msource E:\ --mdest D:\KAPE_cases\%m --mflush --module Loki_LiveResponse,PowerShell_Get-InjectedThread,PowerShell_Get-NetworkConnection,PowerShell_Netscan,PowerShell_Signed,SIDR_WindowsIndexSearchParser,WIFIPassView,MagnetForensics_EDD,Nirsoft_BluetoothView,Nirsoft_LastActivityView,Nirsoft_OpenedFilesView,NirSoft_USBDeview,NirSoft_VideoCacheView,NirSoft_WebBrowserPassView,Nirsoft_WhatInStartup,Nirsoft_WifiHistoryView,Nirsoft_WirelessKeyView,SysInternals_Autoruns,SysInternals_Handle,SysInternals_PsFile,SysInternals_PsInfo,SysInternals_PsList,SysInternals_PsLoggedOn,SysInternals_PsService,SysInternals_PsTree,SysInternals_Tcpvcon,Powrshell_LiveResponse_SystemInfo,PowerShell_Arp_Cache_Extraction,PowerShell_Bitlocker_Key_Extraction,PowerShell_Bitlocker_Status,PowerShell_Defender_Exclusions,PowerShell_DLL_List,PowerShell_Dns_Cache,PowerShell_Local_Group_List,PowerShell_LocalAdmin,PowerShell_NamedPipes,PowerShell_NetUserAdministrators,PowerShell_Network_Configuration,PowerShell_Network_Connections_Status,PowerShell_Network_Share,PowerShell_Process_Cmdline,PowerShell_ProcessList_CimInstance,PowerShell_ProcessList_WMI,PowerShell_Services_List,PowerShell_SMBMapping,PowerShell_SMBOpenFile,PowerShell_SMBSession,PowerShell_Startup_Commands,PowerShell_User_List,PowerShell_WMIRepositoryAuditing,Windows_ARPCache,Windows_DNSCache,Windows_GpResult,Windows_IPConfig,Windows_MsInfo,Windows_nbtstat_NetBIOSCache,Windows_nbtstat_NetBIOSSessions,Windows_Net_Accounts,Windows_Net_File,Windows_Net_LocalGroup,Windows_Net_Session,Windows_Net_Share,Windows_Net_Start,Windows_Net_Use,Windows_Net_User,Windows_netsh_portproxy,Windows_NetStat,Windows_qwinsta_RDPSessions,Windows_RoutingTable,Windows_schtasks,Windows_SystemInfo,Reghunter --gui
```
