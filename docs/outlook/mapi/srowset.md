---
title: SRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRowSet
api_type:
- COM
ms.assetid: 7e3761be-afd6-46cb-9a08-25e9016c1241
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 63cef6ef2bb26e8b723c60fe01dd6771aa070ae8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407257"
---
# <a name="srowset"></a><span data-ttu-id="372a7-103">SRowSet</span><span class="sxs-lookup"><span data-stu-id="372a7-103">SRowSet</span></span>

  
  
<span data-ttu-id="372a7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="372a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="372a7-105">SRow 構造体の [配列を格納](srow.md) します。</span><span class="sxs-lookup"><span data-stu-id="372a7-105">Contains an array of [SRow](srow.md) structures.</span></span> <span data-ttu-id="372a7-106">各 **SRow** 構造体は、テーブルの行を表します。</span><span class="sxs-lookup"><span data-stu-id="372a7-106">Each **SRow** structure describes a row from a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="372a7-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="372a7-107">Header file:</span></span>  <br/> |<span data-ttu-id="372a7-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="372a7-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="372a7-109">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="372a7-109">Related macros:</span></span>  <br/> |<span data-ttu-id="372a7-110">[CbNewSRowSet](cbnewsrowset.md)、 [CbSRowSet](cbsrowset.md)、 [SizedSRowSet](sizedsrowset.md)</span><span class="sxs-lookup"><span data-stu-id="372a7-110">[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md)</span></span> <br/> |
   
```cpp
typedef struct _SRowSet
{
  ULONG cRows;
  SRow aRow[MAPI_DIM];
} SRowSet, FAR *LPSRowSet;

```

## <a name="members"></a><span data-ttu-id="372a7-111">Members</span><span class="sxs-lookup"><span data-stu-id="372a7-111">Members</span></span>

 <span data-ttu-id="372a7-112">**cRows**</span><span class="sxs-lookup"><span data-stu-id="372a7-112">**cRows**</span></span>
  
> <span data-ttu-id="372a7-113">aRow **メンバー内** の **SRow 構造体の** 数。</span><span class="sxs-lookup"><span data-stu-id="372a7-113">Count of **SRow** structures in the **aRow** member.</span></span> 
    
 <span data-ttu-id="372a7-114">**aRow**</span><span class="sxs-lookup"><span data-stu-id="372a7-114">**aRow**</span></span>
  
> <span data-ttu-id="372a7-115">**SRow 構造体の** 配列。</span><span class="sxs-lookup"><span data-stu-id="372a7-115">Array of **SRow** structures.</span></span> <span data-ttu-id="372a7-116">テーブル内の行ごとに 1 つの構造があります。</span><span class="sxs-lookup"><span data-stu-id="372a7-116">There is one structure for each row in the table.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="372a7-117">注釈</span><span class="sxs-lookup"><span data-stu-id="372a7-117">Remarks</span></span>

<span data-ttu-id="372a7-118">**SRowSet 構造体は**、テーブルから複数行のデータを記述するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="372a7-118">An **SRowSet** structure is used to describe multiple rows of data from a table.</span></span> <span data-ttu-id="372a7-119">**SRowSet** 構造体は、次の機能に加えて [、IAddrBook、ITableData、](iaddrbookimapiprop.md)[および IMAPITable](imapitableiunknown.md)インターフェイス メソッドで使用されます。 [](itabledataiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="372a7-119">**SRowSet** structures are used in the [IAddrBook](iaddrbookimapiprop.md), [ITableData](itabledataiunknown.md), and [IMAPITable](imapitableiunknown.md) interface methods, in addition to the following functions:</span></span> 
  
- [<span data-ttu-id="372a7-120">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="372a7-120">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
- [<span data-ttu-id="372a7-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="372a7-121">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="372a7-122">FreeProws</span><span class="sxs-lookup"><span data-stu-id="372a7-122">FreeProws</span></span>](freeprows.md)
    
 <span data-ttu-id="372a7-123">**SRowSet** 構造体は、受信者テーブルの行とアドレス一覧内のエントリを同じ扱いを可能にするために [、ADRLIST](adrlist.md) 構造と同じように定義されます。</span><span class="sxs-lookup"><span data-stu-id="372a7-123">**SRowSet** structures are defined the same as [ADRLIST](adrlist.md) structures to allow the rows of a recipient table and the entries in an address list to be treated the same.</span></span> <span data-ttu-id="372a7-124">**SRowSet 構造体と** **ADRLIST** 構造体の両方を [、IMessage::ModifyRecipients](imessage-modifyrecipients.md)や [IAddrBook::Address などのメソッドに渡す場合があります](iaddrbook-address.md)。</span><span class="sxs-lookup"><span data-stu-id="372a7-124">Both **SRowSet** structures and **ADRLIST** structures can be passed to methods such as [IMessage::ModifyRecipients](imessage-modifyrecipients.md) and [IAddrBook::Address](iaddrbook-address.md).</span></span> 
  
<span data-ttu-id="372a7-125">また **、SRowSet** 構造体のメモリ割り当てのルールは **、ADRLIST 構造体の場合と同** じです。</span><span class="sxs-lookup"><span data-stu-id="372a7-125">Also, the rules for memory allocation for **SRowSet** structures are the same as for **ADRLIST** structures.</span></span> <span data-ttu-id="372a7-126">要約すると、行セット内の各行の **lpProps** メンバーが指す配列内の [各 SPropValue](spropvalue.md)構造体は [、MAPIAllocateBuffer](mapiallocatebuffer.md)を使用して個別に割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="372a7-126">To summarize, each [SPropValue](spropvalue.md) structure in the array pointed to by the **lpProps** member of each row in the row set must be allocated separately using [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span> <span data-ttu-id="372a7-127">各プロパティ値の構造体は、割り当てられた **SPropValue** 構造体へのポインターが失われずに **、SRowSet** 構造体の割り当て解除の前に [MAPIFreeBuffer](mapifreebuffer.md)を使用して割り当て解除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="372a7-127">Each property value structure must also be deallocated using [MAPIFreeBuffer](mapifreebuffer.md) before the deallocation of its **SRowSet** structure so that pointers to the allocated **SPropValue** structures are not lost.</span></span> <span data-ttu-id="372a7-128">その後、行の割り当てられたメモリを保持し **、SRowSet** 構造体のコンテキスト外で再利用できます。</span><span class="sxs-lookup"><span data-stu-id="372a7-128">A row's allocated memory can then be preserved and reused outside the context of the **SRowSet** structure.</span></span> 
  
<span data-ttu-id="372a7-129">**SRowSet** 構造体のメモリを割り当てる方法の詳細については [、「ADRLIST および SRowSet 構造体](managing-memory-for-adrlist-and-srowset-structures.md)のメモリの管理」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="372a7-129">For more information about how the memory for **SRowSet** structures should be allocated, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="372a7-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="372a7-130">See also</span></span>



[<span data-ttu-id="372a7-131">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="372a7-131">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="372a7-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="372a7-132">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="372a7-133">SRow</span><span class="sxs-lookup"><span data-stu-id="372a7-133">SRow</span></span>](srow.md)
  
[<span data-ttu-id="372a7-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="372a7-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="372a7-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="372a7-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="372a7-136">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="372a7-136">MAPI Structures</span></span>](mapi-structures.md)

