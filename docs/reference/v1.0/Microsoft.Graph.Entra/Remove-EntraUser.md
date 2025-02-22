---
title: Remove-EntraUser
description: This article provides details on the Remove-EntraUser command.

ms.service: entra
ms.topic: reference
ms.date: 06/26/2024
ms.author: eunicewaweru
ms.reviewer: stevemutungi
manager: CelesteDG
author: msewaweru

external help file: Microsoft.Graph.Entra-Help.xml
Module Name: Microsoft.Graph.Entra
online version:
schema: 2.0.0
---

# Remove-EntraUser

## Synopsis

Removes a user.

## Syntax

```powershell
Remove-EntraUser 
 -ObjectId <String>
 [<CommonParameters>]
```

## Description

The Remove-EntraUser cmdlet removes a user in Microsoft Entra ID.

The calling user must be assigned at least one of the following Microsoft Entra roles:

- User Administrator

- Privileged Authentication Administrator

## Examples

### Example 1: Remove a user

```powershell
Connect-Entra -Scopes 'User.ReadWrite.All'
Remove-EntraUser -ObjectId 'SawyerM@Contoso.com'
```

This command removes the specified user in Microsoft Entra ID.

## Parameters

### -ObjectId

Specifies the ID of a user (as a UPN or ObjectId) in Microsoft Entra ID.

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

## Notes

## Related Links

[Get-EntraUser](Get-EntraUser.md)

[New-EntraUser](New-EntraUser.md)

[Set-EntraUser](Set-EntraUser.md)
