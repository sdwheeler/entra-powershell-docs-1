---
title: New-EntraApplicationKeyCredential
description: This article provides details on the New-EntraApplicationKeyCredential command.

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

# New-EntraApplicationKeyCredential

## Synopsis
Creates a key credential for an application.

## Syntax

```powershell
New-EntraApplicationKeyCredential 
 -ObjectId <String>
 [-CustomKeyIdentifier <String>] 
 [-Type <KeyType>] 
 [-Usage <KeyUsage>]
 [-Value <String>] 
 [-EndDate <DateTime>] 
 [-StartDate <DateTime>]
 [<CommonParameters>]
```

## Description
The New-EntraApplicationKeyCredential cmdlet creates a key credential for an application.

## Examples

### Example 1: Create a new application key credential
```powershell
PS C:\> $AppID = (Get-EntraApplication -Top 1).Objectid
PS C:\> New-EntraApplicationKeyCredential -ObjectId $AppId -CustomKeyIdentifier "Test" -StartDate "11/7/2016" -Type "Symmetric" -Usage "Sign" -Value "123"
```

```output
CustomKeyIdentifier : {84, 101, 115, 116}
EndDate             : 11/7/2017 12:00:00 AM
KeyId               : a5845538-3f67-402d-a03e-36d768f1441e
StartDate           : 11/7/2016 12:00:00 AM
Type                : Symmetric
Usage               : Sign
Value               : {49, 50, 51}
```

The first command gets the ID of an application by using the [Get-EntraApplication](./Get-EntraApplication.md) cmdlet.
The command stores it in the $AppId variable.  

The second command creates the application key credential for the application identified by $AppId.

### Example 2: Use a certificate to add an application key credential
```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2 #create a new certificate object
PS C:\> $cer.Import("C:\Users\PFuller\Desktop\abc.cer") 
PS C:\> $bin = $cer.GetRawCertData()
PS C:\> $base64Value = [System.Convert]::ToBase64String($bin)
PS C:\> $bin = $cer.GetCertHash()
PS C:\> $base64Thumbprint = [System.Convert]::ToBase64String($bin)
PS C:\> $keyid = [System.Guid]::NewGuid().ToString() 
PS C:\> New-EntraApplicationKeyCredential -ObjectId 009d786a-3503-4217-b8ab-db03d71c179a -CustomKeyIdentifier  $base64Thumbprint  -Type AsymmetricX509Cert -Usage Verify -Value $base64Value  -StartDate $cer.GetEffectiveDateString() -EndDate cer.GetExpirationDateString()
```

The first seven commands create values for the application key credential and store them in variables.  

The final command uses a certificate to add an application key credential.

## Parameters

### -CustomKeyIdentifier
Specifies a custom key ID.

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

### -EndDate
Specifies the time when the key becomes invalid as a DateTime object.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ObjectId
Specifies a unique ID of an application in Microsoft Entra ID.

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

### -StartDate
Specifies the time when the key becomes valid as a DateTime object.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Type
Specifies the type of the key.

```yaml
Type: KeyType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Usage
Specifies the key usage.

```yaml
Type: KeyUsage
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Value
Specifies the value for the key.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## Inputs

## Outputs

## Notes

## Related Links

[Get-EntraApplication](Get-EntraApplication.md)

[Get-EntraApplicationKeyCredential](Get-EntraApplicationKeyCredential.md)

[Remove-EntraApplicationKeyCredential](Remove-EntraApplicationKeyCredential.md)

[This cmdlet uses the ADAL library in Microsoft Entra ID. To learn more about ADAL, please follow this link:](https://www.cloudidentity.com/blog/2013/09/12/active-directory-authentication-library-adal-v1-for-net-general-availability/)

