---
title: SSortOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSortOrder
api_type:
- COM
ms.assetid: fe181b9a-5903-4cc0-bcd5-2061b440b5b1
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f9d38c90fa5795d34f78c61ce0faa5f76d8f740d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344549"
---
# <a name="ssortorder"></a><span data-ttu-id="9741c-103">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="9741c-103">SSortOrder</span></span>
 
<span data-ttu-id="9741c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9741c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9741c-105">表の行を並べ替える方法、並べ替えキーとして使用する列、および並べ替えの方向を定義します。</span><span class="sxs-lookup"><span data-stu-id="9741c-105">Defines how to sort the rows of a table, what column to use as the sort key, and the direction of the sort.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9741c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="9741c-106">Header file:</span></span>  <br/> |<span data-ttu-id="9741c-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9741c-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSortOrder
{
  ULONG ulPropTag;
  ULONG ulOrder;
} SSortOrder, FAR *LPSSortOrder;

```

## <a name="members"></a><span data-ttu-id="9741c-108">Members</span><span class="sxs-lookup"><span data-stu-id="9741c-108">Members</span></span>

<span data-ttu-id="9741c-109">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="9741c-109">**ulPropTag**</span></span>
  
> <span data-ttu-id="9741c-110">プロパティタグ。並べ替えキー、または分類された並べ替えの場合は、[カテゴリ] 列を識別します。</span><span class="sxs-lookup"><span data-stu-id="9741c-110">Property tag identifying the sort key or, for a categorized sort, the category column.</span></span>
    
<span data-ttu-id="9741c-111">**ulorder**</span><span class="sxs-lookup"><span data-stu-id="9741c-111">**ulOrder**</span></span>
  
> <span data-ttu-id="9741c-112">データの並べ替え順序を指定します。</span><span class="sxs-lookup"><span data-stu-id="9741c-112">The order in which the data is to be sorted.</span></span> <span data-ttu-id="9741c-113">可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="9741c-113">Possible values are as follow:</span></span>
    
  - <span data-ttu-id="9741c-114">TABLE_SORT_ASCEND: テーブルは昇順で並べ替えられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="9741c-114">TABLE_SORT_ASCEND: The table should be sorted in ascending order.</span></span>
      
  - <span data-ttu-id="9741c-115">TABLE_SORT_COMBINE: 並べ替え操作では、 **ulPropTag**メンバーの並べ替えキーの列として識別されたプロパティを、前の構造で指定され\*\*\*\* た並べ替えキーの列と組み合わせたカテゴリを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9741c-115">TABLE_SORT_COMBINE: The sort operation should create a category that combines the property identified as the sort key column in the **ulPropTag** member with the sort key column specified in the previous **SSortOrder** structure.</span></span> 
      
    <span data-ttu-id="9741c-116">TABLE_SORT_COMBINE は、ssortorderset 構造で、分類された並べ替えに対して[](ssortorderset.md)複数の並べ替え順序を指定するためのエントリとして使用されている場合にのみ使用できます。 \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="9741c-116">TABLE_SORT_COMBINE can only be used when the **SSortOrder** structure is being used as an entry in an [SSortOrderSet](ssortorderset.md) structure to specify multiple sort orders for a categorized sort.</span></span> <span data-ttu-id="9741c-117">TABLE_SORT_COMBINE は、 **ssortorderset**構造の最初の**ssortorder**構造では使用できません。</span><span class="sxs-lookup"><span data-stu-id="9741c-117">TABLE_SORT_COMBINE cannot be used in the first **SSortOrder** structure in an **SSortOrderSet** structure.</span></span> 
      
  - <span data-ttu-id="9741c-118">TABLE_SORT_DESCEND: テーブルは降順で並べ替えられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="9741c-118">TABLE_SORT_DESCEND: The table should be sorted in descending order.</span></span>
      
  - <span data-ttu-id="9741c-119">TABLE_SORT_CATEG_MAX: **ssortorderset**構造で、以前の並べ替え順序で指定されたカテゴリのデータ行について、テーブルを**ulPropTag**メンバーの最大値で並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="9741c-119">TABLE_SORT_CATEG_MAX: The table should be sorted on the maximum value of the **ulPropTag** member for the data rows in the categories specified by the previous sort order in the **SSortOrderSet** structure.</span></span> 
      
  - <span data-ttu-id="9741c-120">TABLE_SORT_CATEG_MIN: テーブルは、 **ssortorderset**構造で、前の並べ替え順序で指定されているカテゴリのデータ行の**ulPropTag**メンバーの最小値で並べ替えられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="9741c-120">TABLE_SORT_CATEG_MIN: The table should be sorted on the minimum value of the **ulPropTag** member for the data rows in the categories specified by the previous sort order in the in **SSortOrderSet** structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9741c-121">解説</span><span class="sxs-lookup"><span data-stu-id="9741c-121">Remarks</span></span>

<span data-ttu-id="9741c-122">**ssortorder**構造は、標準の並べ替え操作または分類された並べ替え操作のどちらを実行するかを示すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="9741c-122">An **SSortOrder** structure is used to describe how to perform either a standard sort operation or a categorized sort operation.</span></span> <span data-ttu-id="9741c-123">\*\*\*\* sorderstructure は、通常、複数の並べ替えキーと方向を記述するために、 **ssortorderset**構造に組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="9741c-123">**SSortOrder** structures are typically combined into an **SSortOrderSet** structure to describe multiple sort keys and directions.</span></span> <span data-ttu-id="9741c-124">**ssortorderset**構造体は、次の関数およびインターフェイスメソッドで使用されます。</span><span class="sxs-lookup"><span data-stu-id="9741c-124">**SSortOrderSet** structures are used in the following functions and interface methods:</span></span> 
  
- [<span data-ttu-id="9741c-125">ITableData::HrGetView</span><span class="sxs-lookup"><span data-stu-id="9741c-125">ITableData::HrGetView</span></span>](itabledata-hrgetview.md)
    
- [<span data-ttu-id="9741c-126">IMAPIFolder::SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="9741c-126">IMAPIFolder::SaveContentsSort</span></span>](imapifolder-savecontentssort.md)
    
- [<span data-ttu-id="9741c-127">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="9741c-127">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
    
- [<span data-ttu-id="9741c-128">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="9741c-128">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
- [<span data-ttu-id="9741c-129">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="9741c-129">FBadSortOrderSet</span></span>](fbadsortorderset.md)
    
- [<span data-ttu-id="9741c-130">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="9741c-130">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
<span data-ttu-id="9741c-131">並べ替えキーとして使用できるテーブルで許可されている列の範囲は、プロバイダーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="9741c-131">The range of allowed columns in a table that can be used as a sort key depends on the provider.</span></span> <span data-ttu-id="9741c-132">現在の列セットの一部である列は、常に並べ替えキーとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="9741c-132">Columns that are part of the current column set can always be used as sort keys.</span></span> <span data-ttu-id="9741c-133">ただし、各プロバイダーは、現在の列セットに含まれていない利用可能な列を使用して並べ替えキーを定義できるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="9741c-133">However, each provider determines whether sort keys can be defined by using available columns that are not in the current column set.</span></span> <span data-ttu-id="9741c-134">使用可能な列は、TBL_ALL_COLUMNS フラグが設定されている場合に[IMAPITable:: querycolumns](imapitable-querycolumns.md)から返される列です。</span><span class="sxs-lookup"><span data-stu-id="9741c-134">An available column is a column that is returned from [IMAPITable::QueryColumns](imapitable-querycolumns.md) when the TBL_ALL_COLUMNS flag is set.</span></span> 
  
<span data-ttu-id="9741c-135">**ulorder**メンバーは、双方向の順序と分類の情報 (たとえば、会話 ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))、つまり会話スレッド (一連のメッセージと返信)) を示します。</span><span class="sxs-lookup"><span data-stu-id="9741c-135">The **ulOrder** member indicates both directional order and categorization information, for example, by conversation ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)), that is, conversational thread, which is a series of messages and replies.</span></span> <span data-ttu-id="9741c-136">行は、すべての NULL エントリが最後に配置された昇順または降順のどちらかの順序で並べ替えることができます。</span><span class="sxs-lookup"><span data-stu-id="9741c-136">Rows can be sorted in either an ascending or descending sequence with all NULL entries positioned last.</span></span> 
  
<span data-ttu-id="9741c-137">TABLE_SORT_COMBINE の値は、 **ulPropTag**で指定された列が前のカテゴリの列と組み合わせて複合カテゴリを形成する必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="9741c-137">The TABLE_SORT_COMBINE value indicates that the column specified in **ulPropTag** should be combined with the previous category column to form a composite category.</span></span> <span data-ttu-id="9741c-138">つまり、TABLE_SORT_COMBINE では、個々の列の一意の値を分類するのではなく、列の組み合わせの一意の値について分類することができます。</span><span class="sxs-lookup"><span data-stu-id="9741c-138">That is, instead of categorizing on unique values of individual columns, TABLE_SORT_COMBINE allows for categorization on unique values of a combination of columns.</span></span> <span data-ttu-id="9741c-139">たとえば、特定の件名の特定の送信者から受信したメッセージをグループ化するために、1つのカテゴリを定義できます。</span><span class="sxs-lookup"><span data-stu-id="9741c-139">For example, a single category could be defined to group messages received from a particular sender on a particular subject.</span></span> <span data-ttu-id="9741c-140">TABLE_SORT_COMBINE に値を設定すると、表示されるカテゴリ行の数が少なくなります。</span><span class="sxs-lookup"><span data-stu-id="9741c-140">Setting the value to TABLE_SORT_COMBINE reduces the number of category rows that are displayed.</span></span> 
  
<span data-ttu-id="9741c-141">複数値を持つ列での並べ替えは、すべてのテーブル実装で汎用的にサポートされているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="9741c-141">Sorting on multi-valued columns is not universally supported by all table implementations.</span></span> <span data-ttu-id="9741c-142">サポートされている場合は、MVI_PROP マクロを使用して MV_FLAG を**ulPropTag**メンバーの property タグに適用し、並べ替えキーを複数値を持つ列として識別します。</span><span class="sxs-lookup"><span data-stu-id="9741c-142">If supported, apply the MV_FLAG using the MVI_PROP macro to the property tag in the **ulPropTag** member to identify the sort key as a multi-valued column.</span></span> <span data-ttu-id="9741c-143">複数値列での並べ替えは、個々の値の使用に基づいています。</span><span class="sxs-lookup"><span data-stu-id="9741c-143">Sorting on a multi-valued column is based on using the individual values.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="9741c-144">TABLE_SORT_CATEG_MAX \*\*\*\* および TABLE_SORT_CATEG_MIN は、現在のダウンロード可能なヘッダーファイルで定義されていない場合があります。その場合は、次の値を使用してコードに追加できます。 >`#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`</span><span class="sxs-lookup"><span data-stu-id="9741c-144">The **ulOrder** member values TABLE_SORT_CATEG_MAX and TABLE_SORT_CATEG_MIN might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`</span></span>
  
<span data-ttu-id="9741c-145">標準および分類された並べ替えの詳細については、「[並べ替えと分類](sorting-and-categorization.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9741c-145">For more information about standard and categorized sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9741c-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="9741c-146">See also</span></span>

- [<span data-ttu-id="9741c-147">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="9741c-147">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="9741c-148">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="9741c-148">MAPI Structures</span></span>](mapi-structures.md)

