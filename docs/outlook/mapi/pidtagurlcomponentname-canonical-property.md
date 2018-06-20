---
title: PidTagUrlComponentName の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3a2b0939bbfa5143e4bd99e74b0f84e3ca7efb12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803659"
---
# <a name="pidtagurlcomponentname-canonical-property"></a><span data-ttu-id="4c9c2-103">PidTagUrlComponentName の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="4c9c2-103">PidTagUrlComponentName Canonical Property</span></span>

  
  
<span data-ttu-id="4c9c2-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4c9c2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4c9c2-105">メッセージの URL コンポーネントの名前です。</span><span class="sxs-lookup"><span data-stu-id="4c9c2-105">The URL component name for a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4c9c2-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="4c9c2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4c9c2-107">PR_URL_COMP_NAME、PR_URL_COMP_NAME_A、PR_URL_COMP_NAME_W</span><span class="sxs-lookup"><span data-stu-id="4c9c2-107">PR_URL_COMP_NAME, PR_URL_COMP_NAME_A, PR_URL_COMP_NAME_W</span></span>  <br/> |
|<span data-ttu-id="4c9c2-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="4c9c2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4c9c2-109">0x10F3</span><span class="sxs-lookup"><span data-stu-id="4c9c2-109">0x10F3</span></span>  <br/> |
|<span data-ttu-id="4c9c2-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="4c9c2-110">Data type:</span></span>  <br/> |<span data-ttu-id="4c9c2-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4c9c2-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4c9c2-112">領域:</span><span class="sxs-lookup"><span data-stu-id="4c9c2-112">Area:</span></span>  <br/> |<span data-ttu-id="4c9c2-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="4c9c2-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c9c2-114">備考</span><span class="sxs-lookup"><span data-stu-id="4c9c2-114">Remarks</span></span>

<span data-ttu-id="4c9c2-115">これらのプロパティは、フォルダー内で一意でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="4c9c2-115">These properties should be unique within a folder.</span></span> <span data-ttu-id="4c9c2-116">表示しない場合は、一連のメッセージが作成されると、メッセージ ・ ストアはメッセージ クラスによって、メッセージのさまざまなプロパティに基づいて、これらのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c9c2-116">If not set when the message is created, the message store should set these properties based on various message properties, depending on the message class.</span></span> <span data-ttu-id="4c9c2-117">たとえば、IPM の**です。注**と**IPM。予定**メッセージにこのプロパティの設定が**あるの PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) のプロパティは、**の IPM に基づく必要があります。連絡先**メッセージは、このプロパティを**dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) のプロパティに基づいて設定を持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c9c2-117">For example, the **IPM.Note** and **IPM.Appointment** messages should have this property set based on the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property and the **IPM.Contact** messages should have this property set based on the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) property.</span></span> <span data-ttu-id="4c9c2-118">他のほとんどのメッセージ クラスでは、このプロパティに基づいて必要がある**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="4c9c2-118">For most other message classes, this property should be based on the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4c9c2-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4c9c2-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4c9c2-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4c9c2-120">Protocol specifications</span></span>

<span data-ttu-id="4c9c2-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c9c2-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c9c2-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="4c9c2-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4c9c2-123">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c9c2-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c9c2-124">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="4c9c2-124">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="4c9c2-125">[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c9c2-125">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c9c2-126">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="4c9c2-126">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4c9c2-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4c9c2-127">Header files</span></span>

<span data-ttu-id="4c9c2-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4c9c2-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="4c9c2-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4c9c2-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="4c9c2-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4c9c2-130">Mapitags.h</span></span>
  
> <span data-ttu-id="4c9c2-131">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4c9c2-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4c9c2-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="4c9c2-132">See also</span></span>



[<span data-ttu-id="4c9c2-133">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4c9c2-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4c9c2-134">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4c9c2-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4c9c2-135">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="4c9c2-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4c9c2-136">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="4c9c2-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

