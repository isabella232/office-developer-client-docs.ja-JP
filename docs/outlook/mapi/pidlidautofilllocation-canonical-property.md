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
ms.openlocfilehash: 31cabf50602f9e0f7a70118ddc794387990862ad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591269"
---
# <a name="pidlidautofilllocation-canonical-property"></a><span data-ttu-id="fca8f-103">PidLidAutoFillLocation 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fca8f-103">PidLidAutoFillLocation Canonical Property</span></span>

  
  
<span data-ttu-id="fca8f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fca8f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fca8f-105">リソースを表す RecipientRow から**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) のプロパティを**dispidLocation** ([PidLidLocation](pidlidlocation-canonical-property.md)) プロパティの値が設定されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="fca8f-105">Indicates that the value of the **dispidLocation** ([PidLidLocation](pidlidlocation-canonical-property.md)) property is set to the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property from the RecipientRow that represents a resource.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fca8f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="fca8f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fca8f-107">dispidAutoFillLocation</span><span class="sxs-lookup"><span data-stu-id="fca8f-107">dispidAutoFillLocation</span></span>  <br/> |
|<span data-ttu-id="fca8f-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="fca8f-108">Property set:</span></span>  <br/> |<span data-ttu-id="fca8f-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="fca8f-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="fca8f-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="fca8f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fca8f-111">0x0000823A</span><span class="sxs-lookup"><span data-stu-id="fca8f-111">0x0000823A</span></span>  <br/> |
|<span data-ttu-id="fca8f-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="fca8f-112">Data type:</span></span>  <br/> |<span data-ttu-id="fca8f-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="fca8f-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="fca8f-114">領域:</span><span class="sxs-lookup"><span data-stu-id="fca8f-114">Area:</span></span>  <br/> |<span data-ttu-id="fca8f-115">会議</span><span class="sxs-lookup"><span data-stu-id="fca8f-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fca8f-116">注釈</span><span class="sxs-lookup"><span data-stu-id="fca8f-116">Remarks</span></span>

<span data-ttu-id="fca8f-117">RecipientRow の詳細については、 [[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)で指定されているプロトコル メッセージと添付ファイルのオブジェクトを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fca8f-117">For more details on RecipientRow, see the Message and Attachment Object protocol as specified in [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fca8f-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="fca8f-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fca8f-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="fca8f-119">Protocol specifications</span></span>

<span data-ttu-id="fca8f-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fca8f-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fca8f-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="fca8f-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fca8f-122">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fca8f-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fca8f-123">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="fca8f-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fca8f-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="fca8f-124">Header files</span></span>

<span data-ttu-id="fca8f-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fca8f-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="fca8f-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="fca8f-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fca8f-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="fca8f-127">See also</span></span>



[<span data-ttu-id="fca8f-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="fca8f-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fca8f-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="fca8f-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fca8f-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="fca8f-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fca8f-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="fca8f-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

