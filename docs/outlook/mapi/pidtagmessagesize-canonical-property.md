---
title: PidTagMessageSize 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSize
api_type:
- HeaderDef
ms.assetid: c67fb54b-8cc7-4fbc-8204-36fcddfa6192
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3a49c6d70cc47ff726a7a99860b5e81a400be0bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355651"
---
# <a name="pidtagmessagesize-canonical-property"></a><span data-ttu-id="24529-103">PidTagMessageSize 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="24529-103">PidTagMessageSize Canonical Property</span></span>

  
  
<span data-ttu-id="24529-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24529-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24529-105">メッセージ オブジェクト上のすべてのプロパティのサイズの合計 (バイト単位) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="24529-105">Contains the sum, in bytes, of the sizes of all properties on a message object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="24529-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="24529-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="24529-107">PR_MESSAGE_SIZE</span><span class="sxs-lookup"><span data-stu-id="24529-107">PR_MESSAGE_SIZE</span></span>  <br/> |
|<span data-ttu-id="24529-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="24529-108">Identifier:</span></span>  <br/> |<span data-ttu-id="24529-109">0x0E08</span><span class="sxs-lookup"><span data-stu-id="24529-109">0x0E08</span></span>  <br/> |
|<span data-ttu-id="24529-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="24529-110">Data type:</span></span>  <br/> |<span data-ttu-id="24529-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="24529-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="24529-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="24529-112">Area:</span></span>  <br/> |<span data-ttu-id="24529-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="24529-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24529-114">注釈</span><span class="sxs-lookup"><span data-stu-id="24529-114">Remarks</span></span>

<span data-ttu-id="24529-115">メッセージ オブジェクトでこのプロパティを公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="24529-115">It is recommended that message objects expose this property.</span></span> <span data-ttu-id="24529-116">メッセージ サイズは、メッセージをあるメッセージ ストアから別のメッセージ ストアに移動するときに転送される概算バイト数を示します。</span><span class="sxs-lookup"><span data-stu-id="24529-116">The message size indicates the approximate number of bytes that are transferred when the message is moved from one message store to another.</span></span> <span data-ttu-id="24529-117">メッセージ オブジェクト上のすべてのプロパティのサイズの合計値は、通常、メッセージ テキスト単独よりもかなり大きくなります。</span><span class="sxs-lookup"><span data-stu-id="24529-117">Being the sum of the sizes of all properties on the message object, it is usually considerably greater than the message text alone.</span></span> 
  
<span data-ttu-id="24529-118">ほとんどのメッセージ ストア プロバイダーは、処理するメッセージに対してこのプロパティを計算します。</span><span class="sxs-lookup"><span data-stu-id="24529-118">Most message store providers compute this property for messages that they handle.</span></span> <span data-ttu-id="24529-119">ただし、一部のメッセージ ストア プロバイダーでは、このプロパティがサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="24529-119">However, some message store providers do not support this property.</span></span> <span data-ttu-id="24529-120">いずれにしても [、IMAPIProp::SaveChanges](imapiprop-savechanges.md) または [IMessage::SubmitMessage](imessage-submitmessage.md) メソッドが呼び出されるまで、このプロパティは使用できません。</span><span class="sxs-lookup"><span data-stu-id="24529-120">In any case, this property is not available until the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) or [IMessage::SubmitMessage](imessage-submitmessage.md) method has been called.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="24529-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="24529-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="24529-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="24529-122">Protocol specifications</span></span>

<span data-ttu-id="24529-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24529-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="24529-124">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="24529-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="24529-125">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24529-125">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="24529-126">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="24529-126">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="24529-127">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24529-127">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="24529-128">フォルダー操作を処理します。</span><span class="sxs-lookup"><span data-stu-id="24529-128">Handles folder operations.</span></span>
    
<span data-ttu-id="24529-129">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24529-129">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="24529-130">コア メッセージ ストア オブジェクトに対して許容される操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="24529-130">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="24529-131">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="24529-131">Header files</span></span>

<span data-ttu-id="24529-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="24529-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="24529-133">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="24529-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="24529-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="24529-134">Mapitags.h</span></span>
  
> <span data-ttu-id="24529-135">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="24529-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="24529-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="24529-136">See also</span></span>



[<span data-ttu-id="24529-137">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="24529-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="24529-138">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="24529-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="24529-139">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="24529-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="24529-140">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="24529-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

