---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-sptrustedrootauthority
applicable: SharePoint Server Subscription Edition
title: Set-SPTrustedRootAuthority
schema: 2.0.0
---

# Set-SPTrustedRootAuthority

## SYNOPSIS
Creates a new trusted root authority.

## SYNTAX

### ManualUpdateCertificateParameterSet
```
Set-SPTrustedRootAuthority [-Identity] <SPTrustedRootAuthorityPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Certificate <X509Certificate2>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### MetadataEndPointParameterSet
```
Set-SPTrustedRootAuthority [-Identity] <SPTrustedRootAuthorityPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-MetadataEndPoint <Uri>] [-WhatIf]
 [<CommonParameters>]
```

## DESCRIPTION
The `Set-SPTrustedRootAuthority` cmdlet creates a new trusted root authority.
If a certificate file is used, the certificate must be an X509 certificate without private keys, otherwise an exception is raised.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
$cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
$cert.Import('C:\LiveIDSigningCert.pfx')
Get-SPTrustedRootAuthority -Name "WFEFarm1" | Set-SPTrustedRootAuthority -Certificate $cert
```

This example updates the certificate of the trusted root authority WFEFarm1.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the trusted root authority to update.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a trusted root authority (for example, WFEFarm1); or an instance of a valid SPTrustedRootAuthority object.

```yaml
Type: SPTrustedRootAuthorityPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
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

### -Certificate

> Applicable: SharePoint Server Subscription Edition

Specifies the X.509 certificate of the trusted root authority.

The type must be a name of a valid X.509 certificate; for example, Certificate1.

```yaml
Type: X509Certificate2
Parameter Sets: ManualUpdateCertificateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

> Applicable: SharePoint Server Subscription Edition

Prompts you for confirmation before running the cmdlet.

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

### -MetadataEndPoint

> Applicable: SharePoint Server Subscription Edition

{{Fill MetadataEndPoint Description}}

```yaml
Type: Uri
Parameter Sets: MetadataEndPointParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

> Applicable: SharePoint Server Subscription Edition

Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
