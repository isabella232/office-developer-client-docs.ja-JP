---
title: PidLidSharingLocalType 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: aa1f76a3f410294de9c7ebfb3e64bbb1cd6cc25c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394714"
---
# <a name="pidlidsharinglocaltype-canonical-property"></a><span data-ttu-id="00b28-103">PidLidSharingLocalType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="00b28-103">PidLidSharingLocalType Canonical Property</span></span>

  
  
<span data-ttu-id="00b28-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00b28-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00b28-105">共有されているフォルダーの**PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) プロパティの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="00b28-105">Specifies the value of the **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) property of the folder that is being shared.</span></span> <span data-ttu-id="00b28-106">これは、共有メッセージのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="00b28-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="00b28-107">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="00b28-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="00b28-108">dispidSharingLocalType</span><span class="sxs-lookup"><span data-stu-id="00b28-108">dispidSharingLocalType</span></span>  <br/> |
|<span data-ttu-id="00b28-109">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="00b28-109">Property set:</span></span>  <br/> |<span data-ttu-id="00b28-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="00b28-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="00b28-111">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="00b28-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="00b28-112">0x00008A14</span><span class="sxs-lookup"><span data-stu-id="00b28-112">0x00008A14</span></span>  <br/> |
|<span data-ttu-id="00b28-113">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="00b28-113">Data type:</span></span>  <br/> |<span data-ttu-id="00b28-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="00b28-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="00b28-115">エリア:</span><span class="sxs-lookup"><span data-stu-id="00b28-115">Area:</span></span>  <br/> |<span data-ttu-id="00b28-116">共有</span><span class="sxs-lookup"><span data-stu-id="00b28-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00b28-117">備考</span><span class="sxs-lookup"><span data-stu-id="00b28-117">Remarks</span></span>

<span data-ttu-id="00b28-118">このプロパティの値は、次のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="00b28-118">The value of this property must be one of the following:</span></span>
  
- <span data-ttu-id="00b28-119">"IPF。予定]</span><span class="sxs-lookup"><span data-stu-id="00b28-119">"IPF.Appointment"</span></span>
    
- <span data-ttu-id="00b28-120">"IPF。連絡先"</span><span class="sxs-lookup"><span data-stu-id="00b28-120">"IPF.Contact"</span></span>
    
- <span data-ttu-id="00b28-121">"IPF。タスク</span><span class="sxs-lookup"><span data-stu-id="00b28-121">"IPF.Task"</span></span>
    
- <span data-ttu-id="00b28-122">"IPF。StickyNote」</span><span class="sxs-lookup"><span data-stu-id="00b28-122">"IPF.StickyNote"</span></span>
    
- <span data-ttu-id="00b28-123">"IPF。仕訳帳"</span><span class="sxs-lookup"><span data-stu-id="00b28-123">"IPF.Journal"</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="00b28-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="00b28-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="00b28-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="00b28-125">Protocol specifications</span></span>

<span data-ttu-id="00b28-126">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00b28-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00b28-127">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="00b28-127">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="00b28-128">[[MS OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00b28-128">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00b28-129">クライアント間でのメールボックスのフォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="00b28-129">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="00b28-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="00b28-130">Header files</span></span>

<span data-ttu-id="00b28-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="00b28-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="00b28-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="00b28-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="00b28-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="00b28-133">See also</span></span>



[<span data-ttu-id="00b28-134">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="00b28-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="00b28-135">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="00b28-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="00b28-136">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="00b28-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="00b28-137">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="00b28-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

