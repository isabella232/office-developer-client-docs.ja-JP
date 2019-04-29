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
# <a name="srow"></a><span data-ttu-id="b7acd-103">SRow</span><span class="sxs-lookup"><span data-stu-id="b7acd-103">SRow</span></span>

<span data-ttu-id="b7acd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7acd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7acd-105">特定のオブジェクトに対して選択されたプロパティを含むテーブルの行を記述します。</span><span class="sxs-lookup"><span data-stu-id="b7acd-105">Describes a row from a table that contains selected properties for a specific object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b7acd-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="b7acd-106">Header file:</span></span>  <br/> |<span data-ttu-id="b7acd-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b7acd-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRow
{
  ULONG ulAdrEntryPad;
  ULONG cValues;
  LPSPropValue lpProps;
} SRow, FAR *LPSRow;

```

## <a name="members"></a><span data-ttu-id="b7acd-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="b7acd-108">Members</span></span>

<span data-ttu-id="b7acd-109">**ulAdrEntryPad**</span><span class="sxs-lookup"><span data-stu-id="b7acd-109">**ulAdrEntryPad**</span></span>
  
> <span data-ttu-id="b7acd-110">**lpprops**メンバーが指すプロパティ値を適切に配置するためのパディングバイト。</span><span class="sxs-lookup"><span data-stu-id="b7acd-110">Padding bytes to properly align the property values pointed to by the **lpProps** member.</span></span> 
    
<span data-ttu-id="b7acd-111">**cvalues**</span><span class="sxs-lookup"><span data-stu-id="b7acd-111">**cValues**</span></span>
  
> <span data-ttu-id="b7acd-112">**lpprops**が指すプロパティ値の数。</span><span class="sxs-lookup"><span data-stu-id="b7acd-112">Count of property values pointed to by **lpProps**.</span></span> 
    
<span data-ttu-id="b7acd-113">**lpprops**</span><span class="sxs-lookup"><span data-stu-id="b7acd-113">**lpProps**</span></span>
  
> <span data-ttu-id="b7acd-114">行の列のプロパティ値を記述する[spropvalue](spropvalue.md)構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b7acd-114">Pointer to an array of [SPropValue](spropvalue.md) structures that describe the property values for the columns in the row.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b7acd-115">注釈</span><span class="sxs-lookup"><span data-stu-id="b7acd-115">Remarks</span></span>

<span data-ttu-id="b7acd-116">**srow**構造は、テーブル内の行について記述します。</span><span class="sxs-lookup"><span data-stu-id="b7acd-116">An **SRow** structure describes a row in a table.</span></span> <span data-ttu-id="b7acd-117">これは、テーブル通知に付随する[TABLE_NOTIFICATION](table_notification.md)構造に含まれています。</span><span class="sxs-lookup"><span data-stu-id="b7acd-117">It is included in the [TABLE_NOTIFICATION](table_notification.md) structure that accompanies a table notification.</span></span> 
  
<span data-ttu-id="b7acd-118">**srow**構造体は、次のメソッドで使用されます。</span><span class="sxs-lookup"><span data-stu-id="b7acd-118">**SRow** structures are used in the following methods:</span></span> 
  
- [<span data-ttu-id="b7acd-119">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="b7acd-119">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
    
- [<span data-ttu-id="b7acd-120">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="b7acd-120">IAddrBook::SetSearchPath</span></span>](iaddrbook-setsearchpath.md)
    
- [<span data-ttu-id="b7acd-121">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="b7acd-121">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
    
- [<span data-ttu-id="b7acd-122">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="b7acd-122">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- <span data-ttu-id="b7acd-123">[itabledata: IUnknown](itabledataiunknown.md)(多くのメソッド)</span><span class="sxs-lookup"><span data-stu-id="b7acd-123">[ITableData : IUnknown](itabledataiunknown.md) (many methods)</span></span> 
    
- [<span data-ttu-id="b7acd-124">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="b7acd-124">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="b7acd-125">FreeProws</span><span class="sxs-lookup"><span data-stu-id="b7acd-125">FreeProws</span></span>](freeprows.md)
    
- [<span data-ttu-id="b7acd-126">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="b7acd-126">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
<span data-ttu-id="b7acd-127">複数の行を記述する必要がある場合は、 [srowset](srowset.md)構造体を使用します。</span><span class="sxs-lookup"><span data-stu-id="b7acd-127">When more than one row needs to be described, an [SRowSet](srowset.md) structure is used.</span></span> <span data-ttu-id="b7acd-128">**srowset**構造体には、 **srowset**構造の配列と、配列内の構造体の数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b7acd-128">An **SRowSet** structure contains an array of **SRow** structures and a count of structures in the array.</span></span> 
  
<span data-ttu-id="b7acd-129">次の図は、 **srow**と**srow**データ構造の関係を示しています。</span><span class="sxs-lookup"><span data-stu-id="b7acd-129">The following illustration shows the relationship between an **SRow** and an **SRowSet** data structure.</span></span> 
  
<span data-ttu-id="b7acd-130">**SRow と SRowSet の関係**</span><span class="sxs-lookup"><span data-stu-id="b7acd-130">**Relationship between SRow and SRowSet**</span></span>
  
<span data-ttu-id="b7acd-131">![srow と srow の関係](media/amapi_17.gif "srow と srow の関係")</span><span class="sxs-lookup"><span data-stu-id="b7acd-131">![Relationship between SRow and SRowSet](media/amapi_17.gif "Relationship between SRow and SRowSet")</span></span>
  
<span data-ttu-id="b7acd-132">**srow**構造体は、 [adrentry](adrentry.md)構造と同じように定義されています。</span><span class="sxs-lookup"><span data-stu-id="b7acd-132">**SRow** structures are defined the same as [ADRENTRY](adrentry.md) structures.</span></span> <span data-ttu-id="b7acd-133">したがって、受信者テーブルの行とアドレス一覧のエントリは同じ処理を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="b7acd-133">Therefore, a row of a recipient table and an entry in an address list can be treated the same.</span></span> 
  
<span data-ttu-id="b7acd-134">**srow**構造のメモリを割り当てる方法については、「 [adrlist および srow 構造体のメモリの管理](managing-memory-for-adrlist-and-srowset-structures.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b7acd-134">For information about how the memory for **SRow** structures should be allocated, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b7acd-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="b7acd-135">See also</span></span>

- [<span data-ttu-id="b7acd-136">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="b7acd-136">ADRENTRY</span></span>](adrentry.md)
- [<span data-ttu-id="b7acd-137">SPropValue</span><span class="sxs-lookup"><span data-stu-id="b7acd-137">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="b7acd-138">SRowSet</span><span class="sxs-lookup"><span data-stu-id="b7acd-138">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="b7acd-139">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b7acd-139">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="b7acd-140">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="b7acd-140">MAPI Structures</span></span>](mapi-structures.md)
- [<span data-ttu-id="b7acd-141">adrlist および srowset 構造のためのメモリの管理</span><span class="sxs-lookup"><span data-stu-id="b7acd-141">Managing Memory for ADRLIST and SRowSet Structures</span></span>](managing-memory-for-adrlist-and-srowset-structures.md)

