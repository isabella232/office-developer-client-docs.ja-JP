---
title: PidLidAutoFillLocation 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAutoFillLocation
api_type:
- COM
ms.assetid: e4db6cae-4730-45d0-8b8a-9bd484c8bd3f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2d1edf371486c5db0aa8b869726c8a9a7b62ab06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344997"
---
# <a name="pidlidautofilllocation-canonical-property"></a><span data-ttu-id="e9aad-103">PidLidAutoFillLocation 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e9aad-103">PidLidAutoFillLocation Canonical Property</span></span>

  
  
<span data-ttu-id="e9aad-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9aad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9aad-105">**dispidlocation** ([PidLidLocation](pidlidlocation-canonical-property.md)) プロパティの値が、リソースを表す受信者行の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティに設定されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="e9aad-105">Indicates that the value of the **dispidLocation** ([PidLidLocation](pidlidlocation-canonical-property.md)) property is set to the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property from the RecipientRow that represents a resource.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e9aad-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e9aad-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e9aad-107">dispidautofilllocation</span><span class="sxs-lookup"><span data-stu-id="e9aad-107">dispidAutoFillLocation</span></span>  <br/> |
|<span data-ttu-id="e9aad-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="e9aad-108">Property set:</span></span>  <br/> |<span data-ttu-id="e9aad-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="e9aad-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="e9aad-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="e9aad-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e9aad-111">0x0000823a</span><span class="sxs-lookup"><span data-stu-id="e9aad-111">0x0000823A</span></span>  <br/> |
|<span data-ttu-id="e9aad-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e9aad-112">Data type:</span></span>  <br/> |<span data-ttu-id="e9aad-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e9aad-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e9aad-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="e9aad-114">Area:</span></span>  <br/> |<span data-ttu-id="e9aad-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="e9aad-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9aad-116">解説</span><span class="sxs-lookup"><span data-stu-id="e9aad-116">Remarks</span></span>

<span data-ttu-id="e9aad-117">[[受信者]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)行の詳細については、「OXCMSG」で指定されているように、Message および Attachment オブジェクトのプロトコルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e9aad-117">For more details on RecipientRow, see the Message and Attachment Object protocol as specified in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e9aad-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e9aad-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e9aad-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e9aad-119">Protocol specifications</span></span>

<span data-ttu-id="e9aad-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9aad-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9aad-121">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e9aad-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e9aad-122">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9aad-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9aad-123">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e9aad-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e9aad-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="e9aad-124">Header files</span></span>

<span data-ttu-id="e9aad-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e9aad-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="e9aad-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e9aad-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e9aad-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="e9aad-127">See also</span></span>



[<span data-ttu-id="e9aad-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e9aad-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e9aad-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e9aad-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e9aad-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e9aad-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e9aad-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e9aad-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

