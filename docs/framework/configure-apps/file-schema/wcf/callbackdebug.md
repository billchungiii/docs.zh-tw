---
title: '&lt;callbackDebug&gt;'
ms.date: 03/30/2017
ms.assetid: 4073feda-1857-4be4-9947-227afb847ced
ms.openlocfilehash: 5bd2356c3bb798e948341cb3c4ba504ac886ed44
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/09/2019
ms.locfileid: "54145077"
---
# <a name="ltcallbackdebuggt"></a>&lt;callbackDebug&gt;
指定 Windows Communication Foundation (WCF) 回呼物件的偵錯服務。  
  
 \<system.ServiceModel>  
\<行為 >  
\<endpointBehaviors>  
\<行為 >  
\<callbackDebug >  
  
## <a name="syntax"></a>語法  
  
```xml  
<callbackDebug includeExceptionDetailInFaults="Boolean" />
```  
  
## <a name="type"></a>類型  
 `Type`  
  
## <a name="attributes-and-elements"></a>屬性和項目  
 下列各節描述屬性、子項目和父項目。  
  
### <a name="attributes"></a>屬性  
  
|屬性|描述|  
|---------------|-----------------|  
|`includeExceptionDetailInFaults`|這個值會指定用戶端回呼物件是否將 SOAP 錯誤中的 Managed 例外狀況資訊傳回給服務。<br /><br /> 如果您以程式設計方式將這個屬性設定為 `true`，您可以讓用戶端回呼物件中的 Managed 例外狀況資訊的流動回到服務，以達偵錯的目的。 **注意：** 將 Managed 例外狀況資訊傳回用戶端時，可能會有安全性風險。 這是因為例外狀況細節會公開內部服務實作 (Implementation) 的相關資訊，可能會被未經授權的用戶端加以利用。|  
  
### <a name="child-elements"></a>子元素  
 無。  
  
### <a name="parent-elements"></a>父項目  
  
|項目|描述|  
|-------------|-----------------|  
|[\<行為 >](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|指定端點行為。|  
  
## <a name="see-also"></a>另請參閱  
 <xref:System.ServiceModel.Configuration.CallbackDebugElement>  
 <xref:System.ServiceModel.Description.CallbackDebugBehavior>
