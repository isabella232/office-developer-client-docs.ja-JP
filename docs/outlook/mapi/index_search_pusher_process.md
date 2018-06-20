---
title: INDEX_SEARCH_PUSHER_PROCESS
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6b39504f-6eed-2605-048d-2707f38a7d9a
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: ada6d4127d503aae0b068d40d2bb48cb6b833ea0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801059"
---
# <a name="indexsearchpusherprocess"></a>INDEX_SEARCH_PUSHER_PROCESS

  
  
**適用されます**: Outlook 
  
通知を送信、MAPI プロトコル ハンドラーは、そのストア内のオブジェクトのインデックス作成の準備ができているプロセスを指定します。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
typedef struct _INDEX_SEARCH_PUSHER_PROCESS {  
    DWORD dwPID;  
} INDEX_SEARCH_PUSHER_PROCESS; 
```

## <a name="members"></a>メンバー

 *dwPID* 
  
>  MAPI プロトコル ハンドラーのインデクサーにインデックス作成の通知を送信するプロセスのプロセス ID です。 
    

