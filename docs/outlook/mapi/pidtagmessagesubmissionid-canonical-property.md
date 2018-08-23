---
title: PidTagMessageSubmissionId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSubmissionId
api_type:
- HeaderDef
ms.assetid: 0a799fe5-04e2-4e1d-b0cd-9bdd2577d299
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3a26a8483e584ccc5cf9f33e0dbd75f379c01633
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569667"
---
# <a name="pidtagmessagesubmissionid-canonical-property"></a><span data-ttu-id="de3a0-103">PidTagMessageSubmissionId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="de3a0-103">PidTagMessageSubmissionId Canonical Property</span></span>

  
  
<span data-ttu-id="de3a0-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de3a0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de3a0-105">メッセージ転送エージェント (MTA) のメッセージ転送システム (MTS) 識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="de3a0-105">Contains a message transfer system (MTS) identifier for the message transfer agent (MTA).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="de3a0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="de3a0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="de3a0-107">PR_MESSAGE_SUBMISSION_ID</span><span class="sxs-lookup"><span data-stu-id="de3a0-107">PR_MESSAGE_SUBMISSION_ID</span></span>  <br/> |
|<span data-ttu-id="de3a0-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="de3a0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="de3a0-109">0x0047</span><span class="sxs-lookup"><span data-stu-id="de3a0-109">0x0047</span></span>  <br/> |
|<span data-ttu-id="de3a0-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="de3a0-110">Data type:</span></span>  <br/> |<span data-ttu-id="de3a0-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="de3a0-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="de3a0-112">領域:</span><span class="sxs-lookup"><span data-stu-id="de3a0-112">Area:</span></span>  <br/> |<span data-ttu-id="de3a0-113">メール</span><span class="sxs-lookup"><span data-stu-id="de3a0-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de3a0-114">注釈</span><span class="sxs-lookup"><span data-stu-id="de3a0-114">Remarks</span></span>

<span data-ttu-id="de3a0-115">メッセージの送信が正常に完了すると、MTA では、このプロパティが返されます。</span><span class="sxs-lookup"><span data-stu-id="de3a0-115">This property is returned by the MTA upon successful completion of message submission.</span></span> <span data-ttu-id="de3a0-116">要求の取り消しなど、このメッセージに関する MTA と今後の接続では、このプロパティで MTS 識別子を使用します。</span><span class="sxs-lookup"><span data-stu-id="de3a0-116">Any future contact with the MTA regarding this message, such as requesting cancellation, uses the MTS identifier in this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="de3a0-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="de3a0-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="de3a0-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="de3a0-118">Protocol specifications</span></span>

<span data-ttu-id="de3a0-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de3a0-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de3a0-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="de3a0-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="de3a0-121">[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de3a0-121">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de3a0-122">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="de3a0-122">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="de3a0-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="de3a0-123">Header files</span></span>

<span data-ttu-id="de3a0-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="de3a0-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="de3a0-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="de3a0-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="de3a0-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="de3a0-126">Mapitags.h</span></span>
  
> <span data-ttu-id="de3a0-127">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="de3a0-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="de3a0-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="de3a0-128">See also</span></span>



[<span data-ttu-id="de3a0-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="de3a0-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="de3a0-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="de3a0-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="de3a0-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="de3a0-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="de3a0-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="de3a0-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

