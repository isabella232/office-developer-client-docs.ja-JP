---
title: INDEX_SEARCH_PUSHER_PROCESS
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6b39504f-6eed-2605-048d-2707f38a7d9a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 64e5cf31dffdc794a22bcbd6d503a2b688f9c733
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423350"
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
    

