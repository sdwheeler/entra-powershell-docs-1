---
title: Set-EntraDirSyncConfiguration
description: This article provides details on the Set-EntraDirSyncConfiguration command.

ms.service: entra
ms.topic: reference
ms.date: 06/26/2024
ms.author: eunicewaweru
ms.reviewer: stevemutungi
manager: CelesteDG
author: msewaweru

external help file: Microsoft.Graph.Entra-help.xml
Module Name: Microsoft.Graph.Entra
online version:
schema: 2.0.0
---

# Set-EntraDirSyncConfiguration

## Synopsis
Modifies the directory synchronization settings.

## Syntax

```powershell
Set-EntraDirSyncConfiguration 
 -AccidentalDeletionThreshold <UInt32>
 [-Force]
 [-TenantId <Guid>]
 [<CommonParameters>]
```

## Description
The Set-EntraDirSyncConfiguration cmdlet modifies the directory synchronization settings.

## Examples

### Example 1: Set directory synchronization settings
```powershell
PS C:\> Set-EntraDirSyncConfiguration -AccidentalDeletionThreshold 600 -Force
```

This command sets directory synchronization settings.

### Example 2: Set directory synchronization settings by TenantId
```powershell
PS C:\> Set-EntraDirSyncConfiguration -AccidentalDeletionThreshold 600 -TenantId "d5aec55f-2d12-4442-8d2f-ccca95d4390e" -Force
```

This command sets directory synchronization settings by TenantId.

## Parameters

### -AccidentalDeletionThreshold
Specifies the accidental deletion threshold.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Forces the command to run without asking for user confirmation.

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

### -TenantId
Specifies the unique ID of the tenant on which to perform the operation. The default value is the tenant of the current user. This parameter applies only to partner users.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## Inputs

### System.UInt32

### System.Guid

## Outputs

### System.Object
## Notes

## Related Links

[Get-EntraDirSyncConfiguration](Get-EntraDirSyncConfiguration.md)