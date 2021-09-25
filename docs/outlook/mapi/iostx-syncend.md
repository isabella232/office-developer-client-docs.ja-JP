---
title: IOSTXSyncEnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IOSTX.SyncEnd
api_type:
- COM
ms.assetid: da9de705-bdab-6cb8-35ea-61f03cdc4ff5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 416b4ddc3a5798b1621907f7bc22f9bc440a655a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613815"
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

