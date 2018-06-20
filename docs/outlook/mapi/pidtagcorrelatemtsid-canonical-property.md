---
title: PidTagCorrelateMtsid の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 57da2d4c78914323b5dafa4f5ba5b7628d0e2f2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802653"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a><span data-ttu-id="5e09c-103">PidTagCorrelateMtsid の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="5e09c-103">PidTagCorrelateMtsid Canonical Property</span></span>

  
  
<span data-ttu-id="5e09c-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5e09c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5e09c-105">レポートを送信したメッセージに関連づけるために使用するメッセージ転送システム (MTS) 識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5e09c-105">Contains the message transfer system (MTS) identifier used in correlating reports with sent messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5e09c-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="5e09c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5e09c-107">PR_CORRELATE_MTSID</span><span class="sxs-lookup"><span data-stu-id="5e09c-107">PR_CORRELATE_MTSID</span></span>  <br/> |
|<span data-ttu-id="5e09c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="5e09c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5e09c-109">0x0E0D</span><span class="sxs-lookup"><span data-stu-id="5e09c-109">0x0E0D</span></span>  <br/> |
|<span data-ttu-id="5e09c-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="5e09c-110">Data type:</span></span>  <br/> |<span data-ttu-id="5e09c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5e09c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5e09c-112">領域:</span><span class="sxs-lookup"><span data-stu-id="5e09c-112">Area:</span></span>  <br/> |<span data-ttu-id="5e09c-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="5e09c-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5e09c-114">備考</span><span class="sxs-lookup"><span data-stu-id="5e09c-114">Remarks</span></span>

<span data-ttu-id="5e09c-115">トランスポート プロバイダーでは、TRUE にこのプロパティのセットを使用して発信されたメッセージが検出されると、そのメッセージの MTS 識別子をこのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="5e09c-115">When a transport provider encounters a submitted message with this property set to TRUE, it sets this property to the MTS identifier for that message.</span></span> <span data-ttu-id="5e09c-116">伝送においては、次の個人間メッセージ (IPM) の [送信済みアイテム フォルダー内のメッセージにこのプロパティが格納されます。</span><span class="sxs-lookup"><span data-stu-id="5e09c-116">Following transmission, this property is stored with the message in the interpersonal message (IPM) Sent Items folder.</span></span>
  
<span data-ttu-id="5e09c-117">X.400 など、MTS の id で関連付けをサポートしているメッセージング システムでは、元のメッセージとそれへの応答として生成されるすべてのレポートがトランスポート エンベロープの一部としての識別子を保持します。</span><span class="sxs-lookup"><span data-stu-id="5e09c-117">Messaging systems that support correlation by MTS identifier, such as X.400, retain the identifier as part of the transport envelope of the original message and also of any reports generated in response to it.</span></span> <span data-ttu-id="5e09c-118">レポートが配信されるとこのようなメッセージング システムから、トランスポート プロバイダーは、レポートのトランスポート エンベロープから MTS 識別子を元にこのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="5e09c-118">When a report is delivered from such a messaging system, the transport provider sets this property to the original MTS identifier from the report's transport envelope.</span></span> <span data-ttu-id="5e09c-119">このプロパティは、レポートと共に保存されます。</span><span class="sxs-lookup"><span data-stu-id="5e09c-119">This property is then stored with the report.</span></span>
  
<span data-ttu-id="5e09c-120">クライアント アプリケーションは、このプロパティを持つすべてのメッセージの検索結果のフォルダーを管理できます。</span><span class="sxs-lookup"><span data-stu-id="5e09c-120">A client application can maintain a search-results folder of all messages having this property.</span></span> <span data-ttu-id="5e09c-121">レポートは、このようなメッセージで、クライアントで検索結果フォルダーに制限を適用、メッセージの元のバージョンを検索し、新しい情報では、元のメッセージ情報を関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="5e09c-121">When a report comes in for such a message, the client can apply restrictions to the search-results folder, find the original version of the message, and correlate the original message information with the new information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5e09c-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5e09c-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5e09c-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5e09c-123">Header files</span></span>

<span data-ttu-id="5e09c-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5e09c-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="5e09c-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5e09c-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="5e09c-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5e09c-126">Mapitags.h</span></span>
  
> <span data-ttu-id="5e09c-127">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5e09c-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5e09c-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="5e09c-128">See also</span></span>



[<span data-ttu-id="5e09c-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5e09c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5e09c-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5e09c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5e09c-131">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="5e09c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5e09c-132">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="5e09c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

