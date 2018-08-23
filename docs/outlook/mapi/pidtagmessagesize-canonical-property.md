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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c52fd6d6caaec6f215856daead809ceb0bd76729
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574994"
---
# <a name="pidtagmessagesize-canonical-property"></a><span data-ttu-id="24b96-103">PidTagMessageSize 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="24b96-103">PidTagMessageSize Canonical Property</span></span>

  
  
<span data-ttu-id="24b96-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24b96-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24b96-105">メッセージ オブジェクトのすべてのプロパティのサイズの合計 (バイト単位) にはが含まれています。</span><span class="sxs-lookup"><span data-stu-id="24b96-105">Contains the sum, in bytes, of the sizes of all properties on a message object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="24b96-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="24b96-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="24b96-107">PR_MESSAGE_SIZE</span><span class="sxs-lookup"><span data-stu-id="24b96-107">PR_MESSAGE_SIZE</span></span>  <br/> |
|<span data-ttu-id="24b96-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="24b96-108">Identifier:</span></span>  <br/> |<span data-ttu-id="24b96-109">0x0E08</span><span class="sxs-lookup"><span data-stu-id="24b96-109">0x0E08</span></span>  <br/> |
|<span data-ttu-id="24b96-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="24b96-110">Data type:</span></span>  <br/> |<span data-ttu-id="24b96-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="24b96-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="24b96-112">領域:</span><span class="sxs-lookup"><span data-stu-id="24b96-112">Area:</span></span>  <br/> |<span data-ttu-id="24b96-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="24b96-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24b96-114">注釈</span><span class="sxs-lookup"><span data-stu-id="24b96-114">Remarks</span></span>

<span data-ttu-id="24b96-115">メッセージ オブジェクトがこのプロパティを公開することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="24b96-115">It is recommended that message objects expose this property.</span></span> <span data-ttu-id="24b96-116">メッセージのサイズは、メッセージが別の 1 つのメッセージ ・ ストアに移動した場合に転送されるバイトのおおよその数を示します。</span><span class="sxs-lookup"><span data-stu-id="24b96-116">The message size indicates the approximate number of bytes that are transferred when the message is moved from one message store to another.</span></span> <span data-ttu-id="24b96-117">メッセージ オブジェクトのすべてのプロパティのサイズの合計である、多くのメッセージのテキストだけよりもかなり大きいです。</span><span class="sxs-lookup"><span data-stu-id="24b96-117">Being the sum of the sizes of all properties on the message object, it is usually considerably greater than the message text alone.</span></span> 
  
<span data-ttu-id="24b96-118">ほとんどのメッセージは、プロバイダーの計算、処理されるメッセージに対してこのプロパティを格納します。</span><span class="sxs-lookup"><span data-stu-id="24b96-118">Most message store providers compute this property for messages that they handle.</span></span> <span data-ttu-id="24b96-119">ただし、いくつかのメッセージ ストア プロバイダーはこのプロパティをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="24b96-119">However, some message store providers do not support this property.</span></span> <span data-ttu-id="24b96-120">どのような場合は、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)または[IMessage::SubmitMessage](imessage-submitmessage.md)メソッドが呼び出されるまでこのプロパティは使用できません。</span><span class="sxs-lookup"><span data-stu-id="24b96-120">In any case, this property is not available until the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) or [IMessage::SubmitMessage](imessage-submitmessage.md) method has been called.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="24b96-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="24b96-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="24b96-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="24b96-122">Protocol specifications</span></span>

<span data-ttu-id="24b96-123">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24b96-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="24b96-124">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="24b96-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="24b96-125">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24b96-125">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="24b96-126">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="24b96-126">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="24b96-127">[[MS OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24b96-127">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="24b96-128">フォルダーの操作を処理します。</span><span class="sxs-lookup"><span data-stu-id="24b96-128">Handles folder operations.</span></span>
    
<span data-ttu-id="24b96-129">[[MS OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24b96-129">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="24b96-130">コア メッセージのストア オブジェクトの許可された操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="24b96-130">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="24b96-131">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="24b96-131">Header files</span></span>

<span data-ttu-id="24b96-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="24b96-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="24b96-133">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="24b96-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="24b96-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="24b96-134">Mapitags.h</span></span>
  
> <span data-ttu-id="24b96-135">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="24b96-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="24b96-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="24b96-136">See also</span></span>



[<span data-ttu-id="24b96-137">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="24b96-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="24b96-138">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="24b96-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="24b96-139">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="24b96-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="24b96-140">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="24b96-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

