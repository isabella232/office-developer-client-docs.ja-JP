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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 5c634fe200dde4bfe6f190f8bfa9e5dfa0868db4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804017"
---
# <a name="srowset"></a><span data-ttu-id="e05d7-103">SRowSet</span><span class="sxs-lookup"><span data-stu-id="e05d7-103">SRowSet</span></span>

  
  
<span data-ttu-id="e05d7-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e05d7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e05d7-105">[SRow](srow.md)構造体の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e05d7-105">Contains an array of [SRow](srow.md) structures.</span></span> <span data-ttu-id="e05d7-106">各**SRow**構造体では、テーブルからの行について説明します。</span><span class="sxs-lookup"><span data-stu-id="e05d7-106">Each **SRow** structure describes a row from a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e05d7-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e05d7-107">Header file:</span></span>  <br/> |<span data-ttu-id="e05d7-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e05d7-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e05d7-109">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="e05d7-109">Related macros:</span></span>  <br/> |<span data-ttu-id="e05d7-110">[CbNewSRowSet](cbnewsrowset.md)、 [CbSRowSet](cbsrowset.md)、 [SizedSRowSet](sizedsrowset.md)</span><span class="sxs-lookup"><span data-stu-id="e05d7-110">[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md)</span></span> <br/> |
   
```cpp
typedef struct _SRowSet
{
  ULONG cRows;
  SRow aRow[MAPI_DIM];
} SRowSet, FAR *LPSRowSet;

```

## <a name="members"></a><span data-ttu-id="e05d7-111">Members</span><span class="sxs-lookup"><span data-stu-id="e05d7-111">Members</span></span>

 <span data-ttu-id="e05d7-112">**カラス**</span><span class="sxs-lookup"><span data-stu-id="e05d7-112">**cRows**</span></span>
  
> <span data-ttu-id="e05d7-113">**ARow**メンバーに**SRow**構造体の数です。</span><span class="sxs-lookup"><span data-stu-id="e05d7-113">Count of **SRow** structures in the **aRow** member.</span></span> 
    
 <span data-ttu-id="e05d7-114">**aRow**</span><span class="sxs-lookup"><span data-stu-id="e05d7-114">**aRow**</span></span>
  
> <span data-ttu-id="e05d7-115">**SRow**構造体の配列です。</span><span class="sxs-lookup"><span data-stu-id="e05d7-115">Array of **SRow** structures.</span></span> <span data-ttu-id="e05d7-116">テーブル内の行ごとに 1 つの構造があります。</span><span class="sxs-lookup"><span data-stu-id="e05d7-116">There is one structure for each row in the table.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e05d7-117">注釈</span><span class="sxs-lookup"><span data-stu-id="e05d7-117">Remarks</span></span>

<span data-ttu-id="e05d7-118">**SRowSet**構造体を使用して、複数のテーブルからデータ行を記述します。</span><span class="sxs-lookup"><span data-stu-id="e05d7-118">An **SRowSet** structure is used to describe multiple rows of data from a table.</span></span> <span data-ttu-id="e05d7-119">**SRowSet**構造体は、次の関数だけでなく、 [IAddrBook](iaddrbookimapiprop.md)、 [ITableData](itabledataiunknown.md)、および[IMAPITable](imapitableiunknown.md)インターフェイス メソッドで使用されます。</span><span class="sxs-lookup"><span data-stu-id="e05d7-119">**SRowSet** structures are used in the [IAddrBook](iaddrbookimapiprop.md), [ITableData](itabledataiunknown.md), and [IMAPITable](imapitableiunknown.md) interface methods, in addition to the following functions:</span></span> 
  
- [<span data-ttu-id="e05d7-120">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="e05d7-120">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
- [<span data-ttu-id="e05d7-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="e05d7-121">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="e05d7-122">FreeProws</span><span class="sxs-lookup"><span data-stu-id="e05d7-122">FreeProws</span></span>](freeprows.md)
    
 <span data-ttu-id="e05d7-123">**SRowSet**構造体を定義するアドレス一覧に受信者テーブルおよびエントリの行を許可する[ADRLIST](adrlist.md)構造体を同等に扱うのと同じです。</span><span class="sxs-lookup"><span data-stu-id="e05d7-123">**SRowSet** structures are defined the same as [ADRLIST](adrlist.md) structures to allow the rows of a recipient table and the entries in an address list to be treated the same.</span></span> <span data-ttu-id="e05d7-124">**SRowSet**構造体と構造体の**ADRLIST**の両方は、 [IMessage::ModifyRecipients](imessage-modifyrecipients.md)や[IAddrBook::Address](iaddrbook-address.md)などのメソッドに渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="e05d7-124">Both **SRowSet** structures and **ADRLIST** structures can be passed to methods such as [IMessage::ModifyRecipients](imessage-modifyrecipients.md) and [IAddrBook::Address](iaddrbook-address.md).</span></span> 
  
<span data-ttu-id="e05d7-125">また、 **SRowSet**構造体のメモリの割り当て規則は、 **ADRLIST**構造体の場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="e05d7-125">Also, the rules for memory allocation for **SRowSet** structures are the same as for **ADRLIST** structures.</span></span> <span data-ttu-id="e05d7-126">要約するは[MAPIAllocateBuffer](mapiallocatebuffer.md)を使用して個別に、行の行ごとの**lpProps**のメンバーによって設定するのには配列内の各[SPropValue](spropvalue.md)構造体を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="e05d7-126">To summarize, each [SPropValue](spropvalue.md) structure in the array pointed to by the **lpProps** member of each row in the row set must be allocated separately using [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span> <span data-ttu-id="e05d7-127">**SRowSet**構造の割り当てを解除する前に割り当てられた**SPropValue**構造体へのポインターが失われないように[MAPIFreeBuffer](mapifreebuffer.md)を使用して各プロパティ値の構造体を解放することもする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e05d7-127">Each property value structure must also be deallocated using [MAPIFreeBuffer](mapifreebuffer.md) before the deallocation of its **SRowSet** structure so that pointers to the allocated **SPropValue** structures are not lost.</span></span> <span data-ttu-id="e05d7-128">行のメモリが割り当てられているし、ある保持し、 **SRowSet**構造体のコンテキストの外部で再利用します。</span><span class="sxs-lookup"><span data-stu-id="e05d7-128">A row's allocated memory can then be preserved and reused outside the context of the **SRowSet** structure.</span></span> 
  
<span data-ttu-id="e05d7-129">**SRowSet**構造体のメモリの割り当て方法の詳細については、 [ADRLIST および SRowSet 構造体のメモリを管理する](managing-memory-for-adrlist-and-srowset-structures.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e05d7-129">For more information about how the memory for **SRowSet** structures should be allocated, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e05d7-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="e05d7-130">See also</span></span>



[<span data-ttu-id="e05d7-131">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="e05d7-131">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="e05d7-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="e05d7-132">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="e05d7-133">SRow</span><span class="sxs-lookup"><span data-stu-id="e05d7-133">SRow</span></span>](srow.md)
  
[<span data-ttu-id="e05d7-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="e05d7-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="e05d7-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e05d7-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="e05d7-136">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="e05d7-136">MAPI Structures</span></span>](mapi-structures.md)

