---
title: HDRSYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bf6892d0-a923-e926-5361-59efa49ebdc0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2131197ca24804eec74270100fa70c05c47a27cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410253"
---
# <a name="hdrsync"></a><span data-ttu-id="9e81c-103">HDRSYNC</span><span class="sxs-lookup"><span data-stu-id="9e81c-103">HDRSYNC</span></span>

  
  
<span data-ttu-id="9e81c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e81c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e81c-105">ダウンロード メッセージ ヘッダーの状態中にメッセージ ヘッダーを [同期する情報](download-message-header-state.md)です。</span><span class="sxs-lookup"><span data-stu-id="9e81c-105">Information for synchronizing a message header during the [download message header state](download-message-header-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9e81c-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="9e81c-106">Quick info</span></span>

```cpp
struct HDRSYNC 
{ 
    UPMSG *pupmsg; 
    FEID feidPar; 
    LPSTREAM pstmReserved; 
    ULONG ulFlags; 
    LPMESSAGE pmsgFull; 
};
```

## <a name="members"></a><span data-ttu-id="9e81c-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="9e81c-107">Members</span></span>

 <span data-ttu-id="9e81c-108">_pupmsg_</span><span class="sxs-lookup"><span data-stu-id="9e81c-108">_pupmsg_</span></span>
  
- <span data-ttu-id="9e81c-109">[out]ローカル ストア内の現在のメッセージ ヘッダーに関する情報。</span><span class="sxs-lookup"><span data-stu-id="9e81c-109">[out] Information for the current message header in the local store.</span></span>
    
 <span data-ttu-id="9e81c-110">_feidPar_</span><span class="sxs-lookup"><span data-stu-id="9e81c-110">_feidPar_</span></span>
  
- <span data-ttu-id="9e81c-111">[out]メッセージ アイテムの親フォルダーのエントリ ID。</span><span class="sxs-lookup"><span data-stu-id="9e81c-111">[out] Entry ID for the parent folder of the message item.</span></span>
    
 <span data-ttu-id="9e81c-112">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="9e81c-112">_pstmReserved_</span></span>
  
- <span data-ttu-id="9e81c-113">[out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="9e81c-113">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="9e81c-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9e81c-114">_ulFlags_</span></span>
  
- <span data-ttu-id="9e81c-115">[in]動作を変更するフラグ:</span><span class="sxs-lookup"><span data-stu-id="9e81c-115">[in] Flags to modify behavior:</span></span>
    
- <span data-ttu-id="9e81c-116">HSF_LOCAL</span><span class="sxs-lookup"><span data-stu-id="9e81c-116">HSF_LOCAL</span></span>
    
  - <span data-ttu-id="9e81c-117">[in]完全なアイテムは、ヘッダー アイテムと同じローカル ストアに存在します。</span><span class="sxs-lookup"><span data-stu-id="9e81c-117">[in] Full item resides in the same local store as the header item.</span></span>
    
- <span data-ttu-id="9e81c-118">HSF_COPYDESTRUCTIVE</span><span class="sxs-lookup"><span data-stu-id="9e81c-118">HSF_COPYDESTRUCTIVE</span></span>
    
  -  <span data-ttu-id="9e81c-119">[in]内部コピー操作を最適化します。</span><span class="sxs-lookup"><span data-stu-id="9e81c-119">[in] Optimize internal copy operations.</span></span> <span data-ttu-id="9e81c-120">これにより、データが失われる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9e81c-120">This might cause data loss.</span></span> <span data-ttu-id="9e81c-121">**HSF_LOCAL** 設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e81c-121">**HSF_LOCAL** must be set.</span></span> 
    
- <span data-ttu-id="9e81c-122">HSF_OK</span><span class="sxs-lookup"><span data-stu-id="9e81c-122">HSF_OK</span></span>
    
  - <span data-ttu-id="9e81c-123">[in]ヘッダーの同期が成功しました。</span><span class="sxs-lookup"><span data-stu-id="9e81c-123">[in] Header synchronization was successful.</span></span> <span data-ttu-id="9e81c-124">クライアントは、サーバーから情報をダウンロードした後、これを設定します。</span><span class="sxs-lookup"><span data-stu-id="9e81c-124">The client sets this after downloading information from the server.</span></span>
    
     <span data-ttu-id="9e81c-125">_pmsgFull_</span><span class="sxs-lookup"><span data-stu-id="9e81c-125">_pmsgFull_</span></span>
    
  - <span data-ttu-id="9e81c-126">[in]サーバーからダウンロードされたメッセージ ヘッダーを含む完全なメッセージ アイテム。</span><span class="sxs-lookup"><span data-stu-id="9e81c-126">[in] The full message item including the message header downloaded from the server.</span></span> <span data-ttu-id="9e81c-127">LPMESSAGE の型定義については、mapidefs.h **を参照してください**。</span><span class="sxs-lookup"><span data-stu-id="9e81c-127">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="9e81c-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="9e81c-128">See also</span></span>



[<span data-ttu-id="9e81c-129">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="9e81c-129">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="9e81c-130">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="9e81c-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="9e81c-131">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="9e81c-131">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="9e81c-132">FEID</span><span class="sxs-lookup"><span data-stu-id="9e81c-132">FEID</span></span>](feid.md)

