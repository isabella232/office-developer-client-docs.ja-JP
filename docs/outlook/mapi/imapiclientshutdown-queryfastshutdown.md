---
title: IMAPIClientShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIClientShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: b743b5b6-4a7c-46b8-99eb-afd13ee947db
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 487ef45b6ef611114d841f8f4c585a059d09265d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580014"
---
# <a name="imapiclientshutdownqueryfastshutdown"></a>IMAPIClientShutdown::QueryFastShutdown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
読み込まれた MAPI プロバイダーによって提供される高速シャットダウンのサポートを MAPI サブシステムに照会します。
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>戻り値

S_OK
  
> MAPI サブシステムは、高速シャットダウンを実行する MAPI クライアントをサポートします。
    
MAPI_E_NO_SUPPORT
  
> MAPI プロバイダーは、高速シャットダウンを実行する MAPI クライアントをサポートしていない。
    
## <a name="remarks"></a>注釈

MAPI サブシステムが MAPI クライアントで高速シャットダウンをサポートするかどうかは、ユーザーの Windows レジストリ設定、または高速シャットダウン用の MAPI クライアントの既定の動作によって異なります。 また、読み込まれた MAPI プロバイダーが高速シャットダウンをサポートする機能にも依存します。 詳細については、「Fast [Shutdown User Options」を参照してください](fast-shutdown-user-options.md)。
  
## <a name="see-also"></a>関連項目



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[MAPI でのクライアント シャットダウン](client-shutdown-in-mapi.md)

