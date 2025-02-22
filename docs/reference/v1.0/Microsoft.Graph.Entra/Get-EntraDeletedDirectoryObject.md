---
title: Get-EntraDeletedDirectoryObject
description: This article provides details on the Get-EntraDeletedDirectoryObject command.

ms.service: entra
ms.topic: reference
ms.date: 06/26/2024
ms.author: eunicewaweru
ms.reviewer: stevemutungi
manager: CelesteDG

external help file: Microsoft.Graph.Entra-Help.xml
Module Name: Microsoft.Graph.Entra
online version:
schema: 2.0.0
---

# Get-EntraDeletedDirectoryObject

## Synopsis

This cmdlet is used to retrieve a soft deleted directory object from the directory.

## Syntax

```powershell
Get-EntraDeletedDirectoryObject 
 -Id <String> 
 [<CommonParameters>]
```

## Description

This cmdlet is used to retrieve a soft deleted directory object from the directory.
Soft delete for groups is currently only implemented for Unified Groups (also known as
Office 365 Groups).

## Examples

### Example 1: Retrieve a deleted directory object.

```powershell
Connect-Entra -Scopes 'AdministrativeUnit.Read.All', 'Application.Read.All','Group.Read.All','User.Read.All'
Get-EntraDeletedDirectoryObject -Id 'aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb'
```

```output
Id                                   DeletedDateTime
--                                   ---------------
aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb 2/2/2024 5:33:56 AM
```

This example shows how to retrieve the deleted directory object with `Id` `aaaaaaaa-0000-1111-2222-bbbbbbbbbbbb` from the directory

## Parameters

### -Id

The Id of the directory object to retrieve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: `-Debug`, `-ErrorAction`, `-ErrorVariable`, `-InformationAction`, `-InformationVariable`, `-OutVariable`, `-OutBuffer`, `-PipelineVariable`, `-Verbose`, `-WarningAction`, and `-WarningVariable`. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## Inputs

## Outputs

### System.Object

## Notes

## Related Links
