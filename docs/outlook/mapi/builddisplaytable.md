---
title: BuildDisplayTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BuildDisplayTable
api_type:
- HeaderDef
ms.assetid: 0846415b-6fe1-4504-8620-108af6719015
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8c5e6078be05ff846b7737ff53e9a6338fcb2141
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318096"
---
# <a name="builddisplaytable"></a><span data-ttu-id="0f704-103">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="0f704-103">BuildDisplayTable</span></span>

  
  
<span data-ttu-id="0f704-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f704-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f704-105">1つ以上の[dtpage](dtpage.md)構造に含まれるプロパティページデータから、表示テーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="0f704-105">Creates a display table from the property page data contained in one or more [DTPAGE](dtpage.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0f704-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0f704-106">Header file:</span></span>  <br/> |<span data-ttu-id="0f704-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="0f704-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0f704-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="0f704-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0f704-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0f704-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0f704-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="0f704-110">Called by:</span></span>  <br/> |<span data-ttu-id="0f704-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="0f704-111">Service providers</span></span>  <br/> |
   
```cpp
STDAPI BuildDisplayTable(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  LPMALLOC lpMalloc,
  HINSTANCE hInstance,
  UINT cPages,
  LPDTPAGE lpPage,
  ULONG ulFlags,
  LPMAPITABLE * lppTable,
  LPTABLEDATA * lppTblData
);
```

## <a name="parameters"></a><span data-ttu-id="0f704-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0f704-112">Parameters</span></span>

 <span data-ttu-id="0f704-113">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="0f704-113">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="0f704-114">順番メモリの割り当てに使用される[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0f704-114">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="0f704-115">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="0f704-115">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="0f704-116">順番追加のメモリを割り当てるために使用される[MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0f704-116">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="0f704-117">_lpfreebuffer_</span><span class="sxs-lookup"><span data-stu-id="0f704-117">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="0f704-118">順番メモリを解放するために使用される[MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0f704-118">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="0f704-119">_lpmalloc_</span><span class="sxs-lookup"><span data-stu-id="0f704-119">_lpMalloc_</span></span>
  
> <span data-ttu-id="0f704-120">使用NULL に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f704-120">Unused; should be set to NULL.</span></span> 
    
 <span data-ttu-id="0f704-121">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="0f704-121">_hInstance_</span></span>
  
> <span data-ttu-id="0f704-122">順番**builddisplaytable**がリソースを取得する MAPI オブジェクトのインスタンス。</span><span class="sxs-lookup"><span data-stu-id="0f704-122">[in] An instance of a MAPI object from which **BuildDisplayTable** retrieves resources.</span></span> 
    
 <span data-ttu-id="0f704-123">_cpages_</span><span class="sxs-lookup"><span data-stu-id="0f704-123">_cPages_</span></span>
  
> <span data-ttu-id="0f704-124">順番_lppage_パラメーターで指定された配列内の[dtpage](dtpage.md)構造体の数。</span><span class="sxs-lookup"><span data-stu-id="0f704-124">[in] Count of [DTPAGE](dtpage.md) structures in the array pointed to by the  _lpPage_ parameter.</span></span> 
    
 <span data-ttu-id="0f704-125">_lppage_</span><span class="sxs-lookup"><span data-stu-id="0f704-125">_lpPage_</span></span>
  
> <span data-ttu-id="0f704-126">順番作成するテーブルの表示ページに関する情報を含む**dtpage**構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0f704-126">[in] Pointer to an array of **DTPAGE** structures that contain information about the display table pages to be built.</span></span> 
    
 <span data-ttu-id="0f704-127">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0f704-127">_ulFlags_</span></span>
  
> <span data-ttu-id="0f704-128">順番フラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="0f704-128">[in] Bitmask of flags.</span></span> <span data-ttu-id="0f704-129">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="0f704-129">The following flag can be set:</span></span>
    
<span data-ttu-id="0f704-130">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0f704-130">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="0f704-131">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="0f704-131">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="0f704-132">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="0f704-132">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="0f704-133">_lpptable_</span><span class="sxs-lookup"><span data-stu-id="0f704-133">_lppTable_</span></span>
  
> <span data-ttu-id="0f704-134">読み上げ表示テーブルへのポインターへのポインター。これには[IMAPITable](imapitableiunknown.md)インターフェイスが公開されます。</span><span class="sxs-lookup"><span data-stu-id="0f704-134">[out] Pointer to a pointer to the display table, which exposes the [IMAPITable](imapitableiunknown.md) interface.</span></span> 
    
 <span data-ttu-id="0f704-135">_lppTblData_</span><span class="sxs-lookup"><span data-stu-id="0f704-135">_lppTblData_</span></span>
  
> <span data-ttu-id="0f704-136">[入力]_lpptable_パラメーターで返されるテーブルの[itabledata](itabledataiunknown.md)インターフェイスを公開するテーブルデータオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="0f704-136">[in, out] Pointer to a pointer to a table data object exposing the [ITableData](itabledataiunknown.md) interface on the table returned in the  _lppTable_ parameter.</span></span> <span data-ttu-id="0f704-137">テーブルデータオブジェクトが必要ない場合は、ポインター値ではなく、 _lppTblData_を NULL に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f704-137">If no table data object is desired,  _lppTblData_ should be set to NULL instead of a pointer value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0f704-138">戻り値</span><span class="sxs-lookup"><span data-stu-id="0f704-138">Return value</span></span>

<span data-ttu-id="0f704-139">なし</span><span class="sxs-lookup"><span data-stu-id="0f704-139">None</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0f704-140">解説</span><span class="sxs-lookup"><span data-stu-id="0f704-140">Remarks</span></span>

<span data-ttu-id="0f704-141">MAPI では、特に、 _lpAllocateBuffer_、 _lpAllocateMore_、および_lpfreebuffer_が指す関数を使用して、オブジェクトインターフェイスを呼び出すときに使用するメモリをクライアントアプリケーションに割り当てます。[imapiprop:: GetProps](imapiprop-getprops.md) and [IMAPITable:: QueryRows](imapitable-queryrows.md)など。</span><span class="sxs-lookup"><span data-stu-id="0f704-141">MAPI uses the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0f704-142">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="0f704-142">Notes to callers</span></span>

<span data-ttu-id="0f704-143">考えられるすべての情報は、ダイアログリソースから読み取られます。次のようになります。</span><span class="sxs-lookup"><span data-stu-id="0f704-143">Everything possible is read from the dialog resource, including:</span></span>
  
- <span data-ttu-id="0f704-144">ページのタイトル。これは、リソースのダイアログタイトルから読み取る[dtblpage](dtblpage.md)構造の_ulblpszlabel_メンバーです。</span><span class="sxs-lookup"><span data-stu-id="0f704-144">The page title that is, the  _ulbLpszLabel_ member of the [DTBLPAGE](dtblpage.md) structure read from the dialog title in the resource.</span></span> 
    
- <span data-ttu-id="0f704-145">すべてのコントロールのタイトル。他のコントロール構造の_ulblpszlabel_メンバーは、リソースのコントロールテキストから読み取ります。</span><span class="sxs-lookup"><span data-stu-id="0f704-145">All control titles that is, the  _ulbLpszLabel_ members of other control structures read from the control text in the resource.</span></span> 
    
 <span data-ttu-id="0f704-146">**builddisplaytable**は、入力制御構造で渡されたものをダイアログリソースからの情報で上書きします。これは、 **builddisplaytable**の呼び出し元がページまたはコントロールのタイトルを動的に指定できないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="0f704-146">**BuildDisplayTable** overwrites anything passed in the input control structures with information from the dialog resource, which means the caller of **BuildDisplayTable** cannot dynamically specify page or control titles.</span></span> <span data-ttu-id="0f704-147">**builddisplaytable**を持つことができるようにする必要がある呼び出し元は、 _lppTableData_でテーブルデータオブジェクトを返し、その中の行を変更することができます。または、代わりにテーブルデータオブジェクトに手動で表示テーブルを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="0f704-147">Callers who need to do that can have **BuildDisplayTable** return the table data object in  _lppTableData_ and change rows in it; or they can build the display table by hand in a table data object instead.</span></span> 
  
<span data-ttu-id="0f704-148">_lppTableData_が NULL に設定されていない場合、プロバイダーは、表示テーブルの操作が完了したときに、テーブルデータオブジェクトを解放することを担当します。</span><span class="sxs-lookup"><span data-stu-id="0f704-148">If  _lppTableData_ is not set to NULL, the provider is responsible for freeing the table data object when it is finished with the display table.</span></span> 
  

