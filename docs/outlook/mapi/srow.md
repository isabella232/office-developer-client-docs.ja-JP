---
title: SRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRow
api_type:
- COM
ms.assetid: 369c2d5c-8c2b-4314-9cb2-aaa89580aa2b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2e75bc6f8e14258787a6c9d80dfbf6334ec698b4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410435"
---
# <a name="srow"></a><span data-ttu-id="7a4d6-103">SRow</span><span class="sxs-lookup"><span data-stu-id="7a4d6-103">SRow</span></span>

<span data-ttu-id="7a4d6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a4d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a4d6-105">特定のオブジェクトの選択したプロパティを含むテーブルの行について説明します。</span><span class="sxs-lookup"><span data-stu-id="7a4d6-105">Describes a row from a table that contains selected properties for a specific object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7a4d6-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="7a4d6-106">Header file:</span></span>  <br/> |<span data-ttu-id="7a4d6-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7a4d6-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRow
{
  ULONG ulAdrEntryPad;
  ULONG cValues;
  LPSPropValue lpProps;
} SRow, FAR *LPSRow;

```

## <a name="members"></a><span data-ttu-id="7a4d6-108">Members</span><span class="sxs-lookup"><span data-stu-id="7a4d6-108">Members</span></span>

<span data-ttu-id="7a4d6-109">**ulAdrEntryPad**</span><span class="sxs-lookup"><span data-stu-id="7a4d6-109">**ulAdrEntryPad**</span></span>
  
> <span data-ttu-id="7a4d6-110">lpProps メンバーが指すプロパティ値を適切に揃える埋 **め込みバイト** 。</span><span class="sxs-lookup"><span data-stu-id="7a4d6-110">Padding bytes to properly align the property values pointed to by the **lpProps** member.</span></span> 
    
<span data-ttu-id="7a4d6-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="7a4d6-111">**cValues**</span></span>
  
> <span data-ttu-id="7a4d6-112">lpProps が指すプロパティ **値の数** です。</span><span class="sxs-lookup"><span data-stu-id="7a4d6-112">Count of property values pointed to by **lpProps**.</span></span> 
    
<span data-ttu-id="7a4d6-113">**lpProps**</span><span class="sxs-lookup"><span data-stu-id="7a4d6-113">**lpProps**</span></span>
  
> <span data-ttu-id="7a4d6-114">行内の列のプロパティ値を記述する [SPropValue](spropvalue.md) 構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7a4d6-114">Pointer to an array of [SPropValue](spropvalue.md) structures that describe the property values for the columns in the row.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7a4d6-115">注釈</span><span class="sxs-lookup"><span data-stu-id="7a4d6-115">Remarks</span></span>

<span data-ttu-id="7a4d6-116">**SRow 構造体は**、テーブル内の行を表します。</span><span class="sxs-lookup"><span data-stu-id="7a4d6-116">An **SRow** structure describes a row in a table.</span></span> <span data-ttu-id="7a4d6-117">これは、テーブル通知に [TABLE_NOTIFICATION](table_notification.md) の構造に含まれています。</span><span class="sxs-lookup"><span data-stu-id="7a4d6-117">It is included in the [TABLE_NOTIFICATION](table_notification.md) structure that accompanies a table notification.</span></span> 
  
<span data-ttu-id="7a4d6-118">**SRow** 構造体は、次のメソッドで使用されます。</span><span class="sxs-lookup"><span data-stu-id="7a4d6-118">**SRow** structures are used in the following methods:</span></span> 
  
- [<span data-ttu-id="7a4d6-119">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="7a4d6-119">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
    
- [<span data-ttu-id="7a4d6-120">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="7a4d6-120">IAddrBook::SetSearchPath</span></span>](iaddrbook-setsearchpath.md)
    
- [<span data-ttu-id="7a4d6-121">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="7a4d6-121">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
    
- [<span data-ttu-id="7a4d6-122">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="7a4d6-122">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- <span data-ttu-id="7a4d6-123">[ITableData : IUnknown](itabledataiunknown.md) (多くのメソッド)</span><span class="sxs-lookup"><span data-stu-id="7a4d6-123">[ITableData : IUnknown](itabledataiunknown.md) (many methods)</span></span> 
    
- [<span data-ttu-id="7a4d6-124">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="7a4d6-124">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="7a4d6-125">FreeProws</span><span class="sxs-lookup"><span data-stu-id="7a4d6-125">FreeProws</span></span>](freeprows.md)
    
- [<span data-ttu-id="7a4d6-126">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="7a4d6-126">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
<span data-ttu-id="7a4d6-127">複数の行を記述する必要がある場合は [、SRowSet](srowset.md) 構造体が使用されます。</span><span class="sxs-lookup"><span data-stu-id="7a4d6-127">When more than one row needs to be described, an [SRowSet](srowset.md) structure is used.</span></span> <span data-ttu-id="7a4d6-128">**SRowSet 構造体** には **、SRow** 構造体の配列と配列内の構造体の数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7a4d6-128">An **SRowSet** structure contains an array of **SRow** structures and a count of structures in the array.</span></span> 
  
<span data-ttu-id="7a4d6-129">次の図は **、SRow** と **SRowSet データ構造の関係を** 示しています。</span><span class="sxs-lookup"><span data-stu-id="7a4d6-129">The following illustration shows the relationship between an **SRow** and an **SRowSet** data structure.</span></span> 
  
<span data-ttu-id="7a4d6-130">**SRow と SRowSet の関係**</span><span class="sxs-lookup"><span data-stu-id="7a4d6-130">**Relationship between SRow and SRowSet**</span></span>
  
<span data-ttu-id="7a4d6-131">![SRow と SRowSet の SRow と SRowSet](media/amapi_17.gif "")のリレーションシップ</span><span class="sxs-lookup"><span data-stu-id="7a4d6-131">![Relationship between SRow and SRowSet](media/amapi_17.gif "Relationship between SRow and SRowSet")</span></span>
  
<span data-ttu-id="7a4d6-132">**SRow** 構造体は [ADRENTRY 構造体と同じ定義](adrentry.md) です。</span><span class="sxs-lookup"><span data-stu-id="7a4d6-132">**SRow** structures are defined the same as [ADRENTRY](adrentry.md) structures.</span></span> <span data-ttu-id="7a4d6-133">したがって、受信者テーブルの行とアドレス一覧内のエントリを同じように処理できます。</span><span class="sxs-lookup"><span data-stu-id="7a4d6-133">Therefore, a row of a recipient table and an entry in an address list can be treated the same.</span></span> 
  
<span data-ttu-id="7a4d6-134">**SRow** 構造体のメモリを割り当てる方法については [、「ADRLIST および SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)構造体のメモリの管理」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7a4d6-134">For information about how the memory for **SRow** structures should be allocated, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7a4d6-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="7a4d6-135">See also</span></span>

- [<span data-ttu-id="7a4d6-136">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="7a4d6-136">ADRENTRY</span></span>](adrentry.md)
- [<span data-ttu-id="7a4d6-137">SPropValue</span><span class="sxs-lookup"><span data-stu-id="7a4d6-137">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="7a4d6-138">SRowSet</span><span class="sxs-lookup"><span data-stu-id="7a4d6-138">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="7a4d6-139">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7a4d6-139">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="7a4d6-140">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="7a4d6-140">MAPI Structures</span></span>](mapi-structures.md)
- [<span data-ttu-id="7a4d6-141">ADRLIST および SRowSet 構造体のメモリの管理</span><span class="sxs-lookup"><span data-stu-id="7a4d6-141">Managing Memory for ADRLIST and SRowSet Structures</span></span>](managing-memory-for-adrlist-and-srowset-structures.md)

