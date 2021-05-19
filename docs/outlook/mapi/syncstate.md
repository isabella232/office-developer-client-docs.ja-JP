---
title: SYNCSTATE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 63c47e94-f603-aef9-afed-e3819bd79408
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 64348347ea930e6a6a80b9a9075299d2e3109eda
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417631"
---
# <a name="syncstate"></a><span data-ttu-id="a3c83-103">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="a3c83-103">SYNCSTATE</span></span>

<span data-ttu-id="a3c83-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3c83-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3c83-105">この構造は、レプリケーションステート マシンの状態を定義します。</span><span class="sxs-lookup"><span data-stu-id="a3c83-105">This structure defines the states for the replication state machine.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a3c83-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="a3c83-106">Quick info</span></span>

```cpp
typedef enum { 
    LR_SYNC_IDLE = 0, 
    LR_SYNC, 
    LR_SYNC_UPLOAD_HIERARCHY, 
    LR_SYNC_UPLOAD_FOLDER, 
    LR_SYNC_CONTENTS, 
    LR_SYNC_UPLOAD_TABLE, 
    LR_SYNC_UPLOAD_MESSAGE, 
    LR_SYNC_UPLOAD_MESSAGE_READ = 8, 
    LR_SYNC_UPLOAD_MESSAGE_DEL, 
    LR_SYNC_DOWNLOAD_HIERARCHY, 
    LR_SYNC_DOWNLOAD_TABLE, 
    LR_SYNC_DOWNLOAD_HEADER = 17 
} SYNCSTATE; 

```

## <a name="see-also"></a><span data-ttu-id="a3c83-107">関連項目</span><span class="sxs-lookup"><span data-stu-id="a3c83-107">See also</span></span>

- [<span data-ttu-id="a3c83-108">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="a3c83-108">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="a3c83-109">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="a3c83-109">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="a3c83-110">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="a3c83-110">MAPI Constants</span></span>](mapi-constants.md)

