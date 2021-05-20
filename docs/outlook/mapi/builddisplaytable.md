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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8c5e6078be05ff846b7737ff53e9a6338fcb2141
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431597"
---
# <a name="builddisplaytable"></a><span data-ttu-id="16f6e-103">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="16f6e-103">BuildDisplayTable</span></span>

  
  
<span data-ttu-id="16f6e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16f6e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16f6e-105">1 つ以上の DTPAGE 構造に含まれるプロパティ ページ データから表示テーブル [を作成](dtpage.md) します。</span><span class="sxs-lookup"><span data-stu-id="16f6e-105">Creates a display table from the property page data contained in one or more [DTPAGE](dtpage.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="16f6e-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="16f6e-106">Header file:</span></span>  <br/> |<span data-ttu-id="16f6e-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="16f6e-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="16f6e-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="16f6e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="16f6e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="16f6e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="16f6e-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="16f6e-110">Called by:</span></span>  <br/> |<span data-ttu-id="16f6e-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="16f6e-111">Service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="16f6e-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="16f6e-112">Parameters</span></span>

 <span data-ttu-id="16f6e-113">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="16f6e-113">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="16f6e-114">[in]メモリの割 [り当てに使用する MAPIAllocateBuffer](mapiallocatebuffer.md) 関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="16f6e-114">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="16f6e-115">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="16f6e-115">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="16f6e-116">[in]追加のメモリ [の割り当てに使用する MAPIAllocateMore](mapiallocatemore.md) 関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="16f6e-116">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="16f6e-117">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="16f6e-117">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="16f6e-118">[in]メモリを解放するために使用する [MAPIFreeBuffer](mapifreebuffer.md) 関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="16f6e-118">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="16f6e-119">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="16f6e-119">_lpMalloc_</span></span>
  
> <span data-ttu-id="16f6e-120">未使用。は NULL に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="16f6e-120">Unused; should be set to NULL.</span></span> 
    
 <span data-ttu-id="16f6e-121">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="16f6e-121">_hInstance_</span></span>
  
> <span data-ttu-id="16f6e-122">[in] **BuildDisplayTable** がリソースを取得する MAPI オブジェクトのインスタンス。</span><span class="sxs-lookup"><span data-stu-id="16f6e-122">[in] An instance of a MAPI object from which **BuildDisplayTable** retrieves resources.</span></span> 
    
 <span data-ttu-id="16f6e-123">_cPages_</span><span class="sxs-lookup"><span data-stu-id="16f6e-123">_cPages_</span></span>
  
> <span data-ttu-id="16f6e-124">[in]lpPage [パラメーターが指](dtpage.md) す配列内の  _DTPAGE 構造体の_ 数。</span><span class="sxs-lookup"><span data-stu-id="16f6e-124">[in] Count of [DTPAGE](dtpage.md) structures in the array pointed to by the  _lpPage_ parameter.</span></span> 
    
 <span data-ttu-id="16f6e-125">_lpPage_</span><span class="sxs-lookup"><span data-stu-id="16f6e-125">_lpPage_</span></span>
  
> <span data-ttu-id="16f6e-126">[in]作成する表示テーブル ページに関する情報を含む **DTPAGE** 構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="16f6e-126">[in] Pointer to an array of **DTPAGE** structures that contain information about the display table pages to be built.</span></span> 
    
 <span data-ttu-id="16f6e-127">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="16f6e-127">_ulFlags_</span></span>
  
> <span data-ttu-id="16f6e-128">[in]フラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="16f6e-128">[in] Bitmask of flags.</span></span> <span data-ttu-id="16f6e-129">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="16f6e-129">The following flag can be set:</span></span>
    
<span data-ttu-id="16f6e-130">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="16f6e-130">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="16f6e-131">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="16f6e-131">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="16f6e-132">このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="16f6e-132">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="16f6e-133">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="16f6e-133">_lppTable_</span></span>
  
> <span data-ttu-id="16f6e-134">[out] [IMAPITable](imapitableiunknown.md) インターフェイスを公開する表示テーブルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="16f6e-134">[out] Pointer to a pointer to the display table, which exposes the [IMAPITable](imapitableiunknown.md) interface.</span></span> 
    
 <span data-ttu-id="16f6e-135">_lppTblData_</span><span class="sxs-lookup"><span data-stu-id="16f6e-135">_lppTblData_</span></span>
  
> <span data-ttu-id="16f6e-136">[in, out]_lppTable_ パラメーターで返されるテーブルの [ITableData](itabledataiunknown.md)インターフェイスを公開するテーブル データ オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="16f6e-136">[in, out] Pointer to a pointer to a table data object exposing the [ITableData](itabledataiunknown.md) interface on the table returned in the  _lppTable_ parameter.</span></span> <span data-ttu-id="16f6e-137">テーブル データ オブジェクトが必要ない場合は、ポインター値の代わりに  _lppTblData_ を NULL に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="16f6e-137">If no table data object is desired,  _lppTblData_ should be set to NULL instead of a pointer value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="16f6e-138">戻り値</span><span class="sxs-lookup"><span data-stu-id="16f6e-138">Return value</span></span>

<span data-ttu-id="16f6e-139">なし</span><span class="sxs-lookup"><span data-stu-id="16f6e-139">None</span></span>
  
## <a name="remarks"></a><span data-ttu-id="16f6e-140">注釈</span><span class="sxs-lookup"><span data-stu-id="16f6e-140">Remarks</span></span>

<span data-ttu-id="16f6e-141">MAPI では、ほとんどのメモリ割り当ておよび割り当て解除に _lpAllocateBuffer_ _、lpAllocateMore、lpFreeBuffer_ が指す関数を使用して、特に [IMAPIProp::GetProps](imapiprop-getprops.md)や [IMAPITable::QueryRows](imapitable-queryrows.md)などのオブジェクト インターフェイスを呼び出す際にクライアント アプリケーションで使用するメモリを割り当てる。 </span><span class="sxs-lookup"><span data-stu-id="16f6e-141">MAPI uses the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="16f6e-142">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="16f6e-142">Notes to callers</span></span>

<span data-ttu-id="16f6e-143">可能な限り、次のダイアログ リソースから読み取り可能です。</span><span class="sxs-lookup"><span data-stu-id="16f6e-143">Everything possible is read from the dialog resource, including:</span></span>
  
- <span data-ttu-id="16f6e-144">[DTBLPAGE](dtblpage.md)構造の _ulbLpszLabel_ メンバーであるページ タイトルは、リソースのダイアログ タイトルから読み取ります。</span><span class="sxs-lookup"><span data-stu-id="16f6e-144">The page title that is, the  _ulbLpszLabel_ member of the [DTBLPAGE](dtblpage.md) structure read from the dialog title in the resource.</span></span> 
    
- <span data-ttu-id="16f6e-145">リソース内のコントロール テキストから読み取った他のコントロール構造の  _ulbLpszLabel_ メンバーであるすべてのコントロール タイトル。</span><span class="sxs-lookup"><span data-stu-id="16f6e-145">All control titles that is, the  _ulbLpszLabel_ members of other control structures read from the control text in the resource.</span></span> 
    
 <span data-ttu-id="16f6e-146">**BuildDisplayTable** は、ダイアログ リソースからの情報を使用して、入力コントロール構造で渡された内容を上書きします。 **つまり、BuildDisplayTable** の呼び出し元はページまたはコントロールのタイトルを動的に指定できません。</span><span class="sxs-lookup"><span data-stu-id="16f6e-146">**BuildDisplayTable** overwrites anything passed in the input control structures with information from the dialog resource, which means the caller of **BuildDisplayTable** cannot dynamically specify page or control titles.</span></span> <span data-ttu-id="16f6e-147">これを行う必要がある呼び出し元は **、BuildDisplayTable** が  _lppTableData_ のテーブル データ オブジェクトを返し、その中の行を変更できます。または、代わりにテーブル データ オブジェクトで表示テーブルを手で作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="16f6e-147">Callers who need to do that can have **BuildDisplayTable** return the table data object in  _lppTableData_ and change rows in it; or they can build the display table by hand in a table data object instead.</span></span> 
  
<span data-ttu-id="16f6e-148">_lppTableData が_ NULL に設定されていない場合、プロバイダーは、表示テーブルの終了時にテーブル データ オブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="16f6e-148">If  _lppTableData_ is not set to NULL, the provider is responsible for freeing the table data object when it is finished with the display table.</span></span> 
  

