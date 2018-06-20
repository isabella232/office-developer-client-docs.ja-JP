---
title: PidTagRowid の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e8d0e79e01040c1cc3d46e73a7e6a456a915a67f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803363"
---
# <a name="pidtagrowid-canonical-property"></a><span data-ttu-id="18de3-103">PidTagRowid の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="18de3-103">PidTagRowid Canonical Property</span></span>

  
  
<span data-ttu-id="18de3-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="18de3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="18de3-105">受信者テーブルまたはステータス テーブル内で受信者の一意の識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="18de3-105">Contains a unique identifier for a recipient in a recipient table or status table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="18de3-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="18de3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="18de3-107">PR_ROWID</span><span class="sxs-lookup"><span data-stu-id="18de3-107">PR_ROWID</span></span>  <br/> |
|<span data-ttu-id="18de3-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="18de3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="18de3-109">0x3000</span><span class="sxs-lookup"><span data-stu-id="18de3-109">0x3000</span></span>  <br/> |
|<span data-ttu-id="18de3-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="18de3-110">Data type:</span></span>  <br/> |<span data-ttu-id="18de3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="18de3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="18de3-112">領域:</span><span class="sxs-lookup"><span data-stu-id="18de3-112">Area:</span></span>  <br/> |<span data-ttu-id="18de3-113">一般的な MAPI</span><span class="sxs-lookup"><span data-stu-id="18de3-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18de3-114">備考</span><span class="sxs-lookup"><span data-stu-id="18de3-114">Remarks</span></span>

<span data-ttu-id="18de3-115">このプロパティは、テーブルを所有するオブジェクトの有効期間にのみ有効な一時的な値です。</span><span class="sxs-lookup"><span data-stu-id="18de3-115">This property is a temporary value that is valid only for the life of the object that owns the table.</span></span> <span data-ttu-id="18de3-116">テーブルの列として表示されますが、保存されていません。</span><span class="sxs-lookup"><span data-stu-id="18de3-116">It appears as a column of the table but is not stored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="18de3-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="18de3-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="18de3-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="18de3-118">Protocol specifications</span></span>

<span data-ttu-id="18de3-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18de3-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18de3-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="18de3-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="18de3-121">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18de3-121">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18de3-122">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="18de3-122">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="18de3-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="18de3-123">Header files</span></span>

<span data-ttu-id="18de3-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="18de3-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="18de3-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="18de3-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="18de3-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="18de3-126">Mapitags.h</span></span>
  
> <span data-ttu-id="18de3-127">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="18de3-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="18de3-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="18de3-128">See also</span></span>



[<span data-ttu-id="18de3-129">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="18de3-129">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="18de3-130">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="18de3-130">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)


[<span data-ttu-id="18de3-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="18de3-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="18de3-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="18de3-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="18de3-133">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="18de3-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="18de3-134">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="18de3-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

