---
title: PidLidIsRecurring 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidIsRecurring
api_type:
- COM
ms.assetid: 1f8ecc22-badc-4278-a3c6-fcd398f5bf24
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c920cd42a27c03ffcff63bbd2e0049ddb6f81158
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315436"
---
# <a name="pidlidisrecurring-canonical-property"></a><span data-ttu-id="b1650-103">PidLidIsRecurring 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b1650-103">PidLidIsRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="b1650-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1650-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1650-105">オブジェクトが定期的なアイテムに関連付けられているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="b1650-105">Specifies whether or not the object is associated with a recurring series.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b1650-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b1650-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b1650-107">LID_IS_RECURRING</span><span class="sxs-lookup"><span data-stu-id="b1650-107">LID_IS_RECURRING</span></span>  <br/> |
|<span data-ttu-id="b1650-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="b1650-108">Property set:</span></span>  <br/> |<span data-ttu-id="b1650-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="b1650-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="b1650-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="b1650-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b1650-111">0x00000005</span><span class="sxs-lookup"><span data-stu-id="b1650-111">0x00000005</span></span>  <br/> |
|<span data-ttu-id="b1650-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b1650-112">Data type:</span></span>  <br/> |<span data-ttu-id="b1650-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b1650-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="b1650-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="b1650-114">Area:</span></span>  <br/> |<span data-ttu-id="b1650-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="b1650-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1650-116">解説</span><span class="sxs-lookup"><span data-stu-id="b1650-116">Remarks</span></span>

<span data-ttu-id="b1650-117">値 TRUE は、オブジェクトが定期的なアイテムまたは例外 (孤立インスタンスを含む) のいずれかを表すことを示します。</span><span class="sxs-lookup"><span data-stu-id="b1650-117">A value of TRUE indicates that the object represents either a recurring series or an exception (including an orphan instance).</span></span> <span data-ttu-id="b1650-118">値が FALSE の場合、またはこのプロパティが存在しない場合は、オブジェクトが1つのインスタンスを表すことを示します。</span><span class="sxs-lookup"><span data-stu-id="b1650-118">A value of FALSE, or the absence of this property, indicates that the object represents a single instance.</span></span> <span data-ttu-id="b1650-119">このプロパティと**PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md)) プロパティの違いに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b1650-119">Note the difference between this property and the **PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b1650-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b1650-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b1650-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b1650-121">Protocol specifications</span></span>

<span data-ttu-id="b1650-122">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1650-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1650-123">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="b1650-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b1650-124">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1650-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1650-125">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="b1650-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b1650-126">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="b1650-126">Header files</span></span>

<span data-ttu-id="b1650-127">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b1650-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="b1650-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b1650-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b1650-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="b1650-129">See also</span></span>



[<span data-ttu-id="b1650-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="b1650-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b1650-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b1650-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b1650-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b1650-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b1650-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b1650-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

