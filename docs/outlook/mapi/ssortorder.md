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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f9d38c90fa5795d34f78c61ce0faa5f76d8f740d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439724"
---
# <a name="ssortorder"></a><span data-ttu-id="e9d8f-103">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="e9d8f-103">SSortOrder</span></span>
 
<span data-ttu-id="e9d8f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9d8f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9d8f-105">テーブルの行の並べ替え方法、並べ替えキーとして使用する列、並べ替えの方向を定義します。</span><span class="sxs-lookup"><span data-stu-id="e9d8f-105">Defines how to sort the rows of a table, what column to use as the sort key, and the direction of the sort.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e9d8f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e9d8f-106">Header file:</span></span>  <br/> |<span data-ttu-id="e9d8f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e9d8f-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSortOrder
{
  ULONG ulPropTag;
  ULONG ulOrder;
} SSortOrder, FAR *LPSSortOrder;

```

## <a name="members"></a><span data-ttu-id="e9d8f-108">Members</span><span class="sxs-lookup"><span data-stu-id="e9d8f-108">Members</span></span>

<span data-ttu-id="e9d8f-109">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="e9d8f-109">**ulPropTag**</span></span>
  
> <span data-ttu-id="e9d8f-110">並べ替えキーまたは分類された並べ替えのカテゴリ列を識別するプロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="e9d8f-110">Property tag identifying the sort key or, for a categorized sort, the category column.</span></span>
    
<span data-ttu-id="e9d8f-111">**ulOrder**</span><span class="sxs-lookup"><span data-stu-id="e9d8f-111">**ulOrder**</span></span>
  
> <span data-ttu-id="e9d8f-112">データを並べ替える順序。</span><span class="sxs-lookup"><span data-stu-id="e9d8f-112">The order in which the data is to be sorted.</span></span> <span data-ttu-id="e9d8f-113">指定できる値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e9d8f-113">Possible values are as follow:</span></span>
    
  - <span data-ttu-id="e9d8f-114">TABLE_SORT_ASCEND: テーブルは昇順に並べ替える必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9d8f-114">TABLE_SORT_ASCEND: The table should be sorted in ascending order.</span></span>
      
  - <span data-ttu-id="e9d8f-115">TABLE_SORT_COMBINE: 並べ替え操作では **、ulPropTag** メンバーの並べ替えキー列として識別されるプロパティと、前の **SSortOrder** 構造体で指定された並べ替えキー列を組み合わせたカテゴリを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9d8f-115">TABLE_SORT_COMBINE: The sort operation should create a category that combines the property identified as the sort key column in the **ulPropTag** member with the sort key column specified in the previous **SSortOrder** structure.</span></span> 
      
    <span data-ttu-id="e9d8f-116">TABLE_SORT_COMBINE **SSortOrder** 構造体を [SSortOrderSet](ssortorderset.md) 構造体のエントリとして使用して、分類された並べ替えに対して複数の並べ替え順序を指定する場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="e9d8f-116">TABLE_SORT_COMBINE can only be used when the **SSortOrder** structure is being used as an entry in an [SSortOrderSet](ssortorderset.md) structure to specify multiple sort orders for a categorized sort.</span></span> <span data-ttu-id="e9d8f-117">TABLE_SORT_COMBINE **SSortOrderSet** 構造体の最初の **SSortOrder 構造体では使用** できません。</span><span class="sxs-lookup"><span data-stu-id="e9d8f-117">TABLE_SORT_COMBINE cannot be used in the first **SSortOrder** structure in an **SSortOrderSet** structure.</span></span> 
      
  - <span data-ttu-id="e9d8f-118">TABLE_SORT_DESCEND: テーブルは降順で並べ替える必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9d8f-118">TABLE_SORT_DESCEND: The table should be sorted in descending order.</span></span>
      
  - <span data-ttu-id="e9d8f-119">TABLE_SORT_CATEG_MAX: **SSortOrderSet** 構造体の前の並べ替え順序で指定されたカテゴリのデータ行の **ulPropTag** メンバーの最大値でテーブルを並べ替える必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9d8f-119">TABLE_SORT_CATEG_MAX: The table should be sorted on the maximum value of the **ulPropTag** member for the data rows in the categories specified by the previous sort order in the **SSortOrderSet** structure.</span></span> 
      
  - <span data-ttu-id="e9d8f-120">TABLE_SORT_CATEG_MIN:**テーブルは、SSortOrderSet** 構造体の前の並べ替え順序で指定されたカテゴリのデータ行の **ulPropTag** メンバーの最小値で並べ替える必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9d8f-120">TABLE_SORT_CATEG_MIN: The table should be sorted on the minimum value of the **ulPropTag** member for the data rows in the categories specified by the previous sort order in the in **SSortOrderSet** structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e9d8f-121">注釈</span><span class="sxs-lookup"><span data-stu-id="e9d8f-121">Remarks</span></span>

<span data-ttu-id="e9d8f-122">**SSortOrder 構造体を** 使用して、標準の並べ替え操作または分類された並べ替え操作を実行する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="e9d8f-122">An **SSortOrder** structure is used to describe how to perform either a standard sort operation or a categorized sort operation.</span></span> <span data-ttu-id="e9d8f-123">**SSortOrder** 構造体は通常、複数の並べ替えキーと方向を記述するために **SSortOrderSet** 構造体に組み合わされます。</span><span class="sxs-lookup"><span data-stu-id="e9d8f-123">**SSortOrder** structures are typically combined into an **SSortOrderSet** structure to describe multiple sort keys and directions.</span></span> <span data-ttu-id="e9d8f-124">**SSortOrderSet** 構造体は、次の関数およびインターフェイス メソッドで使用されます。</span><span class="sxs-lookup"><span data-stu-id="e9d8f-124">**SSortOrderSet** structures are used in the following functions and interface methods:</span></span> 
  
- [<span data-ttu-id="e9d8f-125">ITableData::HrGetView</span><span class="sxs-lookup"><span data-stu-id="e9d8f-125">ITableData::HrGetView</span></span>](itabledata-hrgetview.md)
    
- [<span data-ttu-id="e9d8f-126">IMAPIFolder::SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="e9d8f-126">IMAPIFolder::SaveContentsSort</span></span>](imapifolder-savecontentssort.md)
    
- [<span data-ttu-id="e9d8f-127">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="e9d8f-127">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
    
- [<span data-ttu-id="e9d8f-128">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="e9d8f-128">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
- [<span data-ttu-id="e9d8f-129">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="e9d8f-129">FBadSortOrderSet</span></span>](fbadsortorderset.md)
    
- [<span data-ttu-id="e9d8f-130">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="e9d8f-130">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
<span data-ttu-id="e9d8f-131">並べ替えキーとして使用できるテーブル内の列の範囲は、プロバイダーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="e9d8f-131">The range of allowed columns in a table that can be used as a sort key depends on the provider.</span></span> <span data-ttu-id="e9d8f-132">現在の列セットの一部である列は、常に並べ替えキーとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="e9d8f-132">Columns that are part of the current column set can always be used as sort keys.</span></span> <span data-ttu-id="e9d8f-133">ただし、各プロバイダーは、現在の列セットに含めされていない使用可能な列を使用して並べ替えキーを定義できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="e9d8f-133">However, each provider determines whether sort keys can be defined by using available columns that are not in the current column set.</span></span> <span data-ttu-id="e9d8f-134">使用可能な列は [、IMAPITable::QueryColumns](imapitable-querycolumns.md) のフラグが設定されているときに返TBL_ALL_COLUMNS列です。</span><span class="sxs-lookup"><span data-stu-id="e9d8f-134">An available column is a column that is returned from [IMAPITable::QueryColumns](imapitable-querycolumns.md) when the TBL_ALL_COLUMNS flag is set.</span></span> 
  
<span data-ttu-id="e9d8f-135">**ulOrder** メンバーは、方向順序と分類の両方の情報 (たとえば、会話 ([PidTagConversationTopic)](pidtagconversationtopic-canonical-property.md)、つまり、一連のメッセージと返信である会話スレッドを示します。</span><span class="sxs-lookup"><span data-stu-id="e9d8f-135">The **ulOrder** member indicates both directional order and categorization information, for example, by conversation ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)), that is, conversational thread, which is a series of messages and replies.</span></span> <span data-ttu-id="e9d8f-136">行は、すべての NULL エントリが最後に配置された昇順または降順で並べ替えできます。</span><span class="sxs-lookup"><span data-stu-id="e9d8f-136">Rows can be sorted in either an ascending or descending sequence with all NULL entries positioned last.</span></span> 
  
<span data-ttu-id="e9d8f-137">このTABLE_SORT_COMBINEは **、ulPropTag** で指定された列を前のカテゴリ列と組み合わせて複合カテゴリを形成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9d8f-137">The TABLE_SORT_COMBINE value indicates that the column specified in **ulPropTag** should be combined with the previous category column to form a composite category.</span></span> <span data-ttu-id="e9d8f-138">つまり、個々の列の一意の値を分類する代わりにTABLE_SORT_COMBINE列の組み合わせの一意の値を分類できます。</span><span class="sxs-lookup"><span data-stu-id="e9d8f-138">That is, instead of categorizing on unique values of individual columns, TABLE_SORT_COMBINE allows for categorization on unique values of a combination of columns.</span></span> <span data-ttu-id="e9d8f-139">たとえば、特定の件名の特定の送信者から受信したメッセージをグループ化するために、1 つのカテゴリを定義できます。</span><span class="sxs-lookup"><span data-stu-id="e9d8f-139">For example, a single category could be defined to group messages received from a particular sender on a particular subject.</span></span> <span data-ttu-id="e9d8f-140">値を設定するとTABLE_SORT_COMBINE表示されるカテゴリ行の数が減らされます。</span><span class="sxs-lookup"><span data-stu-id="e9d8f-140">Setting the value to TABLE_SORT_COMBINE reduces the number of category rows that are displayed.</span></span> 
  
<span data-ttu-id="e9d8f-141">複数値の列での並べ替えは、すべてのテーブル実装で汎用的にサポートされるとは言えな。</span><span class="sxs-lookup"><span data-stu-id="e9d8f-141">Sorting on multi-valued columns is not universally supported by all table implementations.</span></span> <span data-ttu-id="e9d8f-142">サポートされている場合は、MV_FLAG マクロMVI_PROPを **ulPropTag** メンバーのプロパティ タグに適用して、並べ替えキーを複数値の列として識別します。</span><span class="sxs-lookup"><span data-stu-id="e9d8f-142">If supported, apply the MV_FLAG using the MVI_PROP macro to the property tag in the **ulPropTag** member to identify the sort key as a multi-valued column.</span></span> <span data-ttu-id="e9d8f-143">複数値の列での並べ替えは、個々の値の使用に基づいて行います。</span><span class="sxs-lookup"><span data-stu-id="e9d8f-143">Sorting on a multi-valued column is based on using the individual values.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="e9d8f-144">**ulOrder** メンバー値 TABLE_SORT_CATEG_MAX および TABLE_SORT_CATEG_MIN は、現在使用しているダウンロード可能なヘッダー ファイルで定義されていない可能性があります。その場合は、次の値を使用してコードに追加>`#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`</span><span class="sxs-lookup"><span data-stu-id="e9d8f-144">The **ulOrder** member values TABLE_SORT_CATEG_MAX and TABLE_SORT_CATEG_MIN might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`</span></span>
  
<span data-ttu-id="e9d8f-145">標準の並べ替えと分類された並べ替えの詳細については、「並べ替え [と分類」を参照してください](sorting-and-categorization.md)。</span><span class="sxs-lookup"><span data-stu-id="e9d8f-145">For more information about standard and categorized sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e9d8f-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="e9d8f-146">See also</span></span>

- [<span data-ttu-id="e9d8f-147">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="e9d8f-147">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="e9d8f-148">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="e9d8f-148">MAPI Structures</span></span>](mapi-structures.md)

