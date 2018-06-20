---
title: PidLidForwardInstance の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidForwardInstance
api_type:
- COM
ms.assetid: 055bdcaf-5002-44a6-b2b6-87244b2bea93
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0c32a60c7655f4e468a03013cb3979bde228ea3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801985"
---
# <a name="pidlidforwardinstance-canonical-property"></a><span data-ttu-id="7037d-103">PidLidForwardInstance の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="7037d-103">PidLidForwardInstance Canonical Property</span></span>

  
  
<span data-ttu-id="7037d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7037d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7037d-105">転送された (開催者によって転送された) 場合でも、開催者から送信された招待状をしているのではなく、会議出席依頼が定期的な一連の例外を表すことを示します。</span><span class="sxs-lookup"><span data-stu-id="7037d-105">Indicates that the meeting request represents an exception to a recurring series, and it was forwarded (even when forwarded by the organizer) rather than being an invitation sent by the organizer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7037d-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="7037d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7037d-107">dispidFwrdInstance</span><span class="sxs-lookup"><span data-stu-id="7037d-107">dispidFwrdInstance</span></span>  <br/> |
|<span data-ttu-id="7037d-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="7037d-108">Property set:</span></span>  <br/> |<span data-ttu-id="7037d-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="7037d-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="7037d-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="7037d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7037d-111">0x0000820A</span><span class="sxs-lookup"><span data-stu-id="7037d-111">0x0000820A</span></span>  <br/> |
|<span data-ttu-id="7037d-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="7037d-112">Data type:</span></span>  <br/> |<span data-ttu-id="7037d-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="7037d-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="7037d-114">領域:</span><span class="sxs-lookup"><span data-stu-id="7037d-114">Area:</span></span>  <br/> |<span data-ttu-id="7037d-115">会議</span><span class="sxs-lookup"><span data-stu-id="7037d-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7037d-116">備考</span><span class="sxs-lookup"><span data-stu-id="7037d-116">Remarks</span></span>

<span data-ttu-id="7037d-117">このプロパティの値は、会議出席依頼が転送されたインスタンスではないことを示します。</span><span class="sxs-lookup"><span data-stu-id="7037d-117">A value of FALSE for this property indicates that the meeting request is not a forwarded instance.</span></span> <span data-ttu-id="7037d-118">このプロパティが必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="7037d-118">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7037d-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7037d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7037d-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7037d-120">Protocol specifications</span></span>

<span data-ttu-id="7037d-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7037d-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7037d-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="7037d-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7037d-123">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7037d-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7037d-124">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="7037d-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7037d-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7037d-125">Header files</span></span>

<span data-ttu-id="7037d-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7037d-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="7037d-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7037d-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7037d-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="7037d-128">See also</span></span>



[<span data-ttu-id="7037d-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7037d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7037d-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7037d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7037d-131">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="7037d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7037d-132">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="7037d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

