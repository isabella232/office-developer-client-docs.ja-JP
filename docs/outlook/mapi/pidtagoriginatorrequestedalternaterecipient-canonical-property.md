---
title: PidTagOriginatorRequestedAlternateRecipient の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c7abd0ae93c5b38c756ec0915dda6a4cdfcebaa5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803124"
---
# <a name="pidtagoriginatorrequestedalternaterecipient-canonical-property"></a><span data-ttu-id="f1472-103">PidTagOriginatorRequestedAlternateRecipient の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="f1472-103">PidTagOriginatorRequestedAlternateRecipient Canonical Property</span></span>

  
  
<span data-ttu-id="f1472-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f1472-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f1472-105">送信者によって指定された代替受信者のエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f1472-105">Contains an entry identifier for an alternate recipient designated by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f1472-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="f1472-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f1472-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span><span class="sxs-lookup"><span data-stu-id="f1472-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span></span>  <br/> |
|<span data-ttu-id="f1472-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f1472-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f1472-109">0x0C09</span><span class="sxs-lookup"><span data-stu-id="f1472-109">0x0C09</span></span>  <br/> |
|<span data-ttu-id="f1472-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="f1472-110">Data type:</span></span>  <br/> |<span data-ttu-id="f1472-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f1472-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f1472-112">領域:</span><span class="sxs-lookup"><span data-stu-id="f1472-112">Area:</span></span>  <br/> |<span data-ttu-id="f1472-113">MIME</span><span class="sxs-lookup"><span data-stu-id="f1472-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f1472-114">備考</span><span class="sxs-lookup"><span data-stu-id="f1472-114">Remarks</span></span>

<span data-ttu-id="f1472-115">このプロパティは、自動転送されたメッセージで使用されます。</span><span class="sxs-lookup"><span data-stu-id="f1472-115">This property is used in autoforwarded messages.</span></span> <span data-ttu-id="f1472-116">自動転送が許可されていない場合、または別の受信者が指定されていない場合は、配信不能レポートを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f1472-116">If autoforwarding is not permitted or if no alternate recipient has been designated, a nondelivery report should be generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f1472-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f1472-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f1472-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f1472-118">Header files</span></span>

<span data-ttu-id="f1472-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f1472-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="f1472-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f1472-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="f1472-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f1472-121">Mapitags.h</span></span>
  
> <span data-ttu-id="f1472-122">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f1472-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f1472-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="f1472-123">See also</span></span>



[<span data-ttu-id="f1472-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f1472-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f1472-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f1472-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f1472-126">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="f1472-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f1472-127">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="f1472-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

