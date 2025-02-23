---
external help file: Microsoft.Rtc.Management.Hosted.dll-help.xml
online version: https://docs.microsoft.com/powershell/module/skype/get-csorganizationalautoattendanttenantinformation
applicable: Skype for Business Online
title: Get-CsOrganizationalAutoAttendantTenantInformation
schema: 2.0.0
manager: bulenteg
author: tomkau
ms.author: tomkau
ms.reviewer:
---

# Get-CsOrganizationalAutoAttendantTenantInformation

## SYNOPSIS
> [!CAUTION]
> This cmdlet has been deprecated and is no longer supported.  This cmdlet will be removed in the near future.
> 
> Please use [Get-CsAutoAttendantTenantInformation](Get-CsAutoAttendantTenantInformation.md) cmdlet instead.

Gets the default tenant information for Auto Attendant (AA) feature.

## SYNTAX

```
Get-CsOrganizationalAutoAttendantTenantInformation [-Tenant <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The Get-CsOrganizationalAutoAttendantTenantInformation cmdlet gets the default tenant information for Auto Attendant (AA) feature.

## EXAMPLES

### -------------------------- Example 1 --------------------------
```
Get-CsOrganizationalAutoAttendantTenantInformation
```

Gets the default auto attendant information for the logged in tenant.


## PARAMETERS

### -Tenant

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 
Applicable: Skype for Business Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### Microsoft.Rtc.Management.Hosted.OAA.Models.TenantInformation

## NOTES

## RELATED LINKS

