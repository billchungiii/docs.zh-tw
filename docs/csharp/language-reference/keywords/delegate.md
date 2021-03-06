---
title: delegate - C# 參考
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- delegate_CSharpKeyword
- delegate
- CS0123
helpviewer_keywords:
- delegate keyword [C#]
- function pointers [C#]
ms.assetid: 0bb8cb6d-2f87-47c7-9d1f-d65c1cd01e9f
ms.openlocfilehash: 233b0255121cf6e7a5283041d594e2d843f105fb
ms.sourcegitcommit: d6e419f9d9cd7e8f21ebf5acde6d016c16332579
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2018
ms.locfileid: "53286464"
---
# <a name="delegate-c-reference"></a>delegate (C# 參考)

委派類型的宣告類似方法簽章。 它具有傳回值以及任意類型之任何數目的參數：

```csharp
public delegate void TestDelegate(string message);
public delegate int TestDelegate(MyType m, long num);
```

`delegate` 是可用來封裝具名或匿名方法的參考型別。 委派類似 C++ 中的函式指標，但委派是型別安全而且安全的。 如需委派的應用程式，請參閱[委派](../../../csharp/programming-guide/delegates/index.md)和[泛型委派](../../../csharp/programming-guide/generics/generic-delegates.md)。

## <a name="remarks"></a>備註

委派是[事件](../../../csharp/programming-guide/events/index.md)的基礎。

委派的具現化方式是將它與具名或匿名方法建立關聯。 如需詳細資訊，請參閱[具名方法](../../../csharp/programming-guide/delegates/delegates-with-named-vs-anonymous-methods.md)和[匿名方法](../../../csharp/programming-guide/statements-expressions-operators/anonymous-methods.md)。

委派必須使用具有相容傳回型別和輸入參數的方法或 Lambda 運算式進行具現化。 如需方法簽章中所允許變異程度的詳細資訊，請參閱 [Variance in Delegates](../../programming-guide/concepts/covariance-contravariance/using-variance-in-delegates.md) (委派中的變異數)。 若與匿名方法搭配使用，則會一起宣告要與它建立關聯的委派和程式碼。 本節討論兩種具現化委派的方式。

## <a name="example"></a>範例

[!code-csharp[csrefKeywordsTypes#8](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/keywordsTypes.cs#8)]

## <a name="c-language-specification"></a>C# 語言規格

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>另請參閱

- [C# 參考](../../../csharp/language-reference/index.md)  
- [C# 程式設計指南](../../../csharp/programming-guide/index.md)  
- [C# 關鍵字](../../../csharp/language-reference/keywords/index.md)  
- [參考型別](../../../csharp/language-reference/keywords/reference-types.md)  
- [委派](../../../csharp/programming-guide/delegates/index.md)  
- [事件](../../../csharp/programming-guide/events/index.md)  
- [具名方法委派與匿名方法委派](../../../csharp/programming-guide/delegates/delegates-with-named-vs-anonymous-methods.md) 
- [匿名方法](../../../csharp/programming-guide/statements-expressions-operators/anonymous-methods.md)
- [Lambda 運算式](../../../csharp/programming-guide/statements-expressions-operators/lambda-expressions.md)
