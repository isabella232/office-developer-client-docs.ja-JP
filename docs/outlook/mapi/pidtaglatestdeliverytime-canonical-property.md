---
title: PidTagLatestDeliveryTime の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLatestDeliveryTime
api_type:
- HeaderDef
ms.assetid: 6c2e64bc-786e-4867-a504-46f4d1214337
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0cf25dc5a1182d019ea183f2c0714925f220aeb8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802933"
---
# <a name="pidtaglatestdeliverytime-canonical-property"></a><span data-ttu-id="20837-103">PidTagLatestDeliveryTime の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="20837-103">PidTagLatestDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="20837-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="20837-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="20837-105">最新の日付と時刻のメッセージ転送エージェント (MTA) がメッセージを配信する場合が含まれています。</span><span class="sxs-lookup"><span data-stu-id="20837-105">Contains the latest date and time when a message transfer agent (MTA) should deliver a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="20837-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="20837-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="20837-107">PR_LATEST_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="20837-107">PR_LATEST_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="20837-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="20837-108">Identifier:</span></span>  <br/> |<span data-ttu-id="20837-109">0x0019</span><span class="sxs-lookup"><span data-stu-id="20837-109">0x0019</span></span>  <br/> |
|<span data-ttu-id="20837-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="20837-110">Data type:</span></span>  <br/> |<span data-ttu-id="20837-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="20837-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="20837-112">領域:</span><span class="sxs-lookup"><span data-stu-id="20837-112">Area:</span></span>  <br/> |<span data-ttu-id="20837-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="20837-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="20837-114">備考</span><span class="sxs-lookup"><span data-stu-id="20837-114">Remarks</span></span>

<span data-ttu-id="20837-115">MTA は、このプロパティは、指定の時間でメッセージを配信することはできません、する場合は、メッセージを配信せずをキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="20837-115">If an MTA cannot deliver a message by the time this property specifies, it cancels the message without delivery.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="20837-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="20837-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="20837-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="20837-117">Header files</span></span>

<span data-ttu-id="20837-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="20837-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="20837-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="20837-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="20837-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="20837-120">Mapitags.h</span></span>
  
> <span data-ttu-id="20837-121">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="20837-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="20837-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="20837-122">See also</span></span>



[<span data-ttu-id="20837-123">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="20837-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="20837-124">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="20837-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="20837-125">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="20837-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="20837-126">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="20837-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

