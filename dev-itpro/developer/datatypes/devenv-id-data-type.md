---
title: "ID Data Type"
ms.custom: na
ms.date: 10/01/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: "dynamics365-business-central"
ms.assetid: 96328bb5-ef6c-413f-9294-e18d6639d919
caps.latest.revision: 12
author: SusanneWindfeldPedersen
---
# ID Data Type
Sets a unique numeric ID for this codeunit, table, page, report, XMLport, or control.  
  
## Applies To  
  
-   Codeunits  
  
-   Menu items  
  
-   Pages, including the page object, controls, and actions  
  
-   Queries, including the query object, data items, columns, and filter rows  
  
-   Tables  
  
-   XMLports  
  
## Remarks  
 The ID must be unique within the scope of the object. For example, two code units, tables, or page cannot have the same ID, and no control can have the same ID as another control on that object.  
  
 The ID is used for reference purposes. As a result, you can use the value of the [Name Data Type](devenv-name-data-type.md) to reference objects in your code. The Name is automatically converted to the ID when the code is compiled.  
  
 If you do not set the **ID** data type, you will be prompted for one when you save the object. For controls, a numeric ID is assigned based on the next available number for the page or the report. You can change this ID.  
  
## See Also  
 [Name Data Type](devenv-name-data-type.md)  
 [AL Data Types](devenv-al-data-types.md)