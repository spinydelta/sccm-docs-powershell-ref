---
description: Creates a file replication route for Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: New-CMFileReplicationRoute
---

# New-CMFileReplicationRoute

## SYNOPSIS
Creates a file replication route for Configuration Manager.

## SYNTAX

```
New-CMFileReplicationRoute -DestinationSiteCode <String> [-DestinationSiteServerName <String>]
 [-FileReplicationAccountName <String>] -SourceSiteCode <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMFileReplicationRoute** cmdlet creates a file replication route for Configuration Manager.
Configuration Manager uses file replication routes to transfer file-based data between sites in a hierarchy.
Each file replication route identifies a destination site to which file-based data can transfer.

File replication routes were known as addresses in versions of Configuration Manager before Configuration Manager.
The functionality of file replication routes is the same as that of addresses in earlier versions.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a file replication route
```
PS XYZ:\> New-CMFileReplicationRoute -DestinationSiteCode "IM5" -SourceSiteCode "IM1" -DestinationSiteServerName "ImgDataServer01" -FileReplicationAccountName "AdminRepl01"
```

This command creates a file replication route from the site that has the site code IM1 to the site that has the site code IM5 on the server named ImgDataServer01.
Configuration Manager uses the account named AdminRepl01 to manage data transfer over this route.

## PARAMETERS

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationSiteCode
Specifies a destination site for data transfers by using a site code.

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

### -DestinationSiteServerName
Specifies a destination site server for data transfers by using a site server name.

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

### -DisableWildcardHandling

This parameter treats wildcard characters as literal character values. You can't combine it with **ForceWildcardHandling**.

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

### -FileReplicationAccountName
Specifies the account that Configuration Manager uses to install a site on the specified server and maintain communications between the site and other sites.
This account must have local administrative credentials.

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

### -ForceWildcardHandling

This parameter processes wildcard characters and may lead to unexpected behavior (not recommended). You can't combine it with **DisableWildcardHandling**.

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

### -SourceSiteCode
Specifies a source site for data transfers by using a site code.

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

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### IResultObject#SMS_SCI_Address
## NOTES

## RELATED LINKS

[Get-CMFileReplicationRoute](Get-CMFileReplicationRoute.md)

[Remove-CMFileReplicationRoute](Remove-CMFileReplicationRoute.md)

[Set-CMFileReplicationRoute](Set-CMFileReplicationRoute.md)


