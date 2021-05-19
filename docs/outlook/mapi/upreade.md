---
title: UPREADE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d146ee74-0c3a-5fdd-b1aa-af6498550801
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1df2c665f8e9d7a0bd6d47ec59b2adf706bead75
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434145"
---
# <a name="upreade"></a><span data-ttu-id="fc133-103">UPREADE</span><span class="sxs-lookup"><span data-stu-id="fc133-103">UPREADE</span></span>

<span data-ttu-id="fc133-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc133-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc133-105">アップロードの読み取り状態状態の間にアイテムの読み取り状態をアップロード [する拡張情報](upload-read-status-state.md)。</span><span class="sxs-lookup"><span data-stu-id="fc133-105">Extended information for uploading the read state of an item during the [upload read status state](upload-read-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="fc133-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="fc133-106">Quick info</span></span>

```cpp
struct UPREADE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
};
```

## <a name="members"></a><span data-ttu-id="fc133-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="fc133-107">Members</span></span>

<span data-ttu-id="fc133-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fc133-108">_ulFlags_</span></span>
  
>  <span data-ttu-id="fc133-109">[out]/[in] アップロード時の適切な動作を判断するフラグ。</span><span class="sxs-lookup"><span data-stu-id="fc133-109">[out]/[in] Flags to determine the appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="fc133-110">UPR_ASSOC</span><span class="sxs-lookup"><span data-stu-id="fc133-110">UPR_ASSOC</span></span>
    
    - <span data-ttu-id="fc133-111">[out]アイテムは非表示です。</span><span class="sxs-lookup"><span data-stu-id="fc133-111">[out] Item is hidden.</span></span>
    
  - <span data-ttu-id="fc133-112">UPR_READ</span><span class="sxs-lookup"><span data-stu-id="fc133-112">UPR_READ</span></span>
    
    - <span data-ttu-id="fc133-113">[out]アイテムの読み取り状態が変更されました。</span><span class="sxs-lookup"><span data-stu-id="fc133-113">[out] The read status of the item has been changed.</span></span>
    
  - <span data-ttu-id="fc133-114">UPR_OK</span><span class="sxs-lookup"><span data-stu-id="fc133-114">UPR_OK</span></span>
    
    - <span data-ttu-id="fc133-115">[in]アップロード成功しました。</span><span class="sxs-lookup"><span data-stu-id="fc133-115">[in] Upload was successful.</span></span> <span data-ttu-id="fc133-116">クライアントは、サーバーに情報をアップロードした後にこれを設定します。</span><span class="sxs-lookup"><span data-stu-id="fc133-116">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="fc133-117">UPR_COMMIT</span><span class="sxs-lookup"><span data-stu-id="fc133-117">UPR_COMMIT</span></span>
    
    - <span data-ttu-id="fc133-118">[in]アップロードをバッチ処理するために、アップロード テーブルの状態の最後まで待機するのではなく、アイテムの読[](upload-table-state.md)み取り状態を確認します。</span><span class="sxs-lookup"><span data-stu-id="fc133-118">[in] Upload the read status of the item now, instead of waiting to the end of the [upload table state](upload-table-state.md) to batch-process more than one item.</span></span> 
    
<span data-ttu-id="fc133-119">_skey_</span><span class="sxs-lookup"><span data-stu-id="fc133-119">_skey_</span></span>
  
> <span data-ttu-id="fc133-120">[out]アイテムのソース キー。</span><span class="sxs-lookup"><span data-stu-id="fc133-120">[out] Source key of the item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fc133-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="fc133-121">See also</span></span>

- [<span data-ttu-id="fc133-122">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="fc133-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="fc133-123">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="fc133-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="fc133-124">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="fc133-124">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="fc133-125">UPREAD</span><span class="sxs-lookup"><span data-stu-id="fc133-125">UPREAD</span></span>](upread.md)

