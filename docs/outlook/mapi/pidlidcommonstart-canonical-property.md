---
title: PidLidCommonStart 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCommonStart
api_type:
- COM
ms.assetid: d999852d-ce98-4c3c-a772-87f5db4aa04e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e2d3dee4d268a1747d6b77acf62f24c6ec459bdc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801846"
---
# <a name="pidlidcommonstart-canonical-property"></a><span data-ttu-id="e7ac4-103">PidLidCommonStart 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e7ac4-103">PidLidCommonStart Canonical Property</span></span>

  
  
<span data-ttu-id="e7ac4-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e7ac4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e7ac4-105">メッセージの開始日時を表します。</span><span class="sxs-lookup"><span data-stu-id="e7ac4-105">Represents the start date and time of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e7ac4-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e7ac4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e7ac4-107">dispidCommonStart</span><span class="sxs-lookup"><span data-stu-id="e7ac4-107">dispidCommonStart</span></span>  <br/> |
|<span data-ttu-id="e7ac4-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="e7ac4-108">Property set:</span></span>  <br/> |<span data-ttu-id="e7ac4-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="e7ac4-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="e7ac4-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="e7ac4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e7ac4-111">0x00008516</span><span class="sxs-lookup"><span data-stu-id="e7ac4-111">0x00008516</span></span>  <br/> |
|<span data-ttu-id="e7ac4-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e7ac4-112">Data type:</span></span>  <br/> |<span data-ttu-id="e7ac4-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="e7ac4-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="e7ac4-114">領域:</span><span class="sxs-lookup"><span data-stu-id="e7ac4-114">Area:</span></span>  <br/> |<span data-ttu-id="e7ac4-115">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="e7ac4-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7ac4-116">注釈</span><span class="sxs-lookup"><span data-stu-id="e7ac4-116">Remarks</span></span>

<span data-ttu-id="e7ac4-117">このプロパティは、アイテムの開始時刻を示します。</span><span class="sxs-lookup"><span data-stu-id="e7ac4-117">This property indicates the start time for an item.</span></span> <span data-ttu-id="e7ac4-118">**DispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) プロパティの値に等しいかそれより小さい値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e7ac4-118">It must be less than or equal to the value of the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="e7ac4-119">このプロパティの値は、 **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) のプロパティの [世界協定時刻 (UTC) と同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="e7ac4-119">The value of this property must be the Coordinated Universal Time (UTC) equivalent of the **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e7ac4-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e7ac4-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e7ac4-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e7ac4-121">Protocol specifications</span></span>

<span data-ttu-id="e7ac4-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7ac4-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7ac4-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e7ac4-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e7ac4-124">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7ac4-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7ac4-125">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="e7ac4-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="e7ac4-126">[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7ac4-126">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7ac4-127">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e7ac4-127">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e7ac4-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e7ac4-128">Header files</span></span>

<span data-ttu-id="e7ac4-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e7ac4-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="e7ac4-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e7ac4-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e7ac4-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="e7ac4-131">See also</span></span>



[<span data-ttu-id="e7ac4-132">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e7ac4-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e7ac4-133">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e7ac4-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e7ac4-134">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e7ac4-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e7ac4-135">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e7ac4-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

