---
title: IMAPIProviderShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: 12069912-4b87-4945-9123-51106e0d2d54
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 50b49761cf5923b11a450cbce7b7991f5ddd4d82
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418219"
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

