---
title: PidTagOriginalSenderEmailAddress 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderEmailAddress
api_type:
- COM
ms.assetid: cc86505c-e264-435f-ae21-4a10f0bbf082
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ed3d84667d7be9c06d0ddf4d896b8888694edc12
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355273"
---
# <a name="pidtagoriginalsenderemailaddress-canonical-property"></a><span data-ttu-id="14a31-103">PidTagOriginalSenderEmailAddress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="14a31-103">PidTagOriginalSenderEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="14a31-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="14a31-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="14a31-105">メッセージの最初のバージョンの送信者の電子メールアドレス、つまり転送または返信の前にメッセージを格納します。</span><span class="sxs-lookup"><span data-stu-id="14a31-105">Contains the email address of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="14a31-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="14a31-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="14a31-107">PR_ORIGINAL_SENDER_EMAIL_ADDRESS、PR_ORIGINAL_SENDER_EMAIL_ADDRESS_A、PR_ORIGINAL_SENDER_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="14a31-107">PR_ORIGINAL_SENDER_EMAIL_ADDRESS, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_A, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="14a31-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="14a31-108">Identifier:</span></span>  <br/> |<span data-ttu-id="14a31-109">0x0067</span><span class="sxs-lookup"><span data-stu-id="14a31-109">0x0067</span></span>  <br/> |
|<span data-ttu-id="14a31-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="14a31-110">Data type:</span></span>  <br/> |<span data-ttu-id="14a31-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="14a31-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="14a31-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="14a31-112">Area:</span></span>  <br/> |<span data-ttu-id="14a31-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="14a31-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="14a31-114">解説</span><span class="sxs-lookup"><span data-stu-id="14a31-114">Remarks</span></span>

<span data-ttu-id="14a31-115">これらのプロパティは、メッセージの元の送信者のアドレスプロパティの例です。</span><span class="sxs-lookup"><span data-stu-id="14a31-115">These properties are examples of the address properties for the original sender of a message.</span></span> <span data-ttu-id="14a31-116">クライアントアプリケーションでは、最初にメッセージを送信するときに、このプロパティを**PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) の値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="14a31-116">At first submission of the message, the client application should set this property to the value of **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)).</span></span> <span data-ttu-id="14a31-117">メッセージが転送または返信されるときには変更されません。</span><span class="sxs-lookup"><span data-stu-id="14a31-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="14a31-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="14a31-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="14a31-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="14a31-119">Protocol specifications</span></span>

<span data-ttu-id="14a31-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14a31-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14a31-121">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="14a31-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="14a31-122">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14a31-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14a31-123">電子メールメッセージオブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="14a31-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="14a31-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="14a31-124">Header files</span></span>

<span data-ttu-id="14a31-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="14a31-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="14a31-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="14a31-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="14a31-127">Mapitags</span><span class="sxs-lookup"><span data-stu-id="14a31-127">Mapitags.h</span></span>
  
> <span data-ttu-id="14a31-128">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="14a31-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="14a31-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="14a31-129">See also</span></span>



[<span data-ttu-id="14a31-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="14a31-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="14a31-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="14a31-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="14a31-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="14a31-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="14a31-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="14a31-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

