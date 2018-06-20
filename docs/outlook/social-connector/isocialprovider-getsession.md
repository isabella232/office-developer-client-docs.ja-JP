---
title: ISocialProviderGetSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 371b48c5-6d77-4d2d-890c-bb234c7eaabc
description: ISocialSession インターフェイスを取得します。
ms.openlocfilehash: 59e6f61e1954f64d875c6336b211dcb530100252
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804368"
---
# <a name="isocialprovidergetsession"></a>ISocialProvider::GetSession

[ISocialSession](isocialsessioniunknown.md)インターフェイスを取得します。 
  
```cpp
HRESULT _stdcall GetSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a>Parameters

_セッション_
  
> [out]**ISocialSession**インターフェイスです。 
    
## <a name="remarks"></a>備考

Outlook ソーシャル コネクタ (OSC) では、ソーシャル ネットワークにログオンするのには、 **ISocialSession**インターフェイスを使用します。 
  
## <a name="see-also"></a>関連項目

- [ISocialProvider: IUnknown](isocialprovideriunknown.md)

