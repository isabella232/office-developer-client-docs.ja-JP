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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395183"
---
# <a name="pidtagexceptionreplacetime-canonical-property"></a><span data-ttu-id="be73e-103">PidTagExceptionReplaceTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="be73e-103">PidTagExceptionReplaceTime Canonical Property</span></span>

  
  
<span data-ttu-id="be73e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be73e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be73e-105">元の日付と時間のパターン内のインスタンスがあるが発生した場合例外でされていない場合を示します。</span><span class="sxs-lookup"><span data-stu-id="be73e-105">Indicates the original date and time when the instance in the recurrence pattern would have occurred if it were not an exception.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="be73e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="be73e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="be73e-107">PR_EXCEPTION_REPLACETIME</span><span class="sxs-lookup"><span data-stu-id="be73e-107">PR_EXCEPTION_REPLACETIME</span></span>  <br/> |
|<span data-ttu-id="be73e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="be73e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="be73e-109">0x7FF9</span><span class="sxs-lookup"><span data-stu-id="be73e-109">0x7FF9</span></span>  <br/> |
|<span data-ttu-id="be73e-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="be73e-110">Data type:</span></span>  <br/> |<span data-ttu-id="be73e-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="be73e-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="be73e-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="be73e-112">Area:</span></span>  <br/> |<span data-ttu-id="be73e-113">クラスによって定義されたメッセージの転送を可能な</span><span class="sxs-lookup"><span data-stu-id="be73e-113">Message class-defined non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be73e-114">備考</span><span class="sxs-lookup"><span data-stu-id="be73e-114">Remarks</span></span>

<span data-ttu-id="be73e-115">この値は、世界協定時刻 (UTC) で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="be73e-115">This value must be specified in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="be73e-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="be73e-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="be73e-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="be73e-117">Protocol specifications</span></span>

<span data-ttu-id="be73e-118">[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="be73e-118">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="be73e-119">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="be73e-119">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="be73e-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="be73e-120">Header files</span></span>

<span data-ttu-id="be73e-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="be73e-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="be73e-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="be73e-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="be73e-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="be73e-123">Mapitags.h</span></span>
  
> <span data-ttu-id="be73e-124">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="be73e-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="be73e-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="be73e-125">See also</span></span>



[<span data-ttu-id="be73e-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="be73e-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="be73e-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="be73e-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="be73e-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="be73e-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="be73e-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="be73e-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

