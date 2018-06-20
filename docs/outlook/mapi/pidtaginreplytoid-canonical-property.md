---
title: PidTagInReplyToId の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInReplyToId
api_type:
- HeaderDef
ms.assetid: d435a65a-de01-4fb0-bc54-a87a2c4462ac
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 2e8ed4af81de6e48af3e427f2d2d2f94572d241f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802857"
---
# <a name="pidtaginreplytoid-canonical-property"></a><span data-ttu-id="a9d05-103">PidTagInReplyToId の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="a9d05-103">PidTagInReplyToId Canonical Property</span></span>

  
  
<span data-ttu-id="a9d05-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a9d05-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a9d05-105">**PR_INTERNET_MESSAGE_ID** ([PidTagInternetMessageId](pidtaginternetmessageid-canonical-property.md)) プロパティの値元のメッセージにはが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a9d05-105">Contains the original message's **PR_INTERNET_MESSAGE_ID** ([PidTagInternetMessageId](pidtaginternetmessageid-canonical-property.md)) property value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a9d05-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="a9d05-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a9d05-107">PR_IN_REPLY_TO_ID、PR_IN_REPLY_TO_ID_A、PR_IN_REPLY_TO_ID_W</span><span class="sxs-lookup"><span data-stu-id="a9d05-107">PR_IN_REPLY_TO_ID, PR_IN_REPLY_TO_ID_A, PR_IN_REPLY_TO_ID_W</span></span>  <br/> |
|<span data-ttu-id="a9d05-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a9d05-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a9d05-109">0x1042</span><span class="sxs-lookup"><span data-stu-id="a9d05-109">0x1042</span></span>  <br/> |
|<span data-ttu-id="a9d05-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="a9d05-110">Data type:</span></span>  <br/> |<span data-ttu-id="a9d05-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a9d05-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a9d05-112">領域:</span><span class="sxs-lookup"><span data-stu-id="a9d05-112">Area:</span></span>  <br/> |<span data-ttu-id="a9d05-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="a9d05-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9d05-114">備考</span><span class="sxs-lookup"><span data-stu-id="a9d05-114">Remarks</span></span>

<span data-ttu-id="a9d05-115">すべてのメッセージの返信には、これらのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9d05-115">These properties must be set on all message replies.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a9d05-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a9d05-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a9d05-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a9d05-117">Protocol specifications</span></span>

<span data-ttu-id="a9d05-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a9d05-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a9d05-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="a9d05-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a9d05-120">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a9d05-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a9d05-121">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="a9d05-121">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="a9d05-122">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a9d05-122">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a9d05-123">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="a9d05-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a9d05-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a9d05-124">Header files</span></span>

<span data-ttu-id="a9d05-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a9d05-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a9d05-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a9d05-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="a9d05-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a9d05-127">Mapitags.h</span></span>
  
> <span data-ttu-id="a9d05-128">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a9d05-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a9d05-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="a9d05-129">See also</span></span>



[<span data-ttu-id="a9d05-130">PidTagInternetMessageId の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="a9d05-130">PidTagInternetMessageId Canonical Property</span></span>](pidtaginternetmessageid-canonical-property.md)


[<span data-ttu-id="a9d05-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a9d05-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a9d05-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a9d05-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a9d05-133">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="a9d05-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a9d05-134">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="a9d05-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

