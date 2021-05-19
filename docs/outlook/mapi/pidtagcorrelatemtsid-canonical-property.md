---
title: PidTagCorrelateMtsid 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCorrelateMtsid
api_type:
- HeaderDef
ms.assetid: d0fc4e91-ed90-4d27-bd23-f01e99728e2d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 96bfc184752b6a3e15434ad67ac8c2b4b26cac4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426836"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a><span data-ttu-id="d4e65-103">PidTagCorrelateMtsid 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d4e65-103">PidTagCorrelateMtsid Canonical Property</span></span>

  
  
<span data-ttu-id="d4e65-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4e65-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4e65-105">レポートと送信メッセージを関連付ける場合に使用されるメッセージ転送システム (MTS) 識別子が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d4e65-105">Contains the message transfer system (MTS) identifier used in correlating reports with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d4e65-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d4e65-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d4e65-107">PR_CORRELATE_MTSID</span><span class="sxs-lookup"><span data-stu-id="d4e65-107">PR_CORRELATE_MTSID</span></span>  <br/> |
|<span data-ttu-id="d4e65-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d4e65-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d4e65-109">0x0E0D</span><span class="sxs-lookup"><span data-stu-id="d4e65-109">0x0E0D</span></span>  <br/> |
|<span data-ttu-id="d4e65-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d4e65-110">Data type:</span></span>  <br/> |<span data-ttu-id="d4e65-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d4e65-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d4e65-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="d4e65-112">Area:</span></span>  <br/> |<span data-ttu-id="d4e65-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="d4e65-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4e65-114">注釈</span><span class="sxs-lookup"><span data-stu-id="d4e65-114">Remarks</span></span>

<span data-ttu-id="d4e65-115">トランスポート プロバイダーは、このプロパティが TRUE に設定された送信済みメッセージを検出すると、このプロパティをそのメッセージの MTS 識別子に設定します。</span><span class="sxs-lookup"><span data-stu-id="d4e65-115">When a transport provider encounters a submitted message with this property set to TRUE, it sets this property to the MTS identifier for that message.</span></span> <span data-ttu-id="d4e65-116">送信後、このプロパティは、メッセージと一緒に対人間メッセージ (IPM) 送信アイテム フォルダーに格納されます。</span><span class="sxs-lookup"><span data-stu-id="d4e65-116">Following transmission, this property is stored with the message in the interpersonal message (IPM) Sent Items folder.</span></span>
  
<span data-ttu-id="d4e65-117">X.400 などの MTS 識別子による相関関係をサポートするメッセージング システムは、元のメッセージのトランスポート エンベロープの一部として識別子を保持し、そのメッセージに応答して生成されたレポートも保持します。</span><span class="sxs-lookup"><span data-stu-id="d4e65-117">Messaging systems that support correlation by MTS identifier, such as X.400, retain the identifier as part of the transport envelope of the original message and also of any reports generated in response to it.</span></span> <span data-ttu-id="d4e65-118">このようなメッセージング システムからレポートが配信される場合、トランスポート プロバイダーは、このプロパティをレポートのトランスポート エンベロープから元の MTS 識別子に設定します。</span><span class="sxs-lookup"><span data-stu-id="d4e65-118">When a report is delivered from such a messaging system, the transport provider sets this property to the original MTS identifier from the report's transport envelope.</span></span> <span data-ttu-id="d4e65-119">このプロパティは、レポートと一緒に格納されます。</span><span class="sxs-lookup"><span data-stu-id="d4e65-119">This property is then stored with the report.</span></span>
  
<span data-ttu-id="d4e65-120">クライアント アプリケーションは、このプロパティを持つすべてのメッセージの検索結果フォルダーを維持できます。</span><span class="sxs-lookup"><span data-stu-id="d4e65-120">A client application can maintain a search-results folder of all messages having this property.</span></span> <span data-ttu-id="d4e65-121">このようなメッセージのレポートが表示される場合、クライアントは検索結果フォルダーに制限を適用し、元のバージョンのメッセージを見つけて、元のメッセージ情報と新しい情報を関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="d4e65-121">When a report comes in for such a message, the client can apply restrictions to the search-results folder, find the original version of the message, and correlate the original message information with the new information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d4e65-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d4e65-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d4e65-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d4e65-123">Header files</span></span>

<span data-ttu-id="d4e65-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d4e65-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="d4e65-125">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d4e65-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="d4e65-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d4e65-126">Mapitags.h</span></span>
  
> <span data-ttu-id="d4e65-127">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="d4e65-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d4e65-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="d4e65-128">See also</span></span>



[<span data-ttu-id="d4e65-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="d4e65-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d4e65-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d4e65-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d4e65-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d4e65-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d4e65-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d4e65-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

