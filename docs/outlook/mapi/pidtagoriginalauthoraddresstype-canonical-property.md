---
title: PidTagOriginalAuthorAddressType 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 596e416624fb6f2bf1fdaef64c2179feb7787815
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356218"
---
# <a name="pidtagoriginalauthoraddresstype-canonical-property"></a><span data-ttu-id="3540e-103">PidTagOriginalAuthorAddressType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3540e-103">PidTagOriginalAuthorAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="3540e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3540e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3540e-105">メッセージの最初のバージョンの作成者のアドレスの種類 (つまり、転送または返信する前のメッセージ) を含みます。</span><span class="sxs-lookup"><span data-stu-id="3540e-105">Contains the address type of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3540e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="3540e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3540e-107">PR_ORIGINAL_AUTHOR_ADDRTYPE、PR_ORIGINAL_AUTHOR_ADDRTYPE_A、PR_ORIGINAL_AUTHOR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="3540e-107">PR_ORIGINAL_AUTHOR_ADDRTYPE, PR_ORIGINAL_AUTHOR_ADDRTYPE_A, PR_ORIGINAL_AUTHOR_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="3540e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="3540e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3540e-109">0x0079</span><span class="sxs-lookup"><span data-stu-id="3540e-109">0x0079</span></span>  <br/> |
|<span data-ttu-id="3540e-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="3540e-110">Data type:</span></span>  <br/> |<span data-ttu-id="3540e-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3540e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3540e-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="3540e-112">Area:</span></span>  <br/> |<span data-ttu-id="3540e-113">サーバー</span><span class="sxs-lookup"><span data-stu-id="3540e-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3540e-114">解説</span><span class="sxs-lookup"><span data-stu-id="3540e-114">Remarks</span></span>

<span data-ttu-id="3540e-115">これらのプロパティは、メッセージの作成者のアドレスプロパティの例です。</span><span class="sxs-lookup"><span data-stu-id="3540e-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="3540e-116">クライアントアプリケーションでは、最初にメッセージを送信するときに、このプロパティを**PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) プロパティの値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3540e-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) property.</span></span> <span data-ttu-id="3540e-117">メッセージが転送または返信されるときには変更されません。</span><span class="sxs-lookup"><span data-stu-id="3540e-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="3540e-118">元の作成者のプロパティを使用すると、ローカルのメッセージングドメインの外部にある情報を保持できます。</span><span class="sxs-lookup"><span data-stu-id="3540e-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="3540e-119">インターネットからなど、他のメッセージングドメインからメッセージが到着すると、これらのプロパティを使用して元の情報が失われないようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="3540e-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3540e-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3540e-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="3540e-121">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="3540e-121">Header files</span></span>

<span data-ttu-id="3540e-122">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3540e-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="3540e-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3540e-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="3540e-124">Mapitags</span><span class="sxs-lookup"><span data-stu-id="3540e-124">Mapitags.h</span></span>
  
> <span data-ttu-id="3540e-125">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3540e-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3540e-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="3540e-126">See also</span></span>



[<span data-ttu-id="3540e-127">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="3540e-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3540e-128">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3540e-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3540e-129">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="3540e-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3540e-130">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="3540e-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

