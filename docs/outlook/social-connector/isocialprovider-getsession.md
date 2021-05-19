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
ms.openlocfilehash: afa13bddd5cbbc53081f6ae7ddcc1671d1c40303
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419549"
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

