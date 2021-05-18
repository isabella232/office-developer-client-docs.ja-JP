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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c52a1c055792f17477ff5540c4138160544e3b18
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321309"
---
# <a name="pidtagscheduleinfodelegatorwantscopy-canonical-property"></a><span data-ttu-id="a8b35-103">PidTagScheduleInfoDelegatorWantsCopy 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a8b35-103">PidTagScheduleInfoDelegatorWantsCopy Canonical Property</span></span>

  
  
<span data-ttu-id="a8b35-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8b35-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8b35-105">委任者が代理人に送信される会議関連オブジェクトのコピーを受信する場合は TRUE を含む。</span><span class="sxs-lookup"><span data-stu-id="a8b35-105">Contains TRUE if the delegator wants to receive copies of the meeting-related objects that are sent to the delegate.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a8b35-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a8b35-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a8b35-107">PR_SCHDINFO_BOSS_WANTS_COPY</span><span class="sxs-lookup"><span data-stu-id="a8b35-107">PR_SCHDINFO_BOSS_WANTS_COPY</span></span>  <br/> |
|<span data-ttu-id="a8b35-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a8b35-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a8b35-109">0x6842</span><span class="sxs-lookup"><span data-stu-id="a8b35-109">0x6842</span></span>  <br/> |
|<span data-ttu-id="a8b35-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a8b35-110">Data type:</span></span>  <br/> |<span data-ttu-id="a8b35-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="a8b35-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="a8b35-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="a8b35-112">Area:</span></span>  <br/> |<span data-ttu-id="a8b35-113">空き時間情報</span><span class="sxs-lookup"><span data-stu-id="a8b35-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a8b35-114">注釈</span><span class="sxs-lookup"><span data-stu-id="a8b35-114">Remarks</span></span>

<span data-ttu-id="a8b35-115">このプロパティは、デリゲート情報オブジェクトで設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a8b35-115">This property must be set in the delegate information object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a8b35-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a8b35-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a8b35-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a8b35-117">Protocol specifications</span></span>

<span data-ttu-id="a8b35-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a8b35-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a8b35-119">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="a8b35-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a8b35-120">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a8b35-120">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a8b35-121">メールボックスを代理人として接続および構成するためのメソッド、および他のユーザーの代理として動作するメッセージ オブジェクトと予定表オブジェクトとのやり取りを指定します。</span><span class="sxs-lookup"><span data-stu-id="a8b35-121">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="a8b35-122">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a8b35-122">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a8b35-123">ユーザーまたはリソースの可用性を公開します。</span><span class="sxs-lookup"><span data-stu-id="a8b35-123">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a8b35-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a8b35-124">Header files</span></span>

<span data-ttu-id="a8b35-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a8b35-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a8b35-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a8b35-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="a8b35-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a8b35-127">Mapitags.h</span></span>
  
> <span data-ttu-id="a8b35-128">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="a8b35-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a8b35-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="a8b35-129">See also</span></span>



[<span data-ttu-id="a8b35-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a8b35-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a8b35-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a8b35-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a8b35-132">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="a8b35-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a8b35-133">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="a8b35-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

