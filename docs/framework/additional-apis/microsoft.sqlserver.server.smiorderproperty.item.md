---
title: SmiOrderProperty.Item 屬性 (Microsoft.SqlServer.Server)
author: douglaslMS
ms.author: douglasl
ms.date: 12/20/2018
ms.technology:
- dotnet-data
api_name:
- Microsoft.SqlServer.Server.SmiOrderProperty.Item
- Microsoft.SqlServer.Server.SmiOrderProperty.get_Item
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: c586d07e8ea0c2ac0b1efb603e8900d681fd0a91
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/09/2019
ms.locfileid: "54152661"
---
# <a name="smiorderpropertyitem-property"></a>SmiOrderProperty.Item 屬性

取得實體的資料行順序。 包含此屬性的組件有 SQLAccess.dll friend 關聯性。 它適用於 SQL server。 其他資料庫，請使用該資料庫所提供的主控機制。

## <a name="syntax"></a>語法

```csharp
internal SmiColumnOrder Item { get; }
```

## <a name="property-value"></a>屬性值

資料行順序。

## <a name="remarks"></a>備註

> [!WARNING]
> `SmiOrderProperty.Item`屬性內部，且不適合直接在您的程式碼中使用。
>
> 在生產環境應用程式中任何情況下，Microsoft 不支援這個屬性的使用。

## <a name="requirements"></a>需求

**命名空間︰** <xref:Microsoft.SqlServer.Server>

**組件：** System.Data （在 System.Data.dll 中)

**.NET framework 版本：** 自 2.0 起可用。