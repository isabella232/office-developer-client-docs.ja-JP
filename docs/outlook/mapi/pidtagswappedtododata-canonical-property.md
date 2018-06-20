---
title: PidTagSwappedToDoData の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: dedb60c5356e1dbb6d35f27372a09c152da0fed0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803621"
---
# <a name="pidtagswappedtododata-canonical-property"></a><span data-ttu-id="c978e-103">PidTagSwappedToDoData の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="c978e-103">PidTagSwappedToDoData Canonical Property</span></span>

  
  
<span data-ttu-id="c978e-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c978e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c978e-105">メッセージ オブジェクトのフラグが設定された状態に影響しないプロパティの値の 2 番目のセットを保持します。</span><span class="sxs-lookup"><span data-stu-id="c978e-105">Maintains a second set of property values that do not affect the flagged state of the Message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c978e-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="c978e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c978e-107">PR_SWAPPED_TODO_DATA</span><span class="sxs-lookup"><span data-stu-id="c978e-107">PR_SWAPPED_TODO_DATA</span></span>  <br/> |
|<span data-ttu-id="c978e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c978e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c978e-109">0x0E2D</span><span class="sxs-lookup"><span data-stu-id="c978e-109">0x0E2D</span></span>  <br/> |
|<span data-ttu-id="c978e-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="c978e-110">Data type:</span></span>  <br/> |<span data-ttu-id="c978e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c978e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c978e-112">領域:</span><span class="sxs-lookup"><span data-stu-id="c978e-112">Area:</span></span>  <br/> |<span data-ttu-id="c978e-113">MAPI 以外から送信できます。</span><span class="sxs-lookup"><span data-stu-id="c978e-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c978e-114">備考</span><span class="sxs-lookup"><span data-stu-id="c978e-114">Remarks</span></span>

<span data-ttu-id="c978e-115">フラグの送信者または送信者のアラームがサポートされている場合は、フラグをセカンダリ ・ ストレージの場所として機能している、この構造体はすべての送信者のフラグでサポートされている情報のフラグを設定するプロトコルに関連するプロパティとそのすべてを格納するための場所を提供します。送信者フラグまたはメッセージの受信者に送信者の通知情報を公開することがなく、送信者の通知でサポートされているアラームの設定のプロトコルに関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="c978e-115">Acting as the secondary flag storage location if sender flags or sender reminders are supported, this structure provides a location in which to store all of the properties relating to the Informational Flagging Protocol that are supported in sender flags, and all properties relating to the Reminder Settings Protocol that are supported in sender reminders without exposing the sender flag or sender reminder information to the recipients of a message.</span></span>
  
<span data-ttu-id="c978e-116">同様に、この構造体を提供するすべての受信者のフラグでサポートされている情報のフラグを設定するプロトコルに関連するプロパティおよび受信者でサポートされているアラームの設定のプロトコルに関連するプロパティを格納するための以前に送信されたメッセージで通知します。</span><span class="sxs-lookup"><span data-stu-id="c978e-116">Similarly, this structure provides a location in which to store all of the properties relating to the Informational Flagging Protocol that are supported in recipient flags and properties relating to the Reminder Settings Protocol that are supported in recipient reminders on a previously sent message.</span></span>
  
<span data-ttu-id="c978e-117">このプロパティの詳細については、 [[MS OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c978e-117">For more information about this property, see [[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c978e-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c978e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c978e-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c978e-119">Protocol specifications</span></span>

<span data-ttu-id="c978e-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c978e-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c978e-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="c978e-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c978e-122">[[MS OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c978e-122">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c978e-123">プロパティ フラグに関連する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c978e-123">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="c978e-124">[[MS OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c978e-124">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c978e-125">電子メールおよびその他のオブジェクトのアラームの操作モデルのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="c978e-125">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c978e-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c978e-126">Header files</span></span>

<span data-ttu-id="c978e-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c978e-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="c978e-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c978e-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="c978e-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c978e-129">Mapitags.h</span></span>
  
> <span data-ttu-id="c978e-130">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c978e-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c978e-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="c978e-131">See also</span></span>



[<span data-ttu-id="c978e-132">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c978e-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c978e-133">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c978e-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c978e-134">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="c978e-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c978e-135">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="c978e-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

