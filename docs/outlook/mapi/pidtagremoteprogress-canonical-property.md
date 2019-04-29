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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a5a9d0796bc92514ae6d990b7328364b85bc55cd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439843"
---
# <a name="pidtagremoteprogress-canonical-property"></a><span data-ttu-id="a3eed-103">PidTagRemoteProgress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a3eed-103">PidTagRemoteProgress Canonical Property</span></span>

  
  
<span data-ttu-id="a3eed-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3eed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3eed-105">このプロパティには、リモート転送の状態を示す番号が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a3eed-105">This property contains a number that indicates the status of a remote transfer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a3eed-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a3eed-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a3eed-107">PR_REMOTE_PROGRESS</span><span class="sxs-lookup"><span data-stu-id="a3eed-107">PR_REMOTE_PROGRESS</span></span>  <br/> |
|<span data-ttu-id="a3eed-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a3eed-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a3eed-109">0x3E0B</span><span class="sxs-lookup"><span data-stu-id="a3eed-109">0x3E0B</span></span>  <br/> |
|<span data-ttu-id="a3eed-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a3eed-110">Data type:</span></span>  <br/> |<span data-ttu-id="a3eed-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a3eed-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a3eed-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="a3eed-112">Area:</span></span>  <br/> |<span data-ttu-id="a3eed-113">MAPI の状態</span><span class="sxs-lookup"><span data-stu-id="a3eed-113">MAPI Status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a3eed-114">注釈</span><span class="sxs-lookup"><span data-stu-id="a3eed-114">Remarks</span></span>

<span data-ttu-id="a3eed-115">転送が進行中でない場合、このプロパティは1に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3eed-115">If no transfer is in progress, this property should be set to 1.</span></span> <span data-ttu-id="a3eed-116">転送が進行中の場合は、転送の完了率を示す 0 ~ 100 の値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3eed-116">If a transfer is in progress, it should be set to a value from 0 to 100 indicating the transfer's percent of completion.</span></span>
  
<span data-ttu-id="a3eed-117">数値状態コードに関連付けられたテキストは、 **PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)) プロパティに表示されます。</span><span class="sxs-lookup"><span data-stu-id="a3eed-117">The text associated with the numeric status code appears in the **PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="a3eed-118">このプロパティには、次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a3eed-118">The following flags can be set for this property:</span></span>
  
<span data-ttu-id="a3eed-119">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="a3eed-119">MSGSTATUS_REMOTE_DELETE</span></span>
  
> <span data-ttu-id="a3eed-120">メッセージの転送が削除されます。</span><span class="sxs-lookup"><span data-stu-id="a3eed-120">The message transfer is deleted.</span></span>
    
<span data-ttu-id="a3eed-121">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="a3eed-121">MSGSTATUS_REMOTE_DOWNLOAD</span></span>
  
> <span data-ttu-id="a3eed-122">メッセージの転送が進行中です。</span><span class="sxs-lookup"><span data-stu-id="a3eed-122">The message transfer is in progress.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="a3eed-123">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a3eed-123">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a3eed-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="a3eed-124">Header files</span></span>

<span data-ttu-id="a3eed-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a3eed-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a3eed-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a3eed-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="a3eed-127">Mapitags</span><span class="sxs-lookup"><span data-stu-id="a3eed-127">Mapitags.h</span></span>
  
> <span data-ttu-id="a3eed-128">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a3eed-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a3eed-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="a3eed-129">See also</span></span>



[<span data-ttu-id="a3eed-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a3eed-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a3eed-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a3eed-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a3eed-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a3eed-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a3eed-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a3eed-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

