---
title: PidLidAttendeeCriticalChange 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAttendeeCriticalChange
api_type:
- COM
ms.assetid: 2b46966d-c63d-4241-92d4-001d6a674e97
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e05cf37d7605942abc9a2073957264503b8d92db
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574070"
---
# <a name="pidlidattendeecriticalchange-canonical-property"></a><span data-ttu-id="b7afa-103">PidLidAttendeeCriticalChange 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b7afa-103">PidLidAttendeeCriticalChange Canonical Property</span></span>

  
  
<span data-ttu-id="b7afa-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7afa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7afa-105">会議に関連するオブジェクトが送信されたときの日時を指定します。</span><span class="sxs-lookup"><span data-stu-id="b7afa-105">Specifies the date and time when the meeting-related object was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b7afa-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b7afa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b7afa-107">LID_ATTENDEE_CRITICAL_CHANGE</span><span class="sxs-lookup"><span data-stu-id="b7afa-107">LID_ATTENDEE_CRITICAL_CHANGE</span></span>  <br/> |
|<span data-ttu-id="b7afa-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="b7afa-108">Property set:</span></span>  <br/> |<span data-ttu-id="b7afa-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="b7afa-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="b7afa-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="b7afa-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b7afa-111">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b7afa-111">0x00000001</span></span>  <br/> |
|<span data-ttu-id="b7afa-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b7afa-112">Data type:</span></span>  <br/> |<span data-ttu-id="b7afa-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="b7afa-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="b7afa-114">領域:</span><span class="sxs-lookup"><span data-stu-id="b7afa-114">Area:</span></span>  <br/> |<span data-ttu-id="b7afa-115">会議</span><span class="sxs-lookup"><span data-stu-id="b7afa-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7afa-116">注釈</span><span class="sxs-lookup"><span data-stu-id="b7afa-116">Remarks</span></span>

<span data-ttu-id="b7afa-117">値は、世界協定時刻 (UTC) で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7afa-117">The value must be specified in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b7afa-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b7afa-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b7afa-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b7afa-119">Protocol specifications</span></span>

<span data-ttu-id="b7afa-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7afa-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7afa-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="b7afa-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b7afa-122">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7afa-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7afa-123">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="b7afa-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b7afa-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b7afa-124">Header files</span></span>

<span data-ttu-id="b7afa-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b7afa-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="b7afa-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b7afa-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b7afa-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="b7afa-127">See also</span></span>



[<span data-ttu-id="b7afa-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b7afa-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b7afa-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b7afa-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b7afa-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b7afa-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b7afa-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b7afa-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

