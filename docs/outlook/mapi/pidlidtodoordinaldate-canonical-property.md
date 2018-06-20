---
title: PidLidToDoOrdinalDate の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d708424ccb15be15746fe8a33eea73a8e0f99323
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802253"
---
# <a name="pidlidtodoordinaldate-canonical-property"></a><span data-ttu-id="7587b-103">PidLidToDoOrdinalDate の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="7587b-103">PidLidToDoOrdinalDate Canonical Property</span></span>

  
  
<span data-ttu-id="7587b-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7587b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7587b-105">統合の to do リスト内のオブジェクトの並べ替え順序を決定します。</span><span class="sxs-lookup"><span data-stu-id="7587b-105">Determines the sort order of objects in a consolidated to-do list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7587b-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="7587b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7587b-107">dispidToDoOrdinalDate</span><span class="sxs-lookup"><span data-stu-id="7587b-107">dispidToDoOrdinalDate</span></span>  <br/> |
|<span data-ttu-id="7587b-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="7587b-108">Property set:</span></span>  <br/> |<span data-ttu-id="7587b-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="7587b-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="7587b-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="7587b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7587b-111">0x000085A0</span><span class="sxs-lookup"><span data-stu-id="7587b-111">0x000085A0</span></span>  <br/> |
|<span data-ttu-id="7587b-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="7587b-112">Data type:</span></span>  <br/> |<span data-ttu-id="7587b-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="7587b-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="7587b-114">領域:</span><span class="sxs-lookup"><span data-stu-id="7587b-114">Area:</span></span>  <br/> |<span data-ttu-id="7587b-115">タスク</span><span class="sxs-lookup"><span data-stu-id="7587b-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7587b-116">備考</span><span class="sxs-lookup"><span data-stu-id="7587b-116">Remarks</span></span>

<span data-ttu-id="7587b-117">オブジェクトのフラグを設定すると、現在の時刻を世界協定時刻 (UTC) でこのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7587b-117">When an object is flagged, this property should be set to the current time in Coordinated Universal Time (UTC).</span></span> 
  
<span data-ttu-id="7587b-118">Sor としてこのプロパティを使用する場合、適切な場所にタスクが表示されるようにこのプロパティの新しい値を決定するのに、適切なアルゴリズムを使用できるクライアントでは、ドラッグを使用して統合タスク ・ リストまたはその他の機構内のタスクの順序を変更するのにユーザーを許可している場合残ったフィールドです。</span><span class="sxs-lookup"><span data-stu-id="7587b-118">If the client allows a user to reorder tasks within the consolidated task list via dragging or other mechanisms, they can use any suitable algorithm to determine the new value of this property so that the task appears in the correct place when this property is used as a sorting field.</span></span>
  
<span data-ttu-id="7587b-119">オブジェクトと同数の並べ替えの結果を並べ替えるには、このプロパティを使用する場合、 **dispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) のプロパティは、リンク付けブレーカーとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="7587b-119">When this property is used to sort objects and the sort results in a tie, the **dispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) property is used as a tie breaker.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7587b-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7587b-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7587b-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7587b-121">Protocol specifications</span></span>

<span data-ttu-id="7587b-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7587b-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7587b-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="7587b-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7587b-124">[[MS OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7587b-124">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7587b-125">プロパティ フラグに関連する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="7587b-125">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7587b-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7587b-126">Header files</span></span>

<span data-ttu-id="7587b-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7587b-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="7587b-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7587b-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7587b-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="7587b-129">See also</span></span>



[<span data-ttu-id="7587b-130">PidLidToDoSubOrdinal の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="7587b-130">PidLidToDoSubOrdinal Canonical Property</span></span>](pidlidtodosubordinal-canonical-property.md)


[<span data-ttu-id="7587b-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7587b-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7587b-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7587b-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7587b-133">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="7587b-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7587b-134">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="7587b-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

