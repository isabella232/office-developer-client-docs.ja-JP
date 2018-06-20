---
title: PidLidRecurring の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRecurring
api_type:
- COM
ms.assetid: 3d39a053-277f-4d59-ab2e-cee81710f2ab
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 36bf204823711e87ac6250f0997445f2745fbc19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802107"
---
# <a name="pidlidrecurring-canonical-property"></a><span data-ttu-id="63e0a-103">PidLidRecurring の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="63e0a-103">PidLidRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="63e0a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="63e0a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="63e0a-105">予定のメッセージが繰り返しかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="63e0a-105">Specifies whether an appointment message is recurrent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="63e0a-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="63e0a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="63e0a-107">dispidRecurring</span><span class="sxs-lookup"><span data-stu-id="63e0a-107">dispidRecurring</span></span>  <br/> |
|<span data-ttu-id="63e0a-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="63e0a-108">Property set:</span></span>  <br/> |<span data-ttu-id="63e0a-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="63e0a-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="63e0a-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="63e0a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="63e0a-111">0x00008223</span><span class="sxs-lookup"><span data-stu-id="63e0a-111">0x00008223</span></span>  <br/> |
|<span data-ttu-id="63e0a-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="63e0a-112">Data type:</span></span>  <br/> |<span data-ttu-id="63e0a-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="63e0a-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="63e0a-114">領域:</span><span class="sxs-lookup"><span data-stu-id="63e0a-114">Area:</span></span>  <br/> |<span data-ttu-id="63e0a-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="63e0a-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="63e0a-116">備考</span><span class="sxs-lookup"><span data-stu-id="63e0a-116">Remarks</span></span>

<span data-ttu-id="63e0a-117">予定は定期的な予定の場合で、定期的なしない場合は、FALSE の場合、このプロパティは TRUE です。</span><span class="sxs-lookup"><span data-stu-id="63e0a-117">This property is TRUE if the appointment is a recurring appointment, and is FALSE if it is not recurring.</span></span>
  
<span data-ttu-id="63e0a-118">このプロパティは、オブジェクトが定期的な系列を表すかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="63e0a-118">This property specifies whether or not the object represents a recurring series.</span></span> <span data-ttu-id="63e0a-119">TRUE の値は、オブジェクトが一連の定期的なであることを示します。</span><span class="sxs-lookup"><span data-stu-id="63e0a-119">A value of TRUE indicates that the object represents a recurring series.</span></span> <span data-ttu-id="63e0a-120">値 FALSE、または、このプロパティがない場合は、オブジェクトが 1 つのインスタンスまたは (孤立したインスタンスを含む) の例外のいずれかを表すことを示します。</span><span class="sxs-lookup"><span data-stu-id="63e0a-120">A value of FALSE, or the absence of this property, indicates that the object represents either a single instance or an exception (including an orphan instance).</span></span> <span data-ttu-id="63e0a-121">このプロパティは、 **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) のプロパティの違いに注意してください。</span><span class="sxs-lookup"><span data-stu-id="63e0a-121">Note the difference between this property and the **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="63e0a-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="63e0a-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="63e0a-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="63e0a-123">Protocol specifications</span></span>

<span data-ttu-id="63e0a-124">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63e0a-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63e0a-125">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="63e0a-125">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="63e0a-126">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63e0a-126">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63e0a-127">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="63e0a-127">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="63e0a-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="63e0a-128">Header files</span></span>

<span data-ttu-id="63e0a-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="63e0a-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="63e0a-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="63e0a-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="63e0a-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="63e0a-131">See also</span></span>



[<span data-ttu-id="63e0a-132">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="63e0a-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="63e0a-133">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="63e0a-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="63e0a-134">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="63e0a-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="63e0a-135">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="63e0a-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

