---
title: i識別 alsessiongetnetworkidentifier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534e404f-54c6-4d2b-a8d0-d2ee990a972f
description: 特定のソーシャルネットワーク接続の一意のソーシャルネットワーク識別子を表す文字列を取得します。
ms.openlocfilehash: 3051abd6dcccec878e8c53332980731772d543eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433277"
---
# <a name="isocialsessiongetnetworkidentifier"></a>ISocialSession::GetNetworkIdentifier

特定のソーシャルネットワーク接続の一意のソーシャルネットワーク識別子を表す文字列を取得します。 
  
```cpp
HRESULT _stdcall GetNetworkIdentifier([out, retval] BSTR* networkIdentifier);
```

## <a name="parameters"></a>パラメーター

_networkidentifier_
  
> 読み上げ一意のソーシャルネットワーク識別子を含む文字列。
    
## <a name="remarks"></a>注釈

一意のネットワーク識別子は、Outlook social Connector (.osc) プロバイダーのソーシャルネットワークを識別する文字列です。 このメソッドは、E_NOTIMPL を返すこともできます。
  
## <a name="see-also"></a>関連項目

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

