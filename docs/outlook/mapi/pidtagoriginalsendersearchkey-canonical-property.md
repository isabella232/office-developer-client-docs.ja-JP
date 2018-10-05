---
title: PidTagOriginalSenderSearchKey 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 97ab08d3da3725187ef2d5c70bec80e9142bdd21
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396466"
---
# <a name="pidtagoriginalsendersearchkey-canonical-property"></a><span data-ttu-id="9382d-103">PidTagOriginalSenderSearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9382d-103">PidTagOriginalSenderSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="9382d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9382d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9382d-105">転送または返信する前にメッセージは、メッセージの最初のバージョンに、差出人の検索キーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="9382d-105">Contains the search key for the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9382d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9382d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9382d-107">PR_ORIGINAL_SENDER_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="9382d-107">PR_ORIGINAL_SENDER_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="9382d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9382d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9382d-109">0x005C</span><span class="sxs-lookup"><span data-stu-id="9382d-109">0x005C</span></span>  <br/> |
|<span data-ttu-id="9382d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9382d-110">Data type:</span></span>  <br/> |<span data-ttu-id="9382d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9382d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9382d-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="9382d-112">Area:</span></span>  <br/> |<span data-ttu-id="9382d-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="9382d-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9382d-114">備考</span><span class="sxs-lookup"><span data-stu-id="9382d-114">Remarks</span></span>

<span data-ttu-id="9382d-115">このプロパティは、メッセージの元の送信者のアドレスのプロパティのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="9382d-115">This property is one of the address properties for the original sender of a message.</span></span> <span data-ttu-id="9382d-116">メッセージの最初の提出書類は、クライアント アプリケーションは、 **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) プロパティの値にこのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9382d-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) property.</span></span> <span data-ttu-id="9382d-117">メッセージを転送または返信するときは変更されません。</span><span class="sxs-lookup"><span data-stu-id="9382d-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9382d-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9382d-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9382d-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9382d-119">Protocol specifications</span></span>

<span data-ttu-id="9382d-120">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9382d-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9382d-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="9382d-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9382d-122">[[MS OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9382d-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9382d-123">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="9382d-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9382d-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="9382d-124">Header files</span></span>

<span data-ttu-id="9382d-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9382d-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="9382d-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9382d-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="9382d-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9382d-127">Mapitags.h</span></span>
  
> <span data-ttu-id="9382d-128">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9382d-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9382d-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="9382d-129">See also</span></span>



[<span data-ttu-id="9382d-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9382d-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9382d-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9382d-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9382d-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9382d-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9382d-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9382d-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

