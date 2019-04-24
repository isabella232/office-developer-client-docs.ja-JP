---
title: PidTagOriginallyIntendedRecipAddrtype 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginallyIntendedRecipAddrtype
api_type:
- COM
ms.assetid: dcfb6bd5-bff5-4a50-aec7-4bdfdabf7631
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a826f1bdf150b42b61a61b2f53870e9f170e0777
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342596"
---
# <a name="pidtagoriginallyintendedrecipaddrtype-canonical-property"></a><span data-ttu-id="dfa94-103">PidTagOriginallyIntendedRecipAddrtype 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="dfa94-103">PidTagOriginallyIntendedRecipAddrtype Canonical Property</span></span>

  
  
<span data-ttu-id="dfa94-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dfa94-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dfa94-105">autoforwarded メッセージの最初に意図した受信者のアドレスの種類が含まれています。</span><span class="sxs-lookup"><span data-stu-id="dfa94-105">Contains the address type of the originally intended recipient of an autoforwarded message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dfa94-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="dfa94-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dfa94-107">PR_ORIGINALLY_INTENDED_RECIP_ADDRTYPE、PR_ORIGINALLY_INTENDED_RECIP_ADDRTYPE_A、PR_ORIGINALLY_INTENDED_RECIP_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="dfa94-107">PR_ORIGINALLY_INTENDED_RECIP_ADDRTYPE, PR_ORIGINALLY_INTENDED_RECIP_ADDRTYPE_A, PR_ORIGINALLY_INTENDED_RECIP_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="dfa94-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="dfa94-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dfa94-109">0x007b</span><span class="sxs-lookup"><span data-stu-id="dfa94-109">0x007B</span></span>  <br/> |
|<span data-ttu-id="dfa94-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="dfa94-110">Data type:</span></span>  <br/> |<span data-ttu-id="dfa94-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="dfa94-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="dfa94-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="dfa94-112">Area:</span></span>  <br/> |<span data-ttu-id="dfa94-113">サーバー</span><span class="sxs-lookup"><span data-stu-id="dfa94-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dfa94-114">解説</span><span class="sxs-lookup"><span data-stu-id="dfa94-114">Remarks</span></span>

<span data-ttu-id="dfa94-115">これらのプロパティは、最初に意図したメッセージ受信者のアドレスプロパティの1つです。</span><span class="sxs-lookup"><span data-stu-id="dfa94-115">These properties are one of the address properties for the originally intended message recipient.</span></span> <span data-ttu-id="dfa94-116">メッセージを転送した自動エージェントによって設定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="dfa94-116">It must be set by the automatic agent that has forwarded the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="dfa94-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="dfa94-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="dfa94-118">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="dfa94-118">Header files</span></span>

<span data-ttu-id="dfa94-119">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dfa94-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="dfa94-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="dfa94-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="dfa94-121">Mapitags</span><span class="sxs-lookup"><span data-stu-id="dfa94-121">Mapitags.h</span></span>
  
> <span data-ttu-id="dfa94-122">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="dfa94-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dfa94-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="dfa94-123">See also</span></span>



[<span data-ttu-id="dfa94-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="dfa94-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dfa94-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="dfa94-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dfa94-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="dfa94-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dfa94-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="dfa94-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

