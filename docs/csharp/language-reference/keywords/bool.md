---
title: bool 關鍵字 - C# 參考
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- bool_CSharpKeyword
- bool
helpviewer_keywords:
- bool keyword [C#]
ms.assetid: 551cfe35-2632-4343-af49-33ad12da08e2
ms.openlocfilehash: a274083ad2e518f8f29384e51d692bcf9a9cb61e
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/11/2018
ms.locfileid: "53237242"
---
# <a name="bool-c-reference"></a>bool (C# 參考)

`bool` 關鍵字是 <xref:System.Boolean?displayProperty=nameWithType> 的別名。 它會用來宣告可儲存布林值 [true](true-literal.md) 和 [false](false-literal.md) 的變數。

> [!NOTE]
> 如果您需要也可以有 `null` 值的布林值變數，請使用 `bool?`。 如需詳細資訊，請參閱[使用可為 Null 的型別](../../programming-guide/nullable-types/using-nullable-types.md)一文的 [bool? 型別](../../programming-guide/nullable-types/using-nullable-types.md#the-bool-type)一節。

## <a name="literals"></a>常值

您可以將布林值指派給 `bool` 變數。 您也可以將評估為 `bool` 的運算式指派給 `bool` 變數。

[!code-csharp[csrefKeywordsTypes#1](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/keywordsTypes.cs#1)]

`bool` 變數的預設值是 `false`。 `bool?` 變數的預設值是 `null`。

## <a name="conversions"></a>轉換

在 C++ 中，`bool` 類型的值可以轉換為 `int` 類型的值；換句話說，`false` 相當於零，`true` 則相當於非零值。 在 C# 中，於 `bool` 類型與其他類型之間不會進行轉換。 例如，下列 `if` 陳述式在 C# 中無效：

[!code-csharp[csrefKeywordsTypes#2](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/keywordsTypes.cs#2)]

若要測試 `int` 類型的變數，您必須明確地比較它與值 (例如零)，如下所示：

[!code-csharp[csrefKeywordsTypes#3](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/keywordsTypes.cs#3)]

## <a name="example"></a>範例

在此範例中，您使用鍵盤輸入字元，而程式會檢查輸入字元是否為字母。 如果是字母，則會檢查是小寫還是大寫。 使用 <xref:System.Char.IsLetter%2A> 和 <xref:System.Char.IsLower%2A> 來執行這些檢查，這兩個都會傳回 `bool` 型別：

[!code-csharp[csrefKeywordsTypes#4](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/keywordsTypes.cs#4)]

## <a name="c-language-specification"></a>C# 語言規格

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>另請參閱

- [C# 參考](../../../csharp/language-reference/index.md)  
- [C# 程式設計指南](../../../csharp/programming-guide/index.md)  
- [C# 關鍵字](../../../csharp/language-reference/keywords/index.md)  
- [整數型別表](../../../csharp/language-reference/keywords/integral-types-table.md)  
- [內建型別表](../../../csharp/language-reference/keywords/built-in-types-table.md)  
- [隱含數值轉換表](../../../csharp/language-reference/keywords/implicit-numeric-conversions-table.md)  
- [明確數值轉換表](../../../csharp/language-reference/keywords/explicit-numeric-conversions-table.md)  