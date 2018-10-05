---
title: PidLidToDoOrdinalDate 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoOrdinalDate
api_type:
- COM
ms.assetid: b6a500fc-07f4-4788-ae46-d179a96a48e2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b0c5e3019efeeb0b9788d81e8730e976bfcc9d75
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401588"
---
# <a name="pidlidtodoordinaldate-canonical-property"></a><span data-ttu-id="1cc5c-103">PidLidToDoOrdinalDate 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1cc5c-103">PidLidToDoOrdinalDate Canonical Property</span></span>

  
  
<span data-ttu-id="1cc5c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1cc5c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1cc5c-105">統合の to do リスト内のオブジェクトの並べ替え順序を決定します。</span><span class="sxs-lookup"><span data-stu-id="1cc5c-105">Determines the sort order of objects in a consolidated to-do list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1cc5c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1cc5c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1cc5c-107">dispidToDoOrdinalDate</span><span class="sxs-lookup"><span data-stu-id="1cc5c-107">dispidToDoOrdinalDate</span></span>  <br/> |
|<span data-ttu-id="1cc5c-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="1cc5c-108">Property set:</span></span>  <br/> |<span data-ttu-id="1cc5c-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="1cc5c-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="1cc5c-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="1cc5c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1cc5c-111">0x000085A0</span><span class="sxs-lookup"><span data-stu-id="1cc5c-111">0x000085A0</span></span>  <br/> |
|<span data-ttu-id="1cc5c-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1cc5c-112">Data type:</span></span>  <br/> |<span data-ttu-id="1cc5c-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="1cc5c-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="1cc5c-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="1cc5c-114">Area:</span></span>  <br/> |<span data-ttu-id="1cc5c-115">タスク</span><span class="sxs-lookup"><span data-stu-id="1cc5c-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1cc5c-116">備考</span><span class="sxs-lookup"><span data-stu-id="1cc5c-116">Remarks</span></span>

<span data-ttu-id="1cc5c-117">オブジェクトのフラグを設定すると、現在の時刻を世界協定時刻 (UTC) でこのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1cc5c-117">When an object is flagged, this property should be set to the current time in Coordinated Universal Time (UTC).</span></span> 
  
<span data-ttu-id="1cc5c-118">Sor としてこのプロパティを使用する場合、適切な場所にタスクが表示されるようにこのプロパティの新しい値を決定するのに、適切なアルゴリズムを使用できるクライアントでは、ドラッグを使用して統合タスク ・ リストまたはその他の機構内のタスクの順序を変更するのにユーザーを許可している場合残ったフィールドです。</span><span class="sxs-lookup"><span data-stu-id="1cc5c-118">If the client allows a user to reorder tasks within the consolidated task list via dragging or other mechanisms, they can use any suitable algorithm to determine the new value of this property so that the task appears in the correct place when this property is used as a sorting field.</span></span>
  
<span data-ttu-id="1cc5c-119">オブジェクトと同数の並べ替えの結果を並べ替えるには、このプロパティを使用する場合、 **dispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) のプロパティは、リンク付けブレーカーとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="1cc5c-119">When this property is used to sort objects and the sort results in a tie, the **dispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) property is used as a tie breaker.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1cc5c-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1cc5c-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1cc5c-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1cc5c-121">Protocol specifications</span></span>

<span data-ttu-id="1cc5c-122">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1cc5c-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1cc5c-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="1cc5c-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1cc5c-124">[[MS OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1cc5c-124">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1cc5c-125">プロパティ フラグに関連する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="1cc5c-125">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1cc5c-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1cc5c-126">Header files</span></span>

<span data-ttu-id="1cc5c-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1cc5c-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="1cc5c-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1cc5c-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1cc5c-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="1cc5c-129">See also</span></span>



[<span data-ttu-id="1cc5c-130">PidLidToDoSubOrdinal 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1cc5c-130">PidLidToDoSubOrdinal Canonical Property</span></span>](pidlidtodosubordinal-canonical-property.md)


[<span data-ttu-id="1cc5c-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1cc5c-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1cc5c-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1cc5c-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1cc5c-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1cc5c-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1cc5c-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1cc5c-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

