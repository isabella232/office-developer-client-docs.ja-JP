---
title: ISocialProviderGetAutoConfiguredSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8d41ced-c2bb-482e-b0bc-1b46c82121bd
description: 自動構成された ISocialSession インターフェイスを取得します。
ms.openlocfilehash: 34f048158a484612b92bcd2750401caecda64ba2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285780"
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

