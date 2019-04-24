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
ms.openlocfilehash: a172fa1e04f1ea50c29955febda47be6e52663b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360754"
---
# <a name="pidtagdistributionlistexpansionhistory-canonical-property"></a><span data-ttu-id="c1986-103">PidTagDistributionListExpansionHistory 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c1986-103">PidTagDistributionListExpansionHistory Canonical Property</span></span>

  
  
<span data-ttu-id="c1986-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1986-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1986-105">メッセージ送信中に配布リストが展開された方法を示す履歴が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c1986-105">Contains a history showing how a distribution list has been expanded during message transmission.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c1986-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c1986-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c1986-107">PR_DL_EXPANSION_HISTORY</span><span class="sxs-lookup"><span data-stu-id="c1986-107">PR_DL_EXPANSION_HISTORY</span></span>  <br/> |
|<span data-ttu-id="c1986-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c1986-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c1986-109">0x0013</span><span class="sxs-lookup"><span data-stu-id="c1986-109">0x0013</span></span>  <br/> |
|<span data-ttu-id="c1986-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c1986-110">Data type:</span></span>  <br/> |<span data-ttu-id="c1986-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c1986-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c1986-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="c1986-112">Area:</span></span>  <br/> |<span data-ttu-id="c1986-113">MAPI エンベロープ</span><span class="sxs-lookup"><span data-stu-id="c1986-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c1986-114">解説</span><span class="sxs-lookup"><span data-stu-id="c1986-114">Remarks</span></span>

<span data-ttu-id="c1986-115">このプロパティは、トランスポートプロバイダーが設定している場合は、クライアントアプリケーションを受信するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="c1986-115">This property is available to receiving client applications if the transport provider has set it.</span></span> <span data-ttu-id="c1986-116">また、メッセージの内容がレポートと共に返される場合は、送信側クライアントでも使用できます。</span><span class="sxs-lookup"><span data-stu-id="c1986-116">It is also available to the sending client if the message content is returned with a report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c1986-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c1986-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c1986-118">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="c1986-118">Header files</span></span>

<span data-ttu-id="c1986-119">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c1986-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="c1986-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c1986-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="c1986-121">Mapitags</span><span class="sxs-lookup"><span data-stu-id="c1986-121">Mapitags.h</span></span>
  
> <span data-ttu-id="c1986-122">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c1986-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c1986-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="c1986-123">See also</span></span>



[<span data-ttu-id="c1986-124">PidTagDistributionListExpansionProhibited 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c1986-124">PidTagDistributionListExpansionProhibited Canonical Property</span></span>](pidtagdistributionlistexpansionprohibited-canonical-property.md)


[<span data-ttu-id="c1986-125">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c1986-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c1986-126">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c1986-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c1986-127">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c1986-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c1986-128">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c1986-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

