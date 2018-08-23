---
title: PidTagOriginatorRequestedAlternateRecipient 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorRequestedAlternateRecipient
api_type:
- COM
ms.assetid: c85b7862-18bc-4e17-94db-9097e0ac4a02
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c7abd0ae93c5b38c756ec0915dda6a4cdfcebaa5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803124"
---
# <a name="pidtagoriginatorrequestedalternaterecipient-canonical-property"></a><span data-ttu-id="f1cff-103">PidTagOriginatorRequestedAlternateRecipient 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f1cff-103">PidTagOriginatorRequestedAlternateRecipient Canonical Property</span></span>

  
  
<span data-ttu-id="f1cff-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f1cff-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f1cff-105">送信者によって指定された代替受信者のエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f1cff-105">Contains an entry identifier for an alternate recipient designated by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f1cff-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f1cff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f1cff-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span><span class="sxs-lookup"><span data-stu-id="f1cff-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span></span>  <br/> |
|<span data-ttu-id="f1cff-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f1cff-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f1cff-109">0x0C09</span><span class="sxs-lookup"><span data-stu-id="f1cff-109">0x0C09</span></span>  <br/> |
|<span data-ttu-id="f1cff-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f1cff-110">Data type:</span></span>  <br/> |<span data-ttu-id="f1cff-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f1cff-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f1cff-112">領域:</span><span class="sxs-lookup"><span data-stu-id="f1cff-112">Area:</span></span>  <br/> |<span data-ttu-id="f1cff-113">MIME</span><span class="sxs-lookup"><span data-stu-id="f1cff-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f1cff-114">注釈</span><span class="sxs-lookup"><span data-stu-id="f1cff-114">Remarks</span></span>

<span data-ttu-id="f1cff-115">このプロパティは、自動転送されたメッセージで使用されます。</span><span class="sxs-lookup"><span data-stu-id="f1cff-115">This property is used in autoforwarded messages.</span></span> <span data-ttu-id="f1cff-116">自動転送が許可されていない場合、または別の受信者が指定されていない場合は、配信不能レポートを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f1cff-116">If autoforwarding is not permitted or if no alternate recipient has been designated, a nondelivery report should be generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f1cff-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f1cff-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f1cff-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f1cff-118">Header files</span></span>

<span data-ttu-id="f1cff-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f1cff-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="f1cff-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f1cff-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="f1cff-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f1cff-121">Mapitags.h</span></span>
  
> <span data-ttu-id="f1cff-122">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f1cff-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f1cff-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="f1cff-123">See also</span></span>



[<span data-ttu-id="f1cff-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f1cff-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f1cff-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f1cff-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f1cff-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f1cff-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f1cff-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f1cff-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

