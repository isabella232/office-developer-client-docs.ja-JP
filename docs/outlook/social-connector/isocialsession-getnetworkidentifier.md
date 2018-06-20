---
title: ISocialSessionGetNetworkIdentifier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534e404f-54c6-4d2b-a8d0-d2ee990a972f
description: 特定のソーシャル ネットワークの接続のソーシャル ネットワークの一意の識別子を表す文字列を取得します。
ms.openlocfilehash: eb618ba8e8bb37278c1fdb09d984fba141a9d686
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804486"
---
# <a name="isocialsessiongetnetworkidentifier"></a>ISocialSession::GetNetworkIdentifier

特定のソーシャル ネットワークの接続のソーシャル ネットワークの一意の識別子を表す文字列を取得します。 
  
```cpp
HRESULT _stdcall GetNetworkIdentifier([out, retval] BSTR* networkIdentifier);
```

## <a name="parameters"></a>Parameters

_networkIdentifier_
  
> [out]ソーシャル ネットワークの一意な識別子を含む文字列です。
    
## <a name="remarks"></a>備考

ネットワークの一意の識別子は、Outlook ソーシャル コネクタ (OSC) プロバイダーのソーシャル ネットワークを識別する文字列です。 このメソッドは E_NOTIMPL を返すこともします。
  
## <a name="see-also"></a>関連項目

- [ISocialSession: IUnknown](isocialsessioniunknown.md)

