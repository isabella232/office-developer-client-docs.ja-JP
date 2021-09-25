---
title: IOSTXInitSync
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IOSTX.InitSync
api_type:
- COM
ms.assetid: e22244a2-ac5f-910a-501f-4483ea0667c2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5157637bfd133f09af180253790ae3299c807417
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587959"
---
# <a name="iostxinitsync"></a>IOSTX::InitSync

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
同期が始まるとローカル メッセージ ストアに通知します。
  
```cpp
HRESULT InitSync( 
    ULONG ulFlags 
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]同期中の適切な動作を決定するフラグ。 Outlook状態マシンの各状態でこれらのフラグを使用して、クライアントに提供する必要がある情報を決定します。 たとえば、クライアントがファイルを渡 **SYNC_ONLY_ASSOCIATED、Outlook** 関連する (または非表示の) アイテムにのみ関連する情報が返されます。 
    
## <a name="see-also"></a>関連項目



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI 定数](mapi-constants.md)

