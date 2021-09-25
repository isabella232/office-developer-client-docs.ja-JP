---
title: ISocialProviderGetSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 371b48c5-6d77-4d2d-890c-bb234c7eaabc
description: ISocialSession インターフェイスを取得します。
ms.openlocfilehash: b26d02622ee4debe1136c3840d20e93648c69d25
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629138"
---
# <a name="isocialprovidergetsession"></a>ISocialProvider::GetSession

[ISocialSession インターフェイスを取得](isocialsessioniunknown.md)します。 
  
```cpp
HRESULT _stdcall GetSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a>パラメーター

_session_
  
> [out] **ISocialSession** インターフェイス。 
    
## <a name="remarks"></a>注釈

ソーシャル Outlook (OSC) は **、ISocialSession** インターフェイスを使用してソーシャル ネットワークにログオンします。 
  
## <a name="see-also"></a>関連項目

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

