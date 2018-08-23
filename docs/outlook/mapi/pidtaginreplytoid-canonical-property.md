---
title: PidTagInReplyToId 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2e8ed4af81de6e48af3e427f2d2d2f94572d241f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802857"
---
# <a name="pidtaginreplytoid-canonical-property"></a><span data-ttu-id="8c07c-103">PidTagInReplyToId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8c07c-103">PidTagInReplyToId Canonical Property</span></span>

  
  
<span data-ttu-id="8c07c-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8c07c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8c07c-105">**PR_INTERNET_MESSAGE_ID** ([PidTagInternetMessageId](pidtaginternetmessageid-canonical-property.md)) プロパティの値元のメッセージにはが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8c07c-105">Contains the original message's **PR_INTERNET_MESSAGE_ID** ([PidTagInternetMessageId](pidtaginternetmessageid-canonical-property.md)) property value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8c07c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8c07c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8c07c-107">PR_IN_REPLY_TO_ID、PR_IN_REPLY_TO_ID_A、PR_IN_REPLY_TO_ID_W</span><span class="sxs-lookup"><span data-stu-id="8c07c-107">PR_IN_REPLY_TO_ID, PR_IN_REPLY_TO_ID_A, PR_IN_REPLY_TO_ID_W</span></span>  <br/> |
|<span data-ttu-id="8c07c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8c07c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8c07c-109">0x1042</span><span class="sxs-lookup"><span data-stu-id="8c07c-109">0x1042</span></span>  <br/> |
|<span data-ttu-id="8c07c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8c07c-110">Data type:</span></span>  <br/> |<span data-ttu-id="8c07c-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8c07c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8c07c-112">領域:</span><span class="sxs-lookup"><span data-stu-id="8c07c-112">Area:</span></span>  <br/> |<span data-ttu-id="8c07c-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="8c07c-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c07c-114">注釈</span><span class="sxs-lookup"><span data-stu-id="8c07c-114">Remarks</span></span>

<span data-ttu-id="8c07c-115">すべてのメッセージの返信には、これらのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c07c-115">These properties must be set on all message replies.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8c07c-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8c07c-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8c07c-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8c07c-117">Protocol specifications</span></span>

<span data-ttu-id="8c07c-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c07c-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c07c-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="8c07c-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8c07c-120">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c07c-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c07c-121">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="8c07c-121">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="8c07c-122">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c07c-122">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c07c-123">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="8c07c-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8c07c-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8c07c-124">Header files</span></span>

<span data-ttu-id="8c07c-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8c07c-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="8c07c-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8c07c-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="8c07c-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8c07c-127">Mapitags.h</span></span>
  
> <span data-ttu-id="8c07c-128">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8c07c-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8c07c-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="8c07c-129">See also</span></span>



[<span data-ttu-id="8c07c-130">PidTagInternetMessageId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8c07c-130">PidTagInternetMessageId Canonical Property</span></span>](pidtaginternetmessageid-canonical-property.md)


[<span data-ttu-id="8c07c-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8c07c-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8c07c-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8c07c-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8c07c-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8c07c-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8c07c-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8c07c-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

