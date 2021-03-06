---
title: Generic Procedures in Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- generic methods [Visual Basic], type inference
- generics [Visual Basic], type inference
- procedures [Visual Basic], generic
- generic procedures
- type inference, generics
- generic methods [Visual Basic]
- type inference
- generics [Visual Basic], procedures
- generic procedures [Visual Basic], type inference
ms.assetid: 95577b28-137f-4d5c-a149-919c828600e5
ms.openlocfilehash: 9a88a979a6b46f897e5f04f4481d4a23e245b165
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/18/2018
ms.locfileid: "45969768"
---
# <a name="generic-procedures-in-visual-basic"></a>Generic Procedures in Visual Basic
A*泛型程序*，也稱為*泛型方法*，是以至少一個型別參數所定義的程序。 這可讓呼叫的程式碼，來調整使其符合需求的資料類型每次呼叫此程序。  
  
 找不到一般只要透過泛型類別或泛型結構內所定義的程序。 若要成為泛型，程序必須採取至少一個型別參數，除了任何可能需要的一般參數。 泛型類別或結構可以包含非泛型程序和非泛型類別、 結構或模組可以包含一般的程序。  
  
 泛型程序可以在其一般的參數清單中，其傳回類型，如果有的話，和其程序程式碼中使用其型別參數。  
  
## <a name="type-inference"></a>類型推斷  
 您可以呼叫泛型程序，而不需要完全提供任何類型引數。 如果您呼叫它如此一來，編譯器會嘗試判斷要傳遞至程序的類型引數的適當資料類型。 這就叫做*型別推斷*。 下列程式碼顯示的呼叫中的編譯器會推斷它應該傳遞型別`String`的型別參數`t`。  
  
 [!code-vb[VbVbalrDataTypes#15](../../../../visual-basic/language-reference/data-types/codesnippet/VisualBasic/generic-procedures_1.vb)]  
  
 如果編譯器無法推斷類型引數，從呼叫的內容，則會回報錯誤。 這類錯誤的其中一個可能的原因是陣列的陣序不符。 比方說，假設您定義一般參數的型別參數的陣列。 如果您呼叫泛型程序提供為不同陣序 （維度數目），陣列不相符會導致失敗的型別推斷。 下列程式碼顯示的呼叫中的二維陣列傳遞至預期的一維陣列的程序。  
  
```vb  
Public Sub demoSub(Of t)(ByVal arg() As t)
End Sub

Public Sub callDemoSub()
    Dim twoDimensions(,) As Integer
    demoSub(twoDimensions)
End Sub
```
  
 您可以只藉由略過所有型別引數來叫用型別推斷。 如果您提供一個類型引數時，您必須將它們全部提供。  
  
 僅針對泛型程序支援的類型推斷。 您無法叫用在泛型類別、 結構、 介面或委派的型別推斷。  
  
## <a name="example"></a>範例  
  
### <a name="description"></a>描述  
 下列範例會定義泛型`Function`尋找特定的項目陣列中的程序。 它會定義一個型別參數，並使用它來建構參數清單中的兩個參數。  
  
### <a name="code"></a>程式碼  
 [!code-vb[VbVbalrDataTypes#14](../../../../visual-basic/language-reference/data-types/codesnippet/VisualBasic/generic-procedures_2.vb)]  
  
### <a name="comments"></a>註解  
 上述範例要求可讓您比較`searchValue`針對每個元素的`searchArray`。 若要確保這項功能，它會限制型別參數`T`實作<xref:System.IComparable%601>介面。 程式碼會使用<xref:System.IComparable%601.CompareTo%2A>方法，而非`=`運算子，因為型別引數提供給不保證`T`支援`=`運算子。  
  
 您可以測試`findElement`為下列程式碼的程序。  
  
 [!code-vb[VbVbalrDataTypes#13](../../../../visual-basic/language-reference/data-types/codesnippet/VisualBasic/generic-procedures_3.vb)]  
  
 上述呼叫`MsgBox`分別顯示"0"、"1"和"-1"。  
  
## <a name="see-also"></a>另請參閱  
 [Visual Basic 中的泛型型別](../../../../visual-basic/programming-guide/language-features/data-types/generic-types.md)  
 [如何：定義可以在不同資料類型上提供完全相同功能的類別](../../../../visual-basic/programming-guide/language-features/data-types/how-to-define-a-class-that-can-provide-identical-functionality.md)  
 [如何：使用泛型類別](../../../../visual-basic/programming-guide/language-features/data-types/how-to-use-a-generic-class.md)  
 [程序](../../../../visual-basic/programming-guide/language-features/procedures/index.md)  
 [程序參數和引數](../../../../visual-basic/programming-guide/language-features/procedures/procedure-parameters-and-arguments.md)  
 [類型清單](../../../../visual-basic/language-reference/statements/type-list.md)  
 [參數清單](../../../../visual-basic/language-reference/statements/parameter-list.md)
