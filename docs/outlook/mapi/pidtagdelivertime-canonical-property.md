---
title: PidTagDeliverTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeliverTime
api_type:
- HeaderDef
ms.assetid: da0ad17b-08ac-4c50-ac1d-13062b890dfd
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 198e388f5cfb6ab0431e7b7a78b9a0be3d103597
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582120"
---
# <a name="pidtagdelivertime-canonical-property"></a><span data-ttu-id="a7f4f-103">PidTagDeliverTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a7f4f-103">PidTagDeliverTime Canonical Property</span></span>

  
  
<span data-ttu-id="a7f4f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7f4f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7f4f-105">元のメッセージが配信されたときの日時が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a7f4f-105">Contains the date and time when the original message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a7f4f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a7f4f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a7f4f-107">PR_DELIVER_TIME</span><span class="sxs-lookup"><span data-stu-id="a7f4f-107">PR_DELIVER_TIME</span></span>  <br/> |
|<span data-ttu-id="a7f4f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a7f4f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a7f4f-109">0x0010</span><span class="sxs-lookup"><span data-stu-id="a7f4f-109">0x0010</span></span>  <br/> |
|<span data-ttu-id="a7f4f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a7f4f-110">Data type:</span></span>  <br/> |<span data-ttu-id="a7f4f-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="a7f4f-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="a7f4f-112">領域:</span><span class="sxs-lookup"><span data-stu-id="a7f4f-112">Area:</span></span>  <br/> |<span data-ttu-id="a7f4f-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="a7f4f-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7f4f-114">注釈</span><span class="sxs-lookup"><span data-stu-id="a7f4f-114">Remarks</span></span>

<span data-ttu-id="a7f4f-115">このプロパティは、元のメッセージが配信レポートを生成しているメッセージング ユーザーに配信された時刻を示す配信レポートの受信者ごとのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="a7f4f-115">This property is a per-recipient property on a delivery report that indicates the time the original message was delivered to the messaging user for which the delivery report is being generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a7f4f-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a7f4f-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a7f4f-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a7f4f-117">Header files</span></span>

<span data-ttu-id="a7f4f-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a7f4f-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="a7f4f-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a7f4f-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="a7f4f-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a7f4f-120">Mapitags.h</span></span>
  
> <span data-ttu-id="a7f4f-121">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a7f4f-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a7f4f-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="a7f4f-122">See also</span></span>



[<span data-ttu-id="a7f4f-123">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="a7f4f-123">IMAPISupport::StatusRecips</span></span>](imapisupport-statusrecips.md)


[<span data-ttu-id="a7f4f-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a7f4f-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a7f4f-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a7f4f-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a7f4f-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a7f4f-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a7f4f-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a7f4f-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

