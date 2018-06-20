---
title: PidLidIsRecurring の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidIsRecurring
api_type:
- COM
ms.assetid: 1f8ecc22-badc-4278-a3c6-fcd398f5bf24
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c21f2885f7e9475c2149e42e2a8d947311916b4f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802025"
---
# <a name="pidlidisrecurring-canonical-property"></a><span data-ttu-id="26d0d-103">PidLidIsRecurring の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="26d0d-103">PidLidIsRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="26d0d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="26d0d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="26d0d-105">オブジェクトが定期的に関連付けられているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="26d0d-105">Specifies whether or not the object is associated with a recurring series.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="26d0d-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="26d0d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="26d0d-107">LID_IS_RECURRING</span><span class="sxs-lookup"><span data-stu-id="26d0d-107">LID_IS_RECURRING</span></span>  <br/> |
|<span data-ttu-id="26d0d-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="26d0d-108">Property set:</span></span>  <br/> |<span data-ttu-id="26d0d-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="26d0d-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="26d0d-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="26d0d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="26d0d-111">0x00000005</span><span class="sxs-lookup"><span data-stu-id="26d0d-111">0x00000005</span></span>  <br/> |
|<span data-ttu-id="26d0d-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="26d0d-112">Data type:</span></span>  <br/> |<span data-ttu-id="26d0d-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="26d0d-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="26d0d-114">領域:</span><span class="sxs-lookup"><span data-stu-id="26d0d-114">Area:</span></span>  <br/> |<span data-ttu-id="26d0d-115">会議</span><span class="sxs-lookup"><span data-stu-id="26d0d-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26d0d-116">備考</span><span class="sxs-lookup"><span data-stu-id="26d0d-116">Remarks</span></span>

<span data-ttu-id="26d0d-117">TRUE の値は、オブジェクトが一連の定期的なまたは例外 (孤立したインスタンスを含む) のいずれかを表すことを示します。</span><span class="sxs-lookup"><span data-stu-id="26d0d-117">A value of TRUE indicates that the object represents either a recurring series or an exception (including an orphan instance).</span></span> <span data-ttu-id="26d0d-118">値 FALSE、または、このプロパティがない場合は、オブジェクトが 1 つのインスタンスを表すことを示します。</span><span class="sxs-lookup"><span data-stu-id="26d0d-118">A value of FALSE, or the absence of this property, indicates that the object represents a single instance.</span></span> <span data-ttu-id="26d0d-119">このプロパティは、 **PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md)) のプロパティの違いに注意してください。</span><span class="sxs-lookup"><span data-stu-id="26d0d-119">Note the difference between this property and the **PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="26d0d-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="26d0d-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="26d0d-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="26d0d-121">Protocol specifications</span></span>

<span data-ttu-id="26d0d-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="26d0d-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="26d0d-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="26d0d-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="26d0d-124">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="26d0d-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="26d0d-125">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="26d0d-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="26d0d-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="26d0d-126">Header files</span></span>

<span data-ttu-id="26d0d-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="26d0d-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="26d0d-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="26d0d-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="26d0d-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="26d0d-129">See also</span></span>



[<span data-ttu-id="26d0d-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="26d0d-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="26d0d-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="26d0d-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="26d0d-132">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="26d0d-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="26d0d-133">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="26d0d-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

