---
external help file: Microsoft.Office.Server.UserProfiles.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/add-spprofilesyncconnection
applicable: SharePoint Server Subscription Edition
title: Add-SPProfileSyncConnection
schema: 2.0.0
---

# Add-SPProfileSyncConnection

## SYNOPSIS
Adds a synchronization connection.

## SYNTAX

```
Add-SPProfileSyncConnection [-ProfileServiceApplication] <SPServiceApplicationPipeBind>
 -ConnectionDomain <String> -ConnectionForestName <String> -ConnectionPassword <SecureString>
 -ConnectionSynchronizationOU <String> -ConnectionUserName <String>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-ConnectionClaimIDMapAttribute <String>]
 [-ConnectionClaimProviderIdValue <String>] [-ConnectionClaimProviderTypeValue <String>]
 [-ConnectionNamingContext <String>] [-ConnectionPort <Int32>] [-ConnectionServerName <String>]
 [-ConnectionUseSSL <Boolean>] [-WhatIf] [-ConnectionFilterOutUnlicensed <Boolean>]
 [-ConnectionUseDisabledFilter <Boolean>] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet was introduced in SharePoint Server with Service Pack 1 (SP1) and SharePoint Foundation with Service Pack 1 (SP1).

Use the Add-SPProfileSyncConnection cmdlet to add a User Profile synchronization connection.

For additional information about profile synchronization connections, see

This cmdlet only works with Active Directory Synchronization Connections

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
Add-SPProfileSyncConnection -ProfileServiceApplication 888ds256-9ad9-53a9-f135-99eecd245670b -ConnectionForestName "fabrikam.com"-ConnectionDomain "Fabrikam" -ConnectionUserName "Testupa" -ConnectionPassword convertto-securestring "Password1" -asplaintext -force -ConnectionSynchronizationOU "OU=SharePoint Users,DC=fabrikam,DC=com"
```

This example adds a user from the fabrikam domain using a specific user profile service application.

## PARAMETERS

### -ProfileServiceApplication

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the User Profile service application.

```yaml
Type: SPServiceApplicationPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ConnectionDomain

> Applicable: SharePoint Server Subscription Edition

Specifies the NetBIOS name of the domain you are connecting to.

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

### -ConnectionForestName

> Applicable: SharePoint Server Subscription Edition

Specifies the fully qualified domain name (FQDN) of the forest you are connecting to.

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

### -ConnectionPassword

> Applicable: SharePoint Server Subscription Edition

Specifies the password of the account used for directory connection.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionSynchronizationOU

> Applicable: SharePoint Server Subscription Edition

Specifies the top level organizational unit (OU) that you would like to synchronize.
The value must be a domain name and you can only include one container per command.

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

### -ConnectionUserName

> Applicable: SharePoint Server Subscription Edition

Specifies the user name to be used for the synchronization connection.

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
If objects are not immediately used, or disposed of by using the Stop-SPAssignment command, an out-of-memory scenario can occur.

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

### -Confirm

> Applicable: SharePoint Server Subscription Edition

Prompts you for confirmation before executing the command.
For more information, type the following command: `get-help about_commonparameters`

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionClaimIDMapAttribute

> Applicable: SharePoint Server Subscription Edition

Specifies the Claims ID used by the Claim Provider, that is, samAccountName.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionClaimProviderIdValue

> Applicable: SharePoint Server Subscription Edition

Specifies the Claims Provider ID or Name for an authentication type while a Web App is configured.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionClaimProviderTypeValue

> Applicable: SharePoint Server Subscription Edition

Specifies the Authentication claim Provider that will be used to encode the User Profile accounts names.
For example, Windows/Forms etc.
This means if a user logs in using the given Authentication Type, then a profile can be found by looking up a claim encoded credentials.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionNamingContext

> Applicable: SharePoint Server Subscription Edition

Specifies the naming context of the directory information tree to connect to.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionPort

> Applicable: SharePoint Server Subscription Edition

Specifies the port to be used to connect to the directory service.
The default port is 389.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionServerName

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the domain controller to connect to.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionUseSSL

> Applicable: SharePoint Server Subscription Edition

Specifies if the connection to the directory service must be over SSL.

The valid values are: $True or $False

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

> Applicable: SharePoint Server Subscription Edition

Displays a message that describes the effect of the command instead of executing the command.
For more information, type the following command: `get-help about_commonparameters`

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionFilterOutUnlicensed

> Applicable: SharePoint Server Subscription Edition

Do not use.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionUseDisabledFilter

> Applicable: SharePoint Server Subscription Edition

Filters out disabled accounts.

>[!NOTE]
This will only filter out accounts which are in a disabled state prior to being imported. It will not filter out accounts which have been disabled after importing.

```yaml
Type: Boolean
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
