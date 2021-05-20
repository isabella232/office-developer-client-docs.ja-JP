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
# <a name="ssortorderset"></a><span data-ttu-id="6991e-103">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="6991e-103">SSortOrderSet</span></span>

  
  
<span data-ttu-id="6991e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6991e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6991e-105">標準または分類された並べ替えに使用されるテーブルの並べ替えキーのコレクションを定義します。</span><span class="sxs-lookup"><span data-stu-id="6991e-105">Defines a collection of sort keys for a table that is used for standard or categorized sorting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6991e-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="6991e-106">Header file:</span></span>  <br/> |<span data-ttu-id="6991e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6991e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="6991e-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="6991e-108">Related macros:</span></span>  <br/> |<span data-ttu-id="6991e-109">[CbNewSsortOrderSet](cbnewssortorderset.md)、 [CbSSortOrderSet](cbssortorderset.md)、 [sizedSsortOrderSet](sizedssortorderset.md)</span><span class="sxs-lookup"><span data-stu-id="6991e-109">[CbNewSSortOrderSet](cbnewssortorderset.md), [CbSSortOrderSet](cbssortorderset.md), [SizedSSortOrderSet](sizedssortorderset.md)</span></span> <br/> |
   
```cpp
typedef struct _SSortOrderSet
{
  ULONG cSorts;
  ULONG cCategories;
  ULONG cExpanded;
  SSortOrder aSort[MAPI_DIM];
} SSortOrderSet, FAR *LPSSortOrderSet;

```

## <a name="members"></a><span data-ttu-id="6991e-110">Members</span><span class="sxs-lookup"><span data-stu-id="6991e-110">Members</span></span>

 <span data-ttu-id="6991e-111">**cSorts**</span><span class="sxs-lookup"><span data-stu-id="6991e-111">**cSorts**</span></span>
  
> <span data-ttu-id="6991e-112">**aSort** メンバーに含まれる [SSortOrder](ssortorder.md)構造体の数。</span><span class="sxs-lookup"><span data-stu-id="6991e-112">Count of [SSortOrder](ssortorder.md) structures that are included in the **aSort** member.</span></span> 
    
 <span data-ttu-id="6991e-113">**cCategories**</span><span class="sxs-lookup"><span data-stu-id="6991e-113">**cCategories**</span></span>
  
> <span data-ttu-id="6991e-114">カテゴリ列として指定されている列の数。</span><span class="sxs-lookup"><span data-stu-id="6991e-114">Count of columns that are designated as category columns.</span></span> <span data-ttu-id="6991e-115">指定できる値の範囲は、分類されていない並べ替えまたは標準の並べ替えを示す **0 から、cSorts** メンバーによって示される番号です。</span><span class="sxs-lookup"><span data-stu-id="6991e-115">Possible values range from zero, which indicates a non-categorized or standard sort, to the number indicated by the **cSorts** member.</span></span> 
    
 <span data-ttu-id="6991e-116">**cExpanded**</span><span class="sxs-lookup"><span data-stu-id="6991e-116">**cExpanded**</span></span>
  
> <span data-ttu-id="6991e-117">展開された状態で開始するカテゴリの数。カテゴリに適用される行はすべてテーブル ビューに表示されます。</span><span class="sxs-lookup"><span data-stu-id="6991e-117">Count of categories that start in an expanded state, where all of the rows that apply to the category are visible in the table view.</span></span> <span data-ttu-id="6991e-118">指定できる値の範囲は、0 ~ **cCategories で示される数値です**。</span><span class="sxs-lookup"><span data-stu-id="6991e-118">Possible values range from 0 to the number indicated by **cCategories**.</span></span>
    
 <span data-ttu-id="6991e-119">**aSort**</span><span class="sxs-lookup"><span data-stu-id="6991e-119">**aSort**</span></span>
  
> <span data-ttu-id="6991e-120">並べ **替え順序を定義する SSortOrder** 構造体の配列。</span><span class="sxs-lookup"><span data-stu-id="6991e-120">Array of **SSortOrder** structures, each defining a sort order.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6991e-121">注釈</span><span class="sxs-lookup"><span data-stu-id="6991e-121">Remarks</span></span>

<span data-ttu-id="6991e-122">**SSortOrderSet** 構造体は、標準および分類された並べ替えに対して複数の並べ替え順序を定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="6991e-122">A **SSortOrderSet** structure is used for defining multiple sort orders for standard and categorized sorting.</span></span> 
  
