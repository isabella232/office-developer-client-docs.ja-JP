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
# <a name="upreade"></a><span data-ttu-id="d904f-103">UPREADE</span><span class="sxs-lookup"><span data-stu-id="d904f-103">UPREADE</span></span>

<span data-ttu-id="d904f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d904f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d904f-105">[アップロード ステータスの状態を読み取り](upload-read-status-state.md)中にはアイテムの読み取り状態をアップロードする情報を拡張します。</span><span class="sxs-lookup"><span data-stu-id="d904f-105">Extended information for uploading the read state of an item during the [upload read status state](upload-read-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d904f-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="d904f-106">Quick info</span></span>

```cpp
struct UPREADE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
};
```

## <a name="members"></a><span data-ttu-id="d904f-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="d904f-107">Members</span></span>

<span data-ttu-id="d904f-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d904f-108">_ulFlags_</span></span>
  
>  <span data-ttu-id="d904f-109">[out]/[in] アップロード中に適切な動作を決定するフラグ。</span><span class="sxs-lookup"><span data-stu-id="d904f-109">[out]/[in] Flags to determine the appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="d904f-110">UPR_ASSOC</span><span class="sxs-lookup"><span data-stu-id="d904f-110">UPR_ASSOC</span></span>
    
    - <span data-ttu-id="d904f-111">[out]アイテムが非表示にします。</span><span class="sxs-lookup"><span data-stu-id="d904f-111">[out] Item is hidden.</span></span>
    
  - <span data-ttu-id="d904f-112">UPR_READ</span><span class="sxs-lookup"><span data-stu-id="d904f-112">UPR_READ</span></span>
    
    - <span data-ttu-id="d904f-113">[out]アイテムの読み取り状態が変更されました。</span><span class="sxs-lookup"><span data-stu-id="d904f-113">[out] The read status of the item has been changed.</span></span>
    
  - <span data-ttu-id="d904f-114">UPR_OK</span><span class="sxs-lookup"><span data-stu-id="d904f-114">UPR_OK</span></span>
    
    - <span data-ttu-id="d904f-115">[in]アップロードが正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="d904f-115">[in] Upload was successful.</span></span> <span data-ttu-id="d904f-116">クライアントでは、情報をサーバーにアップロードした後、これを設定します。</span><span class="sxs-lookup"><span data-stu-id="d904f-116">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="d904f-117">UPR_COMMIT</span><span class="sxs-lookup"><span data-stu-id="d904f-117">UPR_COMMIT</span></span>
    
    - <span data-ttu-id="d904f-118">[in]アップロード アイテムの読み取り状態を[テーブルの状態をアップロード](upload-table-state.md)するバッチ処理の終了を待機しているのではなく複数の項目。</span><span class="sxs-lookup"><span data-stu-id="d904f-118">[in] Upload the read status of the item now, instead of waiting to the end of the [upload table state](upload-table-state.md) to batch-process more than one item.</span></span> 
    
<span data-ttu-id="d904f-119">_skey_</span><span class="sxs-lookup"><span data-stu-id="d904f-119">_skey_</span></span>
  
> <span data-ttu-id="d904f-120">[out]ソース項目のキー。</span><span class="sxs-lookup"><span data-stu-id="d904f-120">[out] Source key of the item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d904f-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="d904f-121">See also</span></span>

- [<span data-ttu-id="d904f-122">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="d904f-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="d904f-123">レプリケーション状態マシンについて</span><span class="sxs-lookup"><span data-stu-id="d904f-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="d904f-124">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="d904f-124">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="d904f-125">UPREAD</span><span class="sxs-lookup"><span data-stu-id="d904f-125">UPREAD</span></span>](upread.md)

