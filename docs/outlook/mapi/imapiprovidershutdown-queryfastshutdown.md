---
title: IMAPIProviderShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProviderShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: 12069912-4b87-4945-9123-51106e0d2d54
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 89846a334ef78aa5b8aba924afcbb625013cd65e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556582"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a>IMAPIProviderShutdown::QueryFastShutdown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI プロバイダーに高速シャットダウンのサポートを照会します。 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>戻り値

S_OK
  
> MAPI プロバイダーは、高速シャットダウンを実行する MAPI クライアントをサポートしています。
    
MAPI_E_NO_SUPPORT
  
> MAPI プロバイダーは、高速シャットダウンを実行する MAPI クライアントをサポートしていない。
    
## <a name="remarks"></a>注釈

クライアントの高速シャットダウンをサポートする必要のない MAPI プロバイダーは [、IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) インターフェイスを実装し **、IMAPIProviderShutdown::QueryFastShutdown** メソッドが MAPI_E_NO_SUPPORT を返す必要があります。 MAPI Outlookとして使用すると、Outlook前にすべての外部参照が解放されるのを待つ必要があります。 
  
高速シャットダウン用のユーザーの Windows レジストリ設定によっては **、IMAPIProviderShutdown** インターフェイスを実装しない場合でも、クライアントの高速シャットダウンが必ずしも妨げであるとは限りません。 
  
## <a name="see-also"></a>関連項目



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[MAPI でのクライアント シャットダウン](client-shutdown-in-mapi.md)

