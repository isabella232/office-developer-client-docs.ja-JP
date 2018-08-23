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
ms.openlocfilehash: 66542d2cc7600ecbcd8de9043b6b40559744c2ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801095"
---
# <a name="iostxsyncend"></a>IOSTX::SyncEnd

  
  
**適用対象**: Outlook 
  
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

