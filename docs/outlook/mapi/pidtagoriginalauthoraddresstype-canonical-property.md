---
title: PidTagOriginalAuthorAddressType の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorAddressType
api_type:
- COM
ms.assetid: 7cdedb1a-e441-469b-be50-2f18203eb30d
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: fb30f2b29691984614891e2345fe97abe6316f58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803044"
---
# <a name="pidtagoriginalauthoraddresstype-canonical-property"></a><span data-ttu-id="1a8e8-103">PidTagOriginalAuthorAddressType の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="1a8e8-103">PidTagOriginalAuthorAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="1a8e8-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1a8e8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1a8e8-105">転送または返信する前にメッセージは、メッセージの最初のバージョンの作成者のアドレスの種類が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1a8e8-105">Contains the address type of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1a8e8-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="1a8e8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1a8e8-107">PR_ORIGINAL_AUTHOR_ADDRTYPE、PR_ORIGINAL_AUTHOR_ADDRTYPE_A、PR_ORIGINAL_AUTHOR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="1a8e8-107">PR_ORIGINAL_AUTHOR_ADDRTYPE, PR_ORIGINAL_AUTHOR_ADDRTYPE_A, PR_ORIGINAL_AUTHOR_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="1a8e8-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1a8e8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1a8e8-109">0x0079</span><span class="sxs-lookup"><span data-stu-id="1a8e8-109">0x0079</span></span>  <br/> |
|<span data-ttu-id="1a8e8-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="1a8e8-110">Data type:</span></span>  <br/> |<span data-ttu-id="1a8e8-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1a8e8-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1a8e8-112">領域:</span><span class="sxs-lookup"><span data-stu-id="1a8e8-112">Area:</span></span>  <br/> |<span data-ttu-id="1a8e8-113">Server</span><span class="sxs-lookup"><span data-stu-id="1a8e8-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a8e8-114">備考</span><span class="sxs-lookup"><span data-stu-id="1a8e8-114">Remarks</span></span>

<span data-ttu-id="1a8e8-115">これらのプロパティでは、メッセージの作成者のアドレスのプロパティの例を示します。</span><span class="sxs-lookup"><span data-stu-id="1a8e8-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="1a8e8-116">メッセージの最初の提出書類は、クライアント アプリケーションは、 **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) プロパティの値にこのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a8e8-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) property.</span></span> <span data-ttu-id="1a8e8-117">メッセージを転送または返信するときは変更されません。</span><span class="sxs-lookup"><span data-stu-id="1a8e8-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="1a8e8-118">ローカルのメッセージング ドメインの外部からの情報の保持の元の作成者プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="1a8e8-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="1a8e8-119">別のメッセージング ドメインからメッセージが到着するなど、インターネットからこれらのプロパティは、元の情報が失われていないことを確認する方法。</span><span class="sxs-lookup"><span data-stu-id="1a8e8-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1a8e8-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1a8e8-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1a8e8-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1a8e8-121">Header files</span></span>

<span data-ttu-id="1a8e8-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1a8e8-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="1a8e8-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1a8e8-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="1a8e8-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1a8e8-124">Mapitags.h</span></span>
  
> <span data-ttu-id="1a8e8-125">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1a8e8-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1a8e8-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="1a8e8-126">See also</span></span>



[<span data-ttu-id="1a8e8-127">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1a8e8-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1a8e8-128">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1a8e8-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1a8e8-129">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="1a8e8-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1a8e8-130">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="1a8e8-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

