---
title: 如何：呼叫屬性程序 (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- Visual Basic code, procedures
- Visual Basic code, properties
- procedures [Visual Basic], calling
- properties [Visual Basic], property procedures
- procedure calls [Visual Basic], property procedures
ms.assetid: 96bc4d74-d9c3-4b7a-954d-58ac8553cd94
ms.openlocfilehash: 61d79b9ff99ec144a9c629872abd2a7e7ebda4d0
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/04/2018
ms.locfileid: "33654813"
---
# <a name="how-to-call-a-property-procedure-visual-basic"></a>如何：呼叫屬性程序 (Visual Basic)
您可以將值儲存在屬性或擷取其值呼叫屬性程序。 存取屬性相同的方式存取的變數。  
  
 屬性的`Set`程序可儲存值，並將其`Get`程序擷取的值。 不過，您沒有明確呼叫這些程序的名稱。 就如同您儲存或擷取變數的值，您可以使用指派陳述式或運算式中的屬性。 Visual Basic 會將屬性的程序呼叫。  
  
### <a name="to-call-a-propertys-get-procedure"></a>若要呼叫的屬性 Get 的程序  
  
1.  使用屬性名稱的運算式中使用變數名稱的方式相同。 您可以使用屬性您可以在任何地方使用的變數或常數。  
  
     -或-  
  
     使用下列相等的屬性名稱 (`=`) 登入指派陳述式。  
  
     下列範例會讀取的值<xref:Microsoft.VisualBasic.DateAndTime.Now%2A>屬性，以隱含方式呼叫其`Get`程序。  
  
     [!code-vb[VbVbalrDateProperties#4](./codesnippet/VisualBasic/how-to-call-a-property-procedure_1.vb)]  
  
2.  如果屬性引數，請遵循以括號來括住的引數清單的屬性名稱。 如果有任何引數，您可以選擇性地省略括號。  
  
3.  將引數放在括號，並以逗號分隔的引數清單。 請確定您提供的引數的屬性會定義的對應參數的順序相同。  
  
 屬性的值加入運算式如同變數或常數會或儲存在變數或指派陳述式左邊的屬性。  
  
### <a name="to-call-a-propertys-set-procedure"></a>呼叫屬性的設定程序  
  
1.  指派陳述式的左邊使用屬性名稱。  
  
     下列範例會設定的值<xref:Microsoft.VisualBasic.DateAndTime.TimeOfDay%2A>屬性，以隱含方式呼叫`Set`程序。  
  
     [!code-vb[VbVbcnProcedures#11](./codesnippet/VisualBasic/how-to-call-a-property-procedure_2.vb)]  
  
2.  如果屬性引數，請遵循以括號來括住的引數清單的屬性名稱。 如果有任何引數，您可以選擇性地省略括號。  
  
3.  將引數放在括號，並以逗號分隔的引數清單。 請確定您提供的引數的屬性會定義的對應參數的順序相同。  
  
 產生的指派陳述式右邊的值會儲存在屬性中。  
  
## <a name="see-also"></a>另請參閱  
 [屬性程序](./property-procedures.md)  
 [程序參數和引數](./procedure-parameters-and-arguments.md)  
 [Property 陳述式](../../../../visual-basic/language-reference/statements/property-statement.md)  
 [在 Visual Basic 中屬性和變數之間的差異](./differences-between-properties-and-variables.md)  
 [如何：建立屬性](./how-to-create-a-property.md)  
 [如何：宣告混合存取層級的屬性](./how-to-declare-a-property-with-mixed-access-levels.md)  
 [如何： 宣告及呼叫在 Visual Basic 中的預設屬性](./how-to-declare-and-call-a-default-property.md)  
 [如何：將值置入屬性](./how-to-put-a-value-in-a-property.md)  
 [如何：取得屬性值](./how-to-get-a-value-from-a-property.md)  
 [Get 陳述式](../../../../visual-basic/language-reference/statements/get-statement.md)  
 [Set 陳述式](../../../../visual-basic/language-reference/statements/set-statement.md)
