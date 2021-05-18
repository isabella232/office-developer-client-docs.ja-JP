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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8d58342e0460352bd9d260cb6e73de358cb2fc23
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359536"
---
# <a name="pidtagrowid-canonical-property"></a><span data-ttu-id="a56a7-103">PidTagRowid 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a56a7-103">PidTagRowid Canonical Property</span></span>

  
  
<span data-ttu-id="a56a7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a56a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a56a7-105">受信者テーブルまたは状態テーブル内の受信者の一意の識別子を含む。</span><span class="sxs-lookup"><span data-stu-id="a56a7-105">Contains a unique identifier for a recipient in a recipient table or status table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a56a7-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a56a7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a56a7-107">PR_ROWID</span><span class="sxs-lookup"><span data-stu-id="a56a7-107">PR_ROWID</span></span>  <br/> |
|<span data-ttu-id="a56a7-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a56a7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a56a7-109">0x3000</span><span class="sxs-lookup"><span data-stu-id="a56a7-109">0x3000</span></span>  <br/> |
|<span data-ttu-id="a56a7-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a56a7-110">Data type:</span></span>  <br/> |<span data-ttu-id="a56a7-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a56a7-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a56a7-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="a56a7-112">Area:</span></span>  <br/> |<span data-ttu-id="a56a7-113">MAPI 共通</span><span class="sxs-lookup"><span data-stu-id="a56a7-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a56a7-114">注釈</span><span class="sxs-lookup"><span data-stu-id="a56a7-114">Remarks</span></span>

<span data-ttu-id="a56a7-115">このプロパティは、テーブルを所有するオブジェクトの有効期間にのみ有効な一時的な値です。</span><span class="sxs-lookup"><span data-stu-id="a56a7-115">This property is a temporary value that is valid only for the life of the object that owns the table.</span></span> <span data-ttu-id="a56a7-116">テーブルの列として表示されますが、格納されません。</span><span class="sxs-lookup"><span data-stu-id="a56a7-116">It appears as a column of the table but is not stored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a56a7-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a56a7-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a56a7-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a56a7-118">Protocol specifications</span></span>

<span data-ttu-id="a56a7-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a56a7-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a56a7-120">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="a56a7-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a56a7-121">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a56a7-121">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a56a7-122">クライアントとサーバー間のデータ転送の順序とフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="a56a7-122">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a56a7-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a56a7-123">Header files</span></span>

<span data-ttu-id="a56a7-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a56a7-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="a56a7-125">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a56a7-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="a56a7-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a56a7-126">Mapitags.h</span></span>
  
> <span data-ttu-id="a56a7-127">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="a56a7-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a56a7-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="a56a7-128">See also</span></span>



[<span data-ttu-id="a56a7-129">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="a56a7-129">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="a56a7-130">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="a56a7-130">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)


[<span data-ttu-id="a56a7-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a56a7-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a56a7-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a56a7-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a56a7-133">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="a56a7-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a56a7-134">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="a56a7-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

