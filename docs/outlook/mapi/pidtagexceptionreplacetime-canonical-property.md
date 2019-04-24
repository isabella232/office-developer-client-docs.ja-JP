---
title: PidTagExceptionReplaceTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExceptionReplaceTime
api_type:
- HeaderDef
ms.assetid: bd4d1311-15e4-4275-a967-c6d11d2e48d2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f255b91cbd428a2ceaa51140519b02d3f8a3b1ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316388"
---
# <a name="pidtagexceptionreplacetime-canonical-property"></a><span data-ttu-id="b839f-103">PidTagExceptionReplaceTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b839f-103">PidTagExceptionReplaceTime Canonical Property</span></span>

  
  
<span data-ttu-id="b839f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b839f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b839f-105">例外でない場合に定期的なパターンのインスタンスが発生したときの元の日付と時刻を示します。</span><span class="sxs-lookup"><span data-stu-id="b839f-105">Indicates the original date and time when the instance in the recurrence pattern would have occurred if it were not an exception.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b839f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b839f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b839f-107">PR_EXCEPTION_REPLACETIME</span><span class="sxs-lookup"><span data-stu-id="b839f-107">PR_EXCEPTION_REPLACETIME</span></span>  <br/> |
|<span data-ttu-id="b839f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b839f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b839f-109">0x7ff9</span><span class="sxs-lookup"><span data-stu-id="b839f-109">0x7FF9</span></span>  <br/> |
|<span data-ttu-id="b839f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b839f-110">Data type:</span></span>  <br/> |<span data-ttu-id="b839f-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="b839f-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="b839f-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="b839f-112">Area:</span></span>  <br/> |<span data-ttu-id="b839f-113">メッセージクラスで定義された、非表示テーブル</span><span class="sxs-lookup"><span data-stu-id="b839f-113">Message class-defined non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b839f-114">解説</span><span class="sxs-lookup"><span data-stu-id="b839f-114">Remarks</span></span>

<span data-ttu-id="b839f-115">この値は協定世界時 (UTC) で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b839f-115">This value must be specified in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b839f-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b839f-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b839f-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b839f-117">Protocol specifications</span></span>

<span data-ttu-id="b839f-118">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b839f-118">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b839f-119">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="b839f-119">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b839f-120">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="b839f-120">Header files</span></span>

<span data-ttu-id="b839f-121">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b839f-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="b839f-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b839f-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="b839f-123">Mapitags</span><span class="sxs-lookup"><span data-stu-id="b839f-123">Mapitags.h</span></span>
  
> <span data-ttu-id="b839f-124">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b839f-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b839f-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="b839f-125">See also</span></span>



[<span data-ttu-id="b839f-126">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="b839f-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b839f-127">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b839f-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b839f-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b839f-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b839f-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b839f-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

