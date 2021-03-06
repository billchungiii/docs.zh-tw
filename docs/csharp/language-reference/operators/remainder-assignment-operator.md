---
title: '%= 運算子 - C# 參考'
ms.custom: seodec18
ms.date: 09/04/2018
f1_keywords:
- '%=_CSharpKeyword'
helpviewer_keywords:
- remainder assignment operator (%=) [C#]
- '%= assignment operator (remainder assignment) [C#]'
ms.assetid: 47e5f068-1d97-4010-bd3b-e21b5d3a77f5
ms.openlocfilehash: d0732f9578b64c894ecc1d3bb15cee11a8d5b6a3
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/11/2018
ms.locfileid: "53245557"
---
# <a name="-operator-c-reference"></a>%= 運算子 (C# 參考)

餘數指派運算子。

使用 `%=` 運算子的運算式，例如  

```csharp
x %= y
```  

相當於  

```csharp
x = x % y
```  

但只會評估 `x` 一次。
  
[餘數運算子](remainder-operator.md) `%` 會計算其運算元進行除法運算之後的餘數。 所有數值型別都支援。

如果使用者定義型別[多載](../keywords/operator.md)[餘數運算子](remainder-operator.md) `%`，餘數指派運算子 `%=` 會隱含多載。
  
下列範例示範 `%=` 運算子的用法：

[!code-csharp-interactive[%= example](~/samples/snippets/csharp/language-reference/operators/RemainderExamples.cs#3)]

## <a name="see-also"></a>另請參閱

- [C# 參考](../index.md)
- [C# 程式設計指南](../../programming-guide/index.md)
- [C# 運算子](index.md)
