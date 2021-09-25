---
title: ISocialSessionGetNetworkIdentifier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 534e404f-54c6-4d2b-a8d0-d2ee990a972f
description: 特定のソーシャル ネットワーク接続の一意のソーシャル ネットワーク識別子を表す文字列を取得します。
ms.openlocfilehash: deaaf3e3380602738e9427d403db658c0f1f62df
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560327"
---
# <a name="isocialsessiongetnetworkidentifier"></a>ISocialSession::GetNetworkIdentifier

特定のソーシャル ネットワーク接続の一意のソーシャル ネットワーク識別子を表す文字列を取得します。 
  
```cpp
HRESULT _stdcall GetNetworkIdentifier([out, retval] BSTR* networkIdentifier);
```

## <a name="parameters"></a>パラメーター

_networkIdentifier_
  
> [out]一意のソーシャル ネットワーク識別子を含む文字列。
    
## <a name="remarks"></a>注釈

一意のネットワーク識別子は、ソーシャル コネクタ (OSC) プロバイダー Outlookを識別する文字列です。 このメソッドは、このメソッドをE_NOTIMPL。
  
## <a name="see-also"></a>関連項目

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

