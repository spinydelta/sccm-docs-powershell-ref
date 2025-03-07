---
description: Creates a migration job in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: New-CMMigrationJob
---

# New-CMMigrationJob

## SYNOPSIS
Creates a migration job in Configuration Manager.

## SYNTAX

### NewMigrationJobByObject (Default)
```
New-CMMigrationJob [-ContentObjectsSiteCodeMapping <Hashtable>] [-Description <String>]
 [-MigrationJobSchedule <DateTime>] -MigrationObject <IResultObject[]> -Name <String> [-ObjectMigrationJobType]
 [-OverwriteAllObject <Boolean>] [-SaveObjectInfoPath <String>] -SecurityScope <IResultObject[]>
 [-SiteCodeReplacementMapping <Hashtable>] [-TransferOrganizationalFolderStructure <Boolean>]
 [-UtcTime <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### NewMigrationJobByCollectionNotMigrateObject
```
New-CMMigrationJob [-CollectionLimitingMapping <Hashtable>] [-CollectionMigrationJobType]
 [-Description <String>] [-EnableProgramAfterAdvertisementMigrated <Boolean>]
 -MigrationCollection <IResultObject[]> [-MigrationJobSchedule <DateTime>] -Name <String>
 [-OverwriteAllObject <Boolean>] [-SaveCollectionInfoPath <String>] [-SaveObjectInfoPath <String>]
 -SecurityScope <IResultObject[]> [-SiteCodeReplacementMapping <Hashtable>]
 [-TransferOrganizationalFolderStructure <Boolean>] [-UtcTime <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewMigrationJobByCollectionMigrateObject
```
New-CMMigrationJob [-CollectionLimitingMapping <Hashtable>] [-CollectionMigrationJobType]
 [-ContentObjectsSiteCodeMapping <Hashtable>] [-Description <String>]
 [-EnableProgramAfterAdvertisementMigrated <Boolean>] [-MigrateObjectWithSpecifiedCollection]
 -MigrationCollection <IResultObject[]> [-MigrationJobSchedule <DateTime>] -MigrationObject <IResultObject[]>
 -Name <String> [-OverwriteAllObject <Boolean>] [-SaveCollectionInfoPath <String>]
 [-SaveObjectInfoPath <String>] -SecurityScope <IResultObject[]> [-SiteCodeReplacementMapping <Hashtable>]
 [-TransferOrganizationalFolderStructure <Boolean>] [-UtcTime <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewMigrationJobByObjectModified
```
New-CMMigrationJob [-ContentObjectsSiteCodeMapping <Hashtable>] [-Description <String>]
 [-MigrationJobSchedule <DateTime>] -MigrationObject <IResultObject[]> -Name <String>
 [-ObjectModifiedAfterMigrationJobType] [-OverwriteAllObject <Boolean>] [-SaveObjectInfoPath <String>]
 -SecurityScope <IResultObject[]> [-SiteCodeReplacementMapping <Hashtable>]
 [-TransferOrganizationalFolderStructure <Boolean>] [-UtcTime <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMMigrationJob** cmdlet creates a migration job in Configuration Manager.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a migration job
```
PS XYZ:\> $CategoryObjects = Get-CMInitialModifiableSecuredCategory
PS XYZ:\> $MigrationEntity = Get-CMMigrationEntity
PS XYZ:\> New-CMMigrationJob -Name "123" -ObjectMigrationJobType -SecurityScope $CategoryObjects -MigrationObject $MigrationEntity
```

The first command uses the Get-CMInitialModifiableSecuredCategory cmdlet and stores the result in the $CategoryObjects variable.

The second command uses the Get-CMMigrationEntity cmdlet and stores the result in the $MigrationEntity variable.

The last command creates a migration job.

## PARAMETERS

### -CollectionLimitingMapping
Specifies key-value pairings to limit a collection.
Collection limiting prevents the addition of collection members you do want in the collection.

```yaml
Type: Hashtable
Parameter Sets: NewMigrationJobByCollectionNotMigrateObject, NewMigrationJobByCollectionMigrateObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionMigrationJobType
Indicates that the job migrates collections, objects, or previously migrated objects.

```yaml
Type: SwitchParameter
Parameter Sets: NewMigrationJobByCollectionNotMigrateObject, NewMigrationJobByCollectionMigrateObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -ContentObjectsSiteCodeMapping
Specifies key-value pairs that map content objects in the new site.

```yaml
Type: Hashtable
Parameter Sets: NewMigrationJobByObject, NewMigrationJobByCollectionMigrateObject, NewMigrationJobByObjectModified
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
Specifies a description for the migration job.

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

### -EnableProgramAfterAdvertisementMigrated
Indicates whether to enable programs associated with an advertisement after they have migrated.

```yaml
Type: Boolean
Parameter Sets: NewMigrationJobByCollectionNotMigrateObject, NewMigrationJobByCollectionMigrateObject
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

### -MigrateObjectWithSpecifiedCollection
Indicates that you migrate associated objects with the collection.

```yaml
Type: SwitchParameter
Parameter Sets: NewMigrationJobByCollectionMigrateObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MigrationCollection
Specifies an array of input objects.

```yaml
Type: IResultObject[]
Parameter Sets: NewMigrationJobByCollectionNotMigrateObject, NewMigrationJobByCollectionMigrateObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MigrationJobSchedule
Specifies a date time, in D.HH:MM:SS format, to schedule the migration job.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MigrationObject
Specifies an array of input objects.

```yaml
Type: IResultObject[]
Parameter Sets: NewMigrationJobByObject, NewMigrationJobByCollectionMigrateObject, NewMigrationJobByObjectModified
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of a migration job in Configuration Manager.

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

### -ObjectMigrationJobType
Indicates that the job type is an object migration job.

```yaml
Type: SwitchParameter
Parameter Sets: NewMigrationJobByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ObjectModifiedAfterMigrationJobType
Indicates that the new migration job only includes objects that were modified since the last migration.

```yaml
Type: SwitchParameter
Parameter Sets: NewMigrationJobByObjectModified
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OverwriteAllObject
Indicates whether to overwrite objects in the destination database.

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

### -SaveCollectionInfoPath
Specifies a path for the collection information.

```yaml
Type: String
Parameter Sets: NewMigrationJobByCollectionNotMigrateObject, NewMigrationJobByCollectionMigrateObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SaveObjectInfoPath
Specifies a path for the object information.

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

### -SecurityScope
Specifies an array of security scope objects.
To obtain a security scope object, use the [Get-CMSecurityScope](Get-CMSecurityScope.md) cmdlet.
The cmdlet applies the security scopes that you specify to data migrated to the destination hierarchy.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCodeReplacementMapping
Specifies key-value pairs that map a migrated collection to a site in the destination.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TransferOrganizationalFolderStructure
Indicates whether to migrate an empty collection.
Configuration Manager converts the empty collection to an organizational folder.

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

### -UtcTime
Indicates whether to use UTC time.

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

### IResultObject#SMS_MigrationJob
## NOTES

## RELATED LINKS

[Get-CMInitialModifiableSecuredCategory](Get-CMInitialModifiableSecuredCategory.md)

[Get-CMMigrationEntity](Get-CMMigrationEntity.md)

[Get-CMSecurityScope](Get-CMSecurityScope.md)
