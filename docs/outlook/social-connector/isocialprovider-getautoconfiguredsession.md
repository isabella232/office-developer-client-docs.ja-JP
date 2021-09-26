---
title: ISocialProviderGetAutoConfiguredSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d8d41ced-c2bb-482e-b0bc-1b46c82121bd
description: 自動構成された ISocialSession インターフェイスを取得します。
ms.openlocfilehash: 5ed880294c12fa381b80210eb7e3fc16473ea7a4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583031"
---
# <a name="isocialprovidergetautoconfiguredsession"></a>ISocialProvider::GetAutoConfiguredSession

自動構成された [ISocialSession](isocialsessioniunknown.md) インターフェイスを取得します。 
  
```cpp
HRESULT _stdcall GetAutoConfiguredSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a>パラメーター

_session_
  
> [out] **ISocialSession** インターフェイス。 
    
## <a name="remarks"></a>注釈

返される **ISocialSession** インターフェイスは、プロバイダー固有のメソッドに基づき、自動的にネットワークにログオンされます。 
  
ソーシャル ネットワークで自動構成をサポートしていない場合、プロバイダーは OSC_E_NOT_IMPLEMENTED エラーを返す必要があります。 エラー コードの詳細については、「[Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md)」を参照してください。
  
## <a name="see-also"></a>関連項目

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

