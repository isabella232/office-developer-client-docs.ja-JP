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
ms.openlocfilehash: 3e9318e396bf195ad701b92372a3136dee7fd0d8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357723"
---
# <a name="pidtagdelivertime-canonical-property"></a><span data-ttu-id="6aa2c-103">PidTagDeliverTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6aa2c-103">PidTagDeliverTime Canonical Property</span></span>

  
  
<span data-ttu-id="6aa2c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6aa2c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6aa2c-105">元のメッセージが配信された日付と時刻が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6aa2c-105">Contains the date and time when the original message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6aa2c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="6aa2c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6aa2c-107">PR_DELIVER_TIME</span><span class="sxs-lookup"><span data-stu-id="6aa2c-107">PR_DELIVER_TIME</span></span>  <br/> |
|<span data-ttu-id="6aa2c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="6aa2c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6aa2c-109">0x0010</span><span class="sxs-lookup"><span data-stu-id="6aa2c-109">0x0010</span></span>  <br/> |
|<span data-ttu-id="6aa2c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="6aa2c-110">Data type:</span></span>  <br/> |<span data-ttu-id="6aa2c-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="6aa2c-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="6aa2c-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="6aa2c-112">Area:</span></span>  <br/> |<span data-ttu-id="6aa2c-113">MAPI エンベロープ</span><span class="sxs-lookup"><span data-stu-id="6aa2c-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6aa2c-114">解説</span><span class="sxs-lookup"><span data-stu-id="6aa2c-114">Remarks</span></span>

<span data-ttu-id="6aa2c-115">このプロパティは、配信レポートが生成されるメッセージングユーザーに、元のメッセージが配信された時刻を示す配信レポートの受信者ごとのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="6aa2c-115">This property is a per-recipient property on a delivery report that indicates the time the original message was delivered to the messaging user for which the delivery report is being generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6aa2c-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6aa2c-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="6aa2c-117">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="6aa2c-117">Header files</span></span>

<span data-ttu-id="6aa2c-118">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6aa2c-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="6aa2c-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6aa2c-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="6aa2c-120">Mapitags</span><span class="sxs-lookup"><span data-stu-id="6aa2c-120">Mapitags.h</span></span>
  
> <span data-ttu-id="6aa2c-121">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6aa2c-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6aa2c-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="6aa2c-122">See also</span></span>



[<span data-ttu-id="6aa2c-123">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="6aa2c-123">IMAPISupport::StatusRecips</span></span>](imapisupport-statusrecips.md)


[<span data-ttu-id="6aa2c-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="6aa2c-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6aa2c-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6aa2c-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6aa2c-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6aa2c-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6aa2c-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6aa2c-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

