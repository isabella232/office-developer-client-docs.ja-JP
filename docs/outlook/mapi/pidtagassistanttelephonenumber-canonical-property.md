---
title: PidTagAssistantTelephoneNumber 標準プロパティ
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6eafe51490b231b9cc64242595aef54bcc85c3ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360418"
---
# <a name="pidtagassistanttelephonenumber-canonical-property"></a><span data-ttu-id="e0dbf-103">PidTagAssistantTelephoneNumber 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e0dbf-103">PidTagAssistantTelephoneNumber Canonical Property</span></span>

  
  
<span data-ttu-id="e0dbf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0dbf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0dbf-105">受信者の管理アシスタントの電話番号を格納します。</span><span class="sxs-lookup"><span data-stu-id="e0dbf-105">Contains the telephone number of the recipient's administrative assistant.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e0dbf-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e0dbf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e0dbf-107">PR_ASSISTANT_TELEPHONE_NUMBER、PR_ASSISTANT_TELEPHONE_NUMBER_A、PR_ASSISTANT_TELEPHONE_NUMBER_W</span><span class="sxs-lookup"><span data-stu-id="e0dbf-107">PR_ASSISTANT_TELEPHONE_NUMBER, PR_ASSISTANT_TELEPHONE_NUMBER_A, PR_ASSISTANT_TELEPHONE_NUMBER_W</span></span>  <br/> |
|<span data-ttu-id="e0dbf-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e0dbf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e0dbf-109">0x3A2E</span><span class="sxs-lookup"><span data-stu-id="e0dbf-109">0x3A2E</span></span>  <br/> |
|<span data-ttu-id="e0dbf-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e0dbf-110">Data type:</span></span>  <br/> |<span data-ttu-id="e0dbf-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="e0dbf-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="e0dbf-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="e0dbf-112">Area:</span></span>  <br/> |<span data-ttu-id="e0dbf-113">Address</span><span class="sxs-lookup"><span data-stu-id="e0dbf-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0dbf-114">注釈</span><span class="sxs-lookup"><span data-stu-id="e0dbf-114">Remarks</span></span>

<span data-ttu-id="e0dbf-115">これらのプロパティは、受信者の ID とアクセス情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="e0dbf-115">These properties provide identification and access information for a recipient.</span></span> <span data-ttu-id="e0dbf-116">受信者とその組織によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="e0dbf-116">They are defined by the recipient and their organization.</span></span> 
  
<span data-ttu-id="e0dbf-117">電話番号は、ユーザー ([PidTagAssistant](pidtagassistant-canonical-property.md)) プロパティで **PR_ASSISTANT** アシスタント用です。</span><span class="sxs-lookup"><span data-stu-id="e0dbf-117">The telephone number is for the assistant specified in the **PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md)) property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e0dbf-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e0dbf-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e0dbf-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e0dbf-119">Protocol specifications</span></span>

<span data-ttu-id="e0dbf-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0dbf-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0dbf-121">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="e0dbf-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e0dbf-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0dbf-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0dbf-123">連絡先と個人用配布リストで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e0dbf-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="e0dbf-124">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0dbf-124">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0dbf-125">ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e0dbf-125">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e0dbf-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e0dbf-126">Header files</span></span>

<span data-ttu-id="e0dbf-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e0dbf-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="e0dbf-128">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e0dbf-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="e0dbf-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e0dbf-129">Mapitags.h</span></span>
  
> <span data-ttu-id="e0dbf-130">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="e0dbf-130">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e0dbf-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="e0dbf-131">See also</span></span>



[<span data-ttu-id="e0dbf-132">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e0dbf-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e0dbf-133">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e0dbf-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e0dbf-134">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="e0dbf-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e0dbf-135">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="e0dbf-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

