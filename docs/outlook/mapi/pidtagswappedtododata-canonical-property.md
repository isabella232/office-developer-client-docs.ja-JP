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
ms.openlocfilehash: 8086bc3ea35fdbb4e0f7758b7931e305259a3a9e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578669"
---
# <a name="pidtagswappedtododata-canonical-property"></a><span data-ttu-id="d0375-103">PidTagSwappedToDoData 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d0375-103">PidTagSwappedToDoData Canonical Property</span></span>

  
  
<span data-ttu-id="d0375-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0375-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0375-105">メッセージ オブジェクトのフラグが設定された状態に影響しないプロパティの値の 2 番目のセットを保持します。</span><span class="sxs-lookup"><span data-stu-id="d0375-105">Maintains a second set of property values that do not affect the flagged state of the Message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d0375-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d0375-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d0375-107">PR_SWAPPED_TODO_DATA</span><span class="sxs-lookup"><span data-stu-id="d0375-107">PR_SWAPPED_TODO_DATA</span></span>  <br/> |
|<span data-ttu-id="d0375-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d0375-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d0375-109">0x0E2D</span><span class="sxs-lookup"><span data-stu-id="d0375-109">0x0E2D</span></span>  <br/> |
|<span data-ttu-id="d0375-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d0375-110">Data type:</span></span>  <br/> |<span data-ttu-id="d0375-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d0375-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d0375-112">領域:</span><span class="sxs-lookup"><span data-stu-id="d0375-112">Area:</span></span>  <br/> |<span data-ttu-id="d0375-113">MAPI 以外から送信できます。</span><span class="sxs-lookup"><span data-stu-id="d0375-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0375-114">注釈</span><span class="sxs-lookup"><span data-stu-id="d0375-114">Remarks</span></span>

<span data-ttu-id="d0375-115">フラグの送信者または送信者のアラームがサポートされている場合は、フラグをセカンダリ ・ ストレージの場所として機能している、この構造体はすべての送信者のフラグでサポートされている情報のフラグを設定するプロトコルに関連するプロパティとそのすべてを格納するための場所を提供します。送信者フラグまたはメッセージの受信者に送信者の通知情報を公開することがなく、送信者の通知でサポートされているアラームの設定のプロトコルに関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="d0375-115">Acting as the secondary flag storage location if sender flags or sender reminders are supported, this structure provides a location in which to store all of the properties relating to the Informational Flagging Protocol that are supported in sender flags, and all properties relating to the Reminder Settings Protocol that are supported in sender reminders without exposing the sender flag or sender reminder information to the recipients of a message.</span></span>
  
<span data-ttu-id="d0375-116">同様に、この構造体を提供するすべての受信者のフラグでサポートされている情報のフラグを設定するプロトコルに関連するプロパティおよび受信者でサポートされているアラームの設定のプロトコルに関連するプロパティを格納するための以前に送信されたメッセージで通知します。</span><span class="sxs-lookup"><span data-stu-id="d0375-116">Similarly, this structure provides a location in which to store all of the properties relating to the Informational Flagging Protocol that are supported in recipient flags and properties relating to the Reminder Settings Protocol that are supported in recipient reminders on a previously sent message.</span></span>
  
<span data-ttu-id="d0375-117">このプロパティの詳細については、 [[MS OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d0375-117">For more information about this property, see [[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d0375-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d0375-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d0375-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d0375-119">Protocol specifications</span></span>

<span data-ttu-id="d0375-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d0375-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d0375-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="d0375-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d0375-122">[[MS OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d0375-122">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d0375-123">プロパティ フラグに関連する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d0375-123">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="d0375-124">[[MS OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d0375-124">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d0375-125">電子メールおよびその他のオブジェクトのアラームの操作モデルのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="d0375-125">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d0375-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d0375-126">Header files</span></span>

<span data-ttu-id="d0375-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d0375-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="d0375-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d0375-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="d0375-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d0375-129">Mapitags.h</span></span>
  
> <span data-ttu-id="d0375-130">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d0375-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d0375-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="d0375-131">See also</span></span>



[<span data-ttu-id="d0375-132">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d0375-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d0375-133">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d0375-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d0375-134">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d0375-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d0375-135">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d0375-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

