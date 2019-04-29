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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 09331e1201b6f6e45bb9e26e618ee59e67efbf8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409581"
---
# <a name="pidtagoriginalauthorsearchkey-canonical-property"></a><span data-ttu-id="bc48b-103">PidTagOriginalAuthorSearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bc48b-103">PidTagOriginalAuthorSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="bc48b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc48b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc48b-105">最初のバージョンのメッセージ、つまり転送または返信する前のメッセージの作成者の検索キーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="bc48b-105">Contains the search key of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bc48b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="bc48b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bc48b-107">PR_ORIGINAL_AUTHOR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="bc48b-107">PR_ORIGINAL_AUTHOR_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="bc48b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="bc48b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bc48b-109">0x0056</span><span class="sxs-lookup"><span data-stu-id="bc48b-109">0x0056</span></span>  <br/> |
|<span data-ttu-id="bc48b-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="bc48b-110">Data type:</span></span>  <br/> |<span data-ttu-id="bc48b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bc48b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bc48b-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="bc48b-112">Area:</span></span>  <br/> |<span data-ttu-id="bc48b-113">サーバー</span><span class="sxs-lookup"><span data-stu-id="bc48b-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bc48b-114">注釈</span><span class="sxs-lookup"><span data-stu-id="bc48b-114">Remarks</span></span>

<span data-ttu-id="bc48b-115">このプロパティは、メッセージの作成者のアドレスプロパティの1つです。</span><span class="sxs-lookup"><span data-stu-id="bc48b-115">This property is one of the address properties for the author of a message.</span></span> <span data-ttu-id="bc48b-116">クライアントアプリケーションでは、最初にメッセージを送信するときに、このプロパティを**PR_SENDER_SEARCH_KEY**[PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)プロパティの値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc48b-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_SEARCH_KEY**[PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md) property.</span></span> <span data-ttu-id="bc48b-117">メッセージが転送または返信されるときには変更されません。</span><span class="sxs-lookup"><span data-stu-id="bc48b-117">It is never changed when the message is forwarded or replied to.</span></span> 
  
<span data-ttu-id="bc48b-118">元の作成者のプロパティを使用すると、ローカルのメッセージングドメインの外部にある情報を保持できます。</span><span class="sxs-lookup"><span data-stu-id="bc48b-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="bc48b-119">インターネットからなど、他のメッセージングドメインからメッセージが到着すると、これらのプロパティを使用して元の情報が失われないようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="bc48b-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bc48b-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bc48b-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="bc48b-121">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="bc48b-121">Header files</span></span>

<span data-ttu-id="bc48b-122">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bc48b-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="bc48b-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bc48b-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="bc48b-124">Mapitags</span><span class="sxs-lookup"><span data-stu-id="bc48b-124">Mapitags.h</span></span>
  
> <span data-ttu-id="bc48b-125">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="bc48b-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bc48b-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="bc48b-126">See also</span></span>



[<span data-ttu-id="bc48b-127">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="bc48b-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bc48b-128">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bc48b-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bc48b-129">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="bc48b-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bc48b-130">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="bc48b-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

