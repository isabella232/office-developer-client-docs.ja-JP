---
title: UPREADE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d146ee74-0c3a-5fdd-b1aa-af6498550801
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 854e674002953c31c47d56096700dca582ce0a5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804196"
---
# <a name="upreade"></a><span data-ttu-id="b37ec-103">UPREADE</span><span class="sxs-lookup"><span data-stu-id="b37ec-103">UPREADE</span></span>

<span data-ttu-id="b37ec-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b37ec-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b37ec-105">[アップロード ステータスの状態を読み取り](upload-read-status-state.md)中にはアイテムの読み取り状態をアップロードする情報を拡張します。</span><span class="sxs-lookup"><span data-stu-id="b37ec-105">Extended information for uploading the read state of an item during the [upload read status state](upload-read-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b37ec-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="b37ec-106">Quick info</span></span>

```cpp
struct UPREADE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
};
```

## <a name="members"></a><span data-ttu-id="b37ec-107">Members</span><span class="sxs-lookup"><span data-stu-id="b37ec-107">Members</span></span>

<span data-ttu-id="b37ec-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b37ec-108">_ulFlags_</span></span>
  
>  <span data-ttu-id="b37ec-109">[out]/[in] アップロード中に適切な動作を決定するフラグ。</span><span class="sxs-lookup"><span data-stu-id="b37ec-109">[out]/[in] Flags to determine the appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="b37ec-110">UPR_ASSOC</span><span class="sxs-lookup"><span data-stu-id="b37ec-110">UPR_ASSOC</span></span>
    
    - <span data-ttu-id="b37ec-111">[out]アイテムが非表示にします。</span><span class="sxs-lookup"><span data-stu-id="b37ec-111">[out] Item is hidden.</span></span>
    
  - <span data-ttu-id="b37ec-112">UPR_READ</span><span class="sxs-lookup"><span data-stu-id="b37ec-112">UPR_READ</span></span>
    
    - <span data-ttu-id="b37ec-113">[out]アイテムの読み取り状態が変更されました。</span><span class="sxs-lookup"><span data-stu-id="b37ec-113">[out] The read status of the item has been changed.</span></span>
    
  - <span data-ttu-id="b37ec-114">UPR_OK</span><span class="sxs-lookup"><span data-stu-id="b37ec-114">UPR_OK</span></span>
    
    - <span data-ttu-id="b37ec-115">[in]アップロードが正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="b37ec-115">[in] Upload was successful.</span></span> <span data-ttu-id="b37ec-116">クライアントでは、情報をサーバーにアップロードした後、これを設定します。</span><span class="sxs-lookup"><span data-stu-id="b37ec-116">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="b37ec-117">UPR_COMMIT</span><span class="sxs-lookup"><span data-stu-id="b37ec-117">UPR_COMMIT</span></span>
    
    - <span data-ttu-id="b37ec-118">[in]アップロード アイテムの読み取り状態を[テーブルの状態をアップロード](upload-table-state.md)するバッチ処理の終了を待機しているのではなく複数の項目。</span><span class="sxs-lookup"><span data-stu-id="b37ec-118">[in] Upload the read status of the item now, instead of waiting to the end of the [upload table state](upload-table-state.md) to batch-process more than one item.</span></span> 
    
<span data-ttu-id="b37ec-119">_skey_</span><span class="sxs-lookup"><span data-stu-id="b37ec-119">_skey_</span></span>
  
> <span data-ttu-id="b37ec-120">[out]ソース項目のキー。</span><span class="sxs-lookup"><span data-stu-id="b37ec-120">[out] Source key of the item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b37ec-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="b37ec-121">See also</span></span>

- [<span data-ttu-id="b37ec-122">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="b37ec-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="b37ec-123">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="b37ec-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="b37ec-124">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="b37ec-124">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="b37ec-125">UPREAD</span><span class="sxs-lookup"><span data-stu-id="b37ec-125">UPREAD</span></span>](upread.md)

