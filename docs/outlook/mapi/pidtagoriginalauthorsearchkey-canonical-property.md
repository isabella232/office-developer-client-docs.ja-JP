---
title: PidTagOriginalAuthorSearchKey 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorSearchKey
api_type:
- COM
ms.assetid: 4a10cf99-c5e6-4a24-b531-3aebb7800bfe
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 225c0813139a74b735b5b8a3d5a729e630cd3511
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563339"
---
# <a name="pidtagoriginalauthorsearchkey-canonical-property"></a><span data-ttu-id="5f8c8-103">PidTagOriginalAuthorSearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5f8c8-103">PidTagOriginalAuthorSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="5f8c8-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f8c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f8c8-105">転送または返信する前にメッセージは、メッセージの最初のバージョンの作成者の検索キーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5f8c8-105">Contains the search key of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5f8c8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5f8c8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5f8c8-107">PR_ORIGINAL_AUTHOR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="5f8c8-107">PR_ORIGINAL_AUTHOR_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="5f8c8-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="5f8c8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5f8c8-109">0x0056</span><span class="sxs-lookup"><span data-stu-id="5f8c8-109">0x0056</span></span>  <br/> |
|<span data-ttu-id="5f8c8-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5f8c8-110">Data type:</span></span>  <br/> |<span data-ttu-id="5f8c8-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5f8c8-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5f8c8-112">領域:</span><span class="sxs-lookup"><span data-stu-id="5f8c8-112">Area:</span></span>  <br/> |<span data-ttu-id="5f8c8-113">Server</span><span class="sxs-lookup"><span data-stu-id="5f8c8-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f8c8-114">注釈</span><span class="sxs-lookup"><span data-stu-id="5f8c8-114">Remarks</span></span>

<span data-ttu-id="5f8c8-115">このプロパティは、メッセージの作成者のアドレスのプロパティのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="5f8c8-115">This property is one of the address properties for the author of a message.</span></span> <span data-ttu-id="5f8c8-116">メッセージの最初の提出書類は、クライアント アプリケーションは、 **PR_SENDER_SEARCH_KEY**の[PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)プロパティの値にこのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f8c8-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_SEARCH_KEY**[PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md) property.</span></span> <span data-ttu-id="5f8c8-117">メッセージを転送または返信するときは変更されません。</span><span class="sxs-lookup"><span data-stu-id="5f8c8-117">It is never changed when the message is forwarded or replied to.</span></span> 
  
<span data-ttu-id="5f8c8-118">ローカルのメッセージング ドメインの外部からの情報の保持の元の作成者プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="5f8c8-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="5f8c8-119">別のメッセージング ドメインからメッセージが到着するなど、インターネットからこれらのプロパティは、元の情報が失われていないことを確認する方法。</span><span class="sxs-lookup"><span data-stu-id="5f8c8-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5f8c8-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5f8c8-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5f8c8-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5f8c8-121">Header files</span></span>

<span data-ttu-id="5f8c8-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5f8c8-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="5f8c8-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5f8c8-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="5f8c8-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5f8c8-124">Mapitags.h</span></span>
  
> <span data-ttu-id="5f8c8-125">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5f8c8-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5f8c8-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="5f8c8-126">See also</span></span>



[<span data-ttu-id="5f8c8-127">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5f8c8-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5f8c8-128">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5f8c8-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5f8c8-129">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5f8c8-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5f8c8-130">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5f8c8-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

