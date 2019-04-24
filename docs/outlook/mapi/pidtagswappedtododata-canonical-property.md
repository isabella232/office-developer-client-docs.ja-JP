---
title: PidTagSwappedToDoData 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSwappedToDoData
api_type:
- COM
ms.assetid: d2a82fc8-de5d-4819-906e-b8314fd06ea0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3ecfa1e89688ae525a28e221424fb4a8194fc217
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359137"
---
# <a name="pidtagswappedtododata-canonical-property"></a><span data-ttu-id="0720c-103">PidTagSwappedToDoData 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0720c-103">PidTagSwappedToDoData Canonical Property</span></span>

  
  
<span data-ttu-id="0720c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0720c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0720c-105">Message オブジェクトのフラグ付き状態に影響しないプロパティ値の2番目のセットを保持します。</span><span class="sxs-lookup"><span data-stu-id="0720c-105">Maintains a second set of property values that do not affect the flagged state of the Message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0720c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="0720c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0720c-107">PR_SWAPPED_TODO_DATA</span><span class="sxs-lookup"><span data-stu-id="0720c-107">PR_SWAPPED_TODO_DATA</span></span>  <br/> |
|<span data-ttu-id="0720c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="0720c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0720c-109">0x0e2d</span><span class="sxs-lookup"><span data-stu-id="0720c-109">0x0E2D</span></span>  <br/> |
|<span data-ttu-id="0720c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="0720c-110">Data type:</span></span>  <br/> |<span data-ttu-id="0720c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0720c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0720c-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="0720c-112">Area:</span></span>  <br/> |<span data-ttu-id="0720c-113">MAPI ノンノンアウトテーブル</span><span class="sxs-lookup"><span data-stu-id="0720c-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0720c-114">解説</span><span class="sxs-lookup"><span data-stu-id="0720c-114">Remarks</span></span>

<span data-ttu-id="0720c-115">第2のフラグの格納場所として機能送信者フラグまたは送信者事前通知がサポートされている場合、この構造では、sender フラグでサポートされている情報フラグ設定プロトコルに関連するすべてのプロパティを格納する場所を提供します。送信者のフラグまたは送信者の事前通知情報をメッセージの受信者に公開せずに、送信者の事前通知でサポートされている、アラーム設定プロトコルに関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="0720c-115">Acting as the secondary flag storage location if sender flags or sender reminders are supported, this structure provides a location in which to store all of the properties relating to the Informational Flagging Protocol that are supported in sender flags, and all properties relating to the Reminder Settings Protocol that are supported in sender reminders without exposing the sender flag or sender reminder information to the recipients of a message.</span></span>
  
<span data-ttu-id="0720c-116">同様に、この構造体には、受信者フラグでサポートされている情報フラグ設定プロトコルに関連するすべてのプロパティと、受信者でサポートされているアラーム設定プロトコルに関連するプロパティが格納される場所があります。以前に送信されたメッセージのアラーム。</span><span class="sxs-lookup"><span data-stu-id="0720c-116">Similarly, this structure provides a location in which to store all of the properties relating to the Informational Flagging Protocol that are supported in recipient flags and properties relating to the Reminder Settings Protocol that are supported in recipient reminders on a previously sent message.</span></span>
  
<span data-ttu-id="0720c-117">このプロパティの詳細については、「 [[OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0720c-117">For more information about this property, see [[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0720c-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0720c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0720c-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="0720c-119">Protocol specifications</span></span>

<span data-ttu-id="0720c-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0720c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0720c-121">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="0720c-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0720c-122">[[OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0720c-122">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0720c-123">フラグに関連するプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="0720c-123">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="0720c-124">[[OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0720c-124">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0720c-125">電子メールおよびその他のオブジェクトの事前通知のプロパティと相互作用モデルを指定します。</span><span class="sxs-lookup"><span data-stu-id="0720c-125">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0720c-126">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="0720c-126">Header files</span></span>

<span data-ttu-id="0720c-127">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0720c-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="0720c-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0720c-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="0720c-129">Mapitags</span><span class="sxs-lookup"><span data-stu-id="0720c-129">Mapitags.h</span></span>
  
> <span data-ttu-id="0720c-130">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0720c-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0720c-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="0720c-131">See also</span></span>



[<span data-ttu-id="0720c-132">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="0720c-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0720c-133">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0720c-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0720c-134">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0720c-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0720c-135">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0720c-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

