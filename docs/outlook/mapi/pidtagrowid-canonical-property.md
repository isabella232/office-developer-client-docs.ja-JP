---
title: PidTagRowid 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRowid
api_type:
- COM
ms.assetid: 0fdcb55a-2971-4c7d-b61e-7ada2d19d0e6
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: efa778f51ac047c911deb6a3c4d5d9e718dc33fb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565040"
---
# <a name="pidtagrowid-canonical-property"></a><span data-ttu-id="245a1-103">PidTagRowid 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="245a1-103">PidTagRowid Canonical Property</span></span>

  
  
<span data-ttu-id="245a1-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="245a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="245a1-105">受信者テーブルまたはステータス テーブル内で受信者の一意の識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="245a1-105">Contains a unique identifier for a recipient in a recipient table or status table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="245a1-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="245a1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="245a1-107">PR_ROWID</span><span class="sxs-lookup"><span data-stu-id="245a1-107">PR_ROWID</span></span>  <br/> |
|<span data-ttu-id="245a1-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="245a1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="245a1-109">0x3000</span><span class="sxs-lookup"><span data-stu-id="245a1-109">0x3000</span></span>  <br/> |
|<span data-ttu-id="245a1-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="245a1-110">Data type:</span></span>  <br/> |<span data-ttu-id="245a1-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="245a1-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="245a1-112">領域:</span><span class="sxs-lookup"><span data-stu-id="245a1-112">Area:</span></span>  <br/> |<span data-ttu-id="245a1-113">一般的な MAPI</span><span class="sxs-lookup"><span data-stu-id="245a1-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="245a1-114">注釈</span><span class="sxs-lookup"><span data-stu-id="245a1-114">Remarks</span></span>

<span data-ttu-id="245a1-115">このプロパティは、テーブルを所有するオブジェクトの有効期間にのみ有効な一時的な値です。</span><span class="sxs-lookup"><span data-stu-id="245a1-115">This property is a temporary value that is valid only for the life of the object that owns the table.</span></span> <span data-ttu-id="245a1-116">テーブルの列として表示されますが、保存されていません。</span><span class="sxs-lookup"><span data-stu-id="245a1-116">It appears as a column of the table but is not stored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="245a1-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="245a1-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="245a1-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="245a1-118">Protocol specifications</span></span>

<span data-ttu-id="245a1-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="245a1-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="245a1-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="245a1-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="245a1-121">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="245a1-121">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="245a1-122">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="245a1-122">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="245a1-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="245a1-123">Header files</span></span>

<span data-ttu-id="245a1-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="245a1-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="245a1-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="245a1-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="245a1-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="245a1-126">Mapitags.h</span></span>
  
> <span data-ttu-id="245a1-127">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="245a1-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="245a1-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="245a1-128">See also</span></span>



[<span data-ttu-id="245a1-129">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="245a1-129">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="245a1-130">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="245a1-130">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)


[<span data-ttu-id="245a1-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="245a1-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="245a1-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="245a1-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="245a1-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="245a1-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="245a1-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="245a1-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

