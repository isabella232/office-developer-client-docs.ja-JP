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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6a76488f56f9d1eb1b344c01de2615627dd5d3ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418149"
---
# <a name="imapiclientshutdownqueryfastshutdown"></a>IMAPIClientShutdown::QueryFastShutdown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
読み込み済みの mapi プロバイダーによって提供される高速シャットダウンのサポートを mapi サブシステムに対して照会します。
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>戻り値

S_OK
  
> mapi サブシステムは、高速シャットダウンを実行するための mapi クライアントをサポートします。
    
MAPI_E_NO_SUPPORT
  
> mapi プロバイダーは、高速シャットダウンを実行するための mapi クライアントをサポートしていません。
    
## <a name="remarks"></a>注釈

mapi サブシステムで高速シャットダウンを実行するための mapi クライアントがサポートされているかどうかは、ユーザーの Windows レジストリ設定または mapi クライアントの高速シャットダウンの既定の動作によって異なります。 また、読み込み済みの MAPI プロバイダーが高速シャットダウンをサポートする機能によっても異なります。 詳細については、「 [Fast Shutdown User Options](fast-shutdown-user-options.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[MAPI でのクライアント シャットダウン](client-shutdown-in-mapi.md)

