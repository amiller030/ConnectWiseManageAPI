---
external help file: ConnectWiseManageAPI-help.xml
Module Name: ConnectWiseManageAPI
online version: https://developer.connectwise.com/manage/rest?a=Company&e=Configurations&o=GET
schema: 2.0.0
---

# Get-CWMCompanyContactNote

## SYNOPSIS
This function will list a contacts notes.

## SYNTAX

```
Get-CWMCompanyContactNote [-parentId] <Int32> [[-id] <Int32>] [[-Condition] <String>] [[-orderBy] <String>]
 [[-childConditions] <String>] [[-customFieldConditions] <String>] [[-page] <Int32>] [[-pageSize] <Int32>]
 [[-fields] <String[]>] [-all] [<CommonParameters>]
```

## DESCRIPTION
Used to return a company contacts notes via ID or conditions.

## EXAMPLES

### Example 1
```powershell
PS C:\> Get-CWMCompanyContactNote -parentId $Contact.id
```

Will return all notes for the given contact.

## PARAMETERS

### -Condition
This is your search condition to return the results you desire.
Example: `(contact/name like "Fred%" and closedFlag = false) and dateEntered \> \[2015-12-23T05:53:27Z\] or summary contains "test" AND  summary != "Some Summary"`

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -all
Return all results

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

### -childConditions
Allows searching arrays on endpoints that list childConditions under parameters

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -customFieldConditions
Allows searching custom fields.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -fields
Allows you to return a partial response with just the fields listed.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -id
The ID of the note you want returned.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: noteId

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -orderBy
Choose which field to sort the results by, 'field/sub desc' or 'field/sub asc'

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -page
Used in pagination to cycle through results.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -pageSize
Number of results returned per page (Defaults to 25)

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -parentId
The ID of the contact you want to return the notes of.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: contactId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS