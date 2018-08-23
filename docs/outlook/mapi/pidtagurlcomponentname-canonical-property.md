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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3a2b0939bbfa5143e4bd99e74b0f84e3ca7efb12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803659"
---
# <a name="pidtagurlcomponentname-canonical-property"></a><span data-ttu-id="84ed4-103">PidTagUrlComponentName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="84ed4-103">PidTagUrlComponentName Canonical Property</span></span>

  
  
<span data-ttu-id="84ed4-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="84ed4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="84ed4-105">メッセージの URL コンポーネントの名前です。</span><span class="sxs-lookup"><span data-stu-id="84ed4-105">The URL component name for a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="84ed4-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="84ed4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="84ed4-107">PR_URL_COMP_NAME、PR_URL_COMP_NAME_A、PR_URL_COMP_NAME_W</span><span class="sxs-lookup"><span data-stu-id="84ed4-107">PR_URL_COMP_NAME, PR_URL_COMP_NAME_A, PR_URL_COMP_NAME_W</span></span>  <br/> |
|<span data-ttu-id="84ed4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="84ed4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="84ed4-109">0x10F3</span><span class="sxs-lookup"><span data-stu-id="84ed4-109">0x10F3</span></span>  <br/> |
|<span data-ttu-id="84ed4-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="84ed4-110">Data type:</span></span>  <br/> |<span data-ttu-id="84ed4-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="84ed4-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="84ed4-112">領域:</span><span class="sxs-lookup"><span data-stu-id="84ed4-112">Area:</span></span>  <br/> |<span data-ttu-id="84ed4-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="84ed4-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84ed4-114">注釈</span><span class="sxs-lookup"><span data-stu-id="84ed4-114">Remarks</span></span>

<span data-ttu-id="84ed4-115">これらのプロパティは、フォルダー内で一意でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="84ed4-115">These properties should be unique within a folder.</span></span> <span data-ttu-id="84ed4-116">表示しない場合は、一連のメッセージが作成されると、メッセージ ・ ストアはメッセージ クラスによって、メッセージのさまざまなプロパティに基づいて、これらのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="84ed4-116">If not set when the message is created, the message store should set these properties based on various message properties, depending on the message class.</span></span> <span data-ttu-id="84ed4-117">たとえば、IPM の**です。注**と**IPM。予定**メッセージにこのプロパティの設定が**あるの PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) のプロパティは、**の IPM に基づく必要があります。連絡先**メッセージは、このプロパティを**dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) のプロパティに基づいて設定を持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="84ed4-117">For example, the **IPM.Note** and **IPM.Appointment** messages should have this property set based on the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property and the **IPM.Contact** messages should have this property set based on the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) property.</span></span> <span data-ttu-id="84ed4-118">他のほとんどのメッセージ クラスでは、このプロパティに基づいて必要がある**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="84ed4-118">For most other message classes, this property should be based on the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="84ed4-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="84ed4-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="84ed4-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="84ed4-120">Protocol specifications</span></span>

<span data-ttu-id="84ed4-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84ed4-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84ed4-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="84ed4-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="84ed4-123">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84ed4-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84ed4-124">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="84ed4-124">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="84ed4-125">[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84ed4-125">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84ed4-126">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="84ed4-126">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="84ed4-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="84ed4-127">Header files</span></span>

<span data-ttu-id="84ed4-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="84ed4-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="84ed4-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="84ed4-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="84ed4-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="84ed4-130">Mapitags.h</span></span>
  
> <span data-ttu-id="84ed4-131">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="84ed4-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="84ed4-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="84ed4-132">See also</span></span>



[<span data-ttu-id="84ed4-133">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="84ed4-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="84ed4-134">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="84ed4-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="84ed4-135">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="84ed4-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="84ed4-136">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="84ed4-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

