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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1604c4a1a0d1bf4008595b0d150b4f7eb3d1c2ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804002"
---
# <a name="ssortorderset"></a><span data-ttu-id="ecde1-103">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="ecde1-103">SSortOrderSet</span></span>

  
  
<span data-ttu-id="ecde1-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ecde1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ecde1-105">標準またはカテゴリ別に並べ替えに使用されるテーブルの並べ替えキーのコレクションを定義します。</span><span class="sxs-lookup"><span data-stu-id="ecde1-105">Defines a collection of sort keys for a table that is used for standard or categorized sorting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ecde1-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ecde1-106">Header file:</span></span>  <br/> |<span data-ttu-id="ecde1-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ecde1-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ecde1-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="ecde1-108">Related macros:</span></span>  <br/> |<span data-ttu-id="ecde1-109">[CbNewSSortOrderSet](cbnewssortorderset.md)、 [CbSSortOrderSet](cbssortorderset.md)、 [SizedSSortOrderSet](sizedssortorderset.md)</span><span class="sxs-lookup"><span data-stu-id="ecde1-109">[CbNewSSortOrderSet](cbnewssortorderset.md), [CbSSortOrderSet](cbssortorderset.md), [SizedSSortOrderSet](sizedssortorderset.md)</span></span> <br/> |
   
```cpp
typedef struct _SSortOrderSet
{
  ULONG cSorts;
  ULONG cCategories;
  ULONG cExpanded;
  SSortOrder aSort[MAPI_DIM];
} SSortOrderSet, FAR *LPSSortOrderSet;

```

## <a name="members"></a><span data-ttu-id="ecde1-110">Members</span><span class="sxs-lookup"><span data-stu-id="ecde1-110">Members</span></span>

 <span data-ttu-id="ecde1-111">**cSorts**</span><span class="sxs-lookup"><span data-stu-id="ecde1-111">**cSorts**</span></span>
  
> <span data-ttu-id="ecde1-112">**ASort**メンバーに含まれる[SSortOrder](ssortorder.md)構造体の数です。</span><span class="sxs-lookup"><span data-stu-id="ecde1-112">Count of [SSortOrder](ssortorder.md) structures that are included in the **aSort** member.</span></span> 
    
 <span data-ttu-id="ecde1-113">**cCategories**</span><span class="sxs-lookup"><span data-stu-id="ecde1-113">**cCategories**</span></span>
  
