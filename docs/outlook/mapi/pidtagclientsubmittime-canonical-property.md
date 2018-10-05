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
ms.openlocfilehash: 851441e419c17d8f5fef27c785ea4b829a4ae443
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385838"
---
# <a name="pidtagclientsubmittime-canonical-property"></a><span data-ttu-id="ac481-103">PidTagClientSubmitTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ac481-103">PidTagClientSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="ac481-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac481-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac481-105">メッセージの送信者にメッセージが送信されたときの日時が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ac481-105">Contains the date and time the message sender submitted a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ac481-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ac481-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ac481-107">PR_CLIENT_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="ac481-107">PR_CLIENT_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="ac481-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ac481-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ac481-109">0x0039</span><span class="sxs-lookup"><span data-stu-id="ac481-109">0x0039</span></span>  <br/> |
|<span data-ttu-id="ac481-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ac481-110">Data type:</span></span>  <br/> |<span data-ttu-id="ac481-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="ac481-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="ac481-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="ac481-112">Area:</span></span>  <br/> |<span data-ttu-id="ac481-113">メッセージの時刻</span><span class="sxs-lookup"><span data-stu-id="ac481-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac481-114">備考</span><span class="sxs-lookup"><span data-stu-id="ac481-114">Remarks</span></span>

<span data-ttu-id="ac481-115">ストア プロバイダーは、クライアント アプリケーションが[IMessage::SubmitMessage](imessage-submitmessage.md)を呼び出したときに**PR_CLIENT_SUBMIT_TIME**を設定します。</span><span class="sxs-lookup"><span data-stu-id="ac481-115">The store provider sets **PR_CLIENT_SUBMIT_TIME** to the time that the client application called [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ac481-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ac481-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ac481-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ac481-117">Protocol specifications</span></span>

<span data-ttu-id="ac481-118">[[MS OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac481-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ac481-119">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="ac481-119">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ac481-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ac481-120">Header files</span></span>

<span data-ttu-id="ac481-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ac481-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="ac481-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ac481-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="ac481-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ac481-123">Mapitags.h</span></span>
  
> <span data-ttu-id="ac481-124">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ac481-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ac481-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="ac481-125">See also</span></span>



[<span data-ttu-id="ac481-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ac481-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ac481-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ac481-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ac481-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ac481-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ac481-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ac481-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

