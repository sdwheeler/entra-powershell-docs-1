---
title: Get-EntraContract
description: This article provides details on the Get-EntraContract command.

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

# Get-EntraContract

## Synopsis

Gets a contract.

## Syntax

### GetQuery (Default)

```powershell
Get-EntraContract 
 [-Top <Int32>] 
 [-All] 
 [-Filter <String>] 
 [<CommonParameters>]
```

### GetById

```powershell
Get-EntraContract 
 -ObjectId <String> 
 [-All] 
 [<CommonParameters>]
```

## Description

The `Get-EntraContract` cmdlet gets a contract information associated to a partner tenant.

The contract object contains the following attributes:

- `contractType` - type of the contract.

Possible values are:  

++ "SyndicationPartner", which indicates a partner that exclusively resells and manages O365 and Intune for this customer.
They resell and support their customers.
++ "BreadthPartner", which indicates that the partner has the ability to provide administrative support for this customer.
However the partner isn't allowed to resell to the customer.
++ "ResellerPartner", which indicates a partner that is similar to a syndication partner, except that it doesn't have exclusive access to a tenant.
In the syndication case, the customer can't buy additional direct subscriptions from Microsoft or from other partners.

- `customerContextId` - unique identifier for the customer tenant referenced by this partnership.

Corresponds to the ObjectId property of the customer tenant's TenantDetail object.

- `defaultDomainName` - a copy of the customer tenant's default domain name.
The copy is made when the partnership with the customer is established.
It isn't automatically updated if the customer tenant's default domain name changes.

- `deletionTimestamp` - this property isn't valid for contracts and always returns null.

- `displayName` - a copy of the customer tenant's display name.
The copy is made when the partnership with the customer is established.
It isn't automatically updated if the customer tenant's display name changes.

- `objectType` - a string that identifies the object type. The value is always `Contract`.

- `ObjectId` - the unique identifier for the partnership.

## Examples

### Example 1: Get all contracts

```powershell
Connect-Entra -Scopes 'Directory.Read.All'
Get-EntraContract
```

This command gets all contracts in the Microsoft Entra ID.

## Parameters

### -All

List all pages.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Filter

Specifies an oData v3.0 filter statement.
This parameter controls which objects are returned.

```yaml
Type: System.String
Parameter Sets: GetQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ObjectId

Specifies the ID of a contract.

```yaml
Type: System.String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Top

Specifies the maximum number of records to return.

```yaml
Type: System.Int32
Parameter Sets: GetQuery
Aliases:

Required: False
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
