---
title: PidTagFreeBusyCountMonths 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyCountMonths
api_type:
- HeaderDef
ms.assetid: 278a77f2-65ec-4281-b406-942cc416a476
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 610e9d396442f981b7bcbf126e3086e6885399d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316192"
---
# <a name="pidtagfreebusycountmonths-canonical-property"></a><span data-ttu-id="d42cb-103">PidTagFreeBusyCountMonths 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d42cb-103">PidTagFreeBusyCountMonths Canonical Property</span></span>

  
  
<span data-ttu-id="d42cb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d42cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d42cb-105">パブリック フォルダーに発行する空き時間情報データの範囲の開始日と終了日を計算するための値を格納します。</span><span class="sxs-lookup"><span data-stu-id="d42cb-105">Contains the value for calculating the start and end dates of the range of free/busy data to be published to public folders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d42cb-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d42cb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d42cb-107">PR_FREEBUSY_COUNT_MONTHS</span><span class="sxs-lookup"><span data-stu-id="d42cb-107">PR_FREEBUSY_COUNT_MONTHS</span></span>  <br/> |
|<span data-ttu-id="d42cb-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d42cb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d42cb-109">0x6869</span><span class="sxs-lookup"><span data-stu-id="d42cb-109">0x6869</span></span>  <br/> |
|<span data-ttu-id="d42cb-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d42cb-110">Data type:</span></span>  <br/> |<span data-ttu-id="d42cb-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d42cb-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d42cb-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="d42cb-112">Area:</span></span>  <br/> |<span data-ttu-id="d42cb-113">メッセージ クラス定義の送信可能</span><span class="sxs-lookup"><span data-stu-id="d42cb-113">Message class-defined transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d42cb-114">注釈</span><span class="sxs-lookup"><span data-stu-id="d42cb-114">Remarks</span></span>

<span data-ttu-id="d42cb-115">このプロパティの値は、0 以上 36 以下である必要があります。</span><span class="sxs-lookup"><span data-stu-id="d42cb-115">This property's value must be greater than or equal to 0 and less than or equal to 36.</span></span> <span data-ttu-id="d42cb-116">これは必須のプロパティではありません。</span><span class="sxs-lookup"><span data-stu-id="d42cb-116">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d42cb-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d42cb-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d42cb-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d42cb-118">Protocol specifications</span></span>

<span data-ttu-id="d42cb-119">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d42cb-119">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d42cb-120">ユーザーまたはリソースの可用性を公開します。</span><span class="sxs-lookup"><span data-stu-id="d42cb-120">Publishes the availability of a user or resource.</span></span>
    
<span data-ttu-id="d42cb-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d42cb-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d42cb-122">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d42cb-122">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d42cb-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d42cb-123">Header files</span></span>

<span data-ttu-id="d42cb-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d42cb-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="d42cb-125">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d42cb-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="d42cb-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d42cb-126">Mapitags.h</span></span>
  
> <span data-ttu-id="d42cb-127">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="d42cb-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d42cb-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="d42cb-128">See also</span></span>



[<span data-ttu-id="d42cb-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="d42cb-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d42cb-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d42cb-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d42cb-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d42cb-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d42cb-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d42cb-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

