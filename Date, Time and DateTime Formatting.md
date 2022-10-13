## Here, we are providing a table of format specifiers supported by the Java String.

|Format Specifier|Data Type|Output|
|:-------|:------------|:---------|
|%a	   | floating point ( except BigDecima l)	|Returns Hex output of floating-point number.|
|%b	   | Any type	|" true " if non-null, " false " if null|
|%c	   | Character	|Unicode character|
|%d	   | integer ( incl. byte, short, int, long, bigint )	|Decimal Integer|
|%e	   | floating point | Decimal number in scientific notation|
|%f	   | floating point | Decimal number|
|%g	   | floating point | Decimal number, possibly in scientific notation depending on the precision and value.|
|%h	   | any type	|Hex String of value from hashCode( ) method.|
|%n	   | None	|Platform-specific line separator.|
|%o	   | integer ( incl. byte, short, int, long, bigint )	|Octal number|
|%s	   | any type	|String value|
|%t	   | Date/Time ( incl. long, Calendar, Date and TemporalAccessor )|	%t is the prefix for Date/Time conversions. More formatting flags are needed after this. See Date/Time conversion below.|
|%x	   | integer ( incl. byte, short, int, long, bigint )|	Hex string.|


## The following table contains the suffix characters for Time Formatting



| Suffix	 | Meaning                                                                                                                                                                          |
|:--------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| H	      | Format time as two-digit hour of the day for the 24-hour clock. The valid values are 00 to 23. 00 is used for midnight.                                                          |
| I	      | Format a two-digit hour of the day for the 12-hour clock. The valid values are 01 to 12.                                                                                         |
| k	      | Format time the same as the H suffix except that it does not add a leading zero to the output. Valid values are 0 to 23.                                                         |
| l	      | Format time the same as 'I' suffix except that it does not add a leading zero. Valid values are 1 to 12.                                                                         |
| M	      | A two-digit minute within an hour. Valid values are 00 to 59.                                                                                                                    |
| S	      | A two-digit second. Valid values are 00 to 60.                                                                                                                                   |
| L	      | A three-digit millisecond. Valid values are 000 to 999.                                                                                                                          |
| N	      | A nine-digit nanosecond. The valid values are 000000000 to 999999999.                                                                                                            |
| p	      | Format a locale-specific morning or afternoon string in lowercase. For US locale, "am" or "pm". To get "AM" and "PM", use the uppercase variant 'T' as the conversion character. |
| z	      | Output the numeric time zone offset from GMT (e.g., +0530).                                                                                                                      |
| Z	      | Output a string abbreviation of the time zone (e.g., CST, EST, IST, etc).                                                                                                        |
| s	      | Output seconds since January 1, 1970 midnight UTC.                                                                                                                               |
| Q	      | Output milliseconds since January 1, 1970 midnight UTC.                                                                                                                          |

## The following table list of suffix characters for Date Formatting

|Letter	| Meaning                                                                                                                                                                                                                         |
|:---------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|B	    | Output locale-specific full name of the month, such as "January", "February", in US locale.                                                                                                                                     |
|b	    | Output locale-specific abbreviated month name, such as "Jan", "Feb", in US locale.                                                                                                                                              |
|h	    | Same as 'b'. Output locale-specific abbreviated month name, such as "Jan", "Feb", in US locale.                                                                                                                                 |
|A	    | Output locale-specific full name for the day of the week, such as "Sunday", "Monday" for US locale.                                                                                                                             |
|a	    | Output locale-specific short name of the day of the week, such as "Sun", "Mon" for US locale.                                                                                                                                   |
|C	    | Divide the four-digit year by 100 and formats the result as two digits. It adds a leading zero if the resulting number is one digit. Valid values are 00 to 99. For example, if the four-digit year is 2014, it will output 20. |
|Y	    | Output a four-digit year with leading zeros if the year contains less than four digits.                                                                                                                                         |
|y	    | Output the last two digits of the year and adds leading zero if necessary. 2011 will output 11                                                                                                                                  |
|j	    | A three-digit day of the year. Valid values are 000 to 366.                                                                                                                                                                     |
|m	    | A two-digit month. Valid values are 01 to 13. The special value of 13 is required to support lunar calendar.                                                                                                                    |
|d	    | A two-digit day of the month. Valid values are 01 to 31.                                                                                                                                                                        |
|e	    | Day of the month. Valid values are 1 to 31.                                                                                                                                                                                     |

## The following table lists of Suffix Characters for Date/Time Formatting

|Format	| Description|
|:---------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|R	    | Output time in 24-hour clock format as "hour:minute". It outputs the same as %tH:%tM. Examples: 11:23|
|T	    | Output time in 24-hour clock in "hour:minute:second" format. It outputs the same as "%tH:%tM:%tS". Examples 11:23:10|
|r	    | Output time in 12-hour clock format as "hour:minute:second morning/afternoon marker". It outputs the same as "%tI:%tM:%tS %Tp". Example, 09:23:45 AM|
|D	    | Output the date as "%tm/%td/%ty", such as "01/19/14"|
|F	    | Output the date as "%tY-%tm-%td", such as "2014-01-19".|
|c	    | Output the date and time as "%ta %tb %td %tT %tZ %tY", such as "Wed Jan 20 12:22:06 CST 2014".|


The following code shows how to use the date time formatter. It uses '<' flag in the format specifier to reuse the value from argument.

