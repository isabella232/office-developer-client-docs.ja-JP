---
title: IOSTXInitSync
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.InitSync
api_type:
- COM
ms.assetid: e22244a2-ac5f-910a-501f-4483ea0667c2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b9086383b45d40d5839284ac785d72438be60e00
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317193"
---
# <a name="iostxinitsync"></a>IOSTX::InitSync

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
同期が開始されようとしていることをローカルメッセージストアに通知します。
  
```cpp
HRESULT InitSync( 
    ULONG ulFlags 
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番同期時に適切な動作を決定するフラグ。 Outlook は、レプリケーション状態マシンの各状態でこれらのフラグを使用して、クライアントに対して提供する必要のある情報を特定します。 たとえば、クライアントが**SYNC_ONLY_ASSOCIATED**に合格した場合、Outlook は関連付けられた (または非表示の) アイテムに関連する情報のみを返します。 
    
## <a name="see-also"></a>関連項目



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI 定数](mapi-constants.md)

