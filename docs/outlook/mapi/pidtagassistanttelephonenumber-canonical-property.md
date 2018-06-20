---
title: PidTagAssistantTelephoneNumber の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAssistantTelephoneNumber
api_type:
- HeaderDef
ms.assetid: edb0782c-6671-4e98-9028-a2f9ad547c1d
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1242415e0698acb210f3e9ef8bfa00fd944816d3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802461"
---
# <a name="pidtagassistanttelephonenumber-canonical-property"></a><span data-ttu-id="e9353-103">PidTagAssistantTelephoneNumber の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="e9353-103">PidTagAssistantTelephoneNumber Canonical Property</span></span>

  
  
<span data-ttu-id="e9353-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e9353-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e9353-105">受信者の管理アシスタントの電話番号が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e9353-105">Contains the telephone number of the recipient's administrative assistant.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e9353-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="e9353-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e9353-107">PR_ASSISTANT_TELEPHONE_NUMBER、PR_ASSISTANT_TELEPHONE_NUMBER_A、PR_ASSISTANT_TELEPHONE_NUMBER_W</span><span class="sxs-lookup"><span data-stu-id="e9353-107">PR_ASSISTANT_TELEPHONE_NUMBER, PR_ASSISTANT_TELEPHONE_NUMBER_A, PR_ASSISTANT_TELEPHONE_NUMBER_W</span></span>  <br/> |
|<span data-ttu-id="e9353-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e9353-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e9353-109">0x3A2E</span><span class="sxs-lookup"><span data-stu-id="e9353-109">0x3A2E</span></span>  <br/> |
|<span data-ttu-id="e9353-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="e9353-110">Data type:</span></span>  <br/> |<span data-ttu-id="e9353-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="e9353-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="e9353-112">領域:</span><span class="sxs-lookup"><span data-stu-id="e9353-112">Area:</span></span>  <br/> |<span data-ttu-id="e9353-113">Address</span><span class="sxs-lookup"><span data-stu-id="e9353-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9353-114">備考</span><span class="sxs-lookup"><span data-stu-id="e9353-114">Remarks</span></span>

<span data-ttu-id="e9353-115">これらのプロパティでは、識別を提供し、受信者の情報にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="e9353-115">These properties provide identification and access information for a recipient.</span></span> <span data-ttu-id="e9353-116">受信者とその構造によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="e9353-116">They are defined by the recipient and their organization.</span></span> 
  
<span data-ttu-id="e9353-117">電話番号が、 **PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md)) のプロパティで指定したアシスタントです。</span><span class="sxs-lookup"><span data-stu-id="e9353-117">The telephone number is for the assistant specified in the **PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md)) property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e9353-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e9353-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e9353-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e9353-119">Protocol specifications</span></span>

<span data-ttu-id="e9353-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9353-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9353-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e9353-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e9353-122">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9353-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9353-123">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e9353-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="e9353-124">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9353-124">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9353-125">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e9353-125">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e9353-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e9353-126">Header files</span></span>

<span data-ttu-id="e9353-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e9353-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="e9353-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e9353-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="e9353-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e9353-129">Mapitags.h</span></span>
  
> <span data-ttu-id="e9353-130">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e9353-130">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e9353-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="e9353-131">See also</span></span>



[<span data-ttu-id="e9353-132">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e9353-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e9353-133">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e9353-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e9353-134">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="e9353-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e9353-135">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="e9353-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

