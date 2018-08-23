---
title: PidTagRemoteProgress 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemoteProgress
api_type:
- COM
ms.assetid: 01cae79e-5b56-4cd4-83a6-f0956ff539fb
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4e6495d5521e0f277ac4d501a987de0142d0960d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803316"
---
# <a name="pidtagremoteprogress-canonical-property"></a><span data-ttu-id="870d2-103">PidTagRemoteProgress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="870d2-103">PidTagRemoteProgress Canonical Property</span></span>

  
  
<span data-ttu-id="870d2-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="870d2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="870d2-105">このプロパティには、リモート転送の状態を示す数値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="870d2-105">This property contains a number that indicates the status of a remote transfer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="870d2-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="870d2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="870d2-107">PR_REMOTE_PROGRESS</span><span class="sxs-lookup"><span data-stu-id="870d2-107">PR_REMOTE_PROGRESS</span></span>  <br/> |
|<span data-ttu-id="870d2-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="870d2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="870d2-109">0x3E0B</span><span class="sxs-lookup"><span data-stu-id="870d2-109">0x3E0B</span></span>  <br/> |
|<span data-ttu-id="870d2-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="870d2-110">Data type:</span></span>  <br/> |<span data-ttu-id="870d2-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="870d2-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="870d2-112">領域:</span><span class="sxs-lookup"><span data-stu-id="870d2-112">Area:</span></span>  <br/> |<span data-ttu-id="870d2-113">MAPI のステータス</span><span class="sxs-lookup"><span data-stu-id="870d2-113">MAPI Status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="870d2-114">注釈</span><span class="sxs-lookup"><span data-stu-id="870d2-114">Remarks</span></span>

<span data-ttu-id="870d2-115">転送が進行中でない場合は、このプロパティを 1 に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="870d2-115">If no transfer is in progress, this property should be set to 1.</span></span> <span data-ttu-id="870d2-116">転送が進行中である場合、設定値を 0 ~ 100% の完了の転送のパーセントを示します。</span><span class="sxs-lookup"><span data-stu-id="870d2-116">If a transfer is in progress, it should be set to a value from 0 to 100 indicating the transfer's percent of completion.</span></span>
  
<span data-ttu-id="870d2-117">数値ステータス コードに関連付けられているテキストは、 **PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)) のプロパティに表示されます。</span><span class="sxs-lookup"><span data-stu-id="870d2-117">The text associated with the numeric status code appears in the **PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="870d2-118">このプロパティには、次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="870d2-118">The following flags can be set for this property:</span></span>
  
<span data-ttu-id="870d2-119">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="870d2-119">MSGSTATUS_REMOTE_DELETE</span></span>
  
> <span data-ttu-id="870d2-120">メッセージ転送が削除されます。</span><span class="sxs-lookup"><span data-stu-id="870d2-120">The message transfer is deleted.</span></span>
    
<span data-ttu-id="870d2-121">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="870d2-121">MSGSTATUS_REMOTE_DOWNLOAD</span></span>
  
> <span data-ttu-id="870d2-122">メッセージの転送は実行中です。</span><span class="sxs-lookup"><span data-stu-id="870d2-122">The message transfer is in progress.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="870d2-123">関連リソース</span><span class="sxs-lookup"><span data-stu-id="870d2-123">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="870d2-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="870d2-124">Header files</span></span>

<span data-ttu-id="870d2-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="870d2-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="870d2-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="870d2-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="870d2-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="870d2-127">Mapitags.h</span></span>
  
> <span data-ttu-id="870d2-128">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="870d2-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="870d2-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="870d2-129">See also</span></span>



[<span data-ttu-id="870d2-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="870d2-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="870d2-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="870d2-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="870d2-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="870d2-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="870d2-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="870d2-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

