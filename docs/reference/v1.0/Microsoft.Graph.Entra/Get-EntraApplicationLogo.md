---
title: Get-EntraApplicationLogo
description: This article provides details on the Get-EntraApplicationLogo command.

ms.service: active-directory
ms.topic: reference
ms.date: 03/21/2024
ms.author: eunicewaweru
ms.reviewer: stevemutungi
manager: CelesteDG
author: msewaweru

external help file: Microsoft.Graph.Entra-Help.xml
Module Name: Microsoft.Graph.Entra
online version:
schema: 2.0.0
---

# Get-EntraApplicationLogo

## SYNOPSIS
Retrieve the logo of an application.

## SYNTAX

```powershell
Get-EntraApplicationLogo 
 -ObjectId <String> 
 [-FileName <String>] 
 [-View <Boolean>] 
 [-FilePath <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The Get-EntraApplicationLogo cmdlet retrieves the logo that is set for an application.

## EXAMPLES

### Example 1
```powershell
PS C:\WINDOWS\system32> Get-EntraApplicationLogo -ObjectId 79592454-dea7-4660-9d91-f1768e5055ac
```

```output
Tag                  :
PhysicalDimension    : {Width=279, Height=390}
Size                 : {Width=279, Height=390}
Width                : 279
Height               : 390
HorizontalResolution : 96
VerticalResolution   : 96
Flags                : 77840
RawFormat            : [ImageFormat: b96b3cae-0728-11d3-9d7b-0000f81ef32e]
PixelFormat          : Format24bppRgb
Palette              : System.Drawing.Imaging.ColorPalette
FrameDimensionsList  : {7462dc86-6180-4c7e-8e3f-ee7333a7a483}
PropertyIdList       : {274, 305, 306, 36867...}
PropertyItems        : {274, 305, 306, 36867...}
```

This example shows how to retrieve the application logo for an application that is specified through the Object ID parameter.

## PARAMETERS

### -FileName
If provided, the application logo is copied to the file who's name is provided in this parameter.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -FilePath
If provided, the application logo is copied with a random filename to the file path that is specified in this parameter.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ObjectId
The ObjectID of the application for which the logo is to be retrieved.

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

### -View
If set to $true, the application's logo is displayed in a new window on the screen.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String
### System.Boolean

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS