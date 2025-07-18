---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spotenantlogentry
applicable: SharePoint Online
title: Get-SPOTenantLogEntry
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Get-SPOTenantLogEntry

## SYNOPSIS

Retrieves SharePoint Online company logs. This cmdlet is reserved for internal Microsoft use.

## SYNTAX

### SiteSubscriptionId (Default)
```
Get-SPOTenantLogEntry [[-StartTimeInUtc] <DateTime>] [[-EndTimeInUtc] <DateTime>] [[-MaxRows] <UInt32>]
 [<CommonParameters>]
```

### CorrelationId
```
Get-SPOTenantLogEntry -CorrelationId <Guid> [[-StartTimeInUtc] <DateTime>] [[-EndTimeInUtc] <DateTime>]
 [[-MaxRows] <UInt32>] [<CommonParameters>]
```

### Source
```
Get-SPOTenantLogEntry -Source <Int32> [[-StartTimeInUtc] <DateTime>] [[-EndTimeInUtc] <DateTime>]
 [[-MaxRows] <UInt32>] [<CommonParameters>]
```

### User
```
Get-SPOTenantLogEntry -User <String> [[-StartTimeInUtc] <DateTime>] [[-EndTimeInUtc] <DateTime>]
 [[-MaxRows] <UInt32>] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see Cmdlet Parameter Sets.

The `Get-SPOTenantLogEntry` cmdlet cannot retrieve all SharePoint Online errors. This cmdlet retrieves a subset of errors that happen due to external systems.

For Beta 2, the only company logs available are for Business Connectivity Services (BCS).

> [!NOTE]
> If you do not use any parameter, the first 1000 rows in descending time range are returned.

You must be at least a SharePoint Online administrator to run the cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [Intro to SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell).

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOTenantLogEntry
```

This example retrieves all logs that are available.

### EXAMPLE 2

```powershell
Get-SPOTenantLogEntry -MaxRows 500
```

This example retrieves the first 500 log entries.

### EXAMPLE 3

```powershell
$endTimeinUTC = Get-SPOTenantLogLastAvailableTimeInUtc
$startTimeinUTC = $endTimeinUTC.AddDays(-14)
$tenantlogs = Get-SPOTenantLogEntry -StartTimeinUtc $startTimeinUTC -EndTimeinUTC $endTimeinUTC
```

This example retrieves log entries recorded over that previous 14 days.

### EXAMPLE 4

```powershell
$endTimeinUTC = Get-SPOTenantLogLastAvailableTimeInUtc
$startTimeinUTC = $endTimeinUTC.AddDays(-14)
$tenantlogs = Get-SPOTenantLogEntry -StartTimeinUtc $startTimeinUTC -EndTimeinUTC $endTimeinUTC -CorrelationId e2c2be70-6382-4ce7-8a44-ae7dadff5597
```

This example retrieves log entries recorded over that previous 14 days that have the CorrelationId of "e2c2be70-6382-4ce7-8a44-ae7dadff5597".

## PARAMETERS

### -CorrelationId

> Applicable: SharePoint Online

Specifies the Correlation ID as a filter.

```yaml
Type: System.Guid
Parameter Sets: CorrelationId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndTimeInUtc

> Applicable: SharePoint Online

Specifies the end time in UTC to search for logs.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxRows

> Applicable: SharePoint Online

Specifies the maximum number of rows in the descending order of timestamp. The value must be less than 5000. The default value is 1000.

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Source

> Applicable: SharePoint Online

Specifies the component that logs the errors.

```yaml
Type: System.Int32
Parameter Sets: Source
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTimeInUtc

> Applicable: SharePoint Online

Specifies the start time in Coordinated Universal Time (UTC) to search for the logs (for example, 01032011:12:00).

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -User

> Applicable: SharePoint Online

Specifies the log-on identity as a filter.

```yaml
Type: System.String
Parameter Sets: User
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