<span data-ttu-id="6991e-123">各 **SSortOrderSet** 構造体には、並べ替えの方向と並べ替えキーとして使用される列を定義する **SSortOrder** 構造体が少なくとも 1 つ含まれる。</span><span class="sxs-lookup"><span data-stu-id="6991e-123">Each **SSortOrderSet** structure contains at least one **SSortOrder** structure defining the direction of the sort and the column that will be used as the sort key.</span></span> <span data-ttu-id="6991e-124">分類された並べ替えでは、この列がカテゴリとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="6991e-124">For categorized sorting, this column is used as the category.</span></span> <span data-ttu-id="6991e-125">**cSorts** メンバーの値が **cCategories** メンバーの値を超えると、カテゴリよりも並べ替えキーが多く **、SSortOrder** 配列の最初に表示される列からカテゴリが作成されます。</span><span class="sxs-lookup"><span data-stu-id="6991e-125">When the value of the **cSorts** member exceeds the value of the **cCategories** member, there are more sort keys than categories, and categories are created from the columns that appear first in the **SSortOrder** array.</span></span> 
  
<span data-ttu-id="6991e-126">たとえば **、cSorts** が 3 に設定され **、cCategories** が 2 に設定されている場合 **、SSortOrder** 配列の最初の 2 つのエントリの **ulPropTag** メンバーによって記述された列がカテゴリ列として使用されます。</span><span class="sxs-lookup"><span data-stu-id="6991e-126">For example, if **cSorts** is set to 3 and **cCategories** is set to 2, the columns described by the **ulPropTag** member of the first two entries in the **SSortOrder** array are used as the category columns.</span></span> <span data-ttu-id="6991e-127">最初のエントリは、トップ レベルのカテゴリ グループとして使用されます。2 番目のエントリをセカンダリ グループ化として指定します。</span><span class="sxs-lookup"><span data-stu-id="6991e-127">The first entry serves as the top-level category grouping; the second entry as the secondary grouping.</span></span> <span data-ttu-id="6991e-128">2 つのカテゴリ列に一致する行はすべて、3 番目のエントリで定義されている並べ替えキーを使用して並べ替えされます。</span><span class="sxs-lookup"><span data-stu-id="6991e-128">All of the rows that match the two category columns are sorted by using the sort key defined in the third entry.</span></span> 
  
<span data-ttu-id="6991e-129">**cExpanded メンバー** は、最初に展開されるカテゴリの数を指定します。</span><span class="sxs-lookup"><span data-stu-id="6991e-129">The **cExpanded** member specifies the number of categories that are at first expanded.</span></span> <span data-ttu-id="6991e-130">複数のカテゴリがある場合、テーブルの実装は、カテゴリとして指定される最初の列から始まり **、cCategories** の数を超えるまで、後続のカテゴリ列の順に続きます。</span><span class="sxs-lookup"><span data-stu-id="6991e-130">When there are multiple categories, the table implementation starts with the first column to be designated as a category and continues in sequential order with the subsequent category columns until the number of **cCategories** has been exceeded.</span></span> <span data-ttu-id="6991e-131">展開された列よりも多くのカテゴリ列がある場合、カテゴリ列は折りたたまれます。</span><span class="sxs-lookup"><span data-stu-id="6991e-131">If there are more category columns than there are expanded columns, the category columns are collapsed.</span></span> <span data-ttu-id="6991e-132">**cExpanded が** 0 に等しい場合、テーブル ユーザーが表示できるのは、トップ レベルの見出し行のみです。</span><span class="sxs-lookup"><span data-stu-id="6991e-132">If **cExpanded** is equal to zero, only the top level heading row is available to the table user for display.</span></span> <span data-ttu-id="6991e-133">**cExpanded が** カテゴリ数より 1 小さい場合、すべての見出し行とリーフ行は使用できません。</span><span class="sxs-lookup"><span data-stu-id="6991e-133">If **cExpanded** is equal to one less than the number of categories, then all of the heading rows and none of the leaf rows are available.</span></span> <span data-ttu-id="6991e-134">**cExpanded が** カテゴリの数と等しい場合、テーブルは完全に展開されます。</span><span class="sxs-lookup"><span data-stu-id="6991e-134">If **cExpanded** is equal to the number of categories, then the table is fully expanded.</span></span> 
  
<span data-ttu-id="6991e-135">標準の並べ替えと分類された並べ替えの詳細については、「並べ替え [と分類」を参照してください](sorting-and-categorization.md)。</span><span class="sxs-lookup"><span data-stu-id="6991e-135">For more information about standard and categorized sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6991e-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="6991e-136">See also</span></span>



[<span data-ttu-id="6991e-137">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="6991e-137">SSortOrder</span></span>](ssortorder.md)
  
[<span data-ttu-id="6991e-138">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="6991e-138">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
  
[<span data-ttu-id="6991e-139">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="6991e-139">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)


[<span data-ttu-id="6991e-140">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="6991e-140">MAPI Structures</span></span>](mapi-structures.md)

