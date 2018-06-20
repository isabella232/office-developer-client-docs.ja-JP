---
title: PidLidOwnerCriticalChange の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidOwnerCriticalChange
api_type:
- COM
ms.assetid: b79aa2b7-b6e0-46dc-89f1-f801a6b5737a
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 316bd4169e3e714e7d36a16cab417a1ee2068594
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802082"
---
# <a name="pidlidownercriticalchange-canonical-property"></a><span data-ttu-id="1ef1a-103">PidLidOwnerCriticalChange の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="1ef1a-103">PidLidOwnerCriticalChange Canonical Property</span></span>

  
  
<span data-ttu-id="1ef1a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1ef1a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1ef1a-105">日付と時刻を開催者が会議出席依頼が送信されたときを指定します。</span><span class="sxs-lookup"><span data-stu-id="1ef1a-105">Specifies the date and time when a meeting request was sent by the organizer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1ef1a-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="1ef1a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1ef1a-107">LID_OWNER_CRITICAL_CHANGE</span><span class="sxs-lookup"><span data-stu-id="1ef1a-107">LID_OWNER_CRITICAL_CHANGE</span></span>  <br/> |
|<span data-ttu-id="1ef1a-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="1ef1a-108">Property set:</span></span>  <br/> |<span data-ttu-id="1ef1a-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="1ef1a-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="1ef1a-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="1ef1a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1ef1a-111">0x0000001A</span><span class="sxs-lookup"><span data-stu-id="1ef1a-111">0x0000001A</span></span>  <br/> |
|<span data-ttu-id="1ef1a-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="1ef1a-112">Data type:</span></span>  <br/> |<span data-ttu-id="1ef1a-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="1ef1a-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="1ef1a-114">領域:</span><span class="sxs-lookup"><span data-stu-id="1ef1a-114">Area:</span></span>  <br/> |<span data-ttu-id="1ef1a-115">会議</span><span class="sxs-lookup"><span data-stu-id="1ef1a-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1ef1a-116">備考</span><span class="sxs-lookup"><span data-stu-id="1ef1a-116">Remarks</span></span>

<span data-ttu-id="1ef1a-117">値は、世界協定時刻 (UTC) で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1ef1a-117">The value must be specified in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1ef1a-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1ef1a-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1ef1a-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1ef1a-119">Protocol specifications</span></span>

<span data-ttu-id="1ef1a-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1ef1a-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1ef1a-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="1ef1a-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1ef1a-122">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1ef1a-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1ef1a-123">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="1ef1a-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1ef1a-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1ef1a-124">Header files</span></span>

<span data-ttu-id="1ef1a-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1ef1a-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="1ef1a-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1ef1a-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1ef1a-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="1ef1a-127">See also</span></span>



[<span data-ttu-id="1ef1a-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1ef1a-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1ef1a-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1ef1a-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1ef1a-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="1ef1a-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1ef1a-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="1ef1a-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

