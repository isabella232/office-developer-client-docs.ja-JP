---
title: PidLidFExceptionalBody 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFExceptionalBody
api_type:
- COM
ms.assetid: 327516e8-ed3f-40fc-9604-03a70aecef5a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 93eb98aee19ea3f46a4e01e2c80150c3efe893a5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393902"
---
# <a name="pidlidfexceptionalbody-canonical-property"></a><span data-ttu-id="0262d-103">PidLidFExceptionalBody 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0262d-103">PidLidFExceptionalBody Canonical Property</span></span>

  
  
<span data-ttu-id="0262d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0262d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0262d-105">例外オブジェクトには、定期的な予定表オブジェクトとは異なるボディ メッセージが埋め込まれていることを示します。</span><span class="sxs-lookup"><span data-stu-id="0262d-105">Indicates that the exception embedded message object has a body that differs from the recurring calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0262d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="0262d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0262d-107">dispidFExceptionalBody</span><span class="sxs-lookup"><span data-stu-id="0262d-107">dispidFExceptionalBody</span></span>  <br/> |
|<span data-ttu-id="0262d-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="0262d-108">Property set:</span></span>  <br/> |<span data-ttu-id="0262d-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="0262d-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="0262d-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="0262d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0262d-111">0x00008206</span><span class="sxs-lookup"><span data-stu-id="0262d-111">0x00008206</span></span>  <br/> |
|<span data-ttu-id="0262d-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="0262d-112">Data type:</span></span>  <br/> |<span data-ttu-id="0262d-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="0262d-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="0262d-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="0262d-114">Area:</span></span>  <br/> |<span data-ttu-id="0262d-115">会議</span><span class="sxs-lookup"><span data-stu-id="0262d-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0262d-116">備考</span><span class="sxs-lookup"><span data-stu-id="0262d-116">Remarks</span></span>

<span data-ttu-id="0262d-117">このプロパティの値が TRUE の場合は、例外によってオブジェクトには、本体が必要です。 メッセージが埋め込まれています。</span><span class="sxs-lookup"><span data-stu-id="0262d-117">If the value of this property is TRUE, then the exception embedded message object must have a body.</span></span> <span data-ttu-id="0262d-118">このプロパティの値が FALSE の場合、またはプロパティが存在しない場合は、クライアントまたはサーバーする必要があります本体から取得、定期的な予定表オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="0262d-118">If the value of this property is FALSE, or if the property does not exist, then a client or server must obtain the body from the recurring calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0262d-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0262d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0262d-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="0262d-120">Protocol specifications</span></span>

<span data-ttu-id="0262d-121">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0262d-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0262d-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="0262d-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0262d-123">[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0262d-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0262d-124">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="0262d-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0262d-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="0262d-125">Header files</span></span>

<span data-ttu-id="0262d-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0262d-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="0262d-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0262d-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0262d-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="0262d-128">See also</span></span>



[<span data-ttu-id="0262d-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0262d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0262d-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0262d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0262d-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0262d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0262d-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0262d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

