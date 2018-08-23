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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 468cda97398bc393b1c0a65e2c13df5ba3ade3aa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568911"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a><span data-ttu-id="81639-103">PidTagCorrelateMtsid 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="81639-103">PidTagCorrelateMtsid Canonical Property</span></span>

  
  
<span data-ttu-id="81639-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81639-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81639-105">レポートを送信したメッセージに関連づけるために使用するメッセージ転送システム (MTS) 識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="81639-105">Contains the message transfer system (MTS) identifier used in correlating reports with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="81639-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="81639-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="81639-107">PR_CORRELATE_MTSID</span><span class="sxs-lookup"><span data-stu-id="81639-107">PR_CORRELATE_MTSID</span></span>  <br/> |
|<span data-ttu-id="81639-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="81639-108">Identifier:</span></span>  <br/> |<span data-ttu-id="81639-109">0x0E0D</span><span class="sxs-lookup"><span data-stu-id="81639-109">0x0E0D</span></span>  <br/> |
|<span data-ttu-id="81639-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="81639-110">Data type:</span></span>  <br/> |<span data-ttu-id="81639-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="81639-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="81639-112">領域:</span><span class="sxs-lookup"><span data-stu-id="81639-112">Area:</span></span>  <br/> |<span data-ttu-id="81639-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="81639-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81639-114">注釈</span><span class="sxs-lookup"><span data-stu-id="81639-114">Remarks</span></span>

<span data-ttu-id="81639-115">トランスポート プロバイダーでは、TRUE にこのプロパティのセットを使用して発信されたメッセージが検出されると、そのメッセージの MTS 識別子をこのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="81639-115">When a transport provider encounters a submitted message with this property set to TRUE, it sets this property to the MTS identifier for that message.</span></span> <span data-ttu-id="81639-116">伝送においては、次の個人間メッセージ (IPM) の [送信済みアイテム フォルダー内のメッセージにこのプロパティが格納されます。</span><span class="sxs-lookup"><span data-stu-id="81639-116">Following transmission, this property is stored with the message in the interpersonal message (IPM) Sent Items folder.</span></span>
  
<span data-ttu-id="81639-117">X.400 など、MTS の id で関連付けをサポートしているメッセージング システムでは、元のメッセージとそれへの応答として生成されるすべてのレポートがトランスポート エンベロープの一部としての識別子を保持します。</span><span class="sxs-lookup"><span data-stu-id="81639-117">Messaging systems that support correlation by MTS identifier, such as X.400, retain the identifier as part of the transport envelope of the original message and also of any reports generated in response to it.</span></span> <span data-ttu-id="81639-118">レポートが配信されるとこのようなメッセージング システムから、トランスポート プロバイダーは、レポートのトランスポート エンベロープから MTS 識別子を元にこのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="81639-118">When a report is delivered from such a messaging system, the transport provider sets this property to the original MTS identifier from the report's transport envelope.</span></span> <span data-ttu-id="81639-119">このプロパティは、レポートと共に保存されます。</span><span class="sxs-lookup"><span data-stu-id="81639-119">This property is then stored with the report.</span></span>
  
<span data-ttu-id="81639-120">クライアント アプリケーションは、このプロパティを持つすべてのメッセージの検索結果のフォルダーを管理できます。</span><span class="sxs-lookup"><span data-stu-id="81639-120">A client application can maintain a search-results folder of all messages having this property.</span></span> <span data-ttu-id="81639-121">レポートは、このようなメッセージで、クライアントで検索結果フォルダーに制限を適用、メッセージの元のバージョンを検索し、新しい情報では、元のメッセージ情報を関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="81639-121">When a report comes in for such a message, the client can apply restrictions to the search-results folder, find the original version of the message, and correlate the original message information with the new information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="81639-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="81639-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="81639-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="81639-123">Header files</span></span>

<span data-ttu-id="81639-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="81639-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="81639-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="81639-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="81639-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="81639-126">Mapitags.h</span></span>
  
> <span data-ttu-id="81639-127">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="81639-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="81639-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="81639-128">See also</span></span>



[<span data-ttu-id="81639-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="81639-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="81639-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="81639-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="81639-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="81639-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="81639-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="81639-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

