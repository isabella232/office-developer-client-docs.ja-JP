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
# <a name="indexsearchpusherprocess"></a><span data-ttu-id="ef085-103">INDEX_SEARCH_PUSHER_PROCESS</span><span class="sxs-lookup"><span data-stu-id="ef085-103">INDEX_SEARCH_PUSHER_PROCESS</span></span>

  
  
<span data-ttu-id="ef085-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ef085-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ef085-105">通知を送信、MAPI プロトコル ハンドラーは、そのストア内のオブジェクトのインデックス作成の準備ができているプロセスを指定します。</span><span class="sxs-lookup"><span data-stu-id="ef085-105">Specifies the process that is sending a notification to the MAPI Protocol Handler that an object in that store is ready for indexing.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ef085-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="ef085-106">Quick info</span></span>

```cpp
typedef struct _INDEX_SEARCH_PUSHER_PROCESS {  
    DWORD dwPID;  
} INDEX_SEARCH_PUSHER_PROCESS; 
```

## <a name="members"></a><span data-ttu-id="ef085-107">Members</span><span class="sxs-lookup"><span data-stu-id="ef085-107">Members</span></span>

 <span data-ttu-id="ef085-108">*dwPID*</span><span class="sxs-lookup"><span data-stu-id="ef085-108">*dwPID*</span></span> 
  
>  <span data-ttu-id="ef085-109">MAPI プロトコル ハンドラーのインデクサーにインデックス作成の通知を送信するプロセスのプロセス ID です。</span><span class="sxs-lookup"><span data-stu-id="ef085-109">Process ID for the process that is sending an indexing notification to the indexer of the MAPI Protocol Handler.</span></span> 
    

