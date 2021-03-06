---
title: '&lt;standardEndpoints&gt;'
ms.date: 03/30/2017
ms.assetid: d62153d7-a6e6-462a-a784-cca61e9c2ba1
ms.openlocfilehash: 623eafbc585492333d7b342aeeeb0844000bd012
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/09/2019
ms.locfileid: "54150925"
---
# <a name="ltstandardendpointsgt"></a>&lt;standardEndpoints&gt;
這個組態區段可讓您定義標準端點的集合，這些端點是可重複使用的預先設定端點。 標準端點會有一個或多個位址、繫結，以及設為固定值的合約屬性。 例如，探索端點中的合約是固定的。 您也可以使用標準端點，以類似定義自訂繫結的新屬性擴充服務端點。  
  
 \<system.ServiceModel>  
  
## <a name="syntax"></a>語法  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a>屬性和項目  
 下列各節描述屬性、子項目和父項目。  
  
### <a name="attributes"></a>屬性  
 無。  
  
### <a name="child-elements"></a>子元素  
  
|項目|描述|  
|-------------|-----------------|  
|[\<announcementEndpoint >](../../../../../docs/framework/configure-apps/file-schema/wcf/announcementendpoint.md)|定義具有固定公告合約的標準端點。 服務可以選擇性地公告其可用性，方法是分別在開啟與關閉該服務時傳送線上及離線公告訊息。 Windows Communication Foundation (WCF) 服務指定公告端點，在[ \<serviceDiscovery >](../../../../../docs/framework/configure-apps/file-schema/wcf/servicediscovery.md)項目，並且使用 AnnouncementClient 來執行公告。 想要從其他服務公告所接聽的用戶端實際上做為 WCF 服務;因此您必須在該用戶端設定公告端點[ \<services >](../../../../../docs/framework/configure-apps/file-schema/wcf/services.md)一節。|  
|[\<discoveryEndpoint >](../../../../../docs/framework/configure-apps/file-schema/wcf/discoveryendpoint.md)|定義具有固定探索合約的標準端點。 加入至服務組態時，此組態項目會指定接聽探索訊息的位置。 加入至用戶端組態時，此組態項目會指定傳送探索查詢的位置。|  
|[\<dynamicEndpoint >](../../../../../docs/framework/configure-apps/file-schema/wcf/dynamicendpoint.md)|這個組態項目定義標準端點，其中包含的資訊可讓您啟用應用程式做為用戶端程式，在執行階段時動態尋找端點位址。|  
|[\<mexEndpoint >](../../../../../docs/framework/configure-apps/file-schema/wcf/mexendpoint.md)|定義具有固定 IMetadataExchange 合約的標準端點。 由於所有中繼資料交換端點都指定 IMetadataExchange 做為它們的合約，因此您可以使用這個標準端點，而不需自行定義端點。|  
|[\<udpAnnoucementEndpoint >](../../../../../docs/framework/configure-apps/file-schema/wcf/udpannoucementendpoint.md)|定義標準端點，此端點可為在 UDP 繫結上傳送公告訊息的服務使用。 此端點具備固定合約，而且支援兩種探索版本。 此外，它擁有固定的 UDP 繫結和預設位址值，如 WS-Discovery 規格 (WS-Discovery 2005 年 4 月或 WS-Discovery 1.1 版) 中所指定。 您可以指定傳送及接收公告訊息時所使用的多點傳送位址。|  
|[\<udpDiscoveryEndpoint >](../../../../../docs/framework/configure-apps/file-schema/wcf/udpdiscoveryendpoint.md)|定義標準端點，該端點已預先設定透過 UDP 多點傳送繫結進行探索作業。 此端點具備固定合約，而且支援兩種 WS-Discovery 通訊協定版本。 此外，它擁有固定的 UDP 繫結和預設位址，如 WS-Discovery 規格 (WS-Discovery 2005 年 4 月或 WS-Discovery V1.1) 中所指定。|  
|[\<webHttpEndpoint >](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpendpoint.md)|定義具有固定的標準端點[ \<webHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md)繫結，會自動加入[ \<webHttp >](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttp.md)行為。 撰寫 REST 服務時，請使用這個端點。|  
|[\<webScriptEndpoint >](../../../../../docs/framework/configure-apps/file-schema/wcf/webscriptendpoint.md)|定義具有固定的標準端點[ \<webHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttpbinding.md)繫結，會自動加入[ \<Enablewebscript&gt >](../../../../../docs/framework/configure-apps/file-schema/wcf/enablewebscript.md)行為。 撰寫從 ASP.NET AJAX 應用程式呼叫的服務時，請使用這個端點。|  
|[\<workflowControlEndpoint >](../../../../../docs/framework/configure-apps/file-schema/wcf/workflowcontrolendpoint.md)|定義一個標準端點，用於控制工作流程執行個體 (建立、執行、暫停、終止等) 的執行。|  
  
### <a name="parent-elements"></a>父項目  
  
|項目|描述|  
|-------------|-----------------|  
|\<system.ServiceModel>|所有 WCF 組態項目的根項目。|  
  
## <a name="see-also"></a>另請參閱  
 [標準端點](../../../../../docs/framework/wcf/feature-details/standard-endpoints.md)
