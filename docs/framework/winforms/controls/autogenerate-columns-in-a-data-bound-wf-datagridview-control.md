---
title: 如何：在資料繫結 Windows Form DataGridView 控制項中自動產生資料行
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data grids [Windows Forms], autogenerating columns
- columns [Windows Forms], autogenerating
- DataGridView control [Windows Forms], data-bound columns
ms.assetid: 699f6f9e-6aa5-4811-902b-6a2c57dec7d6
ms.openlocfilehash: 97fbc2c21f618b9fa0451c17ebf87579f51a3f0d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/04/2018
ms.locfileid: "33524383"
---
# <a name="how-to-autogenerate-columns-in-a-data-bound-windows-forms-datagridview-control"></a>如何：在資料繫結 Windows Form DataGridView 控制項中自動產生資料行
下列程式碼範例示範如何顯示資料行中的繫結的資料來源從<xref:System.Windows.Forms.DataGridView>控制項。 當<xref:System.Windows.Forms.DataGridView.AutoGenerateColumns%2A>屬性值是`true`（預設）、<xref:System.Windows.Forms.DataGridViewColumn>建立每個資料行的資料來源資料表中。  
  
 如果<xref:System.Windows.Forms.DataGridView>控制項已經有資料行，當您設定<xref:System.Windows.Forms.DataGridViewComboBoxColumn.DataSource%2A>屬性，現有的繫結資料行是相較於資料來源中的資料行和相符項目時，會保留。 未繫結的資料行一定會被保留。 會移除資料來源中的沒有相符項目是繫結的資料行。 在控制項中的沒有相符項目是資料來源中的資料行產生新的<xref:System.Windows.Forms.DataGridViewColumn>物件加入至結尾<xref:System.Windows.Forms.DataGridView.Columns%2A>集合。  
  
## <a name="example"></a>範例  
 [!code-csharp[System.Windows.Forms.DataGridViewMisc#020](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#020)]
 [!code-vb[System.Windows.Forms.DataGridViewMisc#020](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#020)]  
  
## <a name="compiling-the-code"></a>編譯程式碼  
 這個範例需要：  
  
-   名為 `customersDataGridView` 的 <xref:System.Windows.Forms.DataGridView> 控制項。  
  
-   A<xref:System.Data.DataSet>名為物件`customersDataSet`具有名為的資料表`Customers`。  
  
-   <xref:System?displayProperty=nameWithType>、<xref:System.Windows.Forms?displayProperty=nameWithType>、<xref:System.Data?displayProperty=nameWithType> 和 <xref:System.Xml?displayProperty=nameWithType> 組件的參考。  
  
## <a name="see-also"></a>另請參閱  
 <xref:System.Windows.Forms.DataGridView>  
 <xref:System.Windows.Forms.DataGridView.AutoGenerateColumns%2A?displayProperty=nameWithType>  
 [在 Windows Forms DataGridView 控制項中顯示資料](../../../../docs/framework/winforms/controls/displaying-data-in-the-windows-forms-datagridview-control.md)  
 [操作說明：移除 Windows Forms DataGridView 控制項中自動產生的資料行](../../../../docs/framework/winforms/controls/remove-autogenerated-columns-from-a-wf-datagridview-control.md)
