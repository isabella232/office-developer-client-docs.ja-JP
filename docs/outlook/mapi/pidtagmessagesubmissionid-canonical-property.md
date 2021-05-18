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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 723affa054cb35a9cc7a2ee28e051e3b9a6d04e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329401"
---
# <a name="pidtagmessagesubmissionid-canonical-property"></a><span data-ttu-id="9281f-103">PidTagMessageSubmissionId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9281f-103">PidTagMessageSubmissionId Canonical Property</span></span>

  
  
<span data-ttu-id="9281f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9281f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9281f-105">メッセージ転送エージェント (MTA) のメッセージ転送システム (MTS) 識別子が含まれる。</span><span class="sxs-lookup"><span data-stu-id="9281f-105">Contains a message transfer system (MTS) identifier for the message transfer agent (MTA).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9281f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9281f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9281f-107">PR_MESSAGE_SUBMISSION_ID</span><span class="sxs-lookup"><span data-stu-id="9281f-107">PR_MESSAGE_SUBMISSION_ID</span></span>  <br/> |
|<span data-ttu-id="9281f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9281f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9281f-109">0x0047</span><span class="sxs-lookup"><span data-stu-id="9281f-109">0x0047</span></span>  <br/> |
|<span data-ttu-id="9281f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9281f-110">Data type:</span></span>  <br/> |<span data-ttu-id="9281f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9281f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9281f-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="9281f-112">Area:</span></span>  <br/> |<span data-ttu-id="9281f-113">メール</span><span class="sxs-lookup"><span data-stu-id="9281f-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9281f-114">注釈</span><span class="sxs-lookup"><span data-stu-id="9281f-114">Remarks</span></span>

<span data-ttu-id="9281f-115">このプロパティは、メッセージの送信が正常に完了すると、MTA によって返されます。</span><span class="sxs-lookup"><span data-stu-id="9281f-115">This property is returned by the MTA upon successful completion of message submission.</span></span> <span data-ttu-id="9281f-116">キャンセルの要求など、このメッセージに関する MTA との今後の連絡先は、このプロパティの MTS 識別子を使用します。</span><span class="sxs-lookup"><span data-stu-id="9281f-116">Any future contact with the MTA regarding this message, such as requesting cancellation, uses the MTS identifier in this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9281f-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9281f-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9281f-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9281f-118">Protocol specifications</span></span>

<span data-ttu-id="9281f-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9281f-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9281f-120">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="9281f-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9281f-121">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9281f-121">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9281f-122">メッセージオブジェクトと添付ファイル オブジェクトを効率的なストリーム表現にエンコードおよびデコードします。</span><span class="sxs-lookup"><span data-stu-id="9281f-122">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9281f-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="9281f-123">Header files</span></span>

<span data-ttu-id="9281f-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9281f-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="9281f-125">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9281f-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="9281f-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9281f-126">Mapitags.h</span></span>
  
> <span data-ttu-id="9281f-127">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="9281f-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9281f-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="9281f-128">See also</span></span>



[<span data-ttu-id="9281f-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="9281f-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9281f-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9281f-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9281f-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="9281f-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9281f-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="9281f-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

