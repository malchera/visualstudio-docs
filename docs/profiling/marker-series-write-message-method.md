---
title: "marker_series::write_message Method | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.technology: "vs-ide-debug"
ms.topic: "conceptual"
f1_keywords: 
  - "cvmarkersobj/Concurrency::diagnostic::marker_series::write_message"
helpviewer_keywords: 
  - "Concurrency::diagnostic::marker_series::write_message method"
ms.assetid: 546121bc-67e0-4a5a-a456-12bd78fd6de2
author: "mikejo5000"
ms.author: "mikejo"
manager: douge
ms.workload: 
  - "multiple"
---
# marker_series::write_message Method
Writes a message to the Concurrency Visualizer trace file.  
  
## Syntax  
  
```cpp  
void write_message(  
   _In_ LPCTSTR _Format,  
   ...  
);  
void write_message(  
   marker_importance _Importance,  
   _In_ LPCTSTR _Format,  
   ...  
);  
void write_message(  
   int _Category,  
   _In_ LPCTSTR _Format,  
   ...  
);  
void write_message(  
   marker_importance _Importance,  
   int _Category,  
   _In_ LPCTSTR _Format,  
   ...  
);  
```  
  
#### Parameters  
 `_Format`  
 A composite format string that contains text intermixed with zero or more format items, which correspond to objects in the argument list.  
  
 `_Importance`  
 Importance level.  
  
 `_Category`  
 Category.Importance level.  
  
## Requirements  
 **Header:** cvmarkersobj.h  
  
 **Namespace:** Concurrency::diagnostic  
  
## See Also  
 [marker_series Class](../profiling/marker-series-class.md)