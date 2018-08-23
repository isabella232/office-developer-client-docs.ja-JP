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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4301fb504439cf0ebd70b5ece589c812cb74844e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585298"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a>IMAPIProviderShutdown::QueryFastShutdown

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
クエリは高速シャット ダウンの MAPI プロバイダーをサポートします。 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>�߂�l

S_OK
  
> MAPI プロバイダーには、高速シャット ダウンを実行するのには MAPI クライアントがサポートされています。
    
MAPI_E_NO_SUPPORT
  
> MAPI プロバイダーは、高速シャット ダウンを実行するのには MAPI クライアントをサポートしていません。
    
## <a name="remarks"></a>注釈

クライアントの高速シャット ダウンをサポートするために必要としない MAPI プロバイダーの[IMAPIProviderShutdown](imapiprovidershutdowniunknown.md)インターフェイスを実装し、MAPI_E_NO_SUPPORT を返す**IMAPIProviderShutdown::QueryFastShutdown**メソッドがある必要がありますも。 MAPI クライアントとして outlook でこのすべての外部参照を終了する前に解放するまで待機するように Outlook が発生します。 
  
によって**IMAPIProviderShutdown**インターフェイスを実装しない、高速シャット ダウンのレジストリ設定が必ずしもユーザーの Windows クライアントの高速シャット ダウンを防止します。 
  
## <a name="see-also"></a>関連項目



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Mapi クライアントのシャット ダウン](client-shutdown-in-mapi.md)

