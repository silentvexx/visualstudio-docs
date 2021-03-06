---
title: "SccEndBatch Function | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "SccEndBatch"
helpviewer_keywords: 
  - "SccEndBatch function"
ms.assetid: 100e7833-fe0a-45c0-9fca-3e61fd1165b7
caps.latest.revision: 13
author: "gregvanl"
ms.author: "gregvanl"
manager: ghogen
---
# SccEndBatch Function
This function concludes a batch of source control operations. These batches may not be nested.  
  
## Syntax  
  
```cpp  
SCCRTN SccEndBatch(void);  
```  
  
#### Parameters  
 None.  
  
## Return Value  
 The source control plug-in implementation of this function is expected to return one of the following values:  
  
|Value|Description|  
|-----------|-----------------|  
|SCC_OK|Batch of operations successfully concluded.|  
|SCC_E_UNKNOWNERROR|Nonspecific failure.|  
  
## Remarks  
 Source control batches are used to execute the same source control operations across multiple projects or multiple contexts. Batches can be used to eliminate redundant dialog boxes from the user experience during a batched operation. The [SccBeginBatch](../extensibility/sccbeginbatch-function.md) and the `SccEndBatch` function are used as a pair to indicate the beginning and end of an operation. They cannot be nested.  
  
## See Also  
 [Source Control Plug-in API Functions](../extensibility/source-control-plug-in-api-functions.md)   
 [SccBeginBatch](../extensibility/sccbeginbatch-function.md)