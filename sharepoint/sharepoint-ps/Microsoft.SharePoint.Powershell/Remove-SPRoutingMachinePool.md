---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
Module Name: Microsoft.SharePoint.Powershell
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/remove-sproutingmachinepool
applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019
title: Remove-SPRoutingMachinePool
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# Remove-SPRoutingMachinePool

## SYNOPSIS
Removes a routing pool from Request Manager.

## SYNTAX

```
Remove-SPRoutingMachinePool [-Identity] <SPRoutingMachinePoolPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [<CommonParameters>]
```

## DESCRIPTION
Use the `Remove-SPRoutingMachinePool` cmdlet to remove a routing pool from the Request Manager object by using the Identity parameter.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```
C:\PS>$web=Get-SPWebApplication -Identity <URL of web application>

C:\PS>$rm=Get-SPRequestManagementSettings -Identity $web

C:\PS>$pool=Get-SPRoutingMachinePool -RequestManagementSettings $rm

Remove-SPRoutingMachinePool -Identity $pool
```

This example removes a routing pool for the specified identity by using the $pool variable.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the Request Manager object to remove.

```yaml
Type: SPRoutingMachinePoolPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AssignmentCollection

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Manages objects for the purpose of proper disposal.
Use of objects, such as SPWeb or SPSite, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management.
Using the SPAssignment object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory.
When SPWeb, SPSite, or SPSiteAdministration objects are used, the objects are automatically disposed of if an assignment collection or the Global parameter is not used.

When the Global parameter is used, all objects are contained in the global store.
If objects are not immediately used, or disposed of by using the `Stop-SPAssignment` command, an out-of-memory scenario can occur.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-SPRoutingMachinePool](Add-SPRoutingMachinePool.md)

[Get-SPRoutingMachinePool](Get-SPRoutingMachinePool.md)

[Set-SPRoutingMachinePool](Set-SPRoutingMachinePool.md)
