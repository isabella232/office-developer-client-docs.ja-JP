---
title: PidTagOriginalSentRepresentingEmailAddress 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: e2c3d2c3-5451-45cb-b0ec-bdbf5b39a0ba
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2530e27993163505b28fa7d08fd5caf4cc9b03be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341189"
---
# <a name="pidtagoriginalsentrepresentingemailaddress-canonical-property"></a><span data-ttu-id="7440a-103">PidTagOriginalSentRepresentingEmailAddress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7440a-103">PidTagOriginalSentRepresentingEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="7440a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7440a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7440a-105">元のメッセージが送信されたメッセージングユーザーの電子メールアドレスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7440a-105">Contains the email address of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7440a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7440a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7440a-107">PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS、PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS_A、PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="7440a-107">PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS, PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS_A, PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="7440a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7440a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7440a-109">0x0069</span><span class="sxs-lookup"><span data-stu-id="7440a-109">0x0069</span></span>  <br/> |
|<span data-ttu-id="7440a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7440a-110">Data type:</span></span>  <br/> |<span data-ttu-id="7440a-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7440a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7440a-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="7440a-112">Area:</span></span>  <br/> |<span data-ttu-id="7440a-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="7440a-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7440a-114">解説</span><span class="sxs-lookup"><span data-stu-id="7440a-114">Remarks</span></span>

<span data-ttu-id="7440a-115">これらのプロパティは、元のメッセージの送信者のアドレスプロパティの例です。</span><span class="sxs-lookup"><span data-stu-id="7440a-115">These properties are examples of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="7440a-116">会話スレッドで使用されます。</span><span class="sxs-lookup"><span data-stu-id="7440a-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="7440a-117">クライアントアプリケーションが別のクライアントの代わりにメッセージを送信する場合は、最初にメッセージを送信するときに、これらのプロパティを**PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md)) プロパティの値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7440a-117">A client application sending a message on behalf of another client should set these properties to the value of the **PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="7440a-118">一度設定すると、変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="7440a-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7440a-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7440a-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7440a-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7440a-120">Protocol specifications</span></span>

<span data-ttu-id="7440a-121">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7440a-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7440a-122">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="7440a-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7440a-123">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7440a-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7440a-124">電子メールメッセージオブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="7440a-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7440a-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="7440a-125">Header files</span></span>

<span data-ttu-id="7440a-126">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7440a-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="7440a-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7440a-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="7440a-128">Mapitags</span><span class="sxs-lookup"><span data-stu-id="7440a-128">Mapitags.h</span></span>
  
> <span data-ttu-id="7440a-129">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7440a-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7440a-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="7440a-130">See also</span></span>



[<span data-ttu-id="7440a-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="7440a-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7440a-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7440a-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7440a-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7440a-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7440a-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7440a-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

