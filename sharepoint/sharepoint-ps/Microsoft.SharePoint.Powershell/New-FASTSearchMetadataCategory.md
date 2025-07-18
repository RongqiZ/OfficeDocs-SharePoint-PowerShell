---
external help file: sharepointserver.xml
Module Name: Microsoft.SharePoint.Powershell
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/new-fastsearchmetadatacategory
applicable: FAST Server for SharePoint 2010
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
title: New-FASTSearchMetadataCategory
---

# New-FASTSearchMetadataCategory

## SYNOPSIS
Creates a new category for crawled properties.

## SYNTAX

```
New-FASTSearchMetadataCategory -Name <String> -Propset <Guid> [<CommonParameters>]
```

## DESCRIPTION
This cmdlet creates a new category for crawled properties.
A category is identified by its name and its property set global unique identifier (GUID).

All crawled properties that are members of a category share the same property set GUID as the category.

For permissions and the most current information about FAST Search Server 2010 for SharePoint cmdlets, see the online documentation, (https://go.microsoft.com/fwlink/?LinkId=163227).

## EXAMPLES

### EXAMPLE 1 (FAST Server for SharePoint 2010)
```
C:\PS>$guid = [guid]::NewGuid()
New-FASTSearchMetadataCategory -Name ExampleCategory -Propset $guid
```

This example creates a category named "ExampleCategory" with a new GUID generated by the system.
New crawled properties can then be mapped to this category by specifying the GUID when calling New-FASTSearchMetadataCrawledProperty or Set-FASTSearchMetadataCrawledProperty.

See Set-FASTSearchMetadataCategory for descriptions of category properties.

## PARAMETERS

### -Name

> Applicable: FAST Server for SharePoint 2010

The name of the new category.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Propset

> Applicable: FAST Server for SharePoint 2010

The property set Global Unique Identifier (GUID) assigned to this category.
A GUID is a 128-bit integer that has a very low probability of being duplicated.
The GUID can be specified either in the form of a System.Guid object, or as a 128-bit integer with the format "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx".
A crawled property can only be mapped to one category at a time.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-FASTSearchMetadataCategory](Get-FASTSearchMetadataCategory.md)

[Remove-FASTSearchMetadataCategory](Remove-FASTSearchMetadataCategory.md)

[Set-FASTSearchMetadataCategory](Set-FASTSearchMetadataCategory.md)

[New-FASTSearchMetadataCrawledProperty](New-FASTSearchMetadataCrawledProperty.md)

[Set-FASTSearchMetadataCrawledProperty](Set-FASTSearchMetadataCrawledProperty.md)
