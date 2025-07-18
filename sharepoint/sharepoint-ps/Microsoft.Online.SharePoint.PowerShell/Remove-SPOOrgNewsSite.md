---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/remove-spoorgnewssite
applicable: SharePoint Online
title: Remove-SPOOrgNewsSite
schema: 2.0.0
author: trent-green
ms.author: trgreen
---

# Remove-SPOOrgNewsSite

## SYNOPSIS

Removes a given site from the list of organizational news sites based on its URL in your SharePoint Online Tenant

## SYNTAX

```
Remove-SPOOrgNewsSite -OrgNewsSiteUrl <String> [<CommonParameters>]
```

## DESCRIPTION

This cmdlet will remove a site from list of organizational news sites based on its URL.

## EXAMPLES

### EXAMPLE 1

```powershell
Remove-SPOOrgNewsSite -OrgNewsSiteUrl https://contoso.sharepoint.com/sites/Marketing
```

This example removes <https://contoso.sharepoint.com/sites/Marketing> from the list of organizational news sites.

## PARAMETERS

### -OrgNewsSiteUrl

> Applicable: SharePoint Online

The URL of a site to be marked as an organizational news site.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

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

[Get-SPOOrgNewsSite](Get-SPOOrgNewsSite.md)

[Set-SPOOrgNewsSite](Set-SPOOrgNewsSite.md)
