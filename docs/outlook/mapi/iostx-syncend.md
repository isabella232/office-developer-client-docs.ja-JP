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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 364914df1c5897241dfeb89cce2cc3c62018ce24
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439577"
---
# <a name="iostxsyncend"></a>IOSTX::SyncEnd

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
現在の状態で同期を終了し、その状態を終了します。
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a>注釈

クライアントは **、IOSTX::SyncBeg** への各呼び出しに対して [IOSTX::SyncEnd を呼び出す必要があります](iostx-syncbeg.md)。 対応するデータ構造には、クライアントが現在の状態を正常に完了したかどうかを示す情報が保持Outlook内部状態をクリーンアップできます。
  
## <a name="see-also"></a>関連項目



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI 定数](mapi-constants.md)

