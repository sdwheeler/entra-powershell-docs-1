---
external help file: Microsoft.Graph.Entra.Beta-Help.xml
Module Name: Microsoft.Graph.Entra.Beta
online version:
schema: 2.0.0
---

# Remove-EntraBetaFeatureRolloutPolicy

## Synopsis
Allows an admin to remove the policy for cloud authentication roll-out in Azure AD.

## Syntax

```
Remove-EntraBetaFeatureRolloutPolicy -Id <String> [<CommonParameters>]
```

## Description
An admin will use this cmdlet to remove the cloud authentication roll-out policy and have all users where policy applied to be free of the policy.
Users in groups that were assigned to the policy will fall back to the global authentication method (most common case will be federation).

## Examples

### Example 1: Removes the policy for cloud authentication roll-out in Azure AD.
```
PS C:\> Remove-EntraBetaFeatureRolloutPolicy -Id "7b10cf40-bc0e-46b5-9456-4520179eef5d"
```

This command removes the policy for cloud authentication roll-out in Azure AD.

## Parameters

### -Id
The unique identifier of the cloud authentication roll-out policy in Azure AD.

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

[New-EntraBetaFeatureRolloutPolicy]()

[Get-EntraBetaFeatureRolloutPolicy]()

[Set-EntraBetaFeatureRolloutPolicy]()

