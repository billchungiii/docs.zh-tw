---
title: '&lt;BaseAddresses&gt;'
ms.date: 03/30/2017
ms.assetid: 78918102-2898-46e0-9ea8-6b8afe65603e
ms.openlocfilehash: 0af5dee41c6adf560c90874e6e9a44b62c5decc6
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/09/2019
ms.locfileid: "54147344"
---
# <a name="ltbaseaddressesgt"></a>&lt;BaseAddresses&gt;
代表 `baseAddress` 項目的集合，這些項目是自我裝載環境中之服務主機的基底位址。 如果基底位址存在，即可以相對於基底位址的位址設定端點。  
  
 \<system.ServiceModel>  
\<用戶端 >  
\<端點 >  
\<主控件 >  
\<baseAddresses >  
  
## <a name="syntax"></a>語法  
  
```xml  
<baseAddresses>
  <add baseAddress="string" />
</baseAddresses>
```  
  
## <a name="type"></a>類型  
 `Type`  
  
## <a name="attributes-and-elements"></a>屬性和項目  
 下列各節描述屬性、子項目和父項目。  
  
### <a name="attributes"></a>屬性  
 無。  
  
### <a name="child-elements"></a>子元素  
  
|項目|描述|  
|-------------|-----------------|  
|[\<add>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-baseaddresses.md)|指定由服務主機使用之基底位址的組態項目。|  
  
### <a name="parent-elements"></a>父項目  
  
|項目|描述|  
|-------------|-----------------|  
|[\<主控件 >](../../../../../docs/framework/configure-apps/file-schema/wcf/host.md)|指定服務主機設定的組態項目。|  
  
## <a name="see-also"></a>另請參閱  
 <xref:System.ServiceModel.Configuration.HostElement>  
 <xref:System.ServiceModel.ServiceHost>  
 <xref:System.ServiceModel.ServiceHostBase.BaseAddresses%2A>  
 [裝載](../../../../../docs/framework/wcf/feature-details/hosting.md)
