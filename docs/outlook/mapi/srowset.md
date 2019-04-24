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
ms.openlocfilehash: 63cef6ef2bb26e8b723c60fe01dd6771aa070ae8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341637"
---
# <a name="srowset"></a><span data-ttu-id="f562d-103">SRowSet</span><span class="sxs-lookup"><span data-stu-id="f562d-103">SRowSet</span></span>

  
  
<span data-ttu-id="f562d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f562d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f562d-105">[srow](srow.md)構造の配列を格納します。</span><span class="sxs-lookup"><span data-stu-id="f562d-105">Contains an array of [SRow](srow.md) structures.</span></span> <span data-ttu-id="f562d-106">各**srow**構造は、テーブルの行について記述します。</span><span class="sxs-lookup"><span data-stu-id="f562d-106">Each **SRow** structure describes a row from a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f562d-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f562d-107">Header file:</span></span>  <br/> |<span data-ttu-id="f562d-108">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f562d-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f562d-109">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="f562d-109">Related macros:</span></span>  <br/> |<span data-ttu-id="f562d-110">[CbNewSRowSet](cbnewsrowset.md)、 [cbsrowset](cbsrowset.md)、 [sizedsrowset](sizedsrowset.md)</span><span class="sxs-lookup"><span data-stu-id="f562d-110">[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md)</span></span> <br/> |
   
```cpp
typedef struct _SRowSet
{
  ULONG cRows;
  SRow aRow[MAPI_DIM];
} SRowSet, FAR *LPSRowSet;

```

## <a name="members"></a><span data-ttu-id="f562d-111">Members</span><span class="sxs-lookup"><span data-stu-id="f562d-111">Members</span></span>

 <span data-ttu-id="f562d-112">**cRows**</span><span class="sxs-lookup"><span data-stu-id="f562d-112">**cRows**</span></span>
  
> <span data-ttu-id="f562d-113">**arow**メンバーの**srow**構造のカウント。</span><span class="sxs-lookup"><span data-stu-id="f562d-113">Count of **SRow** structures in the **aRow** member.</span></span> 
    
 <span data-ttu-id="f562d-114">**arow**</span><span class="sxs-lookup"><span data-stu-id="f562d-114">**aRow**</span></span>
  
> <span data-ttu-id="f562d-115">**srow**構造の配列。</span><span class="sxs-lookup"><span data-stu-id="f562d-115">Array of **SRow** structures.</span></span> <span data-ttu-id="f562d-116">表の各行には1つの構造があります。</span><span class="sxs-lookup"><span data-stu-id="f562d-116">There is one structure for each row in the table.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f562d-117">解説</span><span class="sxs-lookup"><span data-stu-id="f562d-117">Remarks</span></span>

<span data-ttu-id="f562d-118">**srowset**構造体は、テーブルの複数のデータ行を記述するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f562d-118">An **SRowSet** structure is used to describe multiple rows of data from a table.</span></span> <span data-ttu-id="f562d-119">**srowset**構造体は、次の関数に加えて、 [IAddrBook](iaddrbookimapiprop.md)、 [itabledata](itabledataiunknown.md)、および[IMAPITable](imapitableiunknown.md)インターフェイスメソッドで使用されます。</span><span class="sxs-lookup"><span data-stu-id="f562d-119">**SRowSet** structures are used in the [IAddrBook](iaddrbookimapiprop.md), [ITableData](itabledataiunknown.md), and [IMAPITable](imapitableiunknown.md) interface methods, in addition to the following functions:</span></span> 
  
- [<span data-ttu-id="f562d-120">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="f562d-120">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
- [<span data-ttu-id="f562d-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="f562d-121">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="f562d-122">FreeProws</span><span class="sxs-lookup"><span data-stu-id="f562d-122">FreeProws</span></span>](freeprows.md)
    
 <span data-ttu-id="f562d-123">**srowset**構造体は[adrlist](adrlist.md)構造体と同じように定義されており、受信者テーブルの行とアドレス一覧のエントリを同じように扱うことができます。</span><span class="sxs-lookup"><span data-stu-id="f562d-123">**SRowSet** structures are defined the same as [ADRLIST](adrlist.md) structures to allow the rows of a recipient table and the entries in an address list to be treated the same.</span></span> <span data-ttu-id="f562d-124">[IMessage:: modifyrecipients](imessage-modifyrecipients.md)および[IAddrBook:: Address](iaddrbook-address.md)などのメソッドには、 **srowset**構造体と**adrlist**構造体の両方を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="f562d-124">Both **SRowSet** structures and **ADRLIST** structures can be passed to methods such as [IMessage::ModifyRecipients](imessage-modifyrecipients.md) and [IAddrBook::Address](iaddrbook-address.md).</span></span> 
  
<span data-ttu-id="f562d-125">また、 **srowset**構造体のメモリ割り当ての規則は、 **adrlist**構造体の場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="f562d-125">Also, the rules for memory allocation for **SRowSet** structures are the same as for **ADRLIST** structures.</span></span> <span data-ttu-id="f562d-126">要約すると、 [MAPIAllocateBuffer](mapiallocatebuffer.md)を使用して、行セット内の各行の**lpprops**メンバが指す各[spropvalue](spropvalue.md)構造体を個別に割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="f562d-126">To summarize, each [SPropValue](spropvalue.md) structure in the array pointed to by the **lpProps** member of each row in the row set must be allocated separately using [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span> <span data-ttu-id="f562d-127">各プロパティ値構造体は、 **srowset**構造体を解放する前に[MAPIFreeBuffer](mapifreebuffer.md)を使用して割り当てを解除して、割り当てられた**spropvalue**構造体へのポインターが失われないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f562d-127">Each property value structure must also be deallocated using [MAPIFreeBuffer](mapifreebuffer.md) before the deallocation of its **SRowSet** structure so that pointers to the allocated **SPropValue** structures are not lost.</span></span> <span data-ttu-id="f562d-128">行の割り当てられたメモリは保持され、 **srowset**構造のコンテキスト外で再利用できます。</span><span class="sxs-lookup"><span data-stu-id="f562d-128">A row's allocated memory can then be preserved and reused outside the context of the **SRowSet** structure.</span></span> 
  
<span data-ttu-id="f562d-129">**srowset**構造体のメモリを割り当てる方法の詳細については、「 [adrlist および srowset 構造体のメモリの管理](managing-memory-for-adrlist-and-srowset-structures.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f562d-129">For more information about how the memory for **SRowSet** structures should be allocated, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f562d-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="f562d-130">See also</span></span>



[<span data-ttu-id="f562d-131">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="f562d-131">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="f562d-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="f562d-132">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="f562d-133">SRow</span><span class="sxs-lookup"><span data-stu-id="f562d-133">SRow</span></span>](srow.md)
  
[<span data-ttu-id="f562d-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="f562d-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="f562d-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f562d-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="f562d-136">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="f562d-136">MAPI Structures</span></span>](mapi-structures.md)

