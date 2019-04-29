---
title: SSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSortOrderSet
api_type:
- COM
ms.assetid: e7f9be6a-92e7-44a8-93ee-b087713a31df
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: db19c3908c419b98b8deb71e2a86d0aa6eebe240
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438100"
---
# <a name="ssortorderset"></a><span data-ttu-id="b029e-103">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="b029e-103">SSortOrderSet</span></span>

  
  
<span data-ttu-id="b029e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b029e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b029e-105">標準または分類された並べ替えに使用されるテーブルの並べ替えキーのコレクションを定義します。</span><span class="sxs-lookup"><span data-stu-id="b029e-105">Defines a collection of sort keys for a table that is used for standard or categorized sorting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b029e-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="b029e-106">Header file:</span></span>  <br/> |<span data-ttu-id="b029e-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b029e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b029e-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="b029e-108">Related macros:</span></span>  <br/> |<span data-ttu-id="b029e-109">[CbNewSSortOrderSet](cbnewssortorderset.md)、 [cbssortorderset](cbssortorderset.md)、 [sizedssortorderset](sizedssortorderset.md)</span><span class="sxs-lookup"><span data-stu-id="b029e-109">[CbNewSSortOrderSet](cbnewssortorderset.md), [CbSSortOrderSet](cbssortorderset.md), [SizedSSortOrderSet](sizedssortorderset.md)</span></span> <br/> |
   
```cpp
typedef struct _SSortOrderSet
{
  ULONG cSorts;
  ULONG cCategories;
  ULONG cExpanded;
  SSortOrder aSort[MAPI_DIM];
} SSortOrderSet, FAR *LPSSortOrderSet;

```

## <a name="members"></a><span data-ttu-id="b029e-110">メンバー</span><span class="sxs-lookup"><span data-stu-id="b029e-110">Members</span></span>

 <span data-ttu-id="b029e-111">**csorts**</span><span class="sxs-lookup"><span data-stu-id="b029e-111">**cSorts**</span></span>
  
> <span data-ttu-id="b029e-112">**asort**メンバに含まれている、 [ssortorder](ssortorder.md)構造の数。</span><span class="sxs-lookup"><span data-stu-id="b029e-112">Count of [SSortOrder](ssortorder.md) structures that are included in the **aSort** member.</span></span> 
    
 <span data-ttu-id="b029e-113">**ccategories**</span><span class="sxs-lookup"><span data-stu-id="b029e-113">**cCategories**</span></span>
  
> <span data-ttu-id="b029e-114">カテゴリ列として指定されている列の数。</span><span class="sxs-lookup"><span data-stu-id="b029e-114">Count of columns that are designated as category columns.</span></span> <span data-ttu-id="b029e-115">指定できる値は、分類されていない、または標準の並べ替えを示す0から、 **csorts**メンバーによって示される番号までです。</span><span class="sxs-lookup"><span data-stu-id="b029e-115">Possible values range from zero, which indicates a non-categorized or standard sort, to the number indicated by the **cSorts** member.</span></span> 
    
 <span data-ttu-id="b029e-116">**cexpanded**</span><span class="sxs-lookup"><span data-stu-id="b029e-116">**cExpanded**</span></span>
  
> <span data-ttu-id="b029e-117">展開状態で開始されるカテゴリの数。これにより、カテゴリに適用されるすべての行がテーブルビューに表示されます。</span><span class="sxs-lookup"><span data-stu-id="b029e-117">Count of categories that start in an expanded state, where all of the rows that apply to the category are visible in the table view.</span></span> <span data-ttu-id="b029e-118">指定可能な値の範囲は、0から**ccategories**で示されている数までです。</span><span class="sxs-lookup"><span data-stu-id="b029e-118">Possible values range from 0 to the number indicated by **cCategories**.</span></span>
    
 <span data-ttu-id="b029e-119">**asort**</span><span class="sxs-lookup"><span data-stu-id="b029e-119">**aSort**</span></span>
  
> <span data-ttu-id="b029e-120">ソート順序を定義する、 **ssortorder**構造の配列。</span><span class="sxs-lookup"><span data-stu-id="b029e-120">Array of **SSortOrder** structures, each defining a sort order.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b029e-121">注釈</span><span class="sxs-lookup"><span data-stu-id="b029e-121">Remarks</span></span>

<span data-ttu-id="b029e-122">**ssortorderset**構造は、標準および分類された並べ替えに対して複数の並べ替え順序を定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b029e-122">A **SSortOrderSet** structure is used for defining multiple sort orders for standard and categorized sorting.</span></span> 
  
