---
title: PidLidToDoSubOrdinal 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoSubOrdinal
api_type:
- COM
ms.assetid: e3bc15ef-155e-49fd-88e5-64713df9b939
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c4ea125a5bde89e0885be4c04e3f106f202b1e18
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344920"
---
# <a name="pidlidtodosubordinal-canonical-property"></a><span data-ttu-id="5afa3-103">PidLidToDoSubOrdinal 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5afa3-103">PidLidToDoSubOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="5afa3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5afa3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5afa3-105">**dispidToDoOrdinalDate** [(PidLidToDoOrdinalDate)](pidlidtodoordinaldate-canonical-property.md)プロパティがオブジェクトを並べ替え、その結果をタイに並べ替える場合、タイ ブレーカーとして機能します。</span><span class="sxs-lookup"><span data-stu-id="5afa3-105">Acts as a tie breaker when the **dispidToDoOrdinalDate** ([PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)) property sorts objects and the result in a tie.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5afa3-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5afa3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5afa3-107">dispidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="5afa3-107">dispidToDoSubOrdinal</span></span>  <br/> |
|<span data-ttu-id="5afa3-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="5afa3-108">Property set:</span></span>  <br/> |<span data-ttu-id="5afa3-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="5afa3-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="5afa3-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="5afa3-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5afa3-111">0x000085A1</span><span class="sxs-lookup"><span data-stu-id="5afa3-111">0x000085A1</span></span>  <br/> |
|<span data-ttu-id="5afa3-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5afa3-112">Data type:</span></span>  <br/> |<span data-ttu-id="5afa3-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5afa3-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5afa3-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="5afa3-114">Area:</span></span>  <br/> |<span data-ttu-id="5afa3-115">タスク</span><span class="sxs-lookup"><span data-stu-id="5afa3-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5afa3-116">注釈</span><span class="sxs-lookup"><span data-stu-id="5afa3-116">Remarks</span></span>

<span data-ttu-id="5afa3-117">使用する場合、このプロパティは辞書的に並べ替える必要があります。</span><span class="sxs-lookup"><span data-stu-id="5afa3-117">If used, this property must be sorted lexicographically.</span></span> <span data-ttu-id="5afa3-118">文字列のコンポーネント文字は、0 から 9 の数字で構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5afa3-118">The component characters of the string must consist of only the numerals zero through nine.</span></span> <span data-ttu-id="5afa3-119">このプロパティは、最初は "55555555" に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5afa3-119">This property should be initially set to "5555555".</span></span> <span data-ttu-id="5afa3-120">このプロパティの長さは、254 文字 (終端の NULL 文字を除く) を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="5afa3-120">The length of this property must not exceed 254 characters (excluding the terminating NULL character).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5afa3-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5afa3-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5afa3-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5afa3-122">Protocol specifications</span></span>

<span data-ttu-id="5afa3-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5afa3-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5afa3-124">プロパティ セットの定義と関連するプロトコル仕様への参照Exchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="5afa3-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5afa3-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5afa3-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5afa3-126">フラグに関連するプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="5afa3-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5afa3-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5afa3-127">Header files</span></span>

<span data-ttu-id="5afa3-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5afa3-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="5afa3-129">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5afa3-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5afa3-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="5afa3-130">See also</span></span>



[<span data-ttu-id="5afa3-131">PidLidToDoOrdinalDate 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5afa3-131">PidLidToDoOrdinalDate Canonical Property</span></span>](pidlidtodoordinaldate-canonical-property.md)


[<span data-ttu-id="5afa3-132">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="5afa3-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5afa3-133">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5afa3-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5afa3-134">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="5afa3-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5afa3-135">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="5afa3-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

