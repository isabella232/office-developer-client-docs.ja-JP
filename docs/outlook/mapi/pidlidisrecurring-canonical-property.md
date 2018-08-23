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
ms.openlocfilehash: f7813125e18f437087fa06c57f8442c84a81d80d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574063"
---
# <a name="pidlidisrecurring-canonical-property"></a><span data-ttu-id="308e6-103">PidLidIsRecurring 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="308e6-103">PidLidIsRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="308e6-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="308e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="308e6-105">オブジェクトが定期的に関連付けられているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="308e6-105">Specifies whether or not the object is associated with a recurring series.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="308e6-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="308e6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="308e6-107">LID_IS_RECURRING</span><span class="sxs-lookup"><span data-stu-id="308e6-107">LID_IS_RECURRING</span></span>  <br/> |
|<span data-ttu-id="308e6-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="308e6-108">Property set:</span></span>  <br/> |<span data-ttu-id="308e6-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="308e6-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="308e6-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="308e6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="308e6-111">0x00000005</span><span class="sxs-lookup"><span data-stu-id="308e6-111">0x00000005</span></span>  <br/> |
|<span data-ttu-id="308e6-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="308e6-112">Data type:</span></span>  <br/> |<span data-ttu-id="308e6-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="308e6-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="308e6-114">領域:</span><span class="sxs-lookup"><span data-stu-id="308e6-114">Area:</span></span>  <br/> |<span data-ttu-id="308e6-115">会議</span><span class="sxs-lookup"><span data-stu-id="308e6-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="308e6-116">注釈</span><span class="sxs-lookup"><span data-stu-id="308e6-116">Remarks</span></span>

<span data-ttu-id="308e6-117">TRUE の値は、オブジェクトが一連の定期的なまたは例外 (孤立したインスタンスを含む) のいずれかを表すことを示します。</span><span class="sxs-lookup"><span data-stu-id="308e6-117">A value of TRUE indicates that the object represents either a recurring series or an exception (including an orphan instance).</span></span> <span data-ttu-id="308e6-118">値 FALSE、または、このプロパティがない場合は、オブジェクトが 1 つのインスタンスを表すことを示します。</span><span class="sxs-lookup"><span data-stu-id="308e6-118">A value of FALSE, or the absence of this property, indicates that the object represents a single instance.</span></span> <span data-ttu-id="308e6-119">このプロパティは、 **PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md)) のプロパティの違いに注意してください。</span><span class="sxs-lookup"><span data-stu-id="308e6-119">Note the difference between this property and the **PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="308e6-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="308e6-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="308e6-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="308e6-121">Protocol specifications</span></span>

<span data-ttu-id="308e6-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="308e6-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="308e6-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="308e6-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="308e6-124">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="308e6-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="308e6-125">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="308e6-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="308e6-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="308e6-126">Header files</span></span>

<span data-ttu-id="308e6-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="308e6-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="308e6-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="308e6-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="308e6-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="308e6-129">See also</span></span>



[<span data-ttu-id="308e6-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="308e6-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="308e6-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="308e6-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="308e6-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="308e6-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="308e6-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="308e6-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

