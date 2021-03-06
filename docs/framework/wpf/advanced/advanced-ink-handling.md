---
title: 筆墨進階處理
ms.date: 03/30/2017
f1_keywords:
- AutoGeneratedOrientationPage
helpviewer_keywords:
- System.Windows.Input.StylusPlugIns classes
- InkCanvas control [WPF]
- ink [WPF], advanced handling
ms.assetid: abc8481a-f983-416f-b051-9168ac8b2ba3
ms.openlocfilehash: eb347f5477974851e91c6a00b423bd4acf1f0b3b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/04/2018
ms.locfileid: "33539024"
---
# <a name="advanced-ink-handling"></a>筆墨進階處理
[!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]隨附<xref:System.Windows.Controls.InkCanvas>，而且您可以將它放在您的應用程式立即開始收集和顯示筆墨的項目。 不過，如果<xref:System.Windows.Controls.InkCanvas>控制項不提供細微的層級的控制，您可以藉由自訂您自己的筆墨收集和使用筆墨呈現類別維護較高的層級的控制<xref:System.Windows.Input.StylusPlugIns>。  
  
 <xref:System.Windows.Input.StylusPlugIns>類別提供一種機制，透過實作的低階控制<xref:System.Windows.Input.Stylus>輸入和動態呈現筆墨。 <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn>類別提供一個機制，讓您實作自訂行為，並將其套用至資料流的資料來自手寫筆裝置以獲得最佳效能。 <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer>，特殊<xref:System.Windows.Input.StylusPlugIns.StylusPlugIn>，可讓您自訂的動態呈現筆墨資料即時表示<xref:System.Windows.Input.StylusPlugIns.DynamicRenderer>繪製數位筆跡立即<xref:System.Windows.Input.StylusPoint>產生資料，因此它會顯示 「 傳送 」 將手寫筆裝置。  
  
## <a name="in-this-section"></a>本節內容  
 [自訂呈現筆墨](../../../../docs/framework/wpf/advanced/custom-rendering-ink.md)  
  [攔截手寫筆的輸入](../../../../docs/framework/wpf/advanced/intercepting-input-from-the-stylus.md)  
  [建立筆墨輸入控制項](../../../../docs/framework/wpf/advanced/creating-an-ink-input-control.md)  
  [筆墨執行緒模型](../../../../docs/framework/wpf/advanced/the-ink-threading-model.md)
