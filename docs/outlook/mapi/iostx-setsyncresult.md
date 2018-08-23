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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f8982bafc0678378ae46dc31a9417cc11bb695a7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563073"
---
# <a name="iostxsetsyncresult"></a>IOSTX::SetSyncResult

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
同期の結果を設定します。
  
```cpp
HRESULT SetSyncResult( 
    HRESULT hrSync 
);
```

## <a name="parameters"></a>パラメーター

 _hrSync_
  
>  [in]同期の結果を返します。 
    
## <a name="remarks"></a>注釈

ローカル ストアの同期の結果を通知するために**IOSTX::SyncEnd**を呼び出す前に**IOSTX::SetSyncResult**を呼び出します。 
  
## <a name="see-also"></a>関連項目



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)


[MAPI �萔](mapi-constants.md)

