---
title: PidTagUrlComponentName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagUrlComponentName
api_type:
- COM
ms.assetid: a21906f9-5408-41ba-a89b-273ab60eeef3
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 26a9d432d98c546aefa8f511ba2c4c9bb26cfd80
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320427"
---
# <a name="pidtagurlcomponentname-canonical-property"></a><span data-ttu-id="102d3-103">PidTagUrlComponentName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="102d3-103">PidTagUrlComponentName Canonical Property</span></span>

  
  
<span data-ttu-id="102d3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="102d3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="102d3-105">メッセージの URL コンポーネント名。</span><span class="sxs-lookup"><span data-stu-id="102d3-105">The URL component name for a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="102d3-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="102d3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="102d3-107">PR_URL_COMP_NAME、PR_URL_COMP_NAME_A、PR_URL_COMP_NAME_W</span><span class="sxs-lookup"><span data-stu-id="102d3-107">PR_URL_COMP_NAME, PR_URL_COMP_NAME_A, PR_URL_COMP_NAME_W</span></span>  <br/> |
|<span data-ttu-id="102d3-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="102d3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="102d3-109">0x10F3</span><span class="sxs-lookup"><span data-stu-id="102d3-109">0x10F3</span></span>  <br/> |
|<span data-ttu-id="102d3-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="102d3-110">Data type:</span></span>  <br/> |<span data-ttu-id="102d3-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="102d3-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="102d3-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="102d3-112">Area:</span></span>  <br/> |<span data-ttu-id="102d3-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="102d3-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="102d3-114">注釈</span><span class="sxs-lookup"><span data-stu-id="102d3-114">Remarks</span></span>

<span data-ttu-id="102d3-115">これらのプロパティは、フォルダー内で一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="102d3-115">These properties should be unique within a folder.</span></span> <span data-ttu-id="102d3-116">メッセージの作成時に設定しない場合、メッセージ ストアは、メッセージ クラスに応じて、さまざまなメッセージ プロパティに基づいてこれらのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="102d3-116">If not set when the message is created, the message store should set these properties based on various message properties, depending on the message class.</span></span> <span data-ttu-id="102d3-117">たとえば **、IPM です。メモ** と **IPM。予定** メッセージには、このプロパティは、PR_SUBJECT **(** [PidTagSubject](pidtagsubject-canonical-property.md)) プロパティと IPM に基づいて **設定されている必要があります。連絡先** メッセージには **、dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) プロパティに基づいてこのプロパティが設定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="102d3-117">For example, the **IPM.Note** and **IPM.Appointment** messages should have this property set based on the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property and the **IPM.Contact** messages should have this property set based on the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) property.</span></span> <span data-ttu-id="102d3-118">他のほとんどのメッセージ クラスでは、このプロパティは、PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティに基づく必要があります。</span><span class="sxs-lookup"><span data-stu-id="102d3-118">For most other message classes, this property should be based on the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="102d3-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="102d3-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="102d3-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="102d3-120">Protocol specifications</span></span>

<span data-ttu-id="102d3-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="102d3-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="102d3-122">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="102d3-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="102d3-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="102d3-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="102d3-124">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="102d3-124">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="102d3-125">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="102d3-125">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="102d3-126">メッセージオブジェクトと添付ファイル オブジェクトを効率的なストリーム表現にエンコードおよびデコードします。</span><span class="sxs-lookup"><span data-stu-id="102d3-126">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="102d3-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="102d3-127">Header files</span></span>

<span data-ttu-id="102d3-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="102d3-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="102d3-129">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="102d3-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="102d3-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="102d3-130">Mapitags.h</span></span>
  
> <span data-ttu-id="102d3-131">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="102d3-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="102d3-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="102d3-132">See also</span></span>



[<span data-ttu-id="102d3-133">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="102d3-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="102d3-134">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="102d3-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="102d3-135">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="102d3-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="102d3-136">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="102d3-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

