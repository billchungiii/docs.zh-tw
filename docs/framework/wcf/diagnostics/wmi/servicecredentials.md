---
title: ServiceCredentials
ms.date: 03/30/2017
ms.assetid: 9c780793-4785-46f7-add9-ac1ebeadb614
ms.openlocfilehash: 26bd0c95f930bf7859ae6409d797afbb596844fa
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2018
ms.locfileid: "50180662"
---
# <a name="servicecredentials"></a>ServiceCredentials
ServiceCredentials  
  
## <a name="syntax"></a>語法  
  
```csharp
class ServiceCredentials : Behavior  
{  
  string ClientCertificate;  
  string IssuedTokenAuthentication;  
  string Peer;  
  string SecureConversationAuthentication;  
  string ServiceCertificate;  
  string UserNameAuthentication;  
  string WindowsAuthentication;  
};  
```  
  
## <a name="methods"></a>方法  
 ServiceCredentials 類別不會定義任何方法。  
  
## <a name="properties"></a>屬性  
 ServiceCredentials 類別有下列屬性：  
  
### <a name="clientcertificate"></a>ClientCertificate  
 資料型別：字串  
  
 存取類型：唯讀  
  
 用戶端憑證驗證與此服務的佈建設定。  
  
### <a name="issuedtokenauthentication"></a>IssuedTokenAuthentication  
 資料型別：字串  
  
 存取類型：唯讀  
  
 這項服務目前發行的權杖驗證設定。  
  
### <a name="peer"></a>對等  
 資料型別：字串  
  
 存取類型：唯讀  
  
 目前的認證驗證與對等傳輸端點將使用的佈建設定。  
  
### <a name="secureconversationauthentication"></a>SecureConversationAuthentication  
 資料型別：字串  
  
 存取類型：唯讀  
  
 指定目前的安全對話設定。  
  
### <a name="servicecertificate"></a>ServiceCertificate  
 資料型別：字串  
  
 存取類型：唯讀  
  
 與這項服務關聯的憑證。  
  
### <a name="usernameauthentication"></a>UserNameAuthentication  
 資料型別：字串  
  
 存取類型：唯讀  
  
 這項服務的使用者名稱和密碼設定。  
  
### <a name="windowsauthentication"></a>WindowsAuthentication  
 資料型別：字串  
  
 存取類型：唯讀  
  
 這項服務的 Windows 驗證設定。  
  
## <a name="requirements"></a>需求  
  
|MOF|於 Servicemodel.mof 中宣告。|  
|---------|-----------------------------------|  
|命名空間|於 root\ServiceModel 中定義|  
  
## <a name="see-also"></a>另請參閱  
 <xref:System.ServiceModel.Description.ServiceCredentials>
