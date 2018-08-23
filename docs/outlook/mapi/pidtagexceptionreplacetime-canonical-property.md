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
ms.openlocfilehash: 506c4e89bda617ef307a64c266416c0538090ab0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802723"
---
# <a name="pidtagexceptionreplacetime-canonical-property"></a><span data-ttu-id="770b4-103">PidTagExceptionReplaceTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="770b4-103">PidTagExceptionReplaceTime Canonical Property</span></span>

  
  
<span data-ttu-id="770b4-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="770b4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="770b4-105">元の日付と時間のパターン内のインスタンスがあるが発生した場合例外でされていない場合を示します。</span><span class="sxs-lookup"><span data-stu-id="770b4-105">Indicates the original date and time when the instance in the recurrence pattern would have occurred if it were not an exception.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="770b4-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="770b4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="770b4-107">PR_EXCEPTION_REPLACETIME</span><span class="sxs-lookup"><span data-stu-id="770b4-107">PR_EXCEPTION_REPLACETIME</span></span>  <br/> |
|<span data-ttu-id="770b4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="770b4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="770b4-109">0x7FF9</span><span class="sxs-lookup"><span data-stu-id="770b4-109">0x7FF9</span></span>  <br/> |
|<span data-ttu-id="770b4-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="770b4-110">Data type:</span></span>  <br/> |<span data-ttu-id="770b4-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="770b4-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="770b4-112">領域:</span><span class="sxs-lookup"><span data-stu-id="770b4-112">Area:</span></span>  <br/> |<span data-ttu-id="770b4-113">クラスによって定義されたメッセージの転送を可能な</span><span class="sxs-lookup"><span data-stu-id="770b4-113">Message class-defined non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="770b4-114">注釈</span><span class="sxs-lookup"><span data-stu-id="770b4-114">Remarks</span></span>

<span data-ttu-id="770b4-115">この値は、世界協定時刻 (UTC) で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="770b4-115">This value must be specified in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="770b4-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="770b4-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="770b4-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="770b4-117">Protocol specifications</span></span>

<span data-ttu-id="770b4-118">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="770b4-118">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="770b4-119">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="770b4-119">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="770b4-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="770b4-120">Header files</span></span>

<span data-ttu-id="770b4-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="770b4-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="770b4-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="770b4-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="770b4-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="770b4-123">Mapitags.h</span></span>
  
> <span data-ttu-id="770b4-124">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="770b4-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="770b4-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="770b4-125">See also</span></span>



[<span data-ttu-id="770b4-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="770b4-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="770b4-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="770b4-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="770b4-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="770b4-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="770b4-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="770b4-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

