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
# <a name="pidtagcorrelatemtsid-canonical-property"></a><span data-ttu-id="48629-103">PidTagCorrelateMtsid 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="48629-103">PidTagCorrelateMtsid Canonical Property</span></span>

  
  
<span data-ttu-id="48629-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48629-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48629-105">送信されたメッセージにレポートを関連付けるために使用されるメッセージ転送システム (MTS) 識別子を含みます。</span><span class="sxs-lookup"><span data-stu-id="48629-105">Contains the message transfer system (MTS) identifier used in correlating reports with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="48629-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="48629-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="48629-107">PR_CORRELATE_MTSID</span><span class="sxs-lookup"><span data-stu-id="48629-107">PR_CORRELATE_MTSID</span></span>  <br/> |
|<span data-ttu-id="48629-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="48629-108">Identifier:</span></span>  <br/> |<span data-ttu-id="48629-109">0x0e0d</span><span class="sxs-lookup"><span data-stu-id="48629-109">0x0E0D</span></span>  <br/> |
|<span data-ttu-id="48629-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="48629-110">Data type:</span></span>  <br/> |<span data-ttu-id="48629-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="48629-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="48629-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="48629-112">Area:</span></span>  <br/> |<span data-ttu-id="48629-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="48629-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48629-114">注釈</span><span class="sxs-lookup"><span data-stu-id="48629-114">Remarks</span></span>

<span data-ttu-id="48629-115">このプロパティが TRUE に設定されている送信済みメッセージがトランスポートプロバイダーによって検出されると、そのメッセージの MTS 識別子にこのプロパティが設定されます。</span><span class="sxs-lookup"><span data-stu-id="48629-115">When a transport provider encounters a submitted message with this property set to TRUE, it sets this property to the MTS identifier for that message.</span></span> <span data-ttu-id="48629-116">送信後、このプロパティはメッセージと共に、IPM (個人間メッセージ) の送信済みアイテムフォルダーに格納されます。</span><span class="sxs-lookup"><span data-stu-id="48629-116">Following transmission, this property is stored with the message in the interpersonal message (IPM) Sent Items folder.</span></span>
  
<span data-ttu-id="48629-117">MTS 識別子による関連付けをサポートするメッセージングシステム (たとえば、X)。識別子は、元のメッセージのトランスポートエンベロープの一部として、また、それに対する応答で生成されたレポートの一部として保持されます。</span><span class="sxs-lookup"><span data-stu-id="48629-117">Messaging systems that support correlation by MTS identifier, such as X.400, retain the identifier as part of the transport envelope of the original message and also of any reports generated in response to it.</span></span> <span data-ttu-id="48629-118">このようなメッセージングシステムからレポートが配信されると、トランスポートプロバイダーは、このプロパティをレポートのトランスポートエンベロープから元の MTS 識別子に設定します。</span><span class="sxs-lookup"><span data-stu-id="48629-118">When a report is delivered from such a messaging system, the transport provider sets this property to the original MTS identifier from the report's transport envelope.</span></span> <span data-ttu-id="48629-119">その後、このプロパティはレポートと共に保存されます。</span><span class="sxs-lookup"><span data-stu-id="48629-119">This property is then stored with the report.</span></span>
  
<span data-ttu-id="48629-120">クライアントアプリケーションは、このプロパティを持つすべてのメッセージの検索結果フォルダーを維持できます。</span><span class="sxs-lookup"><span data-stu-id="48629-120">A client application can maintain a search-results folder of all messages having this property.</span></span> <span data-ttu-id="48629-121">このようなメッセージのレポートがある場合、クライアントは検索結果フォルダーに制限を適用し、元のバージョンのメッセージを検索し、元のメッセージ情報を新しい情報に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="48629-121">When a report comes in for such a message, the client can apply restrictions to the search-results folder, find the original version of the message, and correlate the original message information with the new information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="48629-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="48629-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="48629-123">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="48629-123">Header files</span></span>

<span data-ttu-id="48629-124">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="48629-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="48629-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="48629-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="48629-126">Mapitags</span><span class="sxs-lookup"><span data-stu-id="48629-126">Mapitags.h</span></span>
  
> <span data-ttu-id="48629-127">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="48629-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="48629-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="48629-128">See also</span></span>



[<span data-ttu-id="48629-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="48629-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="48629-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="48629-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="48629-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="48629-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="48629-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="48629-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

