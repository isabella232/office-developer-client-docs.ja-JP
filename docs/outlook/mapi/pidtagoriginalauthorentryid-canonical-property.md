---
title: PidTagOriginalAuthorEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorEntryId
api_type:
- COM
ms.assetid: 34654660-b003-42f5-9fcd-24ebaccd735d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 866c28bc08f669d18487c99c9a13bc7347b605fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356204"
---
# <a name="pidtagoriginalauthorentryid-canonical-property"></a><span data-ttu-id="818f7-103">PidTagOriginalAuthorEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="818f7-103">PidTagOriginalAuthorEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="818f7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="818f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="818f7-105">メッセージの最初のバージョンの作成者のエントリ id、つまり転送または返信の前にメッセージを格納します。</span><span class="sxs-lookup"><span data-stu-id="818f7-105">Contains the entry identifier of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="818f7-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="818f7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="818f7-107">PR_ORIGINAL_AUTHOR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="818f7-107">PR_ORIGINAL_AUTHOR_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="818f7-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="818f7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="818f7-109">0x004c</span><span class="sxs-lookup"><span data-stu-id="818f7-109">0x004C</span></span>  <br/> |
|<span data-ttu-id="818f7-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="818f7-110">Data type:</span></span>  <br/> |<span data-ttu-id="818f7-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="818f7-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="818f7-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="818f7-112">Area:</span></span>  <br/> |<span data-ttu-id="818f7-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="818f7-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="818f7-114">解説</span><span class="sxs-lookup"><span data-stu-id="818f7-114">Remarks</span></span>

<span data-ttu-id="818f7-115">このプロパティは、メッセージの作成者のアドレスプロパティの1つです。</span><span class="sxs-lookup"><span data-stu-id="818f7-115">This property is one of the address properties for the author of a message.</span></span> <span data-ttu-id="818f7-116">クライアントアプリケーションでは、最初にメッセージを送信するときに、このプロパティを**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) の値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="818f7-116">At first submission of the message, the client application should set this property to the value of **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span></span> <span data-ttu-id="818f7-117">メッセージが転送または返信されるときには変更されません。</span><span class="sxs-lookup"><span data-stu-id="818f7-117">It is never changed when the message is forwarded or replied to.</span></span> 
  
<span data-ttu-id="818f7-118">元の作成者プロパティを使用すると、ローカルのメッセージングドメインの外部にある情報を保持できます。</span><span class="sxs-lookup"><span data-stu-id="818f7-118">The original author property allows for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="818f7-119">インターネットからなど、他のメッセージングドメインからメッセージが到着すると、このプロパティによって元の情報が失われないようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="818f7-119">When a message arrives from another messaging domain, such as from the Internet, this property provides a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="818f7-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="818f7-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="818f7-121">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="818f7-121">Header files</span></span>

<span data-ttu-id="818f7-122">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="818f7-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="818f7-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="818f7-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="818f7-124">Mapitags</span><span class="sxs-lookup"><span data-stu-id="818f7-124">Mapitags.h</span></span>
  
> <span data-ttu-id="818f7-125">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="818f7-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="818f7-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="818f7-126">See also</span></span>



[<span data-ttu-id="818f7-127">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="818f7-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="818f7-128">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="818f7-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="818f7-129">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="818f7-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="818f7-130">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="818f7-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

