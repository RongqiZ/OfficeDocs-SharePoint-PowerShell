---
external help file: Microsoft.Office.Server.Search.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/get-spenterprisesearchserviceinstance
applicable: SharePoint Server Subscription Edition
title: Get-SPEnterpriseSearchServiceInstance
schema: 2.0.0
---

# Get-SPEnterpriseSearchServiceInstance

## SYNOPSIS
Returns the search service instance for a farm.

## SYNTAX

```
Get-SPEnterpriseSearchServiceInstance [[-Identity] <SearchServiceInstancePipeBind>]
 [-AssignmentCollection <SPAssignmentCollection>] [-Local] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet returns the SearchServiceInstance object when the object is created, updated, or deleted.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE 1
```powershell
Get-SPEnterpriseSearchServiceInstance -Local
```

This example obtains a reference to the local search service instance.

### EXAMPLE 2
```powershell
Get-SPEnterpriseSearchServiceInstance | ?{$_.Server -match 'SP01'}
```

This example obtains a reference to the search service instance on the SharePoint server named 'SP01'.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the search service instance to return.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a query server (for example, MyQueryServer); or an instance of a valid SearchServiceInstance object.

```yaml
Type: SearchServiceInstancePipeBind
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AssignmentCollection

> Applicable: SharePoint Server Subscription Edition

Manages objects for the purpose of proper disposal. Use of objects, such as SPWeb or SPSite, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the SPAssignment object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When SPWeb, SPSite, or SPSiteAdministration objects are used, the objects are automatically disposed of if an assignment collection or the Global parameter is not used.

When the Global parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the Stop-SPAssignment command, an out-of-memory scenario can occur.

```yaml
Type: SPAssignmentCollection
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Local

> Applicable: SharePoint Server Subscription Edition

Returns the search service instance for the current search server.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
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
