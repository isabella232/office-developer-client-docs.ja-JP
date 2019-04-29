---
title: PidTagOriginalAuthorEmailAddress 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorEmailAddress
api_type:
- COM
ms.assetid: 67cda756-ba71-4f29-a601-55359e44d93b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7918c5d5b585ffb199bfbc140edfb8286b499b40
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436168"
---
# <a name="pidtagoriginalauthoremailaddress-canonical-property"></a><span data-ttu-id="20dc7-103">PidTagOriginalAuthorEmailAddress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="20dc7-103">PidTagOriginalAuthorEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="20dc7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20dc7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20dc7-105">メッセージの最初のバージョンの作成者の電子メールアドレス、つまり転送または返信の前にメッセージを格納します。</span><span class="sxs-lookup"><span data-stu-id="20dc7-105">Contains the email address of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="20dc7-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="20dc7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="20dc7-107">PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS、PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_A、PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="20dc7-107">PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_A, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="20dc7-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="20dc7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="20dc7-109">0x007a</span><span class="sxs-lookup"><span data-stu-id="20dc7-109">0x007A</span></span>  <br/> |
|<span data-ttu-id="20dc7-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="20dc7-110">Data type:</span></span>  <br/> |<span data-ttu-id="20dc7-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="20dc7-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="20dc7-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="20dc7-112">Area:</span></span>  <br/> |<span data-ttu-id="20dc7-113">サーバー</span><span class="sxs-lookup"><span data-stu-id="20dc7-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="20dc7-114">注釈</span><span class="sxs-lookup"><span data-stu-id="20dc7-114">Remarks</span></span>

<span data-ttu-id="20dc7-115">これらのプロパティは、メッセージの作成者のアドレスプロパティの例です。</span><span class="sxs-lookup"><span data-stu-id="20dc7-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="20dc7-116">クライアントアプリケーションは、最初にメッセージを送信するときに、これらのプロパティを**PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) プロパティの値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="20dc7-116">At first submission of the message, the client application should set these properties to the value of the **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="20dc7-117">メッセージが転送または返信されるときには変更されません。</span><span class="sxs-lookup"><span data-stu-id="20dc7-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="20dc7-118">元の作成者のプロパティを使用すると、ローカルのメッセージングドメインの外部にある情報を保持できます。</span><span class="sxs-lookup"><span data-stu-id="20dc7-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="20dc7-119">インターネットからなど、他のメッセージングドメインからメッセージが到着すると、これらのプロパティを使用して元の情報が失われないようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="20dc7-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="20dc7-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="20dc7-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="20dc7-121">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="20dc7-121">Header files</span></span>

<span data-ttu-id="20dc7-122">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="20dc7-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="20dc7-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="20dc7-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="20dc7-124">Mapitags</span><span class="sxs-lookup"><span data-stu-id="20dc7-124">Mapitags.h</span></span>
  
> <span data-ttu-id="20dc7-125">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="20dc7-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="20dc7-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="20dc7-126">See also</span></span>



[<span data-ttu-id="20dc7-127">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="20dc7-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="20dc7-128">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="20dc7-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="20dc7-129">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="20dc7-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="20dc7-130">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="20dc7-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

