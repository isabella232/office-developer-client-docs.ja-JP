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
ms.openlocfilehash: bbf09cb841c633b6f13ae12ec20e120ea3fd7ef7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803122"
---
# <a name="pidtagorigincheck-canonical-property"></a><span data-ttu-id="edb50-103">PidTagOriginCheck 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="edb50-103">PidTagOriginCheck Canonical Property</span></span>

  
  
<span data-ttu-id="edb50-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="edb50-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="edb50-105">配信レポートの受信者を元のメッセージの発生元を検証するを有効にするバイナリの検証値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="edb50-105">Contains a binary verification value that enables a delivery report recipient to verify the origin of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="edb50-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="edb50-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="edb50-107">PR_ORIGIN_CHECK</span><span class="sxs-lookup"><span data-stu-id="edb50-107">PR_ORIGIN_CHECK</span></span>  <br/> |
|<span data-ttu-id="edb50-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="edb50-108">Identifier:</span></span>  <br/> |<span data-ttu-id="edb50-109">0x0027</span><span class="sxs-lookup"><span data-stu-id="edb50-109">0x0027</span></span>  <br/> |
|<span data-ttu-id="edb50-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="edb50-110">Data type:</span></span>  <br/> |<span data-ttu-id="edb50-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="edb50-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="edb50-112">領域:</span><span class="sxs-lookup"><span data-stu-id="edb50-112">Area:</span></span>  <br/> |<span data-ttu-id="edb50-113">Server</span><span class="sxs-lookup"><span data-stu-id="edb50-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="edb50-114">注釈</span><span class="sxs-lookup"><span data-stu-id="edb50-114">Remarks</span></span>

<span data-ttu-id="edb50-115">このプロパティは、送信されたメッセージの送信元を確認するメッセージ転送エージェント (MTA) または配信レポートを受信するメッセージングのユーザーなどのサード パーティ製の手段を提供します。</span><span class="sxs-lookup"><span data-stu-id="edb50-115">This property provides a means for a third party, such as a message transfer agent (MTA) or a messaging user receiving a delivery report, to verify the submitted message's origin.</span></span> <span data-ttu-id="edb50-116">受信したメッセージに存在する場合、このプロパティは、メッセージへの応答として生成されるすべての配信レポートをコピーしてください。</span><span class="sxs-lookup"><span data-stu-id="edb50-116">If present on a received message, this property should be copied onto any delivery report generated in response to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="edb50-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="edb50-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="edb50-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="edb50-118">Header files</span></span>

<span data-ttu-id="edb50-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="edb50-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="edb50-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="edb50-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="edb50-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="edb50-121">Mapitags.h</span></span>
  
> <span data-ttu-id="edb50-122">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="edb50-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="edb50-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="edb50-123">See also</span></span>



[<span data-ttu-id="edb50-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="edb50-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="edb50-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="edb50-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="edb50-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="edb50-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="edb50-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="edb50-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

