---
title: PidTagDeleteAfterSubmit の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeleteAfterSubmit
api_type:
- HeaderDef
ms.assetid: ba69a557-120c-4b1e-bbb7-0e901e7d1ebf
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 7a63b3ad3c45790e043e1ea8e7d996c4847ef8d4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802664"
---
# <a name="pidtagdeleteaftersubmit-canonical-property"></a><span data-ttu-id="23eb8-103">PidTagDeleteAfterSubmit の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="23eb8-103">PidTagDeleteAfterSubmit Canonical Property</span></span>

  
  
<span data-ttu-id="23eb8-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="23eb8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="23eb8-105">クライアント アプリケーションが送信した後、関連付けられているメッセージを削除するのには MAPI を希望する場合は TRUE が含まれています。</span><span class="sxs-lookup"><span data-stu-id="23eb8-105">Contains TRUE if a client application wants MAPI to delete the associated message after submission.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="23eb8-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="23eb8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="23eb8-107">PR_DELETE_AFTER_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="23eb8-107">PR_DELETE_AFTER_SUBMIT</span></span>  <br/> |
|<span data-ttu-id="23eb8-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="23eb8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="23eb8-109">0x0E01</span><span class="sxs-lookup"><span data-stu-id="23eb8-109">0x0E01</span></span>  <br/> |
|<span data-ttu-id="23eb8-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="23eb8-110">Data type:</span></span>  <br/> |<span data-ttu-id="23eb8-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="23eb8-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="23eb8-112">領域:</span><span class="sxs-lookup"><span data-stu-id="23eb8-112">Area:</span></span>  <br/> |<span data-ttu-id="23eb8-113">MAPI 以外から送信できます。</span><span class="sxs-lookup"><span data-stu-id="23eb8-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23eb8-114">備考</span><span class="sxs-lookup"><span data-stu-id="23eb8-114">Remarks</span></span>

<span data-ttu-id="23eb8-115">クライアント アプリケーションでは、 **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) プロパティを使用してこのプロパティを使用して、送信された後にメッセージの処理を制御します。</span><span class="sxs-lookup"><span data-stu-id="23eb8-115">A client application uses this property with the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property to control what happens to a message after it is submitted.</span></span> <span data-ttu-id="23eb8-116">セットは 1 つまたは他の必要があります。</span><span class="sxs-lookup"><span data-stu-id="23eb8-116">Either one or the other should be set, but not both.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="23eb8-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="23eb8-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="23eb8-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="23eb8-118">Protocol specifications</span></span>

<span data-ttu-id="23eb8-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23eb8-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23eb8-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="23eb8-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="23eb8-121">[[MS OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23eb8-121">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23eb8-122">コア メッセージのストア オブジェクトの許可された操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="23eb8-122">Specifies permissible operations for the core message store objects.</span></span>
    
<span data-ttu-id="23eb8-123">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23eb8-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23eb8-124">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="23eb8-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="23eb8-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="23eb8-125">Header files</span></span>

<span data-ttu-id="23eb8-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="23eb8-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="23eb8-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="23eb8-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="23eb8-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="23eb8-128">Mapitags.h</span></span>
  
> <span data-ttu-id="23eb8-129">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="23eb8-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="23eb8-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="23eb8-130">See also</span></span>



[<span data-ttu-id="23eb8-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="23eb8-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="23eb8-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="23eb8-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="23eb8-133">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="23eb8-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="23eb8-134">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="23eb8-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

