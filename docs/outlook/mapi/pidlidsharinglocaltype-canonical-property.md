---
title: PidLidSharingLocalType の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingLocalType
api_type:
- COM
ms.assetid: 6ac438a1-d36f-424f-b4b4-d6f2d26fd350
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ab9bad51efc4aa9b113bc8d215426c642fc60b9d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802176"
---
# <a name="pidlidsharinglocaltype-canonical-property"></a><span data-ttu-id="be978-103">PidLidSharingLocalType の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="be978-103">PidLidSharingLocalType Canonical Property</span></span>

  
  
<span data-ttu-id="be978-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="be978-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="be978-105">共有されているフォルダーの**PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) プロパティの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="be978-105">Specifies the value of the **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) property of the folder that is being shared.</span></span> <span data-ttu-id="be978-106">これは、共有メッセージのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="be978-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="be978-107">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="be978-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="be978-108">dispidSharingLocalType</span><span class="sxs-lookup"><span data-stu-id="be978-108">dispidSharingLocalType</span></span>  <br/> |
|<span data-ttu-id="be978-109">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="be978-109">Property set:</span></span>  <br/> |<span data-ttu-id="be978-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="be978-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="be978-111">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="be978-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="be978-112">0x00008A14</span><span class="sxs-lookup"><span data-stu-id="be978-112">0x00008A14</span></span>  <br/> |
|<span data-ttu-id="be978-113">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="be978-113">Data type:</span></span>  <br/> |<span data-ttu-id="be978-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="be978-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="be978-115">領域:</span><span class="sxs-lookup"><span data-stu-id="be978-115">Area:</span></span>  <br/> |<span data-ttu-id="be978-116">共有</span><span class="sxs-lookup"><span data-stu-id="be978-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be978-117">備考</span><span class="sxs-lookup"><span data-stu-id="be978-117">Remarks</span></span>

<span data-ttu-id="be978-118">このプロパティの値は、次のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="be978-118">The value of this property must be one of the following:</span></span>
  
- <span data-ttu-id="be978-119">"IPF。予定]</span><span class="sxs-lookup"><span data-stu-id="be978-119">"IPF.Appointment"</span></span>
    
- <span data-ttu-id="be978-120">"IPF。連絡先"</span><span class="sxs-lookup"><span data-stu-id="be978-120">"IPF.Contact"</span></span>
    
- <span data-ttu-id="be978-121">"IPF。タスク</span><span class="sxs-lookup"><span data-stu-id="be978-121">"IPF.Task"</span></span>
    
- <span data-ttu-id="be978-122">"IPF。StickyNote」</span><span class="sxs-lookup"><span data-stu-id="be978-122">"IPF.StickyNote"</span></span>
    
- <span data-ttu-id="be978-123">"IPF。仕訳帳"</span><span class="sxs-lookup"><span data-stu-id="be978-123">"IPF.Journal"</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="be978-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="be978-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="be978-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="be978-125">Protocol specifications</span></span>

<span data-ttu-id="be978-126">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="be978-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="be978-127">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="be978-127">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="be978-128">[[MS OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="be978-128">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="be978-129">クライアント間でのメールボックスのフォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="be978-129">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="be978-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="be978-130">Header files</span></span>

<span data-ttu-id="be978-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="be978-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="be978-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="be978-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="be978-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="be978-133">See also</span></span>



[<span data-ttu-id="be978-134">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="be978-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="be978-135">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="be978-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="be978-136">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="be978-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="be978-137">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="be978-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

