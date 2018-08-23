---
title: PidTagOriginCheck 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginCheck
api_type:
- COM
ms.assetid: 27e0ab2f-b373-41ae-b922-2f45f9671ac6
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 27b967b885ef35c04d52699c289dd60248e9abd5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581084"
---
# <a name="pidtagorigincheck-canonical-property"></a><span data-ttu-id="5c7e2-103">PidTagOriginCheck 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5c7e2-103">PidTagOriginCheck Canonical Property</span></span>

  
  
<span data-ttu-id="5c7e2-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c7e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c7e2-105">配信レポートの受信者を元のメッセージの発生元を検証するを有効にするバイナリの検証値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5c7e2-105">Contains a binary verification value that enables a delivery report recipient to verify the origin of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5c7e2-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5c7e2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5c7e2-107">PR_ORIGIN_CHECK</span><span class="sxs-lookup"><span data-stu-id="5c7e2-107">PR_ORIGIN_CHECK</span></span>  <br/> |
|<span data-ttu-id="5c7e2-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="5c7e2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5c7e2-109">0x0027</span><span class="sxs-lookup"><span data-stu-id="5c7e2-109">0x0027</span></span>  <br/> |
|<span data-ttu-id="5c7e2-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5c7e2-110">Data type:</span></span>  <br/> |<span data-ttu-id="5c7e2-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5c7e2-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5c7e2-112">領域:</span><span class="sxs-lookup"><span data-stu-id="5c7e2-112">Area:</span></span>  <br/> |<span data-ttu-id="5c7e2-113">Server</span><span class="sxs-lookup"><span data-stu-id="5c7e2-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c7e2-114">注釈</span><span class="sxs-lookup"><span data-stu-id="5c7e2-114">Remarks</span></span>

<span data-ttu-id="5c7e2-115">このプロパティは、送信されたメッセージの送信元を確認するメッセージ転送エージェント (MTA) または配信レポートを受信するメッセージングのユーザーなどのサード パーティ製の手段を提供します。</span><span class="sxs-lookup"><span data-stu-id="5c7e2-115">This property provides a means for a third party, such as a message transfer agent (MTA) or a messaging user receiving a delivery report, to verify the submitted message's origin.</span></span> <span data-ttu-id="5c7e2-116">受信したメッセージに存在する場合、このプロパティは、メッセージへの応答として生成されるすべての配信レポートをコピーしてください。</span><span class="sxs-lookup"><span data-stu-id="5c7e2-116">If present on a received message, this property should be copied onto any delivery report generated in response to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5c7e2-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5c7e2-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5c7e2-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5c7e2-118">Header files</span></span>

<span data-ttu-id="5c7e2-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5c7e2-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="5c7e2-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5c7e2-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="5c7e2-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5c7e2-121">Mapitags.h</span></span>
  
> <span data-ttu-id="5c7e2-122">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5c7e2-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5c7e2-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="5c7e2-123">See also</span></span>



[<span data-ttu-id="5c7e2-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5c7e2-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5c7e2-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5c7e2-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5c7e2-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5c7e2-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5c7e2-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5c7e2-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

