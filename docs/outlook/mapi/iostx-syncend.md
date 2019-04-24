---
title: iostxsyncend
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332152"
---
# <a name="iostxsyncend"></a>IOSTX::SyncEnd

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
現在の状態で同期を終了し、その状態を終了します。
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a>解説

[iostx:: SyncBeg](iostx-syncbeg.md)への呼び出しごとに、クライアントは**iostx:: syncend**を呼び出す必要があります。 対応するデータ構造には、Outlook が内部状態をクリーンアップできるように、クライアントが現在の状態を正常に完了したかどうかを示す情報が保持されます。
  
## <a name="see-also"></a>関連項目



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[MAPI 定数](mapi-constants.md)

