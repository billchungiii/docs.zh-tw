---
title: get - C# 參考
ms.custom: seodec18
ms.date: 03/10/2017
f1_keywords:
- get_CSharpKeyword
- get
helpviewer_keywords:
- get keyword [C#]
ms.assetid: a52de048-fbe0-41b0-82ec-8e4ac04d3a71
ms.openlocfilehash: e3cd4779b4f865c4c9bb46d4f25819c863de8bc2
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/11/2018
ms.locfileid: "53240030"
---
# <a name="get-c-reference"></a>get (C# 參考)

`get` 關鍵字會在屬性或索引子中定義「存取子」方法，以傳回屬性值或索引子項目。 如需詳細資訊，請參閱[屬性](../../../csharp/programming-guide/classes-and-structs/properties.md)、[自動實作的屬性](../../../csharp/programming-guide/classes-and-structs/auto-implemented-properties.md)和[索引子](../../../csharp/programming-guide/indexers/index.md)。  
  
下列範例會為名為 `Seconds` 的屬性定義 `get` 和 `set` 存取子。 它使用名為 `_seconds` 的私用欄位來支援屬性值。  
 
 [!code-csharp[get#1](../../../../samples/snippets/csharp/language-reference/keywords/get/get-1.cs)]  
  
`get` 存取子通常是由傳回值的單一陳述式所組成，如上述範例所示。 從 C# 7.0 開始，您可以將 `get` 存取子實作為運算式主體成員。 下列範例會將 `get` 和 `set` 存取子實作為運算式主體成員。

 [!code-csharp[get#3](../../../../samples/snippets/csharp/language-reference/keywords/get/get-3.cs)]   
 
如果屬性的 `get` 和 `set` 存取子只會設定或擷取私用支援欄位中的值，而不會執行其他作業，則在此簡單的情況下，您可以利用 C# 編譯器的自動實作屬性支援。 下列程式碼範例會將 `Hours` 實作為自動實作屬性。 
  
 [!code-csharp[get#2](../../../../samples/snippets/csharp/language-reference/keywords/get/get-2.cs)]  
  
## <a name="c-language-specification"></a>C# 語言規格

 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>請參閱

- [C# 參考](../../../csharp/language-reference/index.md)  
- [C# 程式設計指南](../../../csharp/programming-guide/index.md)  
- [C# 關鍵字](../../../csharp/language-reference/keywords/index.md)
- [屬性](../../../csharp/programming-guide/classes-and-structs/properties.md)
