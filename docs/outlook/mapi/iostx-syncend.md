---
title: IOSTXSyncEnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncEnd
api_type:
- COM
ms.assetid: da9de705-bdab-6cb8-35ea-61f03cdc4ff5
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: fd5b2ed23eba30cbe861a20c4fd100cb8ea1aeb0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568841"
---
# <a name="iostxsyncend"></a>IOSTX::SyncEnd

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
現在の状態で同期を終了し、その状態を終了します。
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a>注釈

クライアントは、 [IOSTX::SyncBeg](iostx-syncbeg.md)を呼び出すたびに**IOSTX::SyncEnd**を呼び出す必要があります。 対応するデータ構造は、クライアントが Outlook では、内部の状態をクリーンアップできるように現在の状態を完了正常にかどうかを示す情報を保持します。
  
## <a name="see-also"></a>関連項目



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI �萔](mapi-constants.md)

