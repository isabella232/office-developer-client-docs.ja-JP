---
title: PidTagSentMailEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentMailEntryId
api_type:
- COM
ms.assetid: 8f14dc15-d7d7-4894-b6a8-0d589f576c42
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b53275d3bf26aa8bee3aeaef2148f5ead961e471
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591654"
---
# <a name="pidtagsentmailentryid-canonical-property"></a><span data-ttu-id="f6fb4-103">PidTagSentMailEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f6fb4-103">PidTagSentMailEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="f6fb4-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6fb4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6fb4-105">送信後のメッセージの移動先フォルダーのエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f6fb4-105">Contains the entry identifier of the folder where the message should be moved after submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f6fb4-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f6fb4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f6fb4-107">PR_SENTMAIL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="f6fb4-107">PR_SENTMAIL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="f6fb4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f6fb4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f6fb4-109">0x0E0A</span><span class="sxs-lookup"><span data-stu-id="f6fb4-109">0x0E0A</span></span>  <br/> |
|<span data-ttu-id="f6fb4-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f6fb4-110">Data type:</span></span>  <br/> |<span data-ttu-id="f6fb4-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f6fb4-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f6fb4-112">領域:</span><span class="sxs-lookup"><span data-stu-id="f6fb4-112">Area:</span></span>  <br/> |<span data-ttu-id="f6fb4-113">MAPI 以外から送信できます。</span><span class="sxs-lookup"><span data-stu-id="f6fb4-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f6fb4-114">注釈</span><span class="sxs-lookup"><span data-stu-id="f6fb4-114">Remarks</span></span>

<span data-ttu-id="f6fb4-115">多くの場合、このプロパティは、 **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) は、クライアント アプリケーションの標準の [送信済みアイテム フォルダーからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="f6fb4-115">This property is often copied from the **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) property, the client application's standard Sent Items folder.</span></span>
  
<span data-ttu-id="f6fb4-116">クライアント アプリケーションでは、 **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) プロパティを使用してこのプロパティを使用して、送信された後にメッセージの処理を制御します。</span><span class="sxs-lookup"><span data-stu-id="f6fb4-116">The client application uses this property with the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property to control what happens to a message after it is submitted.</span></span> <span data-ttu-id="f6fb4-117">セットは 1 つまたは他の必要があります。</span><span class="sxs-lookup"><span data-stu-id="f6fb4-117">Either one or the other should be set, but not both.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f6fb4-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f6fb4-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f6fb4-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f6fb4-119">Protocol specifications</span></span>

<span data-ttu-id="f6fb4-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f6fb4-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f6fb4-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="f6fb4-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f6fb4-122">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f6fb4-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f6fb4-123">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="f6fb4-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="f6fb4-124">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f6fb4-124">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f6fb4-125">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="f6fb4-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f6fb4-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f6fb4-126">Header files</span></span>

<span data-ttu-id="f6fb4-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f6fb4-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="f6fb4-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f6fb4-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="f6fb4-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f6fb4-129">Mapitags.h</span></span>
  
> <span data-ttu-id="f6fb4-130">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f6fb4-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f6fb4-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="f6fb4-131">See also</span></span>



[<span data-ttu-id="f6fb4-132">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f6fb4-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f6fb4-133">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f6fb4-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f6fb4-134">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f6fb4-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f6fb4-135">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f6fb4-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

