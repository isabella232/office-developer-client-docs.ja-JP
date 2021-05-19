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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 036f38c1228e08cfc9a2093c027195a802904f19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358836"
---
# <a name="pidtaginreplytoid-canonical-property"></a><span data-ttu-id="91a99-103">PidTagInReplyToId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="91a99-103">PidTagInReplyToId Canonical Property</span></span>

  
  
<span data-ttu-id="91a99-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91a99-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91a99-105">元のメッセージのプロパティ [(PidTagInternetMessageId)](pidtaginternetmessageid-canonical-property.md) **PR_INTERNET_MESSAGE_IDプロパティ** 値を格納します。</span><span class="sxs-lookup"><span data-stu-id="91a99-105">Contains the original message's **PR_INTERNET_MESSAGE_ID** ([PidTagInternetMessageId](pidtaginternetmessageid-canonical-property.md)) property value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="91a99-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="91a99-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="91a99-107">PR_IN_REPLY_TO_ID、PR_IN_REPLY_TO_ID_A、PR_IN_REPLY_TO_ID_W</span><span class="sxs-lookup"><span data-stu-id="91a99-107">PR_IN_REPLY_TO_ID, PR_IN_REPLY_TO_ID_A, PR_IN_REPLY_TO_ID_W</span></span>  <br/> |
|<span data-ttu-id="91a99-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="91a99-108">Identifier:</span></span>  <br/> |<span data-ttu-id="91a99-109">0x1042</span><span class="sxs-lookup"><span data-stu-id="91a99-109">0x1042</span></span>  <br/> |
|<span data-ttu-id="91a99-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="91a99-110">Data type:</span></span>  <br/> |<span data-ttu-id="91a99-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="91a99-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="91a99-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="91a99-112">Area:</span></span>  <br/> |<span data-ttu-id="91a99-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="91a99-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91a99-114">注釈</span><span class="sxs-lookup"><span data-stu-id="91a99-114">Remarks</span></span>

<span data-ttu-id="91a99-115">これらのプロパティは、すべてのメッセージ返信で設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="91a99-115">These properties must be set on all message replies.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="91a99-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="91a99-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="91a99-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="91a99-117">Protocol specifications</span></span>

<span data-ttu-id="91a99-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91a99-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91a99-119">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="91a99-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="91a99-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91a99-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91a99-121">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="91a99-121">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="91a99-122">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91a99-122">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91a99-123">インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="91a99-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="91a99-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="91a99-124">Header files</span></span>

<span data-ttu-id="91a99-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="91a99-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="91a99-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="91a99-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="91a99-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="91a99-127">Mapitags.h</span></span>
  
> <span data-ttu-id="91a99-128">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="91a99-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="91a99-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="91a99-129">See also</span></span>



[<span data-ttu-id="91a99-130">PidTagInternetMessageId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="91a99-130">PidTagInternetMessageId Canonical Property</span></span>](pidtaginternetmessageid-canonical-property.md)


[<span data-ttu-id="91a99-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="91a99-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="91a99-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="91a99-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="91a99-133">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="91a99-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="91a99-134">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="91a99-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

