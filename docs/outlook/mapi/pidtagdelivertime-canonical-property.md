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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3e9318e396bf195ad701b92372a3136dee7fd0d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435279"
---
# <a name="pidtagdelivertime-canonical-property"></a><span data-ttu-id="b7adc-103">PidTagDeliverTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b7adc-103">PidTagDeliverTime Canonical Property</span></span>

  
  
<span data-ttu-id="b7adc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7adc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7adc-105">元のメッセージが配信された日付と時刻が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b7adc-105">Contains the date and time when the original message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b7adc-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b7adc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b7adc-107">PR_DELIVER_TIME</span><span class="sxs-lookup"><span data-stu-id="b7adc-107">PR_DELIVER_TIME</span></span>  <br/> |
|<span data-ttu-id="b7adc-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b7adc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b7adc-109">0x0010</span><span class="sxs-lookup"><span data-stu-id="b7adc-109">0x0010</span></span>  <br/> |
|<span data-ttu-id="b7adc-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b7adc-110">Data type:</span></span>  <br/> |<span data-ttu-id="b7adc-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="b7adc-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="b7adc-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="b7adc-112">Area:</span></span>  <br/> |<span data-ttu-id="b7adc-113">MAPI エンベロープ</span><span class="sxs-lookup"><span data-stu-id="b7adc-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7adc-114">注釈</span><span class="sxs-lookup"><span data-stu-id="b7adc-114">Remarks</span></span>

<span data-ttu-id="b7adc-115">このプロパティは、配信レポートが生成されるメッセージングユーザーに、元のメッセージが配信された時刻を示す配信レポートの受信者ごとのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="b7adc-115">This property is a per-recipient property on a delivery report that indicates the time the original message was delivered to the messaging user for which the delivery report is being generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b7adc-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b7adc-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b7adc-117">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="b7adc-117">Header files</span></span>

<span data-ttu-id="b7adc-118">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b7adc-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="b7adc-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b7adc-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="b7adc-120">Mapitags</span><span class="sxs-lookup"><span data-stu-id="b7adc-120">Mapitags.h</span></span>
  
> <span data-ttu-id="b7adc-121">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b7adc-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b7adc-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="b7adc-122">See also</span></span>



[<span data-ttu-id="b7adc-123">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="b7adc-123">IMAPISupport::StatusRecips</span></span>](imapisupport-statusrecips.md)


[<span data-ttu-id="b7adc-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="b7adc-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b7adc-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b7adc-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b7adc-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b7adc-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b7adc-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b7adc-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

