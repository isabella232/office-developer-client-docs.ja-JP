---
title: PidTagOriginalSenderSearchKey の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderSearchKey
api_type:
- COM
ms.assetid: 164eb9dd-e553-459e-99c1-3da0284bb01f
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 2aa0a8601a72b6d4c40167ac55d3d643bf946708
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803081"
---
# <a name="pidtagoriginalsendersearchkey-canonical-property"></a><span data-ttu-id="ebaf9-103">PidTagOriginalSenderSearchKey の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="ebaf9-103">PidTagOriginalSenderSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="ebaf9-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ebaf9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ebaf9-105">転送または返信する前にメッセージは、メッセージの最初のバージョンに、差出人の検索キーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ebaf9-105">Contains the search key for the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ebaf9-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="ebaf9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ebaf9-107">PR_ORIGINAL_SENDER_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="ebaf9-107">PR_ORIGINAL_SENDER_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="ebaf9-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ebaf9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ebaf9-109">0x005C</span><span class="sxs-lookup"><span data-stu-id="ebaf9-109">0x005C</span></span>  <br/> |
|<span data-ttu-id="ebaf9-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="ebaf9-110">Data type:</span></span>  <br/> |<span data-ttu-id="ebaf9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ebaf9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ebaf9-112">領域:</span><span class="sxs-lookup"><span data-stu-id="ebaf9-112">Area:</span></span>  <br/> |<span data-ttu-id="ebaf9-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="ebaf9-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ebaf9-114">備考</span><span class="sxs-lookup"><span data-stu-id="ebaf9-114">Remarks</span></span>

<span data-ttu-id="ebaf9-115">このプロパティは、メッセージの元の送信者のアドレスのプロパティのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="ebaf9-115">This property is one of the address properties for the original sender of a message.</span></span> <span data-ttu-id="ebaf9-116">メッセージの最初の提出書類は、クライアント アプリケーションは、 **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) プロパティの値にこのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ebaf9-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) property.</span></span> <span data-ttu-id="ebaf9-117">メッセージを転送または返信するときは変更されません。</span><span class="sxs-lookup"><span data-stu-id="ebaf9-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ebaf9-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ebaf9-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ebaf9-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ebaf9-119">Protocol specifications</span></span>

<span data-ttu-id="ebaf9-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ebaf9-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ebaf9-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="ebaf9-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ebaf9-122">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ebaf9-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ebaf9-123">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="ebaf9-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ebaf9-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ebaf9-124">Header files</span></span>

<span data-ttu-id="ebaf9-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ebaf9-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="ebaf9-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ebaf9-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="ebaf9-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ebaf9-127">Mapitags.h</span></span>
  
> <span data-ttu-id="ebaf9-128">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ebaf9-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ebaf9-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="ebaf9-129">See also</span></span>



[<span data-ttu-id="ebaf9-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ebaf9-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ebaf9-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ebaf9-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ebaf9-132">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="ebaf9-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ebaf9-133">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="ebaf9-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

