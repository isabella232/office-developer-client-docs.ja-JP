---
title: IOSTXSetSyncResult
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IOSTX.SetSyncResult
api_type:
- COM
ms.assetid: 7f083ee0-bf36-0059-1589-66e454fe0098
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 664c8f3c1fdbfbdf830c16834f62220fbfe0949b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571578"
---
# <a name="iostxsetsyncresult"></a>IOSTX::SetSyncResult

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
同期の結果を設定します。
  
```cpp
HRESULT SetSyncResult( 
    HRESULT hrSync 
);
```

## <a name="parameters"></a>パラメーター

 _hrSync_
  
>  [in]同期の結果。 
    
## <a name="remarks"></a>注釈

IOSTX:::SyncEnd を呼び出す前に **IOSTX::SetSyncResult** を呼び出して、同期の結果をローカル ストアに通知します。  
  
## <a name="see-also"></a>関連項目



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)


[MAPI 定数](mapi-constants.md)

