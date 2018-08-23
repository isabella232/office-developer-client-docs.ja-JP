---
title: PidTagOriginallyIntendedRecipEmailAddress 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginallyIntendedRecipEmailAddress
api_type:
- COM
ms.assetid: 6a85b695-731a-4401-9c9c-fda6bc308558
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e24ae5f56a043d810eb805720606fd5b44d60cba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803068"
---
# <a name="pidtagoriginallyintendedrecipemailaddress-canonical-property"></a><span data-ttu-id="f0c90-103">PidTagOriginallyIntendedRecipEmailAddress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f0c90-103">PidTagOriginallyIntendedRecipEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="f0c90-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f0c90-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f0c90-105">自動転送されたメッセージの最初の目的の受信者の電子メール アドレスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f0c90-105">Contains the email address of the originally intended recipient of an autoforwarded message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f0c90-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f0c90-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f0c90-107">PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS、PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A、PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="f0c90-107">PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="f0c90-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f0c90-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f0c90-109">0x007C</span><span class="sxs-lookup"><span data-stu-id="f0c90-109">0x007C</span></span>  <br/> |
|<span data-ttu-id="f0c90-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f0c90-110">Data type:</span></span>  <br/> |<span data-ttu-id="f0c90-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f0c90-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f0c90-112">領域:</span><span class="sxs-lookup"><span data-stu-id="f0c90-112">Area:</span></span>  <br/> |<span data-ttu-id="f0c90-113">Server</span><span class="sxs-lookup"><span data-stu-id="f0c90-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f0c90-114">注釈</span><span class="sxs-lookup"><span data-stu-id="f0c90-114">Remarks</span></span>

<span data-ttu-id="f0c90-115">これらのプロパティでは、本来意図されているメッセージの受信者のアドレスのプロパティの例を示します。</span><span class="sxs-lookup"><span data-stu-id="f0c90-115">These properties are examples of the address properties for the originally intended message recipient.</span></span> <span data-ttu-id="f0c90-116">メッセージを転送するには自動エージェントが設定されなければなりません。</span><span class="sxs-lookup"><span data-stu-id="f0c90-116">They must be set by the automatic agent that has forwarded the message.</span></span>
  
<span data-ttu-id="f0c90-117">これらのプロパティは、レポートの X.400 受信者ごとの属性に対応します。</span><span class="sxs-lookup"><span data-stu-id="f0c90-117">These properties correspond to the X.400 report per-recipient attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f0c90-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f0c90-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f0c90-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f0c90-119">Header files</span></span>

<span data-ttu-id="f0c90-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f0c90-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="f0c90-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f0c90-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="f0c90-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f0c90-122">Mapitags.h</span></span>
  
> <span data-ttu-id="f0c90-123">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f0c90-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f0c90-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="f0c90-124">See also</span></span>



[<span data-ttu-id="f0c90-125">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f0c90-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f0c90-126">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f0c90-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f0c90-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f0c90-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f0c90-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f0c90-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

