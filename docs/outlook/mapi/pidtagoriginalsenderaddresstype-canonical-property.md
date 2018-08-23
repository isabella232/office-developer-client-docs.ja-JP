---
title: PidTagOriginalSenderAddressType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderAddressType
api_type:
- COM
ms.assetid: bd777f19-cbb1-4497-8a0b-e05b491c6957
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ba0d68482c06a1f6d9ccdae95f63e980a1fd23e9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563745"
---
# <a name="pidtagoriginalsenderaddresstype-canonical-property"></a><span data-ttu-id="c1bf1-103">PidTagOriginalSenderAddressType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c1bf1-103">PidTagOriginalSenderAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="c1bf1-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1bf1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1bf1-105">最初のバージョンのメッセージを転送または返信する前にメッセージは、送信者のアドレスの種類が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c1bf1-105">Contains the address type of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c1bf1-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c1bf1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c1bf1-107">PR_ORIGINAL_SENDER_ADDRTYPE、PR_ORIGINAL_SENDER_ADDRTYPE_A、PR_ORIGINAL_SENDER_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="c1bf1-107">PR_ORIGINAL_SENDER_ADDRTYPE, PR_ORIGINAL_SENDER_ADDRTYPE_A, PR_ORIGINAL_SENDER_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="c1bf1-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c1bf1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c1bf1-109">0x0066</span><span class="sxs-lookup"><span data-stu-id="c1bf1-109">0x0066</span></span>  <br/> |
|<span data-ttu-id="c1bf1-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c1bf1-110">Data type:</span></span>  <br/> |<span data-ttu-id="c1bf1-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c1bf1-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c1bf1-112">領域:</span><span class="sxs-lookup"><span data-stu-id="c1bf1-112">Area:</span></span>  <br/> |<span data-ttu-id="c1bf1-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="c1bf1-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c1bf1-114">注釈</span><span class="sxs-lookup"><span data-stu-id="c1bf1-114">Remarks</span></span>

<span data-ttu-id="c1bf1-115">これらのプロパティでは、メッセージの元の送信者のアドレスのプロパティの例を示します。</span><span class="sxs-lookup"><span data-stu-id="c1bf1-115">These properties are examples of the address properties for the original sender of a message.</span></span> <span data-ttu-id="c1bf1-116">メッセージの最初の提出書類は、クライアント アプリケーションは、 **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) の値にこれらのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1bf1-116">At first submission of the message, the client application should set these properties to the value of **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)).</span></span> <span data-ttu-id="c1bf1-117">メッセージを転送または返信するときは変更されません。</span><span class="sxs-lookup"><span data-stu-id="c1bf1-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c1bf1-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c1bf1-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c1bf1-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c1bf1-119">Protocol specifications</span></span>

<span data-ttu-id="c1bf1-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c1bf1-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c1bf1-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="c1bf1-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c1bf1-122">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c1bf1-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c1bf1-123">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c1bf1-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c1bf1-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c1bf1-124">Header files</span></span>

<span data-ttu-id="c1bf1-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c1bf1-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c1bf1-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c1bf1-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="c1bf1-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c1bf1-127">Mapitags.h</span></span>
  
> <span data-ttu-id="c1bf1-128">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c1bf1-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c1bf1-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="c1bf1-129">See also</span></span>



[<span data-ttu-id="c1bf1-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c1bf1-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c1bf1-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c1bf1-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c1bf1-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c1bf1-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c1bf1-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c1bf1-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

