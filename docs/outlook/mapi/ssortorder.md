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
ms.openlocfilehash: 331dc05b30390bb803d186f157e0fe9edb779ab0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571669"
---
# <a name="ssortorder"></a><span data-ttu-id="84833-103">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="84833-103">SSortOrder</span></span>
 
<span data-ttu-id="84833-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84833-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84833-105">並べ替えキー、および並べ替えの方向として使用するには、どのような列、テーブルの行をソートする方法を定義します。</span><span class="sxs-lookup"><span data-stu-id="84833-105">Defines how to sort the rows of a table, what column to use as the sort key, and the direction of the sort.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="84833-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="84833-106">Header file:</span></span>  <br/> |<span data-ttu-id="84833-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="84833-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSortOrder
{
  ULONG ulPropTag;
  ULONG ulOrder;
} SSortOrder, FAR *LPSSortOrder;

```

## <a name="members"></a><span data-ttu-id="84833-108">Members</span><span class="sxs-lookup"><span data-stu-id="84833-108">Members</span></span>

<span data-ttu-id="84833-109">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="84833-109">**ulPropTag**</span></span>
  
> <span data-ttu-id="84833-110">キー、または、カテゴリ別の並べ替え、[カテゴリ] 列の並べ替えを識別するプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="84833-110">Property tag identifying the sort key or, for a categorized sort, the category column.</span></span>
    
<span data-ttu-id="84833-111">**ulOrder**</span><span class="sxs-lookup"><span data-stu-id="84833-111">**ulOrder**</span></span>
  
> <span data-ttu-id="84833-112">データの並べ替え順序です。</span><span class="sxs-lookup"><span data-stu-id="84833-112">The order in which the data is to be sorted.</span></span> <span data-ttu-id="84833-113">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="84833-113">Possible values are as follow:</span></span>
    
  - <span data-ttu-id="84833-114">TABLE_SORT_ASCEND: テーブルを昇順で並べ替えする必要があります。</span><span class="sxs-lookup"><span data-stu-id="84833-114">TABLE_SORT_ASCEND: The table should be sorted in ascending order.</span></span>
      
  - <span data-ttu-id="84833-115">TABLE_SORT_COMBINE: 並べ替え操作は、以前の**SSortOrder**構造体で指定した並べ替えキー列を持つ**ulPropTag**のメンバーの並べ替えキー列として識別されるプロパティを結合するカテゴリを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="84833-115">TABLE_SORT_COMBINE: The sort operation should create a category that combines the property identified as the sort key column in the **ulPropTag** member with the sort key column specified in the previous **SSortOrder** structure.</span></span> 
      
    <span data-ttu-id="84833-116">TABLE_SORT_COMBINE は、 **SSortOrder**構造体は、カテゴリ別の並べ替えのさまざまな並べ替え順序を指定する[SSortOrderSet](ssortorderset.md)構造体のエントリとして使用されている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="84833-116">TABLE_SORT_COMBINE can only be used when the **SSortOrder** structure is being used as an entry in an [SSortOrderSet](ssortorderset.md) structure to specify multiple sort orders for a categorized sort.</span></span> <span data-ttu-id="84833-117">TABLE_SORT_COMBINE は、 **SSortOrderSet**構造体の最初の**SSortOrder**構造体では使用できません。</span><span class="sxs-lookup"><span data-stu-id="84833-117">TABLE_SORT_COMBINE cannot be used in the first **SSortOrder** structure in an **SSortOrderSet** structure.</span></span> 
      
  - <span data-ttu-id="84833-118">TABLE_SORT_DESCEND: テーブルの並べ替えを降順に並べ替え。</span><span class="sxs-lookup"><span data-stu-id="84833-118">TABLE_SORT_DESCEND: The table should be sorted in descending order.</span></span>
      
  - <span data-ttu-id="84833-119">TABLE_SORT_CATEG_MAX: **SSortOrderSet**構造体の前の並べ替え順序で指定されたカテゴリ内のデータ行の**ulPropTag**メンバーの最大値でテーブルを並べ替える必要があります。</span><span class="sxs-lookup"><span data-stu-id="84833-119">TABLE_SORT_CATEG_MAX: The table should be sorted on the maximum value of the **ulPropTag** member for the data rows in the categories specified by the previous sort order in the **SSortOrderSet** structure.</span></span> 
      
  - <span data-ttu-id="84833-120">TABLE_SORT_CATEG_MIN: 前の**SSortOrderSet**構造体の並べ替え順序で指定されたカテゴリ内のデータ行の**ulPropTag**メンバーの最小値のテーブルを並べ替える必要があります。</span><span class="sxs-lookup"><span data-stu-id="84833-120">TABLE_SORT_CATEG_MIN: The table should be sorted on the minimum value of the **ulPropTag** member for the data rows in the categories specified by the previous sort order in the in **SSortOrderSet** structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="84833-121">注釈</span><span class="sxs-lookup"><span data-stu-id="84833-121">Remarks</span></span>

<span data-ttu-id="84833-122">**SSortOrder**構造体を使用して、標準的な並べ替え操作またはカテゴリ別に並べ替え操作を実行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="84833-122">An **SSortOrder** structure is used to describe how to perform either a standard sort operation or a categorized sort operation.</span></span> <span data-ttu-id="84833-123">**SSortOrder**構造体を複数の並べ替えキーと方向を記述する**SSortOrderSet**構造に組み合わせます。</span><span class="sxs-lookup"><span data-stu-id="84833-123">**SSortOrder** structures are typically combined into an **SSortOrderSet** structure to describe multiple sort keys and directions.</span></span> <span data-ttu-id="84833-124">**SSortOrderSet**構造体は、次の関数やインターフェイス メソッドで使用されます。</span><span class="sxs-lookup"><span data-stu-id="84833-124">**SSortOrderSet** structures are used in the following functions and interface methods:</span></span> 
  
- [<span data-ttu-id="84833-125">ITableData::HrGetView</span><span class="sxs-lookup"><span data-stu-id="84833-125">ITableData::HrGetView</span></span>](itabledata-hrgetview.md)
    
- [<span data-ttu-id="84833-126">IMAPIFolder::SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="84833-126">IMAPIFolder::SaveContentsSort</span></span>](imapifolder-savecontentssort.md)
    
- [<span data-ttu-id="84833-127">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="84833-127">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
    
- [<span data-ttu-id="84833-128">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="84833-128">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
- [<span data-ttu-id="84833-129">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="84833-129">FBadSortOrderSet</span></span>](fbadsortorderset.md)
    
- [<span data-ttu-id="84833-130">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="84833-130">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
<span data-ttu-id="84833-131">許可されているテーブルの列の並べ替えキーとして使用できる範囲は、プロバイダーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="84833-131">The range of allowed columns in a table that can be used as a sort key depends on the provider.</span></span> <span data-ttu-id="84833-132">現在の列セットの一部である列は、並べ替えキーとして常に使用できます。</span><span class="sxs-lookup"><span data-stu-id="84833-132">Columns that are part of the current column set can always be used as sort keys.</span></span> <span data-ttu-id="84833-133">ただし、各プロバイダーは、現在の列ではなく設定される利用可能な列を使用して、並べ替えキーを定義できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="84833-133">However, each provider determines whether sort keys can be defined by using available columns that are not in the current column set.</span></span> <span data-ttu-id="84833-134">列は、TBL_ALL_COLUMNS フラグが設定されている場合に、 [IMAPITable::QueryColumns](imapitable-querycolumns.md)から返される列です。</span><span class="sxs-lookup"><span data-stu-id="84833-134">An available column is a column that is returned from [IMAPITable::QueryColumns](imapitable-querycolumns.md) when the TBL_ALL_COLUMNS flag is set.</span></span> 
  
<span data-ttu-id="84833-135">**UlOrder**メンバーを示します両方の方向の順序と分類については、たとえば、テーマ ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)) は、メッセージと返信の一連の会話スレッドは、別。</span><span class="sxs-lookup"><span data-stu-id="84833-135">The **ulOrder** member indicates both directional order and categorization information, for example, by conversation ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)), that is, conversational thread, which is a series of messages and replies.</span></span> <span data-ttu-id="84833-136">行は、最後に配置されたすべての NULL エントリを降順または昇順で並べ替えることができます。</span><span class="sxs-lookup"><span data-stu-id="84833-136">Rows can be sorted in either an ascending or descending sequence with all NULL entries positioned last.</span></span> 
  
<span data-ttu-id="84833-137">TABLE_SORT_COMBINE 値は、「複合」カテゴリを作成する前のカテゴリ列に**ulPropTag**で指定された列を組み合わせる必要がありますことを示します。</span><span class="sxs-lookup"><span data-stu-id="84833-137">The TABLE_SORT_COMBINE value indicates that the column specified in **ulPropTag** should be combined with the previous category column to form a composite category.</span></span> <span data-ttu-id="84833-138">個々 の列の一意の値に分類することではなく TABLE_SORT_COMBINE では、列の組み合わせの一意の値に分類されます。</span><span class="sxs-lookup"><span data-stu-id="84833-138">That is, instead of categorizing on unique values of individual columns, TABLE_SORT_COMBINE allows for categorization on unique values of a combination of columns.</span></span> <span data-ttu-id="84833-139">たとえば、特定の件名に特定の送信者から受信したメッセージをグループ化する 1 つのカテゴリを定義できます。</span><span class="sxs-lookup"><span data-stu-id="84833-139">For example, a single category could be defined to group messages received from a particular sender on a particular subject.</span></span> <span data-ttu-id="84833-140">TABLE_SORT_COMBINE に値を設定すると、表示されているカテゴリの行の数が減少します。</span><span class="sxs-lookup"><span data-stu-id="84833-140">Setting the value to TABLE_SORT_COMBINE reduces the number of category rows that are displayed.</span></span> 
  
<span data-ttu-id="84833-141">複数値を持つ列で並べ替えをサポートされていませんユニバーサル テーブルのすべての実装によって。</span><span class="sxs-lookup"><span data-stu-id="84833-141">Sorting on multi-valued columns is not universally supported by all table implementations.</span></span> <span data-ttu-id="84833-142">サポートされている場合は、 **ulPropTag**のメンバーで複数値を持つ列と並べ替えのキーを識別するプロパティ タグに MVI_PROP マクロを使用して MV_FLAG を適用します。</span><span class="sxs-lookup"><span data-stu-id="84833-142">If supported, apply the MV_FLAG using the MVI_PROP macro to the property tag in the **ulPropTag** member to identify the sort key as a multi-valued column.</span></span> <span data-ttu-id="84833-143">複数値を持つ列で並べ替えをすると、個々 の値を使用するのに基づいています。</span><span class="sxs-lookup"><span data-stu-id="84833-143">Sorting on a multi-valued column is based on using the individual values.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="84833-144">**UlOrder**メンバーの値がダウンロード可能なヘッダー ファイルで TABLE_SORT_CATEG_MAX と TABLE_SORT_CATEG_MIN を定義する可能性がありますいない現在がある場合、次の値を使用してコードを追加する場合: >`#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`</span><span class="sxs-lookup"><span data-stu-id="84833-144">The **ulOrder** member values TABLE_SORT_CATEG_MAX and TABLE_SORT_CATEG_MIN might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`</span></span>
  
<span data-ttu-id="84833-145">詳細については、標準的なカテゴリ別に並べ替え、[並べ替えや分類](sorting-and-categorization.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84833-145">For more information about standard and categorized sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="84833-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="84833-146">See also</span></span>

- [<span data-ttu-id="84833-147">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="84833-147">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="84833-148">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="84833-148">MAPI Structures</span></span>](mapi-structures.md)

