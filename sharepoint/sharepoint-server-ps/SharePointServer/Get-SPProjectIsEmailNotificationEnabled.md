---
external help file: microsoft.office.project.server.stsadmcommandhandler.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/get-spprojectisemailnotificationenabled

title: Get-SPProjectIsEmailNotificationEnabled
schema: 2.0.0
---

# Get-SPProjectIsEmailNotificationEnabled

## SYNOPSIS
Returns the Project Web App site level setting for email notifications. True if notifications is turned on, False otherwise.

## SYNTAX

```
Get-SPProjectIsEmailNotificationEnabled [-Url] <Uri> [-AssignmentCollection <SPAssignmentCollection>]
 [<CommonParameters>]
```

## DESCRIPTION
Returns the Project Web App site level setting for email notifications. True if notifications is turned on, False otherwise.

## EXAMPLES

### Example 1
```powershell
Get-SPProjectIsEmailNotificationEnabled -Url https://contoso/sites/pwa
```

Returns the status of email notifications for the PWA site https://contoso/sites/pwa.

## PARAMETERS

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

### -Url

> Applicable: SharePoint Server Subscription Edition

The URL of the Project Web App site.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.SharePoint.PowerShell.SPAssignmentCollection

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
