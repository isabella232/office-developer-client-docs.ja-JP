---
title: ISocialProviderGetAutoConfiguredSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8d41ced-c2bb-482e-b0bc-1b46c82121bd
description: 自動的に構成されている ISocialSession インターフェイスを取得します。
ms.openlocfilehash: 7108a7e42e9b54e069d8d420283c1ebad3367830
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804374"
---
# <a name="isocialprovidergetautoconfiguredsession"></a>ISocialProvider::GetAutoConfiguredSession

自動的に構成されている[ISocialSession](isocialsessioniunknown.md)インターフェイスを取得します。 
  
```cpp
HRESULT _stdcall GetAutoConfiguredSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a>Parameters

_セッション_
  
> [out]**ISocialSession**インターフェイスです。 
    
## <a name="remarks"></a>備考

返される**ISocialSession**インターフェイスは、プロバイダーに固有のメソッドに基づき、ネットワークに自動的にログオンします。 
  
プロバイダーは、ソーシャル ネットワークでは、自動構成をサポートしていない場合、OSC_E_NOT_IMPLEMENTED エラーを返す必要があります。 エラー コードの詳細については、 [Outlook ソーシャル コネクタ プロバイダーのエラー コード](outlook-social-connector-provider-error-codes.md)を参照してください。
  
## <a name="see-also"></a>関連項目

- [ISocialProvider: IUnknown](isocialprovideriunknown.md)

