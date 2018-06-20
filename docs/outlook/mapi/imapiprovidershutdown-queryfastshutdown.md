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
ms.openlocfilehash: d9f08c13f68c7d3d9f41b9a67ac1888d6c507c34
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800701"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a>IMAPIProviderShutdown::QueryFastShutdown

  
  
**適用されます**: Outlook 
  
クエリは高速シャット ダウンの MAPI プロバイダーをサポートします。 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>�߂�l

S_OK
  
> MAPI プロバイダーには、高速シャット ダウンを実行するのには MAPI クライアントがサポートされています。
    
MAPI_E_NO_SUPPORT
  
> MAPI プロバイダーは、高速シャット ダウンを実行するのには MAPI クライアントをサポートしていません。
    
## <a name="remarks"></a>備考

クライアントの高速シャット ダウンをサポートするために必要としない MAPI プロバイダーの[IMAPIProviderShutdown](imapiprovidershutdowniunknown.md)インターフェイスを実装し、MAPI_E_NO_SUPPORT を返す**IMAPIProviderShutdown::QueryFastShutdown**メソッドがある必要がありますも。 MAPI クライアントとして outlook でこのすべての外部参照を終了する前に解放するまで待機するように Outlook が発生します。 
  
によって**IMAPIProviderShutdown**インターフェイスを実装しない、高速シャット ダウンのレジストリ設定が必ずしもユーザーの Windows クライアントの高速シャット ダウンを防止します。 
  
## <a name="see-also"></a>関連項目



[IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md)


[Mapi クライアントのシャット ダウン](client-shutdown-in-mapi.md)

