---
title: PidLidForwardInstance 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidForwardInstance
api_type:
- COM
ms.assetid: 055bdcaf-5002-44a6-b2b6-87244b2bea93
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 47dd6f10d1dbd25ea275ea96a2eddb6e9c6dfacb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571774"
---
# <a name="pidlidforwardinstance-canonical-property"></a><span data-ttu-id="83fdd-103">PidLidForwardInstance 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="83fdd-103">PidLidForwardInstance Canonical Property</span></span>

  
  
<span data-ttu-id="83fdd-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="83fdd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="83fdd-105">転送された (開催者によって転送された) 場合でも、開催者から送信された招待状をしているのではなく、会議出席依頼が定期的な一連の例外を表すことを示します。</span><span class="sxs-lookup"><span data-stu-id="83fdd-105">Indicates that the meeting request represents an exception to a recurring series, and it was forwarded (even when forwarded by the organizer) rather than being an invitation sent by the organizer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="83fdd-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="83fdd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="83fdd-107">dispidFwrdInstance</span><span class="sxs-lookup"><span data-stu-id="83fdd-107">dispidFwrdInstance</span></span>  <br/> |
|<span data-ttu-id="83fdd-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="83fdd-108">Property set:</span></span>  <br/> |<span data-ttu-id="83fdd-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="83fdd-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="83fdd-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="83fdd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="83fdd-111">0x0000820A</span><span class="sxs-lookup"><span data-stu-id="83fdd-111">0x0000820A</span></span>  <br/> |
|<span data-ttu-id="83fdd-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="83fdd-112">Data type:</span></span>  <br/> |<span data-ttu-id="83fdd-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="83fdd-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="83fdd-114">領域:</span><span class="sxs-lookup"><span data-stu-id="83fdd-114">Area:</span></span>  <br/> |<span data-ttu-id="83fdd-115">会議</span><span class="sxs-lookup"><span data-stu-id="83fdd-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="83fdd-116">注釈</span><span class="sxs-lookup"><span data-stu-id="83fdd-116">Remarks</span></span>

<span data-ttu-id="83fdd-117">このプロパティの値は、会議出席依頼が転送されたインスタンスではないことを示します。</span><span class="sxs-lookup"><span data-stu-id="83fdd-117">A value of FALSE for this property indicates that the meeting request is not a forwarded instance.</span></span> <span data-ttu-id="83fdd-118">このプロパティが必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="83fdd-118">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="83fdd-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="83fdd-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="83fdd-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="83fdd-120">Protocol specifications</span></span>

<span data-ttu-id="83fdd-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="83fdd-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="83fdd-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="83fdd-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="83fdd-123">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="83fdd-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="83fdd-124">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="83fdd-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="83fdd-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="83fdd-125">Header files</span></span>

<span data-ttu-id="83fdd-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="83fdd-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="83fdd-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="83fdd-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="83fdd-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="83fdd-128">See also</span></span>



[<span data-ttu-id="83fdd-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="83fdd-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="83fdd-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="83fdd-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="83fdd-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="83fdd-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="83fdd-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="83fdd-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

