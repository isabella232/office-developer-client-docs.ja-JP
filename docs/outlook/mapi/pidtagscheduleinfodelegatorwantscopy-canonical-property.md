---
title: PidTagScheduleInfoDelegatorWantsCopy 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDelegatorWantsCopy
api_type:
- COM
ms.assetid: 48e48e3a-1186-46c4-8ff9-34e03905fb93
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c37f5a3e2f1a5ec4411f2570d8a3fcdce52dfe57
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578648"
---
# <a name="pidtagscheduleinfodelegatorwantscopy-canonical-property"></a><span data-ttu-id="7a1fe-103">PidTagScheduleInfoDelegatorWantsCopy 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7a1fe-103">PidTagScheduleInfoDelegatorWantsCopy Canonical Property</span></span>

  
  
<span data-ttu-id="7a1fe-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a1fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a1fe-105">代理人が代理人に送信される会議に関連するオブジェクトのコピーを受信する必要がある場合、TRUE が格納されます。</span><span class="sxs-lookup"><span data-stu-id="7a1fe-105">Contains TRUE if the delegator wants to receive copies of the meeting-related objects that are sent to the delegate.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7a1fe-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7a1fe-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7a1fe-107">PR_SCHDINFO_BOSS_WANTS_COPY</span><span class="sxs-lookup"><span data-stu-id="7a1fe-107">PR_SCHDINFO_BOSS_WANTS_COPY</span></span>  <br/> |
|<span data-ttu-id="7a1fe-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7a1fe-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7a1fe-109">0x6842</span><span class="sxs-lookup"><span data-stu-id="7a1fe-109">0x6842</span></span>  <br/> |
|<span data-ttu-id="7a1fe-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7a1fe-110">Data type:</span></span>  <br/> |<span data-ttu-id="7a1fe-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="7a1fe-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="7a1fe-112">領域:</span><span class="sxs-lookup"><span data-stu-id="7a1fe-112">Area:</span></span>  <br/> |<span data-ttu-id="7a1fe-113">空き/予約済み</span><span class="sxs-lookup"><span data-stu-id="7a1fe-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a1fe-114">注釈</span><span class="sxs-lookup"><span data-stu-id="7a1fe-114">Remarks</span></span>

<span data-ttu-id="7a1fe-115">代理人の情報オブジェクトにこのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a1fe-115">This property must be set in the delegate information object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7a1fe-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7a1fe-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7a1fe-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7a1fe-117">Protocol specifications</span></span>

<span data-ttu-id="7a1fe-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7a1fe-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7a1fe-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="7a1fe-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7a1fe-120">[[MS OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7a1fe-120">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7a1fe-121">接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のオブジェクトとの対話としてメールボックスを構成するためのメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="7a1fe-121">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="7a1fe-122">[[MS OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7a1fe-122">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7a1fe-123">ユーザーまたはリソースの可用性を発行します。</span><span class="sxs-lookup"><span data-stu-id="7a1fe-123">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7a1fe-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7a1fe-124">Header files</span></span>

<span data-ttu-id="7a1fe-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7a1fe-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="7a1fe-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7a1fe-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="7a1fe-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7a1fe-127">Mapitags.h</span></span>
  
> <span data-ttu-id="7a1fe-128">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7a1fe-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7a1fe-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="7a1fe-129">See also</span></span>



[<span data-ttu-id="7a1fe-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7a1fe-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7a1fe-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7a1fe-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7a1fe-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7a1fe-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7a1fe-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7a1fe-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

