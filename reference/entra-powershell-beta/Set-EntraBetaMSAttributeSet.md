---
title: Set-EntraBetaMSAttributeSet.
description: This article provides details regarding the Set-EntraBetaMSAttributeSet command.

ms.service: active-directory
ms.topic: reference
ms.date: 11/20/2023
ms.author: eunicewaweru
ms.reviewer: stevemutungi
manager: CelesteDG
---

# Set-EntraBetaMSAttributeSet

Reference

Module: **Microsoft.Graph.Entra.Beta**

## SYNOPSIS

Updates an existing attribute set.

## SYNTAX

```powershell
Set-EntraBetaMSAttributeSet 
-Id <String>
[-Description <String>]
[-MaxAttributesPerSet <Int32>]
[<CommonParameters>]
```

## DESCRIPTION

Updates a Microsoft Entra ID attribute set object identified by ID.

## PERMISSIONS

|Permission type|Least privileged permissions|Higher privileged permissions|
|:---|:---|:---|
|Delegated (work or school account)|CustomSecAttributeDefinition.ReadWrite.All|Not available.|
|Delegated (personal Microsoft account)|Not supported.|Not supported.|
|Application|CustomSecAttributeDefinition.ReadWrite.All|Not available.|

## EXAMPLES

### Example 1: Update an attribute set
  
```powershell
 Set-EntraBetaMSAttributeSet -Id "Engineering" -Description "Attributes for cloud engineering team"
```

This example Update an attribute set.

- Attribute set: `Engineering`

### Example 2: Update a Maximum number of custom security attributes

```powershell
Set-EntraBetaMSAttributeSet -Id "Engineering" -MaxAttributesPerSet 20
```

This example updates the maximum number of custom security attributes.

- Attribute set: `Engineering`

## PARAMETERS

### -Description

Description for the attribute set.

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

### -Id

Name of the attribute set.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -MaxAttributesPerSet

Maximum number of custom security attributes that can be defined in the attribute set.

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

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## RELATED LINKS

- Get-EntraBetaMSAttributeSet
- [New-EntraBetaMSAttributeSet](./New-EntraBetaMSAttributeSet.md)