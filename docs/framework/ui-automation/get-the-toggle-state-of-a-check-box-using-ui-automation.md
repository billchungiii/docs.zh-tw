---
title: 使用 UI 自動化取得核取方塊的切換狀態
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- UI Automation, getting toggle states of check boxes
- check boxes, getting toggle states of
- getting, toggle states of check boxes
ms.assetid: 84fc31a3-175f-4e93-90a0-dd29d89b77ce
author: Xansky
ms.author: mhopkins
ms.openlocfilehash: ebe51247a93384ab2d269220b08a1b3f3cb22e03
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/26/2018
ms.locfileid: "47200616"
---
# <a name="get-the-toggle-state-of-a-check-box-using-ui-automation"></a>使用 UI 自動化取得核取方塊的切換狀態
> [!NOTE]
>  這份文件適用於想要使用 <xref:System.Windows.Automation> 命名空間中定義之 Managed [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 類別的 .NET Framework 開發人員。 如需最新資訊[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]，請參閱 < [Windows Automation API： 使用者介面自動化](https://go.microsoft.com/fwlink/?LinkID=156746)。  
  
 本主題說明如何使用[!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)]取得控制項的切換狀態。  
  
## <a name="example"></a>範例  
 這個範例會使用<xref:System.Windows.Automation.AutomationElement.GetCurrentPattern%2A>方法<xref:System.Windows.Automation.AutomationElement>類別來取得<xref:System.Windows.Automation.TogglePattern>物件的控制項，並傳回其<xref:System.Windows.Automation.ToggleState>屬性。  
  
 [!code-csharp[NavigatingWithTreeWalker#1200](../../../samples/snippets/csharp/VS_Snippets_Wpf/NavigatingWithTreeWalker/CSharp/ClientClass.cs#1200)]
 [!code-vb[NavigatingWithTreeWalker#1200](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/NavigatingWithTreeWalker/visualbasic/clientclass.vb#1200)]
