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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a82b1351c9d2d19c32e34b03a537a12bf93deb8a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435762"
---
# <a name="pidtagorigincheck-canonical-property"></a><span data-ttu-id="c9f9a-103">PidTagOriginCheck 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c9f9a-103">PidTagOriginCheck Canonical Property</span></span>

  
  
<span data-ttu-id="c9f9a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9f9a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9f9a-105">配信レポートの受信者が元のメッセージの配信元を確認できるバイナリ検証値を含む。</span><span class="sxs-lookup"><span data-stu-id="c9f9a-105">Contains a binary verification value that enables a delivery report recipient to verify the origin of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c9f9a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c9f9a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c9f9a-107">PR_ORIGIN_CHECK</span><span class="sxs-lookup"><span data-stu-id="c9f9a-107">PR_ORIGIN_CHECK</span></span>  <br/> |
|<span data-ttu-id="c9f9a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c9f9a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c9f9a-109">0x0027</span><span class="sxs-lookup"><span data-stu-id="c9f9a-109">0x0027</span></span>  <br/> |
|<span data-ttu-id="c9f9a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c9f9a-110">Data type:</span></span>  <br/> |<span data-ttu-id="c9f9a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c9f9a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c9f9a-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="c9f9a-112">Area:</span></span>  <br/> |<span data-ttu-id="c9f9a-113">Server</span><span class="sxs-lookup"><span data-stu-id="c9f9a-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9f9a-114">注釈</span><span class="sxs-lookup"><span data-stu-id="c9f9a-114">Remarks</span></span>

<span data-ttu-id="c9f9a-115">このプロパティは、送信されたメッセージの配信元を確認するために、メッセージ転送エージェント (MTA) や配信レポートを受信するメッセージング ユーザーなどのサード パーティに対して手段を提供します。</span><span class="sxs-lookup"><span data-stu-id="c9f9a-115">This property provides a means for a third party, such as a message transfer agent (MTA) or a messaging user receiving a delivery report, to verify the submitted message's origin.</span></span> <span data-ttu-id="c9f9a-116">受信したメッセージに存在する場合、このプロパティは、メッセージに応答して生成された配信レポートにコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9f9a-116">If present on a received message, this property should be copied onto any delivery report generated in response to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c9f9a-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c9f9a-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c9f9a-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c9f9a-118">Header files</span></span>

<span data-ttu-id="c9f9a-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c9f9a-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="c9f9a-120">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c9f9a-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="c9f9a-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c9f9a-121">Mapitags.h</span></span>
  
> <span data-ttu-id="c9f9a-122">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="c9f9a-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c9f9a-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="c9f9a-123">See also</span></span>



[<span data-ttu-id="c9f9a-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c9f9a-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c9f9a-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c9f9a-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c9f9a-126">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c9f9a-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c9f9a-127">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c9f9a-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

