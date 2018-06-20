---
title: PidTagOriginalAuthorEmailAddress の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1954e1760fead9cbe13f0f2394f8095cab7f26ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803058"
---
# <a name="pidtagoriginalauthoremailaddress-canonical-property"></a><span data-ttu-id="8828a-103">PidTagOriginalAuthorEmailAddress の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="8828a-103">PidTagOriginalAuthorEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="8828a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8828a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8828a-105">転送または返信する前にメッセージは、メッセージの最初のバージョンの作成者の電子メール アドレスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8828a-105">Contains the email address of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8828a-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="8828a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8828a-107">PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS、PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_A、PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="8828a-107">PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_A, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="8828a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8828a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8828a-109">0x007A</span><span class="sxs-lookup"><span data-stu-id="8828a-109">0x007A</span></span>  <br/> |
|<span data-ttu-id="8828a-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="8828a-110">Data type:</span></span>  <br/> |<span data-ttu-id="8828a-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8828a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8828a-112">領域:</span><span class="sxs-lookup"><span data-stu-id="8828a-112">Area:</span></span>  <br/> |<span data-ttu-id="8828a-113">Server</span><span class="sxs-lookup"><span data-stu-id="8828a-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8828a-114">備考</span><span class="sxs-lookup"><span data-stu-id="8828a-114">Remarks</span></span>

<span data-ttu-id="8828a-115">これらのプロパティでは、メッセージの作成者のアドレスのプロパティの例を示します。</span><span class="sxs-lookup"><span data-stu-id="8828a-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="8828a-116">メッセージの最初の提出書類は、クライアント アプリケーションは、 **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) プロパティの値にこれらのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8828a-116">At first submission of the message, the client application should set these properties to the value of the **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="8828a-117">メッセージを転送または返信するときは変更されません。</span><span class="sxs-lookup"><span data-stu-id="8828a-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="8828a-118">ローカルのメッセージング ドメインの外部からの情報の保持の元の作成者プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="8828a-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="8828a-119">別のメッセージング ドメインからメッセージが到着するなど、インターネットからこれらのプロパティは、元の情報が失われていないことを確認する方法。</span><span class="sxs-lookup"><span data-stu-id="8828a-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8828a-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8828a-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8828a-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8828a-121">Header files</span></span>

<span data-ttu-id="8828a-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8828a-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="8828a-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8828a-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="8828a-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8828a-124">Mapitags.h</span></span>
  
> <span data-ttu-id="8828a-125">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8828a-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8828a-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="8828a-126">See also</span></span>



[<span data-ttu-id="8828a-127">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8828a-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8828a-128">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8828a-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8828a-129">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="8828a-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8828a-130">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="8828a-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

