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
ms.openlocfilehash: 9495caecd514656f6fd62fb5db6cd8ac2faf4b50
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581742"
---
# <a name="indexsearchpusherprocess"></a>INDEX_SEARCH_PUSHER_PROCESS

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
通知を送信、MAPI プロトコル ハンドラーは、そのストア内のオブジェクトのインデックス作成の準備ができているプロセスを指定します。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
typedef struct _INDEX_SEARCH_PUSHER_PROCESS {  
    DWORD dwPID;  
} INDEX_SEARCH_PUSHER_PROCESS; 
```

## <a name="members"></a>Members

 *dwPID* 
  
>  MAPI プロトコル ハンドラーのインデクサーにインデックス作成の通知を送信するプロセスのプロセス ID です。 
    

