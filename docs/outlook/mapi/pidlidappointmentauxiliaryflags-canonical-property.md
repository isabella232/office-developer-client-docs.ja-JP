---
title: PidLidAppointmentAuxiliaryFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentAuxiliaryFlags
api_type:
- COM
ms.assetid: 56c64e23-4a99-4f80-ba06-dfae2a5fe961
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4414ae866dece0654131d1575fe699676892709f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396835"
---
# <a name="pidlidappointmentauxiliaryflags-canonical-property"></a><span data-ttu-id="4371a-103">PidLidAppointmentAuxiliaryFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4371a-103">PidLidAppointmentAuxiliaryFlags Canonical Property</span></span>

  
  
<span data-ttu-id="4371a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4371a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4371a-105">補助オブジェクトの状態を示すビット フィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="4371a-105">Specifies a bit field that describes the auxiliary state of the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4371a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4371a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4371a-107">dispidApptAuxFlags</span><span class="sxs-lookup"><span data-stu-id="4371a-107">dispidApptAuxFlags</span></span>  <br/> |
|<span data-ttu-id="4371a-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="4371a-108">Property set:</span></span>  <br/> |<span data-ttu-id="4371a-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="4371a-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="4371a-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="4371a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4371a-111">0x00008207</span><span class="sxs-lookup"><span data-stu-id="4371a-111">0x00008207</span></span>  <br/> |
|<span data-ttu-id="4371a-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4371a-112">Data type:</span></span>  <br/> |<span data-ttu-id="4371a-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4371a-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4371a-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="4371a-114">Area:</span></span>  <br/> |<span data-ttu-id="4371a-115">会議</span><span class="sxs-lookup"><span data-stu-id="4371a-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4371a-116">備考</span><span class="sxs-lookup"><span data-stu-id="4371a-116">Remarks</span></span>

<span data-ttu-id="4371a-117">このプロパティが必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="4371a-117">This property is not required.</span></span> <span data-ttu-id="4371a-118">以下は、個々 のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="4371a-118">Below are the individual flags that can be set.</span></span>
  
<span data-ttu-id="4371a-119">C (auxApptFlagCopied、0x00000001)</span><span class="sxs-lookup"><span data-stu-id="4371a-119">C (auxApptFlagCopied, 0x00000001)</span></span>
  
> <span data-ttu-id="4371a-120">このフラグは、カレンダー オブジェクトを別の予定表フォルダーからコピーすることを示します。</span><span class="sxs-lookup"><span data-stu-id="4371a-120">This flag indicates that the calendar object was copied from another calendar folder.</span></span>
    
<span data-ttu-id="4371a-121">R (auxApptFlagForceMtgResponse、0x00000002)</span><span class="sxs-lookup"><span data-stu-id="4371a-121">R (auxApptFlagForceMtgResponse, 0x00000002)</span></span>
  
> <span data-ttu-id="4371a-122">会議出席依頼には、このフラグは、そのクライアントまたはサーバーを送信会議の開催者に返信応答を選択した場合を示します。</span><span class="sxs-lookup"><span data-stu-id="4371a-122">This flag on a meeting request indicates that the client or server should send a meeting response back to the organizer when a response is chosen.</span></span>
    
<span data-ttu-id="4371a-123">F (auxApptFlagForwarded、0x00000004)</span><span class="sxs-lookup"><span data-stu-id="4371a-123">F (auxApptFlagForwarded, 0x00000004)</span></span>
  
> <span data-ttu-id="4371a-124">会議出席依頼には、このフラグは、(開催者による転送を含む) が転送されたことを示します、開催者からの招待状をしているのではなく。</span><span class="sxs-lookup"><span data-stu-id="4371a-124">This flag on a meeting request indicates that it was forwarded (including being forwarded by the organizer), rather than being an invitation from the organizer.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="4371a-125">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4371a-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4371a-126">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4371a-126">Protocol specifications</span></span>

<span data-ttu-id="4371a-127">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4371a-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4371a-128">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="4371a-128">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4371a-129">[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4371a-129">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4371a-130">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="4371a-130">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4371a-131">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4371a-131">Header files</span></span>

<span data-ttu-id="4371a-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4371a-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="4371a-133">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4371a-133">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4371a-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="4371a-134">See also</span></span>



[<span data-ttu-id="4371a-135">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4371a-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4371a-136">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4371a-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4371a-137">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4371a-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4371a-138">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4371a-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

