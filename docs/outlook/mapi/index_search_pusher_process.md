---
title: INDEX_SEARCH_PUSHER_PROCESS
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 6b39504f-6eed-2605-048d-2707f38a7d9a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 34c7f5f2a17ce4b1fb4ed18bf7c3ab89a18cb658
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556358"
---
# <a name="index_search_pusher_process"></a>INDEX_SEARCH_PUSHER_PROCESS

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
そのストア内のオブジェクトがインデックス作成の準備ができているという通知を MAPI プロトコル ハンドラーに送信するプロセスを指定します。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
typedef struct _INDEX_SEARCH_PUSHER_PROCESS {  
    DWORD dwPID;  
} INDEX_SEARCH_PUSHER_PROCESS; 
```

## <a name="members"></a>メンバー

 *dwPID* 
  
>  MAPI プロトコル ハンドラーのインデクサーにインデックス通知を送信するプロセスのプロセス ID。 
    

