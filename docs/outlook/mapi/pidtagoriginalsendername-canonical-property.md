---
title: PidTagOriginalSenderName の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderName
api_type:
- COM
ms.assetid: 5e3b7764-b122-4405-be4f-7fec571c7dfc
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ae0ae8536f4f088bae4561e123afce716b623414
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803083"
---
# <a name="pidtagoriginalsendername-canonical-property"></a><span data-ttu-id="08a0e-103">PidTagOriginalSenderName の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="08a0e-103">PidTagOriginalSenderName Canonical Property</span></span>

  
  
<span data-ttu-id="08a0e-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="08a0e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="08a0e-105">転送または返信する前にメッセージは、メッセージの最初のバージョンの送信者の表示名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="08a0e-105">Contains the display name of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="08a0e-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="08a0e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="08a0e-107">PR_ORIGINAL_SENDER_NAME、PR_ORIGINAL_SENDER_NAME_A、PR_ORIGINAL_SENDER_NAME_W</span><span class="sxs-lookup"><span data-stu-id="08a0e-107">PR_ORIGINAL_SENDER_NAME, PR_ORIGINAL_SENDER_NAME_A, PR_ORIGINAL_SENDER_NAME_W</span></span>  <br/> |
|<span data-ttu-id="08a0e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="08a0e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="08a0e-109">0x005A</span><span class="sxs-lookup"><span data-stu-id="08a0e-109">0x005A</span></span>  <br/> |
|<span data-ttu-id="08a0e-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="08a0e-110">Data type:</span></span>  <br/> |<span data-ttu-id="08a0e-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="08a0e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="08a0e-112">領域:</span><span class="sxs-lookup"><span data-stu-id="08a0e-112">Area:</span></span>  <br/> |<span data-ttu-id="08a0e-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="08a0e-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08a0e-114">備考</span><span class="sxs-lookup"><span data-stu-id="08a0e-114">Remarks</span></span>

<span data-ttu-id="08a0e-115">これらのプロパティでは、メッセージの元の送信者のアドレスのプロパティの例を示します。</span><span class="sxs-lookup"><span data-stu-id="08a0e-115">These properties are examples of the address properties for the original sender of a message.</span></span> <span data-ttu-id="08a0e-116">メッセージの最初の提出書類は、クライアント アプリケーションは、 **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) プロパティの値にこれらのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08a0e-116">At first submission of the message, a client application should set these properties to the value of the **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) property.</span></span> <span data-ttu-id="08a0e-117">メッセージを転送または返信するときは変更されません。</span><span class="sxs-lookup"><span data-stu-id="08a0e-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="08a0e-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="08a0e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="08a0e-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="08a0e-119">Protocol specifications</span></span>

<span data-ttu-id="08a0e-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08a0e-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08a0e-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="08a0e-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="08a0e-122">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08a0e-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08a0e-123">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="08a0e-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="08a0e-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="08a0e-124">Header files</span></span>

<span data-ttu-id="08a0e-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="08a0e-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="08a0e-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="08a0e-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="08a0e-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="08a0e-127">Mapitags.h</span></span>
  
> <span data-ttu-id="08a0e-128">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="08a0e-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="08a0e-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="08a0e-129">See also</span></span>



[<span data-ttu-id="08a0e-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="08a0e-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="08a0e-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="08a0e-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="08a0e-132">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="08a0e-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="08a0e-133">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="08a0e-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

