---
title: PidLidToDoSubOrdinal の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 9965ed059ba4596232111f5fbd86b9d177e3c3dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802251"
---
# <a name="pidlidtodosubordinal-canonical-property"></a><span data-ttu-id="ca59d-103">PidLidToDoSubOrdinal の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="ca59d-103">PidLidToDoSubOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="ca59d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ca59d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ca59d-105">**DispidToDoOrdinalDate** ([PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)) のプロパティがオブジェクトと同数の結果をソートするときは、リンク付けブレーカーとして機能します。</span><span class="sxs-lookup"><span data-stu-id="ca59d-105">Acts as a tie breaker when the **dispidToDoOrdinalDate** ([PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)) property sorts objects and the result in a tie.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ca59d-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="ca59d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ca59d-107">dispidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="ca59d-107">dispidToDoSubOrdinal</span></span>  <br/> |
|<span data-ttu-id="ca59d-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="ca59d-108">Property set:</span></span>  <br/> |<span data-ttu-id="ca59d-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="ca59d-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="ca59d-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="ca59d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ca59d-111">0x000085A1</span><span class="sxs-lookup"><span data-stu-id="ca59d-111">0x000085A1</span></span>  <br/> |
|<span data-ttu-id="ca59d-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="ca59d-112">Data type:</span></span>  <br/> |<span data-ttu-id="ca59d-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ca59d-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ca59d-114">領域:</span><span class="sxs-lookup"><span data-stu-id="ca59d-114">Area:</span></span>  <br/> |<span data-ttu-id="ca59d-115">タスク</span><span class="sxs-lookup"><span data-stu-id="ca59d-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca59d-116">備考</span><span class="sxs-lookup"><span data-stu-id="ca59d-116">Remarks</span></span>

<span data-ttu-id="ca59d-117">使用する場合は、このプロパティを辞書順に並べ替える必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca59d-117">If used, this property must be sorted lexicographically.</span></span> <span data-ttu-id="ca59d-118">文字列のコンポーネントの文字は必要がありますのみの数字 0 から 9 までので構成されます。</span><span class="sxs-lookup"><span data-stu-id="ca59d-118">The component characters of the string must consist of only the numerals zero through nine.</span></span> <span data-ttu-id="ca59d-119">「5555555」に、このプロパティ最初に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca59d-119">This property should be initially set to "5555555".</span></span> <span data-ttu-id="ca59d-120">このプロパティの長さは、254 文字まで (終端の NULL 文字を除く) を超えない必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca59d-120">The length of this property must not exceed 254 characters (excluding the terminating NULL character).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ca59d-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ca59d-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ca59d-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ca59d-122">Protocol specifications</span></span>

<span data-ttu-id="ca59d-123">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca59d-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca59d-124">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="ca59d-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ca59d-125">[[MS OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca59d-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca59d-126">プロパティ フラグに関連する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="ca59d-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ca59d-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ca59d-127">Header files</span></span>

<span data-ttu-id="ca59d-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ca59d-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="ca59d-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ca59d-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ca59d-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="ca59d-130">See also</span></span>



[<span data-ttu-id="ca59d-131">PidLidToDoOrdinalDate の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="ca59d-131">PidLidToDoOrdinalDate Canonical Property</span></span>](pidlidtodoordinaldate-canonical-property.md)


[<span data-ttu-id="ca59d-132">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ca59d-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ca59d-133">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ca59d-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ca59d-134">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="ca59d-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ca59d-135">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="ca59d-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

