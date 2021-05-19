---
title: UPREAD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 568f2336-cb4d-3f2c-a304-d29cdb0bcbcc
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7338edc13227e303ec5fa47da4a5d9ee611c6749
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419885"
---
# <a name="upread"></a><span data-ttu-id="877e7-103">UPREAD</span><span class="sxs-lookup"><span data-stu-id="877e7-103">UPREAD</span></span>

  
  
<span data-ttu-id="877e7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="877e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="877e7-105">アップロードの読み取り状態状態の間にアイテムの読み取り状態 [をアップロードする情報](upload-read-status-state.md)です。</span><span class="sxs-lookup"><span data-stu-id="877e7-105">Information for uploading the read state of items during the [upload read status state](upload-read-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="877e7-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="877e7-106">Quick info</span></span>

```cpp
struct UPREAD 
{ 
    PUPREADE pupre; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="877e7-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="877e7-107">Members</span></span>

 <span data-ttu-id="877e7-108">_pupre_</span><span class="sxs-lookup"><span data-stu-id="877e7-108">_pupre_</span></span>
  
>  <span data-ttu-id="877e7-109">[out] **[UPREADE エントリの](upreade.md)** ベクトル。</span><span class="sxs-lookup"><span data-stu-id="877e7-109">[out] Vector of **[UPREADE](upreade.md)** entries.</span></span> 
    
 <span data-ttu-id="877e7-110">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="877e7-110">_cEnt_</span></span>
  
>  <span data-ttu-id="877e7-111">[out] **UPREADE エントリ** の数。</span><span class="sxs-lookup"><span data-stu-id="877e7-111">[out] Number of **UPREADE** entries.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="877e7-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="877e7-112">See also</span></span>



[<span data-ttu-id="877e7-113">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="877e7-113">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="877e7-114">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="877e7-114">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="877e7-115">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="877e7-115">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="877e7-116">UPREADE</span><span class="sxs-lookup"><span data-stu-id="877e7-116">UPREADE</span></span>](upreade.md)