> <span data-ttu-id="ecde1-114">カテゴリの列として指定されている列の数。</span><span class="sxs-lookup"><span data-stu-id="ecde1-114">Count of columns that are designated as category columns.</span></span> <span data-ttu-id="ecde1-115">使用可能な値の範囲は、分類なし] または [標準の並べ替えを示す、ゼロから**cSorts**のメンバーによって指定された番号です。</span><span class="sxs-lookup"><span data-stu-id="ecde1-115">Possible values range from zero, which indicates a non-categorized or standard sort, to the number indicated by the **cSorts** member.</span></span> 
    
 <span data-ttu-id="ecde1-116">**cExpanded**</span><span class="sxs-lookup"><span data-stu-id="ecde1-116">**cExpanded**</span></span>
  
> <span data-ttu-id="ecde1-117">すべてのカテゴリに該当する行がテーブル ビューに表示される、展開した状態で始まる分類の数です。</span><span class="sxs-lookup"><span data-stu-id="ecde1-117">Count of categories that start in an expanded state, where all of the rows that apply to the category are visible in the table view.</span></span> <span data-ttu-id="ecde1-118">使用可能な値の範囲は、0 から**cCategories**で指定された番号です。</span><span class="sxs-lookup"><span data-stu-id="ecde1-118">Possible values range from 0 to the number indicated by **cCategories**.</span></span>
    
 <span data-ttu-id="ecde1-119">**aSort**</span><span class="sxs-lookup"><span data-stu-id="ecde1-119">**aSort**</span></span>
  
> <span data-ttu-id="ecde1-120">並べ替え順序を定義する各**SSortOrder**の構造体の配列です。</span><span class="sxs-lookup"><span data-stu-id="ecde1-120">Array of **SSortOrder** structures, each defining a sort order.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ecde1-121">注釈</span><span class="sxs-lookup"><span data-stu-id="ecde1-121">Remarks</span></span>

<span data-ttu-id="ecde1-122">**SSortOrderSet**構造体は、標準的なカテゴリ別に並べ替えのさまざまな並べ替え順序を定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ecde1-122">A **SSortOrderSet** structure is used for defining multiple sort orders for standard and categorized sorting.</span></span> 
  
<span data-ttu-id="ecde1-123">**SSortOrderSet**の各構造体には、並べ替えと並べ替えキーとして使用される列の方向を定義するには、少なくとも 1 つの**SSortOrder**構造が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ecde1-123">Each **SSortOrderSet** structure contains at least one **SSortOrder** structure defining the direction of the sort and the column that will be used as the sort key.</span></span> <span data-ttu-id="ecde1-124">カテゴリ別の並べ替えでは、この列がカテゴリとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="ecde1-124">For categorized sorting, this column is used as the category.</span></span> <span data-ttu-id="ecde1-125">**CSorts**メンバーの値は、 **cCategories**メンバーの値を超えているとカテゴリより多くの並べ替えキーがあるカテゴリは、 **SSortOrder**配列の最初に表示される列から作成されます。</span><span class="sxs-lookup"><span data-stu-id="ecde1-125">When the value of the **cSorts** member exceeds the value of the **cCategories** member, there are more sort keys than categories, and categories are created from the columns that appear first in the **SSortOrder** array.</span></span> 
  
<span data-ttu-id="ecde1-126">などの**cSorts**を 3 に設定し、 **cCategories**が 2 に設定されて、する場合は、 **SSortOrder**配列内の最初の 2 つのエントリの**ulPropTag**のメンバーが記載されている列がカテゴリの列として使用されます。</span><span class="sxs-lookup"><span data-stu-id="ecde1-126">For example, if **cSorts** is set to 3 and **cCategories** is set to 2, the columns described by the **ulPropTag** member of the first two entries in the **SSortOrder** array are used as the category columns.</span></span> <span data-ttu-id="ecde1-127">最初のエントリは、グループ化は最上位のカテゴリとして機能します。セカンダリ ・ グループと 2 番目のエントリです。</span><span class="sxs-lookup"><span data-stu-id="ecde1-127">The first entry serves as the top-level category grouping; the second entry as the secondary grouping.</span></span> <span data-ttu-id="ecde1-128">3 番目のエントリで定義されている並べ替えキーを使用してすべての列の 2 つのカテゴリと一致する行が並べ替えられます。</span><span class="sxs-lookup"><span data-stu-id="ecde1-128">All of the rows that match the two category columns are sorted by using the sort key defined in the third entry.</span></span> 
  
<span data-ttu-id="ecde1-129">**CExpanded**メンバーは、最初に展開される項目の数を指定します。</span><span class="sxs-lookup"><span data-stu-id="ecde1-129">The **cExpanded** member specifies the number of categories that are at first expanded.</span></span> <span data-ttu-id="ecde1-130">複数のカテゴリが存在する場合、テーブルの実装から始まり、カテゴリとして指定するのには、最初の列、まで、それ以降のカテゴリ列に順番に**cCategories**の数を超えています。</span><span class="sxs-lookup"><span data-stu-id="ecde1-130">When there are multiple categories, the table implementation starts with the first column to be designated as a category and continues in sequential order with the subsequent category columns until the number of **cCategories** has been exceeded.</span></span> <span data-ttu-id="ecde1-131">拡張された列の数よりも多くのカテゴリの列がある場合は、カテゴリの列が折りたたまれます。</span><span class="sxs-lookup"><span data-stu-id="ecde1-131">If there are more category columns than there are expanded columns, the category columns are collapsed.</span></span> <span data-ttu-id="ecde1-132">**CExpanded**がゼロに等しい場合は、最上位レベルの見出しの行だけが表示のテーブルのユーザーが利用できます。</span><span class="sxs-lookup"><span data-stu-id="ecde1-132">If **cExpanded** is equal to zero, only the top level heading row is available to the table user for display.</span></span> <span data-ttu-id="ecde1-133">**CExpanded**の項目の数より 1 小さい値に等しい場合、し、すべての見出し行とリーフ行の [なし] を利用できます。</span><span class="sxs-lookup"><span data-stu-id="ecde1-133">If **cExpanded** is equal to one less than the number of categories, then all of the heading rows and none of the leaf rows are available.</span></span> <span data-ttu-id="ecde1-134">**CExpanded**は、カテゴリの数に等しく、し、テーブルは完全に展開します。</span><span class="sxs-lookup"><span data-stu-id="ecde1-134">If **cExpanded** is equal to the number of categories, then the table is fully expanded.</span></span> 
  
<span data-ttu-id="ecde1-135">詳細については、標準的なカテゴリ別に並べ替え、[並べ替えや分類](sorting-and-categorization.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ecde1-135">For more information about standard and categorized sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ecde1-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="ecde1-136">See also</span></span>



[<span data-ttu-id="ecde1-137">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="ecde1-137">SSortOrder</span></span>](ssortorder.md)
  
[<span data-ttu-id="ecde1-138">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="ecde1-138">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
  
[<span data-ttu-id="ecde1-139">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="ecde1-139">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)


[<span data-ttu-id="ecde1-140">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="ecde1-140">MAPI Structures</span></span>](mapi-structures.md)

