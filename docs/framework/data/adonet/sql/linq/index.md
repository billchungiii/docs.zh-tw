---
title: LINQ to SQL
ms.date: 03/30/2017
ms.assetid: 73d13345-eece-471a-af40-4cc7a2f11655
ms.openlocfilehash: 141505eed8e76bb5f9811b5d2bdc166885905cde
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2018
ms.locfileid: "50196826"
---
# <a name="linq-to-sql"></a>LINQ to SQL
[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 為 [!INCLUDE[dnprdnshort](../../../../../../includes/dnprdnshort-md.md)] 3.5 版的元件，它所提供的執行階段基礎結構可將關聯式資料當作物件管理。  
  
> [!NOTE]
>  關聯式資料會顯示為二維資料表 (「關聯」或「一般檔案」) 的集合，其中通用資料行會與資料表彼此相關。 若要有效地使用 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]，您必須熟悉關聯式資料庫的基礎原則。  
  
 在 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 中，關聯式資料庫的資料模型會對應至以開發人員的程式設計語言表示的物件模型。 執行應用程式時，[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 會將物件模型中的 Language Integrated Query (LINQ) 轉譯成 SQL，並將這些查詢傳送至資料庫進行執行。 當資料庫傳回結果時，[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 會將結果轉譯回您可以在自己的程式語言中處理的物件。  
  
 開發人員使用 Visual Studio 通常會使用[!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)]，以提供使用者介面實作的許多功能[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]。  
  
 這一版 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 隨附的文件會描述建置 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 應用程式所需的基本建置組塊、處理序和技巧。 您也可以搜尋 Microsoft Docs 特定問題，並可以參與[LINQ 論壇](https://go.microsoft.com/fwlink/?LinkId=76488)，您可以與專家討論更複雜的主題的詳細資料。 最後， [LINQ to SQL： 關聯式資料的.net language-integrated Query](https://go.microsoft.com/fwlink/?LinkId=93205)白皮書詳細說明[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]技術，其中包含 Visual Basic 和 C# 程式碼範例。  
  
## <a name="in-this-section"></a>本節內容  
 [快速入門](../../../../../../docs/framework/data/adonet/sql/linq/getting-started.md)  
 提供 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 的扼要概觀，以及如何著手使用 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 的相關資訊。  
  
 [程式設計手冊](../../../../../../docs/framework/data/adonet/sql/linq/programming-guide.md)  
 提供對應、查詢、更新、偵錯和類似工作的步驟。  
  
 [參考資料](../../../../../../docs/framework/data/adonet/sql/linq/reference.md)  
 提供 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 某些層面的參考資訊。 主題包含 SQL-CLR 型別對應、標準查詢運算子轉譯等等。  
  
 [範例](../../../../../../docs/framework/data/adonet/sql/linq/samples.md)  
 提供 Visual Basic 和 C# 範例的連結。  
  
## <a name="related-sections"></a>相關章節  
 [LINQ (Language-Integrated Query)](https://msdn.microsoft.com/library/a73c4aec-5d15-4e98-b962-1274021ea93d)  
 提供 [!INCLUDE[vbteclinq](../../../../../../includes/vbteclinq-md.md)] 技術的概觀。  
  
 [LINQ](../../../../../visual-basic/programming-guide/language-features/linq/index.md)  
 描述[!INCLUDE[vbteclinq](../../../../../../includes/vbteclinq-md.md)]Visual Basic 使用者的技術。  
  
 [LINQ 和 ADO.NET](../../../../../../docs/framework/data/adonet/linq-and-ado-net.md)  
 [!INCLUDE[vstecado](../../../../../../includes/vstecado-md.md)] 入口網站的連結。  
  
 [LINQ to SQL 逐步解說](https://msdn.microsoft.com/library/308e66ac-f704-4e00-9b4e-7af0045a2374)  
 列出 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 可用的逐步解說。  
  
 [下載範例資料庫](../../../../../../docs/framework/data/adonet/sql/linq/downloading-sample-databases.md)  
 描述如何下載文件中所用的範例程式庫。  
  
 [LinqDataSource 技術概觀](https://msdn.microsoft.com/library/104cfc3f-7385-47d3-8a51-830dfa791136)  
 描述 <xref:System.Web.UI.WebControls.LinqDataSource> 控制項如何透過 [!INCLUDE[vbteclinqext](../../../../../../includes/vbteclinqext-md.md)] 資料來源控制項架構，將 [!INCLUDE[vstecasp](../../../../../../includes/vstecasp-md.md)] 公開給 Web 程式開發人員。
