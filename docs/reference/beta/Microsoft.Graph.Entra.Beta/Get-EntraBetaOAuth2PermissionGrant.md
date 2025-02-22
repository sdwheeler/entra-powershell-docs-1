---
external help file: Microsoft.Graph.Entra.Beta-Help.xml
Module Name: Microsoft.Graph.Entra.Beta
online version:
schema: 2.0.0
---

# Get-EntraBetaOAuth2PermissionGrant

## Synopsis
Gets OAuth2PermissionGrant entities.

## Syntax

```
Get-EntraBetaOAuth2PermissionGrant [-Top <Int32>] [-All] [<CommonParameters>]
```

## Description
The Get-EntraBetaOAuth2PermissionGrant cmdlet gets OAuth2PermissionGrant entities in Azure Active Directory (AD).

## Examples

### Example 1: Get the OAuth2 permission grants
```
PS C:\> Get-EntraBetaOAuth2PermissionGrant

ObjectId                                                         ResourceId                           Scope
--------                                                         ----------                           -----
c-AY9qPNx0-4vVrWPxmED3iGICfrJnZDi2Jsj7SIpfXm6Bnf1yo-RYf1A39lKa4W 27208678-26eb-4376-8b62-6c8fb488a5f5 UserProfile.Read
aPlw7ew41kiuWN7P6Av9X3iGICfrJnZDi2Jsj7SIpfV-R0UdFU0WTZ2ut7ZkWFvD 27208678-26eb-4376-8b62-6c8fb488a5f5 User.Read Directory.AccessAsUser.All
aPlw7ew41kiuWN7P6Av9X3iGICfrJnZDi2Jsj7SIpfXm6Bnf1yo-RYf1A39lKa4W 27208678-26eb-4376-8b62-6c8fb488a5f5 UserProfile.Read user_impersonation
WUarNRz2dUqY0u8dBKwglXiGICfrJnZDi2Jsj7SIpfXm6Bnf1yo-RYf1A39lKa4W 27208678-26eb-4376-8b62-6c8fb488a5f5 User.Read
rbzRnQl5W0C0TpzshPS41HiGICfrJnZDi2Jsj7SIpfU                      27208678-26eb-4376-8b62-6c8fb488a5f5 User.Read
Qp3O0EPJoUOgsLHe2NDOPXiGICfrJnZDi2Jsj7SIpfXm6Bnf1yo-RYf1A39lKa4W 27208678-26eb-4376-8b62-6c8fb488a5f5 User.Read
Qp3O0EPJoUOgsLHe2NDOPUD-XnoDbmtOmpMPVcQFKs7m6Bnf1yo-RYf1A39lKa4W 7a5efe40-6e03-4e6b-9a93-0f55c4052ace MailboxSettings.ReadWrite Files.ReadWrite Files.Read profile email Tasks.ReadWrite Notes.Re...
tCNicMsr30C8E6LrHPvvNniGICfrJnZDi2Jsj7SIpfU                      27208678-26eb-4376-8b62-6c8fb488a5f5 User.Read
tCNicMsr30C8E6LrHPvvNl0FVbgdl8pHjyd2jlKSaDM                      b855055d-971d-47ca-8f27-768e52926833 AllSites.Read
mK8RroiOPk6Yt1owm-5d_HiGICfrJnZDi2Jsj7SIpfU                      27208678-26eb-4376-8b62-6c8fb488a5f5 User.Read
p4wNLtFXh0qcKrNjikytv3iGICfrJnZDi2Jsj7SIpfU                      27208678-26eb-4376-8b62-6c8fb488a5f5 Directory.ReadWrite.All User.Read
p4wNLtFXh0qcKrNjikytv0D-XnoDbmtOmpMPVcQFKs4                      7a5efe40-6e03-4e6b-9a93-0f55c4052ace Directory.ReadWrite.All
```

This command gets the OAuth2 permission grants.

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

### -Top
Specifies the maximum number of records to return.

```yaml
Type: Int32
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

[Remove-EntraBetaOAuth2PermissionGrant]()