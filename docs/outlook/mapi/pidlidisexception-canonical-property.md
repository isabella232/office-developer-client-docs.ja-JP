---
title: PidLidIsException 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidIsException
api_type:
- COM
ms.assetid: 802321fb-4261-4c3e-9de3-8b4f490dae13
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 18dfa8a5936902afe0272274f7a48d01b28f94f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315450"
---
# <a name="pidlidisexception-canonical-property"></a><span data-ttu-id="b7916-103">PidLidIsException 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b7916-103">PidLidIsException Canonical Property</span></span>

  
  
<span data-ttu-id="b7916-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7916-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7916-105">例外 (孤立インスタンスを含む) を表すオブジェクトを示します。</span><span class="sxs-lookup"><span data-stu-id="b7916-105">Indicates that the object that represents an exception (including an orphan instance).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b7916-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b7916-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b7916-107">LID_IS_EXCEPTION</span><span class="sxs-lookup"><span data-stu-id="b7916-107">LID_IS_EXCEPTION</span></span>  <br/> |
|<span data-ttu-id="b7916-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="b7916-108">Property set:</span></span>  <br/> |<span data-ttu-id="b7916-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="b7916-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="b7916-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="b7916-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b7916-111">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="b7916-111">0x0000000A</span></span>  <br/> |
|<span data-ttu-id="b7916-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b7916-112">Data type:</span></span>  <br/> |<span data-ttu-id="b7916-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b7916-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="b7916-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="b7916-114">Area:</span></span>  <br/> |<span data-ttu-id="b7916-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="b7916-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7916-116">解説</span><span class="sxs-lookup"><span data-stu-id="b7916-116">Remarks</span></span>

<span data-ttu-id="b7916-117">値が FALSE の場合、定期的なアイテムまたは単一のインスタンスを表すオブジェクトを示します。</span><span class="sxs-lookup"><span data-stu-id="b7916-117">A value of FALSE indicates that the object that represents a recurring series or a single instance.</span></span> <span data-ttu-id="b7916-118">任意のオブジェクトに対してこのプロパティが存在しない場合は、TRUE の値を持つ例外埋め込みメッセージを除き、FALSE の値が指定されています。</span><span class="sxs-lookup"><span data-stu-id="b7916-118">The absence of this property for any object indicates a value of FALSE except for the exception embedded message, which assumes a value of TRUE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b7916-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b7916-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b7916-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b7916-120">Protocol specifications</span></span>

<span data-ttu-id="b7916-121">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7916-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7916-122">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="b7916-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b7916-123">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7916-123">[[MS-OXOCAL] ](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7916-124">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="b7916-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b7916-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="b7916-125">Header files</span></span>

<span data-ttu-id="b7916-126">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b7916-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="b7916-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b7916-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b7916-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="b7916-128">See also</span></span>



[<span data-ttu-id="b7916-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="b7916-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b7916-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b7916-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b7916-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b7916-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b7916-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b7916-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

