---
external help file: sharepointonline.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/get-spodataconnectionsettingmetadata

title: Get-SPODataConnectionSettingMetadata
schema: 2.0.0
---

# Get-SPODataConnectionSettingMetadata

## SYNOPSIS

Returns a Business Data Connectivity service metadata object.

## SYNTAX

```
Get-SPODataConnectionSettingMetadata -ServiceContext <SPServiceContextPipeBind> -Name <String>
 [-AssignmentCollection <SPAssignmentCollection>] [<CommonParameters>]
```

## DESCRIPTION
Use the `Get-SPODataConnectionSettingMetaData` cmdlet to return a Business Data Connectivity service metadata object for a specific Business Connectivity Services service application.

This cmdlet applies to an on-premises environment only.
You cannot use this command in the SharePoint Online Management Shell.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at https://go.microsoft.com/fwlink/p/?LinkId=251831 (https://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### EXAMPLE 1
```powershell
Get-SPODataConnectionSettingMetadata -ServiceContext "http://contoso" -Name "ContosoServiceApp"
```

This example displays metadata properties of BCS connection named ContosoServiceApp

## PARAMETERS

### -ServiceContext

> Applicable: SharePoint Server Subscription Edition

Specifies the service context which is in the form of an instance of an SPServiceContext object, an SPSiteAdministration object identifier, or a SPSite object.
An example of a service context value is an identifier from the ID field, a string identifier, a URI, or a string representation of a GUID.

```yaml
Type: SPServiceContextPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the Business Connectivity Services connection whose metadata properties the user wants to see displayed.

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

### -AssignmentCollection

> Applicable: SharePoint Server Subscription Edition

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
