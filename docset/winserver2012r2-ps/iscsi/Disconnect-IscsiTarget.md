---
external help file: iSCSITarget.cdxml-help.xml
Module Name: iSCSI
online version: 
schema: 2.0.0
title: Disconnect-IscsiTarget
description: 
keywords: powershell, cmdlet
author: brianlic
manager: alanth
ms.date: 2017-10-29
ms.topic: reference
ms.prod: powershell
ms.technology: powershell
ms.assetid: C6D1C713-F3D8-4BC2-9DDC-B2FD87E0C025
---

# Disconnect-IscsiTarget

## SYNOPSIS
Disconnects sessions to the specified iSCSI target object.

## SYNTAX

### ByNodeAddress (Default)
```
Disconnect-IscsiTarget [-NodeAddress <String[]>] [-SessionIdentifier <String>] [-CimSession <CimSession[]>]
 [-ThrottleLimit <Int32>] [-AsJob] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject (cdxml)
```
Disconnect-IscsiTarget -InputObject <CimInstance[]> [-SessionIdentifier <String>] [-CimSession <CimSession[]>]
 [-ThrottleLimit <Int32>] [-AsJob] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Disconnect-IscsiTarget** cmdlet disconnects a connected iSCSI target.
To view connected iSCSI targets, use the Get-iSCSITarget cmdlet.

## EXAMPLES

### EXAMPLE 1
```
PS C:\> Get-IscsiTarget
IsConnected NodeAddress 
----------- ----------- 
True iqn.1991-05.com.contoso:testiscsi-deepcore-target
PS C:\> $Tar = Get-IscsiTarget
PS C:\> Disconnect-IscsiTarget -NodeAddress $Tar.NodeAddress
Confirm 
Are you sure you want to perform this action? 
Performing operation '' on Target ''.
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): **Y**
```

This example collects information about a connected iSCSI target, and then using that information to run this cmdlet.

## PARAMETERS

### -AsJob
ps_cimcommon_asjob

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CimSession
Runs the cmdlet in a remote session or on a remote computer.
Enter a computer name or a session object, such as the output of a New-CimSessionhttp://go.microsoft.com/fwlink/p/?LinkId=227967 or Get-CimSessionhttp://go.microsoft.com/fwlink/p/?LinkId=227966 cmdlet.
The default is the current session on the local computer.

```yaml
Type: CimSession[]
Parameter Sets: (All)
Aliases: Session

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Accepts an object from the pipeline as input.

```yaml
Type: CimInstance[]
Parameter Sets: InputObject (cdxml)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NodeAddress
Represents the IQN of the discovered target.

```yaml
Type: String[]
Parameter Sets: ByNodeAddress
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Sends items from the interactive window down the pipeline as input to other cmdlets.
By default, this cmdlet does not generate any output. 
                         
To send items from the interactive window down the pipeline, click to select the items and then click OK.
Shift-click and Ctrl-click are supported.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SessionIdentifier
Specifies the session identifier.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThrottleLimit
Specifies the maximum number of concurrent operations that can be established to run the cmdlet.
If this parameter is omitted or a value of `0` is entered, then Windows PowerShell� calculates an optimum throttle limit for the cmdlet based on the number of CIM cmdlets that are running on the computer.
The throttle limit applies only to the current cmdlet, not to the session or to the computer.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### None

## NOTES

## RELATED LINKS

[iSCSI on TechNet](http://www.microsoft.com/iSCSI)

[Storage on TechNet](http://go.microsoft.com/fwlink/?linkid=191356)

[Get-iSCSITarget](./Get-IscsiTarget.md)

