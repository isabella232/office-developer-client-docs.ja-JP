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
ms.openlocfilehash: 0ba27e1eefa85e1651dbd24fa0540f8b1108588a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588469"
---
# <a name="pidtagdistributionlistexpansionhistory-canonical-property"></a><span data-ttu-id="bc875-103">PidTagDistributionListExpansionHistory 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bc875-103">PidTagDistributionListExpansionHistory Canonical Property</span></span>

  
  
<span data-ttu-id="bc875-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc875-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc875-105">メッセージの転送中に配布リストが展開されたかを示す履歴が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bc875-105">Contains a history showing how a distribution list has been expanded during message transmission.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bc875-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="bc875-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bc875-107">PR_DL_EXPANSION_HISTORY</span><span class="sxs-lookup"><span data-stu-id="bc875-107">PR_DL_EXPANSION_HISTORY</span></span>  <br/> |
|<span data-ttu-id="bc875-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="bc875-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bc875-109">0x0013</span><span class="sxs-lookup"><span data-stu-id="bc875-109">0x0013</span></span>  <br/> |
|<span data-ttu-id="bc875-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="bc875-110">Data type:</span></span>  <br/> |<span data-ttu-id="bc875-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bc875-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bc875-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="bc875-112">Area:</span></span>  <br/> |<span data-ttu-id="bc875-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="bc875-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bc875-114">注釈</span><span class="sxs-lookup"><span data-stu-id="bc875-114">Remarks</span></span>

<span data-ttu-id="bc875-115">このプロパティは、トランスポート プロバイダーが設定されている場合、クライアント アプリケーションを受信するのには使用可能です。</span><span class="sxs-lookup"><span data-stu-id="bc875-115">This property is available to receiving client applications if the transport provider has set it.</span></span> <span data-ttu-id="bc875-116">レポートで、メッセージの内容が返された場合は送信側のクライアントで利用できるも。</span><span class="sxs-lookup"><span data-stu-id="bc875-116">It is also available to the sending client if the message content is returned with a report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bc875-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bc875-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="bc875-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="bc875-118">Header files</span></span>

<span data-ttu-id="bc875-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bc875-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="bc875-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bc875-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="bc875-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bc875-121">Mapitags.h</span></span>
  
> <span data-ttu-id="bc875-122">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bc875-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bc875-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="bc875-123">See also</span></span>



[<span data-ttu-id="bc875-124">PidTagDistributionListExpansionProhibited 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bc875-124">PidTagDistributionListExpansionProhibited Canonical Property</span></span>](pidtagdistributionlistexpansionprohibited-canonical-property.md)


[<span data-ttu-id="bc875-125">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bc875-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bc875-126">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bc875-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bc875-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="bc875-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bc875-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="bc875-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

