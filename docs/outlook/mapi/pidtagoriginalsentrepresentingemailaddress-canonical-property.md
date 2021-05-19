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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2530e27993163505b28fa7d08fd5caf4cc9b03be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341189"
---
# <a name="pidtagoriginalsentrepresentingemailaddress-canonical-property"></a><span data-ttu-id="2dcb5-103">PidTagOriginalSentRepresentingEmailAddress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2dcb5-103">PidTagOriginalSentRepresentingEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="2dcb5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2dcb5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2dcb5-105">元のメッセージが送信されたメッセージング ユーザーの電子メール アドレスを格納します。</span><span class="sxs-lookup"><span data-stu-id="2dcb5-105">Contains the email address of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2dcb5-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2dcb5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2dcb5-107">PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS、PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS_A、PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="2dcb5-107">PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS, PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS_A, PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="2dcb5-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2dcb5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2dcb5-109">0x0069</span><span class="sxs-lookup"><span data-stu-id="2dcb5-109">0x0069</span></span>  <br/> |
|<span data-ttu-id="2dcb5-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2dcb5-110">Data type:</span></span>  <br/> |<span data-ttu-id="2dcb5-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2dcb5-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2dcb5-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="2dcb5-112">Area:</span></span>  <br/> |<span data-ttu-id="2dcb5-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="2dcb5-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2dcb5-114">注釈</span><span class="sxs-lookup"><span data-stu-id="2dcb5-114">Remarks</span></span>

<span data-ttu-id="2dcb5-115">これらのプロパティは、メッセージの元の送信者のアドレス プロパティの例です。</span><span class="sxs-lookup"><span data-stu-id="2dcb5-115">These properties are examples of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="2dcb5-116">会話スレッドで使用されます。</span><span class="sxs-lookup"><span data-stu-id="2dcb5-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="2dcb5-117">別のクライアントに代わってメッセージを送信するクライアント アプリケーションは、これらのプロパティをメッセージの最初の送信時に **PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md)) プロパティの値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2dcb5-117">A client application sending a message on behalf of another client should set these properties to the value of the **PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="2dcb5-118">一度設定した場合は、変更する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="2dcb5-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2dcb5-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2dcb5-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2dcb5-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="2dcb5-120">Protocol specifications</span></span>

<span data-ttu-id="2dcb5-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2dcb5-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2dcb5-122">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="2dcb5-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2dcb5-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2dcb5-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2dcb5-124">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="2dcb5-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2dcb5-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2dcb5-125">Header files</span></span>

<span data-ttu-id="2dcb5-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2dcb5-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="2dcb5-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2dcb5-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="2dcb5-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2dcb5-128">Mapitags.h</span></span>
  
> <span data-ttu-id="2dcb5-129">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="2dcb5-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2dcb5-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="2dcb5-130">See also</span></span>



[<span data-ttu-id="2dcb5-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="2dcb5-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2dcb5-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2dcb5-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2dcb5-133">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="2dcb5-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2dcb5-134">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="2dcb5-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

