---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spotenantcdnpolicies
applicable: SharePoint Online
title: Get-SPOTenantCdnPolicies
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Get-SPOTenantCdnPolicies

## SYNOPSIS

Get the public or private Policies applied on your SharePoint Online Tenant. Requires Tenant administrator permissions.

## SYNTAX

```
Get-SPOTenantCdnPolicies -CdnType <SPOTenantCdnType> [<CommonParameters>]
```

## DESCRIPTION

This cmdlet gets the public or private policies applied to a SharePoint Online organization tenant.

## EXAMPLES

### Example 1

```powershell
Get-SPOTenantCdnPolicies -CdnType Public
```

This example returns public CDN policies of your tenant.

### Example 2

```powershell
Get-SPOTenantCdnPolicies -CdnType Private
```

This example returns private CDN policies of your tenant.

## PARAMETERS

### -CdnType

> Applicable: SharePoint Online

Type of CDN on the current SPO Tenant (Public,Private)

```yaml
Type: Microsoft.Online.SharePoint.TenantAdministration.SPOTenantCdnType
Parameter Sets: (All)
Aliases:
Accepted values: Public, Private

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Get-SPOAppErrors](Get-SPOAppErrors.md)

[Set-SPOTenantCdnEnabled](Set-SPOTenantCdnEnabled.md)
