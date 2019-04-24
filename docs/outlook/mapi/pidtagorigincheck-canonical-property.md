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
ms.openlocfilehash: a82b1351c9d2d19c32e34b03a537a12bf93deb8a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335526"
---
# <a name="pidtagorigincheck-canonical-property"></a><span data-ttu-id="50c4e-103">PidTagOriginCheck 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="50c4e-103">PidTagOriginCheck Canonical Property</span></span>

  
  
<span data-ttu-id="50c4e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50c4e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50c4e-105">配信レポートの受信者が元のメッセージの送信元を確認できるようにするバイナリ検証値を格納します。</span><span class="sxs-lookup"><span data-stu-id="50c4e-105">Contains a binary verification value that enables a delivery report recipient to verify the origin of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="50c4e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="50c4e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="50c4e-107">PR_ORIGIN_CHECK</span><span class="sxs-lookup"><span data-stu-id="50c4e-107">PR_ORIGIN_CHECK</span></span>  <br/> |
|<span data-ttu-id="50c4e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="50c4e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="50c4e-109">0x0027</span><span class="sxs-lookup"><span data-stu-id="50c4e-109">0x0027</span></span>  <br/> |
|<span data-ttu-id="50c4e-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="50c4e-110">Data type:</span></span>  <br/> |<span data-ttu-id="50c4e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="50c4e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="50c4e-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="50c4e-112">Area:</span></span>  <br/> |<span data-ttu-id="50c4e-113">サーバー</span><span class="sxs-lookup"><span data-stu-id="50c4e-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50c4e-114">解説</span><span class="sxs-lookup"><span data-stu-id="50c4e-114">Remarks</span></span>

<span data-ttu-id="50c4e-115">このプロパティは、送信されたメッセージの送信元を確認するために、メッセージ転送エージェント (MTA)、または配信レポートを受信するメッセージングユーザーなどのサードパーティに対して、手段を提供します。</span><span class="sxs-lookup"><span data-stu-id="50c4e-115">This property provides a means for a third party, such as a message transfer agent (MTA) or a messaging user receiving a delivery report, to verify the submitted message's origin.</span></span> <span data-ttu-id="50c4e-116">受信したメッセージにこのプロパティがある場合は、メッセージへの応答として生成された配信レポートにこのプロパティをコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="50c4e-116">If present on a received message, this property should be copied onto any delivery report generated in response to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="50c4e-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="50c4e-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="50c4e-118">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="50c4e-118">Header files</span></span>

<span data-ttu-id="50c4e-119">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="50c4e-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="50c4e-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="50c4e-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="50c4e-121">Mapitags</span><span class="sxs-lookup"><span data-stu-id="50c4e-121">Mapitags.h</span></span>
  
> <span data-ttu-id="50c4e-122">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="50c4e-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="50c4e-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="50c4e-123">See also</span></span>



[<span data-ttu-id="50c4e-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="50c4e-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="50c4e-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="50c4e-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="50c4e-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="50c4e-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="50c4e-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="50c4e-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

