---
title: IMAPIClientShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: b743b5b6-4a7c-46b8-99eb-afd13ee947db
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 059d0d4427a8f2d68795a671d77fb9e3d84294f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800463"
---
# <a name="imapiclientshutdownqueryfastshutdown"></a>IMAPIClientShutdown::QueryFastShutdown

  
  
**適用されます**: Outlook 
  
クエリ、MAPI サブシステムの高速シャット ダウンをサポートして読み込まれている MAPI プロバイダーによって提供されます。
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>�߂�l

S_OK
  
> MAPI サブシステムには、高速シャット ダウンを実行するのには MAPI クライアントがサポートされています。
    
MAPI_E_NO_SUPPORT
  
> MAPI プロバイダーは、高速シャット ダウンを実行するのには MAPI クライアントをサポートしていません。
    
## <a name="remarks"></a>備考

MAPI サブシステムが高速シャット ダウンを実行するのには MAPI クライアントをサポートしているかどうかは、ユーザーの Windows レジストリ設定または高速シャット ダウンのために MAPI クライアントの既定の動作によって異なります。 高速シャット ダウンをサポートするために読み込まれている MAPI プロバイダーの機能によっても異なります。 詳細については、[高速シャット ダウンのユーザー オプション](fast-shutdown-user-options.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md)


[Mapi クライアントのシャット ダウン](client-shutdown-in-mapi.md)

