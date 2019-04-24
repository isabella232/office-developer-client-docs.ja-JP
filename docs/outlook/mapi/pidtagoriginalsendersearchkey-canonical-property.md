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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342603"
---
# <a name="pidtagoriginalsendersearchkey-canonical-property"></a><span data-ttu-id="15339-103">PidTagOriginalSenderSearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="15339-103">PidTagOriginalSenderSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="15339-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15339-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15339-105">最初のバージョンのメッセージ、つまり転送または返信の前にメッセージを送信するための検索キーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="15339-105">Contains the search key for the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="15339-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="15339-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="15339-107">PR_ORIGINAL_SENDER_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="15339-107">PR_ORIGINAL_SENDER_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="15339-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="15339-108">Identifier:</span></span>  <br/> |<span data-ttu-id="15339-109">0x005c</span><span class="sxs-lookup"><span data-stu-id="15339-109">0x005C</span></span>  <br/> |
|<span data-ttu-id="15339-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="15339-110">Data type:</span></span>  <br/> |<span data-ttu-id="15339-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="15339-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="15339-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="15339-112">Area:</span></span>  <br/> |<span data-ttu-id="15339-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="15339-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15339-114">解説</span><span class="sxs-lookup"><span data-stu-id="15339-114">Remarks</span></span>

<span data-ttu-id="15339-115">このプロパティは、メッセージの元の送信者のアドレスプロパティの1つです。</span><span class="sxs-lookup"><span data-stu-id="15339-115">This property is one of the address properties for the original sender of a message.</span></span> <span data-ttu-id="15339-116">クライアントアプリケーションでは、最初にメッセージを送信するときに、このプロパティを**PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) プロパティの値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="15339-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) property.</span></span> <span data-ttu-id="15339-117">メッセージが転送または返信されるときには変更されません。</span><span class="sxs-lookup"><span data-stu-id="15339-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="15339-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="15339-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="15339-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="15339-119">Protocol specifications</span></span>

<span data-ttu-id="15339-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15339-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15339-121">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="15339-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="15339-122">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15339-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15339-123">電子メールメッセージオブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="15339-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="15339-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="15339-124">Header files</span></span>

<span data-ttu-id="15339-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="15339-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="15339-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="15339-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="15339-127">Mapitags</span><span class="sxs-lookup"><span data-stu-id="15339-127">Mapitags.h</span></span>
  
> <span data-ttu-id="15339-128">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="15339-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="15339-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="15339-129">See also</span></span>



[<span data-ttu-id="15339-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="15339-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="15339-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="15339-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="15339-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="15339-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="15339-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="15339-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

