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
ms.openlocfilehash: 3a49c6d70cc47ff726a7a99860b5e81a400be0bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355651"
---
# <a name="pidtagmessagesize-canonical-property"></a><span data-ttu-id="4233a-103">PidTagMessageSize 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4233a-103">PidTagMessageSize Canonical Property</span></span>

  
  
<span data-ttu-id="4233a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4233a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4233a-105">メッセージオブジェクトのすべてのプロパティのサイズの合計 (バイト数) を格納します。</span><span class="sxs-lookup"><span data-stu-id="4233a-105">Contains the sum, in bytes, of the sizes of all properties on a message object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4233a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4233a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4233a-107">PR_MESSAGE_SIZE</span><span class="sxs-lookup"><span data-stu-id="4233a-107">PR_MESSAGE_SIZE</span></span>  <br/> |
|<span data-ttu-id="4233a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="4233a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4233a-109">0x0e08</span><span class="sxs-lookup"><span data-stu-id="4233a-109">0x0E08</span></span>  <br/> |
|<span data-ttu-id="4233a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4233a-110">Data type:</span></span>  <br/> |<span data-ttu-id="4233a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4233a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4233a-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="4233a-112">Area:</span></span>  <br/> |<span data-ttu-id="4233a-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="4233a-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4233a-114">解説</span><span class="sxs-lookup"><span data-stu-id="4233a-114">Remarks</span></span>

<span data-ttu-id="4233a-115">このプロパティは、メッセージオブジェクトに公開することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="4233a-115">It is recommended that message objects expose this property.</span></span> <span data-ttu-id="4233a-116">メッセージサイズは、メッセージがあるメッセージストアから別のメッセージストアに移動されたときに転送されるおおよそのバイト数を示します。</span><span class="sxs-lookup"><span data-stu-id="4233a-116">The message size indicates the approximate number of bytes that are transferred when the message is moved from one message store to another.</span></span> <span data-ttu-id="4233a-117">message オブジェクトのすべてのプロパティのサイズの合計は、通常、メッセージテキストだけではなく、非常に大きくなります。</span><span class="sxs-lookup"><span data-stu-id="4233a-117">Being the sum of the sizes of all properties on the message object, it is usually considerably greater than the message text alone.</span></span> 
  
<span data-ttu-id="4233a-118">ほとんどのメッセージストアプロバイダーは、処理するメッセージに対してこのプロパティを計算します。</span><span class="sxs-lookup"><span data-stu-id="4233a-118">Most message store providers compute this property for messages that they handle.</span></span> <span data-ttu-id="4233a-119">ただし、一部のメッセージストアプロバイダーでは、このプロパティをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="4233a-119">However, some message store providers do not support this property.</span></span> <span data-ttu-id="4233a-120">いずれの場合も、このプロパティは、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)または[IMessage:: submitmessage](imessage-submitmessage.md)メソッドが呼び出されるまで使用できません。</span><span class="sxs-lookup"><span data-stu-id="4233a-120">In any case, this property is not available until the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) or [IMessage::SubmitMessage](imessage-submitmessage.md) method has been called.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4233a-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4233a-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4233a-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4233a-122">Protocol specifications</span></span>

<span data-ttu-id="4233a-123">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4233a-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4233a-124">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="4233a-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4233a-125">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4233a-125">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4233a-126">メッセージと添付ファイルオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="4233a-126">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="4233a-127">[[OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4233a-127">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4233a-128">フォルダー操作を処理します。</span><span class="sxs-lookup"><span data-stu-id="4233a-128">Handles folder operations.</span></span>
    
<span data-ttu-id="4233a-129">[[OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4233a-129">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4233a-130">コアメッセージストアオブジェクトに対する許容される操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="4233a-130">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4233a-131">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="4233a-131">Header files</span></span>

<span data-ttu-id="4233a-132">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4233a-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="4233a-133">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4233a-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="4233a-134">Mapitags</span><span class="sxs-lookup"><span data-stu-id="4233a-134">Mapitags.h</span></span>
  
> <span data-ttu-id="4233a-135">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4233a-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4233a-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="4233a-136">See also</span></span>



[<span data-ttu-id="4233a-137">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="4233a-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4233a-138">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4233a-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4233a-139">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4233a-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4233a-140">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4233a-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

