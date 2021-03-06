---
title: 如何：測試 UserControl 的執行階段行為
ms.date: 03/30/2017
helpviewer_keywords:
- UserControl class [Windows Forms], testing
- user controls [Windows Forms], testing
- composite controls [Windows Forms], testing
- UserControl Test Container
- UserControl class [Windows Forms], run-time behavior
ms.assetid: 4e4d5c49-1346-40ac-9d96-40211b573583
ms.openlocfilehash: 40ec136a86b52dcb007d15d5a2917212745961f2
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/04/2018
ms.locfileid: "43512205"
---
# <a name="how-to-test-the-run-time-behavior-of-a-usercontrol"></a>如何：測試 UserControl 的執行階段行為
當您開發<xref:System.Windows.Forms.UserControl>，您要測試其執行階段行為。 您可以建立個別的 Windows 應用程式專案，並將您的控制項上測試表單中，但此程序是很不方便。 更快速且輕鬆的方式是使用**UserControl 測試容器**Visual Studio 所提供。 直接從您的 Windows 控制項程式庫專案，啟動這個測試容器。  
  
> [!IMPORTANT]
>  載入測試容器您<xref:System.Windows.Forms.UserControl>，控制項必須有至少一個公用建構函式。  
  
> [!NOTE]
>  根據您目前使用的設定或版本，您所看到的對話方塊與功能表命令可能會與 [說明] 中描述的不同。 若要變更設定，請從 [ **工具** ] 功能表中選取 [ **匯入和匯出設定** ]。 如需詳細資訊，請參閱[將 Visual Studio IDE 個人化](/visualstudio/ide/personalizing-the-visual-studio-ide)。  
  
> [!NOTE]
>  無法使用測試的 Visual c + + 控制項**UserControl 測試容器**。  
  
### <a name="to-test-the-run-time-behavior-of-a-usercontrol"></a>若要測試 UserControl 的執行階段行為  
  
1.  建立 Windows 控制項程式庫專案，稱為**TestContainerExample**。 如需詳細資訊，請參閱 < [Windows 控制項程式庫範本](https://msdn.microsoft.com/library/722f4e2d-1310-4ed5-8f33-593337ab66b4)。  
  
2.  在  **Windows Form 設計工具**，拖曳<xref:System.Windows.Forms.Label>控制項從**工具箱**拖曳至控制項的設計介面。  
  
3.  按 F5 以建置專案並執行**UserControl 測試容器**。 測試容器會顯示您<xref:System.Windows.Forms.UserControl>中**預覽**窗格。  
  
4.  選取 <xref:System.Windows.Forms.Control.BackColor%2A>中顯示的屬性<xref:System.Windows.Forms.PropertyGrid>右邊的控制項**預覽**窗格。 變更其值， `ControlDark`。 請注意，控制項就會變更為較深的色彩。 請嘗試變更其他屬性值，並觀察您的控制項上的效果。  
  
5.  按一下 **填滿使用者控制項的停駐**下方的核取方塊**預覽**窗格。 請注意，調整大小以填滿窗格的控制項。 調整測試容器的大小，並觀察調整與窗格控制項大小。  
  
6.  關閉測試容器。  
  
7.  將另一個使用者控制項加入**TestContainerExample**專案。 如需詳細資訊，請參閱 < [NIB： 如何： 加入現有項目加入至專案](https://msdn.microsoft.com/library/15f4cfb7-78ab-457f-9f14-099a25a6a2d3)。  
  
8.  在  **Windows Form 設計工具**，拖曳<xref:System.Windows.Forms.Button>控制項從**工具箱**拖曳至控制項的設計介面。  
  
9. 按 F5 以建置專案，並執行測試容器。  
  
10. 按一下 **選取 使用者控制項**<xref:System.Windows.Forms.ComboBox>切換兩個使用者控制項。  
  
## <a name="testing-user-controls-from-another-project"></a>從另一個專案的測試使用者控制項  
 您可以在目前專案的測試容器測試從其他專案的使用者控制項。  
  
#### <a name="to-test-user-controls-from-another-project"></a>若要測試另一個專案中的使用者控制項  
  
1.  建立 Windows 控制項程式庫專案，稱為**TestContainerExample2**。 如需詳細資訊，請參閱 < [Windows 控制項程式庫範本](https://msdn.microsoft.com/library/722f4e2d-1310-4ed5-8f33-593337ab66b4)。  
  
2.  在  **Windows Form 設計工具**，拖曳<xref:System.Windows.Forms.RadioButton>控制項從**工具箱**拖曳至控制項的設計介面。  
  
3.  按 F5 以建置專案，並執行測試容器。 測試容器會顯示您<xref:System.Windows.Forms.UserControl>中**預覽**窗格。  
  
4.  按一下 [**負載**] 按鈕。  
  
5.  在 **開放**對話方塊方塊中，瀏覽至**TestContainerExample**.dll，您在上一個程序中建立。 選取  **TestContainerExample**.dll，然後按一下**開啟**載入使用者控制項的按鈕  
  
6.  使用**選取 使用者控制項**<xref:System.Windows.Forms.ComboBox>切換兩個使用者控制項，從**TestContainerExample**專案。  
  
## <a name="see-also"></a>另請參閱  
 <xref:System.Windows.Forms.UserControl>  
 [操作說明：撰寫複合控制項](../../../../docs/framework/winforms/controls/how-to-author-composite-controls.md)  
 [逐步解說：使用 Visual Basic 撰寫複合控制項](../../../../docs/framework/winforms/controls/walkthrough-authoring-a-composite-control-with-visual-basic.md)  
 [逐步解說：使用 Visual C# 撰寫複合控制項](../../../../docs/framework/winforms/controls/walkthrough-authoring-a-composite-control-with-visual-csharp.md)  
 [使用者控制項設計工具](https://msdn.microsoft.com/library/2abb9eec-ba32-45cb-b73d-8b52a8bd6bf1)
