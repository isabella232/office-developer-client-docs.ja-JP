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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a73f5522e7201f73720318374745776b0ff08353
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570598"
---
# <a name="pidlidwhere-canonical-property"></a><span data-ttu-id="0d385-103">PidLidWhere 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0d385-103">PidLidWhere Canonical Property</span></span>

  
  
<span data-ttu-id="0d385-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d385-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d385-105">イベントの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-105">Specifies the location of an event.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0d385-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="0d385-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0d385-107">LID_WHERE</span><span class="sxs-lookup"><span data-stu-id="0d385-107">LID_WHERE</span></span>  <br/> |
|<span data-ttu-id="0d385-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-108">Property set:</span></span>  <br/> |<span data-ttu-id="0d385-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="0d385-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="0d385-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="0d385-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0d385-111">0x00000002</span><span class="sxs-lookup"><span data-stu-id="0d385-111">0x00000002</span></span>  <br/> |
|<span data-ttu-id="0d385-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="0d385-112">Data type:</span></span>  <br/> |<span data-ttu-id="0d385-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0d385-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0d385-114">領域:</span><span class="sxs-lookup"><span data-stu-id="0d385-114">Area:</span></span>  <br/> |<span data-ttu-id="0d385-115">会議</span><span class="sxs-lookup"><span data-stu-id="0d385-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d385-116">注釈</span><span class="sxs-lookup"><span data-stu-id="0d385-116">Remarks</span></span>

<span data-ttu-id="0d385-117">このプロパティの値は、関連付けられている会議から**dispidLocation** ([PidLidLocation](pidlidlocation-canonical-property.md)) プロパティの値と同じはずです。</span><span class="sxs-lookup"><span data-stu-id="0d385-117">The value of this property should be the same as the value of the **dispidLocation** ([PidLidLocation](pidlidlocation-canonical-property.md)) property from the associated meeting.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0d385-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0d385-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0d385-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="0d385-119">Protocol specifications</span></span>

<span data-ttu-id="0d385-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0d385-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0d385-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="0d385-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0d385-122">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0d385-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0d385-123">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0d385-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="0d385-124">Header files</span></span>

<span data-ttu-id="0d385-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0d385-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="0d385-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0d385-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0d385-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="0d385-127">See also</span></span>



[<span data-ttu-id="0d385-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0d385-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0d385-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0d385-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0d385-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0d385-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0d385-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0d385-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

