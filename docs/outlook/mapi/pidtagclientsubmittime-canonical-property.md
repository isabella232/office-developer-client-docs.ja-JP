---
title: PidTagClientSubmitTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagClientSubmitTime
api_type:
- HeaderDef
ms.assetid: d46e1063-6421-410d-a445-7477fea42089
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8c7ca5b2b6f5f3131c2fcb70ff0043825a68a91f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580125"
---
# <a name="pidtagclientsubmittime-canonical-property"></a><span data-ttu-id="09e0c-103">PidTagClientSubmitTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="09e0c-103">PidTagClientSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="09e0c-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="09e0c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="09e0c-105">メッセージの送信者にメッセージが送信されたときの日時が含まれています。</span><span class="sxs-lookup"><span data-stu-id="09e0c-105">Contains the date and time the message sender submitted a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="09e0c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="09e0c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="09e0c-107">PR_CLIENT_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="09e0c-107">PR_CLIENT_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="09e0c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="09e0c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="09e0c-109">0x0039</span><span class="sxs-lookup"><span data-stu-id="09e0c-109">0x0039</span></span>  <br/> |
|<span data-ttu-id="09e0c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="09e0c-110">Data type:</span></span>  <br/> |<span data-ttu-id="09e0c-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="09e0c-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="09e0c-112">領域:</span><span class="sxs-lookup"><span data-stu-id="09e0c-112">Area:</span></span>  <br/> |<span data-ttu-id="09e0c-113">メッセージの時刻</span><span class="sxs-lookup"><span data-stu-id="09e0c-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="09e0c-114">注釈</span><span class="sxs-lookup"><span data-stu-id="09e0c-114">Remarks</span></span>

<span data-ttu-id="09e0c-115">ストア プロバイダーは、クライアント アプリケーションが[IMessage::SubmitMessage](imessage-submitmessage.md)を呼び出したときに**PR_CLIENT_SUBMIT_TIME**を設定します。</span><span class="sxs-lookup"><span data-stu-id="09e0c-115">The store provider sets **PR_CLIENT_SUBMIT_TIME** to the time that the client application called [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="09e0c-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="09e0c-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="09e0c-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="09e0c-117">Protocol specifications</span></span>

<span data-ttu-id="09e0c-118">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="09e0c-118">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="09e0c-119">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="09e0c-119">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="09e0c-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="09e0c-120">Header files</span></span>

<span data-ttu-id="09e0c-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="09e0c-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="09e0c-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="09e0c-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="09e0c-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="09e0c-123">Mapitags.h</span></span>
  
> <span data-ttu-id="09e0c-124">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="09e0c-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="09e0c-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="09e0c-125">See also</span></span>



[<span data-ttu-id="09e0c-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="09e0c-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="09e0c-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="09e0c-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="09e0c-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="09e0c-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="09e0c-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="09e0c-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

