---
external help file: Microsoft.Graph.Entra.Beta-Help.xml
Module Name: Microsoft.Graph.Entra.Beta
online version:
schema: 2.0.0
---

# Set-EntraBetaUserManager

## Synopsis
Updates a user's manager.

## Syntax

```
Set-EntraBetaUserManager -ObjectId <String> -RefObjectId <String> [<CommonParameters>]
```

## Description
The Set-EntraBetaUserManager cmdlet update the manager for a user in Azure Active Directory (AD).

## Examples

### Example 1: Update a user's manager
```
PS C:\>Set-EntraBetaUserManager -ObjectId "df19e8e6-2ad7-453e-87f5-037f6529ae16" -RefObjectId "df19e8e6-2ad7-453e-87f5-037f6529ae16"
```

This command update's the manager for the specified user.

## Parameters

### -ObjectId
Specifies the ID (as a UPN or ObjectId) of a user in Azure AD.

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

### -RefObjectId
Specifies the ID of the Azure AD object to assign as owner/manager/member.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## Inputs

## Outputs

## Notes

## Related Links

[Get-EntraBetaUserManager]()

[Remove-EntraBetaUserManager]()

