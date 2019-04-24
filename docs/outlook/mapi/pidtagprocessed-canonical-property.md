---
title: PidTagProcessed 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProcessed
api_type:
- COM
ms.assetid: 44884f60-7e36-45b2-9712-4f9821a0dc1f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 5d84e9cb693cbe732295ee1891b4219450eb09ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351437"
---
# <a name="pidtagprocessed-canonical-property"></a><span data-ttu-id="4e101-103">PidTagProcessed 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4e101-103">PidTagProcessed Canonical Property</span></span>

  
  
<span data-ttu-id="4e101-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e101-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e101-105">会議出席依頼が処理された場合は TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="4e101-105">Set to TRUE when the meeting request has been processed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4e101-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4e101-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4e101-107">PR_PROCESSED</span><span class="sxs-lookup"><span data-stu-id="4e101-107">PR_PROCESSED</span></span>  <br/> |
|<span data-ttu-id="4e101-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="4e101-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4e101-109">0x7d01</span><span class="sxs-lookup"><span data-stu-id="4e101-109">0x7D01</span></span>  <br/> |
|<span data-ttu-id="4e101-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4e101-110">Data type:</span></span>  <br/> |<span data-ttu-id="4e101-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="4e101-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="4e101-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="4e101-112">Area:</span></span>  <br/> |<span data-ttu-id="4e101-113">カレンダー</span><span class="sxs-lookup"><span data-stu-id="4e101-113">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e101-114">解説</span><span class="sxs-lookup"><span data-stu-id="4e101-114">Remarks</span></span>

<span data-ttu-id="4e101-115">このプロパティにより、会議出席依頼は1回だけ処理されます。</span><span class="sxs-lookup"><span data-stu-id="4e101-115">This property ensures that meeting requests get processed once.</span></span> <span data-ttu-id="4e101-116">要求の作成者は、このプロパティを FALSE に設定し、要求が予定表にあるときに、受信者がそれを TRUE に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e101-116">The creator of the request should set this property to FALSE and the receiver should set it to TRUE once the request is in the calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4e101-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4e101-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4e101-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4e101-118">Protocol specifications</span></span>

<span data-ttu-id="4e101-119">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4e101-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4e101-120">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="4e101-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4e101-121">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4e101-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4e101-122">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="4e101-122">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="4e101-123">[[OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4e101-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4e101-124">連絡先および個人用配布リストオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="4e101-124">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4e101-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="4e101-125">Header files</span></span>

<span data-ttu-id="4e101-126">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4e101-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="4e101-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4e101-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="4e101-128">Mapitags</span><span class="sxs-lookup"><span data-stu-id="4e101-128">Mapitags.h</span></span>
  
> <span data-ttu-id="4e101-129">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="4e101-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4e101-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="4e101-130">See also</span></span>



[<span data-ttu-id="4e101-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="4e101-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4e101-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4e101-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4e101-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4e101-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4e101-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4e101-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

