---
title: PidTagDistributionListExpansionHistory 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDistributionListExpansionHistory
api_type:
- HeaderDef
ms.assetid: fc1e0162-d655-4761-92e7-b469579c270b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3989532388d9c88c293427a4ce7109579a832ad1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802712"
---
# <a name="pidtagdistributionlistexpansionhistory-canonical-property"></a><span data-ttu-id="0ffb8-103">PidTagDistributionListExpansionHistory 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0ffb8-103">PidTagDistributionListExpansionHistory Canonical Property</span></span>

  
  
<span data-ttu-id="0ffb8-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0ffb8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0ffb8-105">メッセージの転送中に配布リストが展開されたかを示す履歴が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0ffb8-105">Contains a history showing how a distribution list has been expanded during message transmission.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0ffb8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="0ffb8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0ffb8-107">PR_DL_EXPANSION_HISTORY</span><span class="sxs-lookup"><span data-stu-id="0ffb8-107">PR_DL_EXPANSION_HISTORY</span></span>  <br/> |
|<span data-ttu-id="0ffb8-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="0ffb8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0ffb8-109">0x0013</span><span class="sxs-lookup"><span data-stu-id="0ffb8-109">0x0013</span></span>  <br/> |
|<span data-ttu-id="0ffb8-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="0ffb8-110">Data type:</span></span>  <br/> |<span data-ttu-id="0ffb8-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0ffb8-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0ffb8-112">領域:</span><span class="sxs-lookup"><span data-stu-id="0ffb8-112">Area:</span></span>  <br/> |<span data-ttu-id="0ffb8-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="0ffb8-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0ffb8-114">注釈</span><span class="sxs-lookup"><span data-stu-id="0ffb8-114">Remarks</span></span>

<span data-ttu-id="0ffb8-115">このプロパティは、トランスポート プロバイダーが設定されている場合、クライアント アプリケーションを受信するのには使用可能です。</span><span class="sxs-lookup"><span data-stu-id="0ffb8-115">This property is available to receiving client applications if the transport provider has set it.</span></span> <span data-ttu-id="0ffb8-116">レポートで、メッセージの内容が返された場合は送信側のクライアントで利用できるも。</span><span class="sxs-lookup"><span data-stu-id="0ffb8-116">It is also available to the sending client if the message content is returned with a report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0ffb8-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0ffb8-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0ffb8-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="0ffb8-118">Header files</span></span>

<span data-ttu-id="0ffb8-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0ffb8-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="0ffb8-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0ffb8-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="0ffb8-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0ffb8-121">Mapitags.h</span></span>
  
> <span data-ttu-id="0ffb8-122">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0ffb8-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0ffb8-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="0ffb8-123">See also</span></span>



[<span data-ttu-id="0ffb8-124">PidTagDistributionListExpansionProhibited 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0ffb8-124">PidTagDistributionListExpansionProhibited Canonical Property</span></span>](pidtagdistributionlistexpansionprohibited-canonical-property.md)


[<span data-ttu-id="0ffb8-125">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0ffb8-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0ffb8-126">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0ffb8-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0ffb8-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0ffb8-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0ffb8-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0ffb8-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

