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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8b4e090b3dd6bf8ecd2517dee57093106147e22d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804004"
---
# <a name="srow"></a><span data-ttu-id="18e6f-103">SRow</span><span class="sxs-lookup"><span data-stu-id="18e6f-103">SRow</span></span>

<span data-ttu-id="18e6f-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="18e6f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="18e6f-105">特定のオブジェクトの選択したプロパティを含むテーブルから行を説明します。</span><span class="sxs-lookup"><span data-stu-id="18e6f-105">Describes a row from a table that contains selected properties for a specific object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="18e6f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="18e6f-106">Header file:</span></span>  <br/> |<span data-ttu-id="18e6f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="18e6f-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRow
{
  ULONG ulAdrEntryPad;
  ULONG cValues;
  LPSPropValue lpProps;
} SRow, FAR *LPSRow;

```

## <a name="members"></a><span data-ttu-id="18e6f-108">Members</span><span class="sxs-lookup"><span data-stu-id="18e6f-108">Members</span></span>

<span data-ttu-id="18e6f-109">**ulAdrEntryPad**</span><span class="sxs-lookup"><span data-stu-id="18e6f-109">**ulAdrEntryPad**</span></span>
  
> <span data-ttu-id="18e6f-110">埋め込みプロパティの値を正しく配置するのにはバイトで示される**lpProps**のメンバーです。</span><span class="sxs-lookup"><span data-stu-id="18e6f-110">Padding bytes to properly align the property values pointed to by the **lpProps** member.</span></span> 
    
<span data-ttu-id="18e6f-111">**あう**</span><span class="sxs-lookup"><span data-stu-id="18e6f-111">**cValues**</span></span>
  
> <span data-ttu-id="18e6f-112">**LpProps**で指定されたプロパティ値の数。</span><span class="sxs-lookup"><span data-stu-id="18e6f-112">Count of property values pointed to by **lpProps**.</span></span> 
    
<span data-ttu-id="18e6f-113">**lpProps**</span><span class="sxs-lookup"><span data-stu-id="18e6f-113">**lpProps**</span></span>
  
> <span data-ttu-id="18e6f-114">行の列のプロパティ値を記述する[SPropValue](spropvalue.md)構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="18e6f-114">Pointer to an array of [SPropValue](spropvalue.md) structures that describe the property values for the columns in the row.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="18e6f-115">注釈</span><span class="sxs-lookup"><span data-stu-id="18e6f-115">Remarks</span></span>

<span data-ttu-id="18e6f-116">**SRow**構造体では、テーブル内の行について説明します。</span><span class="sxs-lookup"><span data-stu-id="18e6f-116">An **SRow** structure describes a row in a table.</span></span> <span data-ttu-id="18e6f-117">それはテーブルの通知に付随する[TABLE_NOTIFICATION](table_notification.md)構造体に含まれます。</span><span class="sxs-lookup"><span data-stu-id="18e6f-117">It is included in the [TABLE_NOTIFICATION](table_notification.md) structure that accompanies a table notification.</span></span> 
  
<span data-ttu-id="18e6f-118">**SRow**構造体は、次の方法で使用されます。</span><span class="sxs-lookup"><span data-stu-id="18e6f-118">**SRow** structures are used in the following methods:</span></span> 
  
- [<span data-ttu-id="18e6f-119">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="18e6f-119">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
    
- [<span data-ttu-id="18e6f-120">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="18e6f-120">IAddrBook::SetSearchPath</span></span>](iaddrbook-setsearchpath.md)
    
- [<span data-ttu-id="18e6f-121">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="18e6f-121">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
    
- [<span data-ttu-id="18e6f-122">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="18e6f-122">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- <span data-ttu-id="18e6f-123">[ITableData: IUnknown](itabledataiunknown.md)(多くの方法)</span><span class="sxs-lookup"><span data-stu-id="18e6f-123">[ITableData : IUnknown](itabledataiunknown.md) (many methods)</span></span> 
    
- [<span data-ttu-id="18e6f-124">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="18e6f-124">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="18e6f-125">FreeProws</span><span class="sxs-lookup"><span data-stu-id="18e6f-125">FreeProws</span></span>](freeprows.md)
    
- [<span data-ttu-id="18e6f-126">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="18e6f-126">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
<span data-ttu-id="18e6f-127">複数の行を説明する必要がある、 [SRowSet](srowset.md)構造体が使用されます。</span><span class="sxs-lookup"><span data-stu-id="18e6f-127">When more than one row needs to be described, an [SRowSet](srowset.md) structure is used.</span></span> <span data-ttu-id="18e6f-128">**SRowSet**構造体には、 **SRow**構造体の配列と、配列内の構造体の数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="18e6f-128">An **SRowSet** structure contains an array of **SRow** structures and a count of structures in the array.</span></span> 
  
<span data-ttu-id="18e6f-129">**SRow**と**SRowSet**のデータ構造間の関係を次の図に示します。</span><span class="sxs-lookup"><span data-stu-id="18e6f-129">The following illustration shows the relationship between an **SRow** and an **SRowSet** data structure.</span></span> 
  
<span data-ttu-id="18e6f-130">**SRow と SRowSet の関係**</span><span class="sxs-lookup"><span data-stu-id="18e6f-130">**Relationship between SRow and SRowSet**</span></span>
  
<span data-ttu-id="18e6f-131">![SRow と SRowSet との関係](media/amapi_17.gif "SRow と SRowSet との関係")</span><span class="sxs-lookup"><span data-stu-id="18e6f-131">![Relationship between SRow and SRowSet](media/amapi_17.gif "Relationship between SRow and SRowSet")</span></span>
  
<span data-ttu-id="18e6f-132">**SRow**構造体が定義されている[ADRENTRY](adrentry.md)構造体と同じです。</span><span class="sxs-lookup"><span data-stu-id="18e6f-132">**SRow** structures are defined the same as [ADRENTRY](adrentry.md) structures.</span></span> <span data-ttu-id="18e6f-133">受信者テーブルと、[アドレス] ボックスの一覧内のエントリの行は、そのため、同じに扱われます。</span><span class="sxs-lookup"><span data-stu-id="18e6f-133">Therefore, a row of a recipient table and an entry in an address list can be treated the same.</span></span> 
  
<span data-ttu-id="18e6f-134">**SRow**構造体のメモリの割り当て方法については、 [ADRLIST および SRowSet 構造体のメモリを管理する](managing-memory-for-adrlist-and-srowset-structures.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="18e6f-134">For information about how the memory for **SRow** structures should be allocated, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="18e6f-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="18e6f-135">See also</span></span>

- [<span data-ttu-id="18e6f-136">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="18e6f-136">ADRENTRY</span></span>](adrentry.md)
- [<span data-ttu-id="18e6f-137">SPropValue</span><span class="sxs-lookup"><span data-stu-id="18e6f-137">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="18e6f-138">SRowSet</span><span class="sxs-lookup"><span data-stu-id="18e6f-138">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="18e6f-139">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="18e6f-139">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="18e6f-140">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="18e6f-140">MAPI Structures</span></span>](mapi-structures.md)
- [<span data-ttu-id="18e6f-141">ADRLIST および SRowSet 構造のためのメモリ管理</span><span class="sxs-lookup"><span data-stu-id="18e6f-141">Managing Memory for ADRLIST and SRowSet Structures</span></span>](managing-memory-for-adrlist-and-srowset-structures.md)

