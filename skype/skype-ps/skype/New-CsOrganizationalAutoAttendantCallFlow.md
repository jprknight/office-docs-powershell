---
external help file: Microsoft.Rtc.Management.Hosted.dll-help.xml
online version: https://docs.microsoft.com/powershell/module/skype/new-csorganizationalautoattendantcallflow
applicable: Skype for Business Online
title: New-CsOrganizationalAutoAttendantCallFlow
schema: 2.0.0
manager: bulenteg
author: tomkau
ms.author: tomkau
ms.reviewer:
---

# New-CsOrganizationalAutoAttendantCallFlow

## SYNOPSIS
> [!CAUTION]
> This cmdlet has been deprecated and is no longer supported.  This cmdlet will be removed in the near future.
> 
> Please use [New-CsAutoAttendantCallFlow](New-CsAutoAttendantCallFlow.md) cmdlet instead.

Use the New-CsOrganizationalAutoAttendantCallFlow cmdlet to create a new call flow.

## SYNTAX

```
New-CsOrganizationalAutoAttendantCallFlow -Name <String> [-Greetings <List>] -Menu <Menu> [-Tenant <Guid>]
 [-DomainController <Fqdn>] [-Force] [<CommonParameters>]
```

## DESCRIPTION
The New-CsOrganizationalAutoAttendantCallFlow cmdlet creates a new call flow for use with the Auto Attendant (AA) service. The OAA service uses the call flow to handle inbound calls by playing a greeting (if present), and provide callers with actions through a menu.


## EXAMPLES

### -------------------------- Example 1 --------------------------
```
$menuPrompt = New-CsOrganizationalAutoAttendantPrompt -TextToSpeechPrompt "To reach your party by name, enter it now, followed by the pound sign."
$menu = New-CsOrganizationalAutoAttendantMenu -Name "Default Menu" -Prompts @($menuPrompt) -EnableDialByName 
$callFlow = New-CsOrganizationalAutoAttendantCallFlow -Name "Default Call Flow" -Menu $menu
```

This example creates a new call flow that renders the "Default Menu" menu.

### -------------------------- Example 2 --------------------------
```
$menuPrompt = New-CsOrganizationalAutoAttendantPrompt -TextToSpeechPrompt "To reach your party by name, enter it now, followed by the pound sign."
$menu = New-CsOrganizationalAutoAttendantMenu -Name "Default Menu" -Prompts $menuPrompt -EnableDialByName 
$greeting = New-CsOrganizationalAutoAttendantPrompt -TextToSpeechPrompt "Welcome to Contoso!"
$callFlow = New-CsOrganizationalAutoAttendantCallFlow -Name "Default Call Flow" -Menu $menu -Greetings $greeting
```

This example creates a new call flow that plays a greeting before rendering the "Default Menu" menu.

## PARAMETERS

### -Name
The Name parameter represents a unique friendly name for the call flow.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Applicable: Skype for Business Online

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Menu
The Menu parameter identifies the menu to render when the call flow is executed.

You can create a new menu by using the New-CsOrganizationalAutoAttendantMenu cmdlet.

```yaml
Type: Menu
Parameter Sets: (All)
Aliases: 
Applicable: Skype for Business Online

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Greetings
If present, the prompts specified by the Greetings parameter (either TTS or Audio) are played before the call flow's menu is rendered.

You can create prompts by using the New-CsOrganizationalAutoAttendantPrompt cmdlet.

```yaml
Type: List
Parameter Sets: (All)
Aliases: 
Applicable: Skype for Business Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tenant

```yaml
Type: Guid
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
This cmdlet supports the common parameters: `-Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).`

## INPUTS

### None


## OUTPUTS

### Microsoft.Rtc.Management.Hosted.OAA.Models.CallFlow


## NOTES

## RELATED LINKS

[New-CsOrganizationalAutoAttendantMenu](New-CsOrganizationalAutoAttendantMenu.md)

[New-CsOrganizationalAutoAttendantPrompt](New-CsOrganizationalAutoAttendantPrompt.md)
