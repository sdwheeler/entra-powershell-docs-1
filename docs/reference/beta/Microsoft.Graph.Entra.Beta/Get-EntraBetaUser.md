---
external help file: Microsoft.Graph.Entra.Beta-Help.xml
Module Name: Microsoft.Graph.Entra.Beta
online version:
schema: 2.0.0
---

# Get-EntraBetaUser

## Synopsis
Gets a user.

## Syntax

### GetQuery (Default)
```
Get-EntraBetaUser [-Filter <String>] [-All] [-Top <Int32>] [<CommonParameters>]
```

### GetVague
```
Get-EntraBetaUser [-SearchString <String>] [-All] [<CommonParameters>]
```

### GetById
```
Get-EntraBetaUser -ObjectId <String> [-All] [<CommonParameters>]
```

## Description
The Get-EntraBetaUser cmdlet gets a user from Azure Active Directory (AD).

## Examples

### Example 1: Get ten users
```
PS C:\>Get-EntraBetaUser -Top 10
```

This command gets ten users.

### Example 2: Get a user by ID
```
PS C:\>Get-EntraBetaUser -ObjectId "testUpn@tenant.com"
```

This command gets the specified user.

### Example 3: Search among retrieved users
```
PS C:\> Get-EntraBetaUser -SearchString "New"

ObjectId                             DisplayName UserPrincipalName                   UserType
--------                             ----------- -----------------                   --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    NewUser@contoso.onmicrosoft.com     Member
2b450b8e-1db6-42cb-a545-1b05eb8a358b New user    NewTestUser@contoso.onmicrosoft.com Member
```

This cmdlet gets all users that match the value of SearchString against the first characters in DisplayName or UserPrincipalName .

### Example 4: Get a user by userPrincipalName
```
PS C:\>Get-EntraBetaUser -Filter "userPrincipalName eq 'jondoe@contoso.com'"
```

This command gets the specified user.

### Example 5: Get a user by userPrincipalName
```
PS C:\>Get-EntraBetaUser -Filter "startswith(Title,'Sales')"
```

This command gets all the users whos title starts with sales.
ie Sales Manager and Sales Assistant.

## Parameters

### -All
List all pages.

```yaml
Type: SwitchParameter
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
Details on querying with oData can be found here.
https://www.odata.org/documentation/odata-version-3-0/odata-version-3-0-core-protocol/#queryingcollections

```yaml
Type: String
Parameter Sets: GetQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ObjectId
Specifies the ID (as a UPN or ObjectId) of a user in Azure AD.

```yaml
Type: String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -SearchString
Specifies a search string.

```yaml
Type: String
Parameter Sets: GetVague
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Top
Specifies the maximum number of records to return.

```yaml
Type: Int32
Parameter Sets: GetQuery
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

[New-EntraBetaUser]()

[Remove-EntraBetaUser]()

[Set-EntraBetaUser]()

