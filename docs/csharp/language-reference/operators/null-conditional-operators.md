---
title: Null 條件運算子 - C# 參考
ms.custom: seodec18
ms.date: 04/03/2015
helpviewer_keywords:
- null-conditional operators [C#]
- ?. operator [C#]
- ?[] operator [C#]
ms.assetid: 9c7b2c8f-a785-44ca-836c-407bfb6d27f5
ms.openlocfilehash: 4189b07fd280192a4cb39400e4e77cef702c9d08
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/11/2018
ms.locfileid: "53239549"
---
# <a name="-and--null-conditional-operators-c-and-visual-basic"></a>?. and ?[] Null 條件運算子 (C# 和 Visual Basic)
在執行成員存取 (`?.`) 或索引 (`?[]`) 運算之前，測試左運算元的值是否為 null；如果左運算元評估為 `null`，則傳回 `null`。 

這些運算子可協助您撰寫較少的程式碼來處理 Null 檢查，特別是遞減至資料結構。  
  
```csharp  
int? length = customers?.Length; // null if customers is null   
Customer first = customers?[0];  // null if customers is null  
int? count = customers?[0]?.Orders?.Count();  // null if customers, the first customer, or Orders is null  
```  
  
 Null 條件運算子會執行最少運算。  如果條件式成員存取和索引作業鏈結中的一個作業傳回 Null，則鏈結的其餘部分會停止執行。  在下列範例中，如果 `A`、`B` 或 `C` 的計算結果為 Null，則不會執行 `E`。
  
```csharp
A?.B?.C?.Do(E);
A?.B?.C?[E];
```

 Null 條件成員存取的另一個用法是，使用更少的程式碼以執行緒安全的方式叫用委派。  舊方法需要如下的程式碼：  
  
```csharp  
var handler = this.PropertyChanged;  
if (handler != null)  
    handler(…);
```  
  
  
 新方法則更簡單：  
  
```csharp
PropertyChanged?.Invoke(…)  
```  

 新的方法可以保障執行緒安全，因為編譯器產生的程式碼只會評估 `PropertyChanged` 一次，並將結果保留在暫存變數中。 由於沒有 Null 條件式委派引動過程語法 `PropertyChanged?(e)`，因此您必須明確呼叫 `Invoke` 方法。  
  
## <a name="language-specifications"></a>語言規格  

如需詳細資訊，請參閱 [C# 語言規格](../language-specification/index.md)的 [Null 條件運算子](~/_csharplang/spec/expressions.md#null-conditional-operator)。 語言規格是 C# 語法及用法的限定來源。
  
## <a name="see-also"></a>請參閱

- [?? (Null 聯合運算子)](null-coalescing-operator.md)  
- [C# 參考](../../../csharp/language-reference/index.md)  
- [C# 程式設計指南](../../../csharp/programming-guide/index.md)  
