---
title: PidLidFInvited 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFInvited
api_type:
- COM
ms.assetid: ca1ea5ec-20d5-4b70-95de-c2246a10beae
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: efedeb54decf1feae7b31f8af299a154606d7afc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582904"
---
# <a name="pidlidfinvited-canonical-property"></a><span data-ttu-id="8e173-103">PidLidFInvited 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8e173-103">PidLidFInvited Canonical Property</span></span>

  
  
<span data-ttu-id="8e173-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e173-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e173-105">この会議を表す、ミーティングの招待状が送信されたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8e173-105">Indicates whether or not invitations have been sent for the meeting that this meeting represents.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8e173-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8e173-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8e173-107">dispidFInvited</span><span class="sxs-lookup"><span data-stu-id="8e173-107">dispidFInvited</span></span>  <br/> |
|<span data-ttu-id="8e173-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="8e173-108">Property set:</span></span>  <br/> |<span data-ttu-id="8e173-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="8e173-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="8e173-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="8e173-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8e173-111">0x00008229</span><span class="sxs-lookup"><span data-stu-id="8e173-111">0x00008229</span></span>  <br/> |
|<span data-ttu-id="8e173-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8e173-112">Data type:</span></span>  <br/> |<span data-ttu-id="8e173-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="8e173-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="8e173-114">領域:</span><span class="sxs-lookup"><span data-stu-id="8e173-114">Area:</span></span>  <br/> |<span data-ttu-id="8e173-115">会議</span><span class="sxs-lookup"><span data-stu-id="8e173-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e173-116">注釈</span><span class="sxs-lookup"><span data-stu-id="8e173-116">Remarks</span></span>

<span data-ttu-id="8e173-117">値 FALSE、または、このプロパティがない場合は、会議出席依頼が送信されたしないことを示します。</span><span class="sxs-lookup"><span data-stu-id="8e173-117">A value of FALSE, or the absence of this property, indicates that a meeting request has never been sent.</span></span> <span data-ttu-id="8e173-118">TRUE の値は、会議出席依頼が送信されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="8e173-118">A value of TRUE indicates that a meeting request has been sent.</span></span> <span data-ttu-id="8e173-119">会議で TRUE に設定する値を設定すると、その必要がありますままになります。</span><span class="sxs-lookup"><span data-stu-id="8e173-119">Once this value is set to TRUE on a meeting, it must not be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8e173-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8e173-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8e173-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8e173-121">Protocol specifications</span></span>

<span data-ttu-id="8e173-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e173-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e173-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="8e173-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8e173-124">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e173-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e173-125">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="8e173-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8e173-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8e173-126">Header files</span></span>

<span data-ttu-id="8e173-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8e173-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="8e173-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8e173-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8e173-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="8e173-129">See also</span></span>



[<span data-ttu-id="8e173-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8e173-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8e173-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8e173-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8e173-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8e173-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8e173-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8e173-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

