---
title: PidTagOriginalAuthorName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorNam
api_type:
- COM
ms.assetid: beb23742-d844-4d90-9b13-1ad376d4206c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bb62f3a44c9f17070db969683891fb2e2d62eb5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355777"
---
# <a name="pidtagoriginalauthorname-canonical-property"></a><span data-ttu-id="c87ae-103">PidTagOriginalAuthorName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c87ae-103">PidTagOriginalAuthorName Canonical Property</span></span>

  
  
<span data-ttu-id="c87ae-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c87ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c87ae-105">メッセージの最初のバージョンの作成者の表示名、つまり、転送または返信の前にメッセージを格納します。</span><span class="sxs-lookup"><span data-stu-id="c87ae-105">Contains the display name of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c87ae-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c87ae-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c87ae-107">PR_ORIGINAL_AUTHOR_NAME、PR_ORIGINAL_AUTHOR_NAME_A、PR_ORIGINAL_AUTHOR_NAME_W</span><span class="sxs-lookup"><span data-stu-id="c87ae-107">PR_ORIGINAL_AUTHOR_NAME, PR_ORIGINAL_AUTHOR_NAME_A, PR_ORIGINAL_AUTHOR_NAME_W</span></span>  <br/> |
|<span data-ttu-id="c87ae-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c87ae-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c87ae-109">0x004d</span><span class="sxs-lookup"><span data-stu-id="c87ae-109">0x004D</span></span>  <br/> |
|<span data-ttu-id="c87ae-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c87ae-110">Data type:</span></span>  <br/> |<span data-ttu-id="c87ae-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="c87ae-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="c87ae-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="c87ae-112">Area:</span></span>  <br/> |<span data-ttu-id="c87ae-113">電子メール</span><span class="sxs-lookup"><span data-stu-id="c87ae-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c87ae-114">解説</span><span class="sxs-lookup"><span data-stu-id="c87ae-114">Remarks</span></span>

<span data-ttu-id="c87ae-115">これらのプロパティは、メッセージの作成者のアドレスプロパティの例です。</span><span class="sxs-lookup"><span data-stu-id="c87ae-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="c87ae-116">最初にメッセージを送信したときに、クライアントアプリケーションはこれらのプロパティを**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) の値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c87ae-116">At first submission of the message, the client application should set these properties to the value of **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)).</span></span> <span data-ttu-id="c87ae-117">メッセージが転送または返信されるときには変更されません。</span><span class="sxs-lookup"><span data-stu-id="c87ae-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="c87ae-118">元の作成者のプロパティを使用すると、ローカルのメッセージングドメインの外部にある情報を保持できます。</span><span class="sxs-lookup"><span data-stu-id="c87ae-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="c87ae-119">インターネットからなど、他のメッセージングドメインからメッセージが到着すると、これらのプロパティを使用して元の情報が失われないようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="c87ae-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c87ae-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c87ae-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c87ae-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c87ae-121">Protocol specifications</span></span>

<span data-ttu-id="c87ae-122">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c87ae-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c87ae-123">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="c87ae-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c87ae-124">[[OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c87ae-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c87ae-125">IETF RFC2445、RFC2446、RFC2447、予定および会議の各オブジェクトを変換します。</span><span class="sxs-lookup"><span data-stu-id="c87ae-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c87ae-126">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="c87ae-126">Header files</span></span>

<span data-ttu-id="c87ae-127">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c87ae-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="c87ae-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c87ae-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="c87ae-129">Mapitags</span><span class="sxs-lookup"><span data-stu-id="c87ae-129">Mapitags.h</span></span>
  
> <span data-ttu-id="c87ae-130">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c87ae-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c87ae-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="c87ae-131">See also</span></span>



[<span data-ttu-id="c87ae-132">PidTagDisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c87ae-132">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="c87ae-133">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c87ae-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c87ae-134">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c87ae-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c87ae-135">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c87ae-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c87ae-136">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c87ae-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

