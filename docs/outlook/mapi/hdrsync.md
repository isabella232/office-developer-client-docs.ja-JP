---
title: HDRSYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bf6892d0-a923-e926-5361-59efa49ebdc0
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 261a59e628320f384deeb760ba71c9c0386cfde6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576044"
---
# <a name="hdrsync"></a><span data-ttu-id="9e5c6-103">HDRSYNC</span><span class="sxs-lookup"><span data-stu-id="9e5c6-103">HDRSYNC</span></span>

  
  
<span data-ttu-id="9e5c6-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e5c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e5c6-105">[メッセージ ヘッダーの状態をダウンロード](download-message-header-state.md)する時にメッセージ ヘッダーを同期するための情報です。</span><span class="sxs-lookup"><span data-stu-id="9e5c6-105">Information for synchronizing a message header during the [download message header state](download-message-header-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9e5c6-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="9e5c6-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="9e5c6-107">Members</span><span class="sxs-lookup"><span data-stu-id="9e5c6-107">Members</span></span>

 <span data-ttu-id="9e5c6-108">_pupmsg_</span><span class="sxs-lookup"><span data-stu-id="9e5c6-108">_pupmsg_</span></span>
  
- <span data-ttu-id="9e5c6-109">[out]ローカル ストア内の現在のメッセージ ヘッダーの情報です。</span><span class="sxs-lookup"><span data-stu-id="9e5c6-109">[out] Information for the current message header in the local store.</span></span>
    
 <span data-ttu-id="9e5c6-110">_feidPar_</span><span class="sxs-lookup"><span data-stu-id="9e5c6-110">_feidPar_</span></span>
  
- <span data-ttu-id="9e5c6-111">[out]メッセージ アイテムの親フォルダーのエントリ ID です。</span><span class="sxs-lookup"><span data-stu-id="9e5c6-111">[out] Entry ID for the parent folder of the message item.</span></span>
    
 <span data-ttu-id="9e5c6-112">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="9e5c6-112">_pstmReserved_</span></span>
  
- <span data-ttu-id="9e5c6-113">[out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="9e5c6-113">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="9e5c6-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9e5c6-114">_ulFlags_</span></span>
  
- <span data-ttu-id="9e5c6-115">[in]動作を変更するフラグです。</span><span class="sxs-lookup"><span data-stu-id="9e5c6-115">[in] Flags to modify behavior:</span></span>
    
- <span data-ttu-id="9e5c6-116">HSF_LOCAL</span><span class="sxs-lookup"><span data-stu-id="9e5c6-116">HSF_LOCAL</span></span>
    
  - <span data-ttu-id="9e5c6-117">[in]完全なアイテムは、ヘッダー項目と同じローカル ストアに存在します。</span><span class="sxs-lookup"><span data-stu-id="9e5c6-117">[in] Full item resides in the same local store as the header item.</span></span>
    
- <span data-ttu-id="9e5c6-118">HSF_COPYDESTRUCTIVE</span><span class="sxs-lookup"><span data-stu-id="9e5c6-118">HSF_COPYDESTRUCTIVE</span></span>
    
  -  <span data-ttu-id="9e5c6-119">[in]内部のコピー処理を最適化します。</span><span class="sxs-lookup"><span data-stu-id="9e5c6-119">[in] Optimize internal copy operations.</span></span> <span data-ttu-id="9e5c6-120">データが失われる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9e5c6-120">This might cause data loss.</span></span> <span data-ttu-id="9e5c6-121">**HSF_LOCAL**を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e5c6-121">**HSF_LOCAL** must be set.</span></span> 
    
- <span data-ttu-id="9e5c6-122">HSF_OK</span><span class="sxs-lookup"><span data-stu-id="9e5c6-122">HSF_OK</span></span>
    
  - <span data-ttu-id="9e5c6-123">[in]ヘッダーの同期が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="9e5c6-123">[in] Header synchronization was successful.</span></span> <span data-ttu-id="9e5c6-124">クライアントは、サーバーから情報をダウンロードした後、これを設定します。</span><span class="sxs-lookup"><span data-stu-id="9e5c6-124">The client sets this after downloading information from the server.</span></span>
    
     <span data-ttu-id="9e5c6-125">_pmsgFull_</span><span class="sxs-lookup"><span data-stu-id="9e5c6-125">_pmsgFull_</span></span>
    
  - <span data-ttu-id="9e5c6-126">[in]メッセージ ヘッダーを含む完全なメッセージ項目は、サーバーからダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="9e5c6-126">[in] The full message item including the message header downloaded from the server.</span></span> <span data-ttu-id="9e5c6-127">**LPMESSAGE**の型定義の mapidefs.h を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9e5c6-127">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="9e5c6-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="9e5c6-128">See also</span></span>



[<span data-ttu-id="9e5c6-129">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="9e5c6-129">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="9e5c6-130">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="9e5c6-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="9e5c6-131">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="9e5c6-131">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="9e5c6-132">FEID</span><span class="sxs-lookup"><span data-stu-id="9e5c6-132">FEID</span></span>](feid.md)

