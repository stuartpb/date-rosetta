# Date Formatting Rosetta Stone

This document contains examples 

These examples are chosen to illustrate differences in syntax for date formatting across systems.

Inspired by [this spreadsheet](https://docs.google.com/spreadsheet/ccc?key=0AtgZluze7WMJdDBOLUZfSFIzenIwOHNjaWZoeGFqbWc), as linked to in the [Moment.js Format documentation](http://momentjs.com/docs/#/displaying/format/).

A more broad, but less detailed page of examples is at http://rosettacode.org/wiki/Date_format

## Example Date

Each formatting implementation example is designed to match sample output for the date and time of November 12, 1955 at precisely 10:04 Pacific Standard Time.

## Implementations

Each implementation listed provides boilerplate scaffolding code for the formatting examples.

### strftime

This function is called directly by Python's [strftime](https://docs.python.org/3/library/datetime.html#strftime-and-strptime-behavior) and Lua's [os.date](http://www.lua.org/manual/5.3/manual.html#pdf-os.date), which share its syntax.

### LDML

This is the syntax used for specifying date formats in Unicode's Locale Data Markup Language, as specified by http://unicode.org/reports/tr35/tr35-dates.html#Date_Format_Patterns

Unlike most other formatting models, LDML is not strictly designed around formatting dates in the Gregorian calendar: the nuanced differences in the definitions can be found in the specification linked above.

LDML formatting supports zero-padding below the maximum for a field: for instance, "DD" representes a two-digit-padded Day of Year, where the ninth day is "09" but the hundredth day is "100". These forms of padding are of dubious utility, and are not listed.

### Microsoft

This is the syntax used for formatting dates and times in Windows, Office, and .NET. The examples are given in C#:

```C#
DateTime date1 = new DateTime(1955, 11, 12, 22, 4, 0);
CultureInfo ci = CultureInfo.InvariantCulture;
```

### ECMAScript Date

These examples demonstrate how to produce fields using the properties of Date objects in plain JavaScript.

```JavaScript
var example = new Date("1955-11-12 10:04:00 PM PST");
```

### Moment

http://momentjs.com/docs/#/displaying/format/

### DateJS

https://github.com/abritinthebay/datejs/wiki/Format-Specifiers

### XDate

http://arshaw.com/xdate/#Formatting

### Steven Levithan

A "JavaScript Date Format" function by Steven Levithan: http://blog.stevenlevithan.com/archives/date-time-format

### PHP

http://php.net/manual/en/function.date.php

## Formattings

### Era

### Century

### 5-Digit Year of Era

As advocated by the [Long Now Foundation](http://longnow.org/).

### 4-Digit Year of Era

### 3-Digit Year of Era

### 2-Digit Year of Era

### 1-Digit Year of Era

### Month of Year Number

### Month of Year with ordinal

### Month of Year Zero-Padded

### Month of Year Three-Letter Abbreviation

### Month of Year Full Name

### Leap Year status

1 if it is a leap year, 0 otherwise.

#### PHP

```PHP
date("L",example)
```

### Week of Year

### Week of Year with ordinal

### Week of Year Zero-Padded

### Week of Month

### Days In Month

### Day of Month

### Day of Month with ordinal

### Day of Month Zero-Padded

### Day of Year

### Day of Year with ordinal

### Day of Year Zero-Padded

#### LDML

### Day of Week Three-Letter Abbreviation

### Day of Week Two-Letter Abbreviation

### Day of Week First Letter

### Day of Week Full Name

### Day of Week Number

### Day of Week Number with ordinal

### Single Letter Half of Day

### Two Letter Half of Day

### Hour of Full Day

### Hour of Full Day Zero-Padded

### Hour of Half Day

### Hour of Half Day Zero-Padded

### Second of Minute

### Second of Minute Zero-Padded

### Hundredths of Second

### Thousandths of Second Zero-Padded

### Millionths of Second

### Daylight Saving Time

1 if Daylight Saving Time, 0 otherwise.

#### PHP

```PHP
date("L",example)
```

### Time Zone