<span data-ttu-id="b029e-123">各**ssortorderset**構造には、並べ替え\*\*\*\* の方向と、並べ替えキーとして使用される列を定義する、少なくとも1つの sorderstructure が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b029e-123">Each **SSortOrderSet** structure contains at least one **SSortOrder** structure defining the direction of the sort and the column that will be used as the sort key.</span></span> <span data-ttu-id="b029e-124">分類された並べ替えの場合、この列はカテゴリとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="b029e-124">For categorized sorting, this column is used as the category.</span></span> <span data-ttu-id="b029e-125">csorts メンバーの値\*\*\*\* が**csorts**メンバーの値を超えると、カテゴリよりも多くの並べ替えキーが存在し、その列から、 **ssortorder**配列の先頭に表示されている列に分類項目が作成されます。</span><span class="sxs-lookup"><span data-stu-id="b029e-125">When the value of the **cSorts** member exceeds the value of the **cCategories** member, there are more sort keys than categories, and categories are created from the columns that appear first in the **SSortOrder** array.</span></span> 
  
<span data-ttu-id="b029e-126">たとえば、csorts \*\*\*\* が3に設定されていて、 **csorts**が2に設定されている場合、 **ssortorder**配列の最初の2つのエントリの**ulPropTag**メンバによって記述されている列は、カテゴリ列として使用されます。</span><span class="sxs-lookup"><span data-stu-id="b029e-126">For example, if **cSorts** is set to 3 and **cCategories** is set to 2, the columns described by the **ulPropTag** member of the first two entries in the **SSortOrder** array are used as the category columns.</span></span> <span data-ttu-id="b029e-127">最初のエントリは、トップレベルのカテゴリグループとして機能します。2番目のエントリを第2のグループにします。</span><span class="sxs-lookup"><span data-stu-id="b029e-127">The first entry serves as the top-level category grouping; the second entry as the secondary grouping.</span></span> <span data-ttu-id="b029e-128">2つのカテゴリ列に一致するすべての行は、3番目のエントリで定義されている並べ替えキーを使用して並べ替えられます。</span><span class="sxs-lookup"><span data-stu-id="b029e-128">All of the rows that match the two category columns are sorted by using the sort key defined in the third entry.</span></span> 
  
<span data-ttu-id="b029e-129">**cexpanded**メンバーは、最初に展開されたカテゴリの数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b029e-129">The **cExpanded** member specifies the number of categories that are at first expanded.</span></span> <span data-ttu-id="b029e-130">カテゴリが複数ある場合、テーブルの実装は、カテゴリとして指定された最初の列から始まり、 **ccategories**の数を超えない限り、後続のカテゴリの列と連続した順序で続きます。</span><span class="sxs-lookup"><span data-stu-id="b029e-130">When there are multiple categories, the table implementation starts with the first column to be designated as a category and continues in sequential order with the subsequent category columns until the number of **cCategories** has been exceeded.</span></span> <span data-ttu-id="b029e-131">拡張された列の数よりも多くのカテゴリ列がある場合は、カテゴリ列は折りたたまれています。</span><span class="sxs-lookup"><span data-stu-id="b029e-131">If there are more category columns than there are expanded columns, the category columns are collapsed.</span></span> <span data-ttu-id="b029e-132">**cexpanded**が0の場合は、表のユーザーが表示に使用できるのは最上位レベルの見出し行だけです。</span><span class="sxs-lookup"><span data-stu-id="b029e-132">If **cExpanded** is equal to zero, only the top level heading row is available to the table user for display.</span></span> <span data-ttu-id="b029e-133">**cexpanded**がカテゴリの数よりも小さい値に等しい場合は、すべての見出し行とリーフ行のいずれも使用できません。</span><span class="sxs-lookup"><span data-stu-id="b029e-133">If **cExpanded** is equal to one less than the number of categories, then all of the heading rows and none of the leaf rows are available.</span></span> <span data-ttu-id="b029e-134">**cexpanded**がカテゴリの数と等しい場合、テーブルは完全に展開されます。</span><span class="sxs-lookup"><span data-stu-id="b029e-134">If **cExpanded** is equal to the number of categories, then the table is fully expanded.</span></span> 
  
<span data-ttu-id="b029e-135">標準および分類された並べ替えの詳細については、「[並べ替えと分類](sorting-and-categorization.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b029e-135">For more information about standard and categorized sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b029e-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="b029e-136">See also</span></span>



[<span data-ttu-id="b029e-137">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="b029e-137">SSortOrder</span></span>](ssortorder.md)
  
[<span data-ttu-id="b029e-138">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="b029e-138">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
  
[<span data-ttu-id="b029e-139">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="b029e-139">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)


[<span data-ttu-id="b029e-140">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="b029e-140">MAPI Structures</span></span>](mapi-structures.md)

