---
title: exceptionSwallowedOnCallFromCom MDA
ms.date: 03/30/2017
helpviewer_keywords:
- messages, informational
- informational messages
- managed debugging assistants (MDAs), exceptions
- exception handling, managed debugging assistants
- MDAs (managed debugging assistants), exceptions
- ExceptionSwallowedOnCallFromCOM MDA
ms.assetid: 55d6ab12-f251-4aab-aa64-aacbe9d9f974
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b4c1cbf075ef96073061679b6d062075490f5e4e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/04/2018
ms.locfileid: "33390604"
---
# <a name="exceptionswallowedoncallfromcom-mda"></a>exceptionSwallowedOnCallFromCom MDA
透過不含 Unmanaged HRESULT 傳回類型的方法，從 COM 呼叫的通用語言執行平台 (CLR) 擲回例外狀況時，就會啟用 `exceptionSwallowedOnCallFromCOM` Managed 偵錯助理 (MDA)。  
  
## <a name="symptoms"></a>徵兆  
 從 COM 呼叫 Managed 元件時，傳回的值為 FALSE 或 0。 或者，如果方法具有 void 傳回類型，執行方法期間可能不會指出已擲回例外狀況。 在這種情況下，會以無訊息模式攔截例外狀況，而執行作業會返回 COM 呼叫端。  
  
## <a name="cause"></a>原因  
 已擲回例外狀況，但沒有有效的方式來進行提報。  
  
## <a name="resolution"></a>解決方式  
 僅供參考，不一定表示有 Bug。  
  
## <a name="effect-on-the-runtime"></a>對執行階段的影響  
 此 MDA 對 CLR 沒有影響。 它只會提報以無訊息模式攔截例外狀況的相關資料。  
  
## <a name="output"></a>輸出  
 告知性訊息，包含方法名稱、類型名稱和例外狀況訊息。  
  
## <a name="configuration"></a>組態  
  
```xml  
<mdaConfig>  
  <assistants>  
    <exceptionSwallowedOnCallFromCom />  
  </assistants>  
</mdaConfig>  
```  
  
## <a name="see-also"></a>另請參閱  
 <xref:System.Runtime.InteropServices.MarshalAsAttribute>  
 [診斷 Managed 偵錯助理的錯誤](../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)  
 [Interop 封送處理](../../../docs/framework/interop/interop-marshaling.md)
