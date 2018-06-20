---
title: PidTagOriginallyIntendedRecipEmailAddress の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e24ae5f56a043d810eb805720606fd5b44d60cba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803068"
---
# <a name="pidtagoriginallyintendedrecipemailaddress-canonical-property"></a><span data-ttu-id="03237-103">PidTagOriginallyIntendedRecipEmailAddress の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="03237-103">PidTagOriginallyIntendedRecipEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="03237-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="03237-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="03237-105">自動転送されたメッセージの最初の目的の受信者の電子メール アドレスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="03237-105">Contains the email address of the originally intended recipient of an autoforwarded message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="03237-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="03237-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="03237-107">PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS、PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A、PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="03237-107">PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="03237-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="03237-108">Identifier:</span></span>  <br/> |<span data-ttu-id="03237-109">0x007C</span><span class="sxs-lookup"><span data-stu-id="03237-109">0x007C</span></span>  <br/> |
|<span data-ttu-id="03237-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="03237-110">Data type:</span></span>  <br/> |<span data-ttu-id="03237-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="03237-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="03237-112">領域:</span><span class="sxs-lookup"><span data-stu-id="03237-112">Area:</span></span>  <br/> |<span data-ttu-id="03237-113">Server</span><span class="sxs-lookup"><span data-stu-id="03237-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03237-114">備考</span><span class="sxs-lookup"><span data-stu-id="03237-114">Remarks</span></span>

<span data-ttu-id="03237-115">これらのプロパティでは、本来意図されているメッセージの受信者のアドレスのプロパティの例を示します。</span><span class="sxs-lookup"><span data-stu-id="03237-115">These properties are examples of the address properties for the originally intended message recipient.</span></span> <span data-ttu-id="03237-116">メッセージを転送するには自動エージェントが設定されなければなりません。</span><span class="sxs-lookup"><span data-stu-id="03237-116">They must be set by the automatic agent that has forwarded the message.</span></span>
  
<span data-ttu-id="03237-117">これらのプロパティは、レポートの X.400 受信者ごとの属性に対応します。</span><span class="sxs-lookup"><span data-stu-id="03237-117">These properties correspond to the X.400 report per-recipient attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="03237-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="03237-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="03237-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="03237-119">Header files</span></span>

<span data-ttu-id="03237-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="03237-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="03237-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="03237-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="03237-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="03237-122">Mapitags.h</span></span>
  
> <span data-ttu-id="03237-123">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="03237-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="03237-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="03237-124">See also</span></span>



[<span data-ttu-id="03237-125">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="03237-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="03237-126">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="03237-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="03237-127">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="03237-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="03237-128">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="03237-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

