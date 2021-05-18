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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3ecfa1e89688ae525a28e221424fb4a8194fc217
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359137"
---
# <a name="pidtagswappedtododata-canonical-property"></a><span data-ttu-id="768ff-103">PidTagSwappedToDoData 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="768ff-103">PidTagSwappedToDoData Canonical Property</span></span>

  
  
<span data-ttu-id="768ff-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="768ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="768ff-105">Message オブジェクトのフラグ付き状態に影響しないプロパティ値の 2 番目のセットを保持します。</span><span class="sxs-lookup"><span data-stu-id="768ff-105">Maintains a second set of property values that do not affect the flagged state of the Message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="768ff-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="768ff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="768ff-107">PR_SWAPPED_TODO_DATA</span><span class="sxs-lookup"><span data-stu-id="768ff-107">PR_SWAPPED_TODO_DATA</span></span>  <br/> |
|<span data-ttu-id="768ff-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="768ff-108">Identifier:</span></span>  <br/> |<span data-ttu-id="768ff-109">0x0E2D</span><span class="sxs-lookup"><span data-stu-id="768ff-109">0x0E2D</span></span>  <br/> |
|<span data-ttu-id="768ff-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="768ff-110">Data type:</span></span>  <br/> |<span data-ttu-id="768ff-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="768ff-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="768ff-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="768ff-112">Area:</span></span>  <br/> |<span data-ttu-id="768ff-113">MAPI 送信不可</span><span class="sxs-lookup"><span data-stu-id="768ff-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="768ff-114">注釈</span><span class="sxs-lookup"><span data-stu-id="768ff-114">Remarks</span></span>

<span data-ttu-id="768ff-115">送信者フラグまたは送信者アラームがサポートされている場合、セカンダリ フラグの保存場所として機能するこの構造は、送信者フラグでサポートされている情報フラグ プロトコルに関連するすべてのプロパティ、および送信者のアラームでサポートされているアラーム 設定 プロトコルに関連するすべてのプロパティを、送信者フラグまたは送信者アラーム情報をメッセージの受信者に公開せずに保存する場所を提供します。</span><span class="sxs-lookup"><span data-stu-id="768ff-115">Acting as the secondary flag storage location if sender flags or sender reminders are supported, this structure provides a location in which to store all of the properties relating to the Informational Flagging Protocol that are supported in sender flags, and all properties relating to the Reminder Settings Protocol that are supported in sender reminders without exposing the sender flag or sender reminder information to the recipients of a message.</span></span>
  
<span data-ttu-id="768ff-116">同様に、この構造は、以前に送信されたメッセージの受信者アラームでサポートされているリマインダー 設定 プロトコルに関連する受信者フラグとプロパティでサポートされている Informational Flagging Protocol に関連するすべてのプロパティを格納する場所を提供します。</span><span class="sxs-lookup"><span data-stu-id="768ff-116">Similarly, this structure provides a location in which to store all of the properties relating to the Informational Flagging Protocol that are supported in recipient flags and properties relating to the Reminder Settings Protocol that are supported in recipient reminders on a previously sent message.</span></span>
  
<span data-ttu-id="768ff-117">このプロパティの詳細については [、「[MS-OXOFLAG] 」を参照してください](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="768ff-117">For more information about this property, see [[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="768ff-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="768ff-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="768ff-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="768ff-119">Protocol specifications</span></span>

<span data-ttu-id="768ff-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="768ff-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="768ff-121">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="768ff-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="768ff-122">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="768ff-122">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="768ff-123">フラグに関連するプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="768ff-123">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="768ff-124">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="768ff-124">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="768ff-125">メールなどのオブジェクトアラームのプロパティと対話モデルを指定します。</span><span class="sxs-lookup"><span data-stu-id="768ff-125">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="768ff-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="768ff-126">Header files</span></span>

<span data-ttu-id="768ff-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="768ff-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="768ff-128">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="768ff-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="768ff-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="768ff-129">Mapitags.h</span></span>
  
> <span data-ttu-id="768ff-130">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="768ff-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="768ff-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="768ff-131">See also</span></span>



[<span data-ttu-id="768ff-132">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="768ff-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="768ff-133">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="768ff-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="768ff-134">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="768ff-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="768ff-135">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="768ff-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

