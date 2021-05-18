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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4a0e7325618a38addefe562c8207066dfea620f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411373"
---
# <a name="pidtagoriginallyintendedrecipemailaddress-canonical-property"></a><span data-ttu-id="11d35-103">PidTagOriginallyIntendedRecipEmailAddress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="11d35-103">PidTagOriginallyIntendedRecipEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="11d35-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11d35-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11d35-105">自動送信されたメッセージの最初に意図した受信者の電子メール アドレスを格納します。</span><span class="sxs-lookup"><span data-stu-id="11d35-105">Contains the email address of the originally intended recipient of an autoforwarded message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="11d35-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="11d35-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="11d35-107">PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS、PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A、PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="11d35-107">PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="11d35-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="11d35-108">Identifier:</span></span>  <br/> |<span data-ttu-id="11d35-109">0x007C</span><span class="sxs-lookup"><span data-stu-id="11d35-109">0x007C</span></span>  <br/> |
|<span data-ttu-id="11d35-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="11d35-110">Data type:</span></span>  <br/> |<span data-ttu-id="11d35-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="11d35-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="11d35-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="11d35-112">Area:</span></span>  <br/> |<span data-ttu-id="11d35-113">Server</span><span class="sxs-lookup"><span data-stu-id="11d35-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11d35-114">注釈</span><span class="sxs-lookup"><span data-stu-id="11d35-114">Remarks</span></span>

<span data-ttu-id="11d35-115">これらのプロパティは、最初に意図したメッセージ受信者のアドレス プロパティの例です。</span><span class="sxs-lookup"><span data-stu-id="11d35-115">These properties are examples of the address properties for the originally intended message recipient.</span></span> <span data-ttu-id="11d35-116">メッセージを転送した自動エージェントによって設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="11d35-116">They must be set by the automatic agent that has forwarded the message.</span></span>
  
<span data-ttu-id="11d35-117">これらのプロパティは、受信者ごとの X.400 レポート属性に対応します。</span><span class="sxs-lookup"><span data-stu-id="11d35-117">These properties correspond to the X.400 report per-recipient attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="11d35-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="11d35-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="11d35-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="11d35-119">Header files</span></span>

<span data-ttu-id="11d35-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="11d35-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="11d35-121">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="11d35-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="11d35-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="11d35-122">Mapitags.h</span></span>
  
> <span data-ttu-id="11d35-123">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="11d35-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="11d35-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="11d35-124">See also</span></span>



[<span data-ttu-id="11d35-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="11d35-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="11d35-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="11d35-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="11d35-127">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="11d35-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="11d35-128">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="11d35-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

