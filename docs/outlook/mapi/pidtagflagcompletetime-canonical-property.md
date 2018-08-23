---
title: PidTagFlagCompleteTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFlagCompleteTime
api_type:
- HeaderDef
ms.assetid: effc738a-30f4-4a5e-b21d-04b50dad1f45
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6e1c2783abd186146fe738a3396e098711893d3a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583983"
---
# <a name="pidtagflagcompletetime-canonical-property"></a><span data-ttu-id="98126-103">PidTagFlagCompleteTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="98126-103">PidTagFlagCompleteTime Canonical Property</span></span>

  
  
<span data-ttu-id="98126-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98126-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98126-105">世界協定世界時 (UTC) メッセージ オブジェクトが完了したものとしてフラグが設定では、日付と時刻を指定します。</span><span class="sxs-lookup"><span data-stu-id="98126-105">Specifies the date and time in Coordinated Universal Time (UTC) that the message object was flagged as completed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="98126-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="98126-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="98126-107">PR_FLAG_COMPLETE_TIME</span><span class="sxs-lookup"><span data-stu-id="98126-107">PR_FLAG_COMPLETE_TIME</span></span>  <br/> |
|<span data-ttu-id="98126-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="98126-108">Identifier:</span></span>  <br/> |<span data-ttu-id="98126-109">0x1091</span><span class="sxs-lookup"><span data-stu-id="98126-109">0x1091</span></span>  <br/> |
|<span data-ttu-id="98126-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="98126-110">Data type:</span></span>  <br/> |<span data-ttu-id="98126-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="98126-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="98126-112">領域:</span><span class="sxs-lookup"><span data-stu-id="98126-112">Area:</span></span>  <br/> |<span data-ttu-id="98126-113">その他</span><span class="sxs-lookup"><span data-stu-id="98126-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98126-114">注釈</span><span class="sxs-lookup"><span data-stu-id="98126-114">Remarks</span></span>

<span data-ttu-id="98126-115">メッセージ オブジェクトが完全なフラグが設定されない場合、このプロパティは削除されます。</span><span class="sxs-lookup"><span data-stu-id="98126-115">This property is deleted if the message object is not flagged complete.</span></span> <span data-ttu-id="98126-116">時間の最小解像度は、(値は 600,000,000 の倍数である必要があります) の分である必要があります。</span><span class="sxs-lookup"><span data-stu-id="98126-116">The time's smallest resolution must be minutes (the value must be a multiple of 600,000,000).</span></span> <span data-ttu-id="98126-117">このプロパティは、オブジェクトでは、会議に関連するオブジェクトおよび task オブジェクト上に存在する必要がある場合に存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="98126-117">This property must not exist if the object is a meeting-related object, and it should not exist on a task object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="98126-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="98126-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="98126-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="98126-119">Protocol specifications</span></span>

<span data-ttu-id="98126-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98126-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98126-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="98126-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="98126-122">[[MS OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98126-122">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98126-123">プロパティ フラグに関連する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="98126-123">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="98126-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="98126-124">Header files</span></span>

<span data-ttu-id="98126-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="98126-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="98126-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="98126-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="98126-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="98126-127">Mapitags.h</span></span>
  
> <span data-ttu-id="98126-128">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="98126-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="98126-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="98126-129">See also</span></span>



[<span data-ttu-id="98126-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="98126-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="98126-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="98126-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="98126-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="98126-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="98126-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="98126-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

