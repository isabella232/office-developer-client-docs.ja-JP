---
title: IOSTXSetSyncResult
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SetSyncResult
api_type:
- COM
ms.assetid: 7f083ee0-bf36-0059-1589-66e454fe0098
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 78ccf72f17ec350d77f2d22d0e6d2fa7c3d97543
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432871"
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

 _hrsync_
  
>  順番同期の結果。 
    
## <a name="remarks"></a>注釈

同期の結果をローカルストアに通知するには、iostx:: **syncend**を呼び出す前に、 **iostx:: SetSyncResult**を呼び出します。 
  
## <a name="see-also"></a>関連項目



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)


[MAPI 定数](mapi-constants.md)

