---
title: "DateTime Data Type"
ms.custom: na
ms.date: 10/01/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: "dynamics365-business-central"
ms.assetid: 5e81b482-850f-4e8a-8625-5937dabaf1b2
caps.latest.revision: 17
author: SusanneWindfeldPedersen
---
# DateTime Data Type
Denotes a date and time ranging from January 1, 1753, 00:00:00.000 to December 31, 9999, 23:59:59.999. An undefined or blank DateTime is specified by 0DT.  
  
 The displayed text format of a DateTime is determined by your Regional and Language Options in Windows.  
  
## Remarks  
 A DateTime is stored in the database as Coordinated Universal Time (UTC). UTC is the international time standard (formerly Greenwich Mean Time, or GMT). Zero hours UTC is midnight at 0 degrees longitude.  
  
 The DateTime is always displayed as local time in [!INCLUDE[d365fin_long_md](../includes/d365fin_long_md.md)]. Local time is determined by the time zone regional settings used by your computer. You must always enter DateTimes as local time. When you enter a DateTime as local time, it is converted to UTC using the current settings for the time zone and daylight savings time.  
  
 The DateTime data type does not support closing dates.  
  
 By default, DateTimes are displayed using the standard display format. When you use the standard display format, seconds and milliseconds are not displayed until you select the DateTime field. Furthermore, if you export your data using an XMLport or by writing it to a file, the seconds and milliseconds are not exported unless you specify that DateTime fields use another format and display this information. For more information about how DateTime objects are displayed and the formats that are available, see [Format Property](../properties/devenv-format-property.md).  
  
 The only constant available when you use the DateTime data type is the undefined DateTime, 0DT. To assign a constant value to a DateTime variable you must use the [CREATEDATETIME method (DateTime)](../methods/devenv-createdatetime-method-datetime.md).  
  
 If you use a date that is outside the valid date range, a run-time error occurs.  

## Syntax
The syntax for defining DateTime format follows the [ISO standard](https://en.wikipedia.org/wiki/ISO_8601). 
- The syntax for defining Date format is `yyyymmddD`, where `D` is a mandatory letter. For example, `20180325D`, read as the 26th of March, 2018.
- The syntax for defining Time format is `hhmmssT`, where `T` is the time designator. For example, `093125H`, read as 9:13:25.

## Methods
The methods supported for the DateTime data type are:

[CREATEDATETIME method (DateTime)](../methods/devenv-createdatetime-method-datetime.md)   
[CURRENTDATETIME method (DateTime)](../methods/devenv-currentdatetime-method-datetime.md)   
[DT2DATE method (DateTime)](../methods/devenv-dt2date-method-datetime.md)   
[DT2TIME method (DateTime)](../methods/devenv-dt2time-method-datetime.md)   
[ROUNDDATETIME method (DateTime)](../methods/devenv-rounddatetime-method-datetime.md)

## SQL Server  
 In SQL Server, the earliest permitted DateTime is January 1, 1753, 00:00:00.000. The latest permitted DateTime is December 31, 9999, 23:59:59.999.  
  
 If you store a date in the database that is outside the valid range for a SQL DATETIME, a run-time error run-time occurs.  

## See Also  
[AL Data Types](devenv-al-data-types.md)  
[AL Method Reference](../methods/devenv-al-method-reference.md)  