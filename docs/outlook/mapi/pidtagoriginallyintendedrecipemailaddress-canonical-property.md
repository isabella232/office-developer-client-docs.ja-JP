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
ms.openlocfilehash: 4a0e7325618a38addefe562c8207066dfea620f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342543"
---
# <a name="pidtagoriginallyintendedrecipemailaddress-canonical-property"></a><span data-ttu-id="4c185-103">PidTagOriginallyIntendedRecipEmailAddress 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4c185-103">PidTagOriginallyIntendedRecipEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="4c185-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c185-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c185-105">autoforwarded メッセージの最初に意図した受信者の電子メールアドレスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4c185-105">Contains the email address of the originally intended recipient of an autoforwarded message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4c185-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4c185-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4c185-107">PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS、PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A、PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="4c185-107">PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="4c185-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="4c185-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4c185-109">0x007c</span><span class="sxs-lookup"><span data-stu-id="4c185-109">0x007C</span></span>  <br/> |
|<span data-ttu-id="4c185-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4c185-110">Data type:</span></span>  <br/> |<span data-ttu-id="4c185-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4c185-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4c185-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="4c185-112">Area:</span></span>  <br/> |<span data-ttu-id="4c185-113">サーバー</span><span class="sxs-lookup"><span data-stu-id="4c185-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c185-114">解説</span><span class="sxs-lookup"><span data-stu-id="4c185-114">Remarks</span></span>

<span data-ttu-id="4c185-115">これらのプロパティは、最初に意図したメッセージ受信者のアドレスプロパティの例です。</span><span class="sxs-lookup"><span data-stu-id="4c185-115">These properties are examples of the address properties for the originally intended message recipient.</span></span> <span data-ttu-id="4c185-116">これらは、メッセージを転送した自動エージェントによって設定される必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c185-116">They must be set by the automatic agent that has forwarded the message.</span></span>
  
<span data-ttu-id="4c185-117">これらのプロパティは、受信者ごとの-400 レポート属性に対応しています。</span><span class="sxs-lookup"><span data-stu-id="4c185-117">These properties correspond to the X.400 report per-recipient attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4c185-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4c185-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4c185-119">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="4c185-119">Header files</span></span>

<span data-ttu-id="4c185-120">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4c185-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="4c185-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4c185-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="4c185-122">Mapitags</span><span class="sxs-lookup"><span data-stu-id="4c185-122">Mapitags.h</span></span>
  
> <span data-ttu-id="4c185-123">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="4c185-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4c185-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="4c185-124">See also</span></span>



[<span data-ttu-id="4c185-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="4c185-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4c185-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4c185-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4c185-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4c185-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4c185-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4c185-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

