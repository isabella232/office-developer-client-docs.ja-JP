---
title: PidTagReplyRecipientNames 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReplyRecipientNames
api_type:
- COM
ms.assetid: f5ae6124-3e44-400f-95c2-24b19f3085b5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 02dcbcccd003fb0b53356da11a3b90b38e632c2a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355175"
---
# <a name="pidtagreplyrecipientnames-canonical-property"></a><span data-ttu-id="7b54c-103">PidTagReplyRecipientNames 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7b54c-103">PidTagReplyRecipientNames Canonical Property</span></span>

  
  
<span data-ttu-id="7b54c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b54c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b54c-105">応答を取得する受信者の表示名の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7b54c-105">Contains a list of display names for recipients that are to get a reply.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7b54c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7b54c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7b54c-107">PR_REPLY_RECIPIENT_NAMES、PR_REPLY_RECIPIENT_NAMES_A、PR_REPLY_RECIPIENT_NAMES_W</span><span class="sxs-lookup"><span data-stu-id="7b54c-107">PR_REPLY_RECIPIENT_NAMES, PR_REPLY_RECIPIENT_NAMES_A, PR_REPLY_RECIPIENT_NAMES_W</span></span>  <br/> |
|<span data-ttu-id="7b54c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7b54c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7b54c-109">0x0050</span><span class="sxs-lookup"><span data-stu-id="7b54c-109">0x0050</span></span>  <br/> |
|<span data-ttu-id="7b54c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7b54c-110">Data type:</span></span>  <br/> |<span data-ttu-id="7b54c-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7b54c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7b54c-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="7b54c-112">Area:</span></span>  <br/> |<span data-ttu-id="7b54c-113">MAPI エンベロープ</span><span class="sxs-lookup"><span data-stu-id="7b54c-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b54c-114">解説</span><span class="sxs-lookup"><span data-stu-id="7b54c-114">Remarks</span></span>

<span data-ttu-id="7b54c-115">これらのプロパティには、セミコロンで区切られた表示名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7b54c-115">These properties contain the display names separated by semicolons.</span></span>
  
<span data-ttu-id="7b54c-116">このプロパティが存在しない場合、返信は**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) プロパティによって識別されるユーザーにのみ送信されます。</span><span class="sxs-lookup"><span data-stu-id="7b54c-116">When this property is not present, a reply is sent only to the user identified by the **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) property.</span></span> <span data-ttu-id="7b54c-117">**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) とこれらのプロパティが定義されている場合、返信は、これら2つのプロパティによって識別されるすべての受信者に送信されます。</span><span class="sxs-lookup"><span data-stu-id="7b54c-117">When **PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) and these properties are defined, the reply is sent to all of the recipients identified by these two properties.</span></span> <span data-ttu-id="7b54c-118">トランスポートプロバイダーは、これらのプロパティを使用して、通常の応答ロジックを上書きします。</span><span class="sxs-lookup"><span data-stu-id="7b54c-118">A transport provider uses these properties to override the usual reply logic.</span></span>
  
<span data-ttu-id="7b54c-119">**PR_REPLY_RECIPIENT_ENTRIES**またはこれらのプロパティのいずれかが設定されている場合は、もう一方のプロパティも設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b54c-119">If either **PR_REPLY_RECIPIENT_ENTRIES** or these properties are set, the other property must be set also.</span></span> <span data-ttu-id="7b54c-120">これらのプロパティには、同じ数の受信者が含まれている必要があります。また、これらのプロパティは同じ順序で格納されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b54c-120">These properties must contain the same number of recipients, and they must contain them in the same order.</span></span> <span data-ttu-id="7b54c-121">これらの要件を遵守できないと、予期しない結果になることがあります。</span><span class="sxs-lookup"><span data-stu-id="7b54c-121">Failure to observe these requirements can cause unpredictable results.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7b54c-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7b54c-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7b54c-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7b54c-123">Protocol specifications</span></span>

<span data-ttu-id="7b54c-124">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b54c-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b54c-125">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="7b54c-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7b54c-126">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b54c-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b54c-127">電子メールメッセージに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="7b54c-127">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="7b54c-128">[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b54c-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b54c-129">インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="7b54c-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7b54c-130">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="7b54c-130">Header files</span></span>

<span data-ttu-id="7b54c-131">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7b54c-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="7b54c-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7b54c-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="7b54c-133">Mapitags</span><span class="sxs-lookup"><span data-stu-id="7b54c-133">Mapitags.h</span></span>
  
> <span data-ttu-id="7b54c-134">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7b54c-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7b54c-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="7b54c-135">See also</span></span>



[<span data-ttu-id="7b54c-136">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="7b54c-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7b54c-137">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7b54c-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7b54c-138">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7b54c-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7b54c-139">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7b54c-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

