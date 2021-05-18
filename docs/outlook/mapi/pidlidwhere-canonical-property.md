---
title: PidLidWhere 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidWhere
api_type:
- COM
ms.assetid: b21a3aa4-7536-4728-b4a4-273cfb25c57e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 19c3ed57d2a0bdd6902a93ca5f29deb91418b8ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360432"
---
# <a name="pidlidwhere-canonical-property"></a><span data-ttu-id="6c657-103">PidLidWhere 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6c657-103">PidLidWhere Canonical Property</span></span>

  
  
<span data-ttu-id="6c657-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c657-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c657-105">イベントの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="6c657-105">Specifies the location of an event.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6c657-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="6c657-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6c657-107">LID_WHERE</span><span class="sxs-lookup"><span data-stu-id="6c657-107">LID_WHERE</span></span>  <br/> |
|<span data-ttu-id="6c657-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="6c657-108">Property set:</span></span>  <br/> |<span data-ttu-id="6c657-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="6c657-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="6c657-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="6c657-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6c657-111">0x00000002</span><span class="sxs-lookup"><span data-stu-id="6c657-111">0x00000002</span></span>  <br/> |
|<span data-ttu-id="6c657-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="6c657-112">Data type:</span></span>  <br/> |<span data-ttu-id="6c657-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6c657-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6c657-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="6c657-114">Area:</span></span>  <br/> |<span data-ttu-id="6c657-115">会議</span><span class="sxs-lookup"><span data-stu-id="6c657-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c657-116">注釈</span><span class="sxs-lookup"><span data-stu-id="6c657-116">Remarks</span></span>

<span data-ttu-id="6c657-117">このプロパティの値は、関連する会議の **dispidLocation** ([PidLidLocation](pidlidlocation-canonical-property.md)) プロパティの値と同じにしてください。</span><span class="sxs-lookup"><span data-stu-id="6c657-117">The value of this property should be the same as the value of the **dispidLocation** ([PidLidLocation](pidlidlocation-canonical-property.md)) property from the associated meeting.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6c657-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6c657-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6c657-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6c657-119">Protocol specifications</span></span>

<span data-ttu-id="6c657-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c657-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c657-121">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="6c657-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6c657-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c657-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c657-123">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6c657-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6c657-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6c657-124">Header files</span></span>

<span data-ttu-id="6c657-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6c657-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="6c657-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6c657-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6c657-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="6c657-127">See also</span></span>



[<span data-ttu-id="6c657-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="6c657-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6c657-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6c657-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6c657-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="6c657-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6c657-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="6c657-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

