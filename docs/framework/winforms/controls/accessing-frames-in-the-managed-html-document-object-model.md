---
title: 存取 Managed HTML 文件物件模型中的框架
ms.date: 03/30/2017
helpviewer_keywords:
- HTML [Windows Forms], dOM
- managed HTML DOM
- HTML [Windows Forms], managed
- HTML DOM [Windows Forms], managed
- frames [Windows Forms], accessing
- DOM [Windows Forms], accessing frames in managed HTML
ms.assetid: cdeeaa22-0be4-4bbf-9a75-4ddc79199f8d
ms.openlocfilehash: b1a858e88ff27de19e2ebbd69c14060813873c13
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2018
ms.locfileid: "49308483"
---
# <a name="accessing-frames-in-the-managed-html-document-object-model"></a>存取 Managed HTML 文件物件模型中的框架
某些 HTML 文件包含*框架*，或可以保存自己的相異 HTML 文件的 windows。 使用框架可讓您輕鬆地建立 HTML 網頁，該 HTML 網頁的其中一個或多個頁面片段維持靜態，例如導覽列，而其他框架則不斷變更其內容。  
  
 HTML 作者可以用兩種方法之一來建立框架：  
  
-   使用 `FRAMESET` 和 `FRAME` 標記，這會建立固定的視窗。  
  
 -或-  
  
-   使用 `IFRAME` 標記，這會建立可以在執行階段中重新定位的浮動視窗。  
  
1.  因為框架包含 HTML 文件，它們會在文件物件模型 (DOM) 中顯示為視窗項目和框架項目。  
  
2.  當您使用 <xref:System.Windows.Forms.HtmlWindow> 的框架集合存取 `FRAME` 或 `IFRAME` 標記時，您會擷取對應至框架的視窗項目。 這代表框架的所有動態屬性，例如其目前的 URL、文件及大小。  
  
3.  當您使用 <xref:System.Windows.Forms.HtmlWindow> 的 <xref:System.Windows.Forms.HtmlWindow.WindowFrameElement%2A> 屬性、<xref:System.Windows.Forms.HtmlElement.Children%2A> 集合，或例如 <xref:System.Windows.Forms.HtmlElementCollection.GetElementsByName%2A> 或 <xref:System.Windows.Forms.HtmlDocument.GetElementById%2A> 等方法存取 `FRAME` 或 `IFRAME` 標記時，您會擷取框架項目。 這代表框架的靜態屬性，包括在原始 HTML 檔案中指定的 URL。  
  
## <a name="frames-and-security"></a>框架和安全性  
 框架的存取之所以複雜，managed 的 HTML DOM 實作稱為安全性量值的事實*跨框架指令碼安全性*。 如果文件包含 `FRAMESET` 與不同網域中的兩個或更多 `FRAME`，這些 `FRAME` 無法彼此互動。 亦即`FRAME`顯示內容，從您的網站無法存取中的資訊`FRAME`這類裝載協力廠商網站`http://www.adatum.com/`。 此安全性實作是屬於 <xref:System.Windows.Forms.HtmlWindow> 類別的層級。 您可以取得關於裝載另一個網站之 `FRAME` 的一般資訊，例如它的 URL，但您將無法存取其 <xref:System.Windows.Forms.HtmlWindow.Document%2A> 或變更其裝載 `FRAME` 或 `IFRAME` 的大小或位置。  
  
 此規則也適用於以 <xref:System.Windows.Forms.HtmlWindow.Open%2A> 和 <xref:System.Windows.Forms.HtmlWindow.OpenNew%2A> 方法開啟的視窗。 如果您開啟的視窗位於與 <xref:System.Windows.Forms.WebBrowser> 控制項中裝載頁面不同的網域，則您將無法移動該視窗，或檢查其內容。 如果您使用 <xref:System.Windows.Forms.WebBrowser> 控制項來顯示與用來部署 Windows Form 應用程式的網站不同的網站，也會強制這些限制。 如果您使用 [!INCLUDE[ndptecclick](../../../../includes/ndptecclick-md.md)] 部署技術，從網站 A 安裝應用程式，而且您使用 <xref:System.Windows.Forms.WebBrowser> 來顯示網站 B，則您將無法存取網站 B 的資料。  
  
 如需有關跨網站指令碼的詳細資訊，請參閱[關於跨框架指令碼和安全性](https://msdn.microsoft.com/library/ms533028.aspx)。  
  
## <a name="see-also"></a>另請參閱  
 [框架項目&#124;框架物件](https://msdn.microsoft.com/library/ms535250.aspx)  
 [使用 Managed HTML 文件物件模型](../../../../docs/framework/winforms/controls/using-the-managed-html-document-object-model.md)
