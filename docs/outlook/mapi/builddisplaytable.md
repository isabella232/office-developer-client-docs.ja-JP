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
ms.openlocfilehash: 3b5268f0b033126083a463f72e47c64957df07eb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577689"
---
# <a name="builddisplaytable"></a><span data-ttu-id="f64ad-103">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="f64ad-103">BuildDisplayTable</span></span>

  
  
<span data-ttu-id="f64ad-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f64ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f64ad-105">プロパティ ページのデータが 1 つまたは複数の[DTPAGE](dtpage.md)構造体に含まれているから、表示された表を作成します。</span><span class="sxs-lookup"><span data-stu-id="f64ad-105">Creates a display table from the property page data contained in one or more [DTPAGE](dtpage.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f64ad-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f64ad-106">Header file:</span></span>  <br/> |<span data-ttu-id="f64ad-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f64ad-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f64ad-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="f64ad-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f64ad-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f64ad-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f64ad-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f64ad-110">Called by:</span></span>  <br/> |<span data-ttu-id="f64ad-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="f64ad-111">Service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="f64ad-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f64ad-112">Parameters</span></span>

 <span data-ttu-id="f64ad-113">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="f64ad-113">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="f64ad-114">[in]メモリの割り当てに使用する[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f64ad-114">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="f64ad-115">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="f64ad-115">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="f64ad-116">[in]追加メモリの割り当てに使用する[MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f64ad-116">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="f64ad-117">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="f64ad-117">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="f64ad-118">[in]メモリを解放するために使用する、 [MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f64ad-118">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="f64ad-119">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="f64ad-119">_lpMalloc_</span></span>
  
> <span data-ttu-id="f64ad-120">未使用です。NULL に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f64ad-120">Unused; should be set to NULL.</span></span> 
    
 <span data-ttu-id="f64ad-121">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="f64ad-121">_hInstance_</span></span>
  
> <span data-ttu-id="f64ad-122">[in]**BuildDisplayTable**リソースの取得元となる MAPI オブジェクトのインスタンス。</span><span class="sxs-lookup"><span data-stu-id="f64ad-122">[in] An instance of a MAPI object from which **BuildDisplayTable** retrieves resources.</span></span> 
    
 <span data-ttu-id="f64ad-123">_cPages_</span><span class="sxs-lookup"><span data-stu-id="f64ad-123">_cPages_</span></span>
  
> <span data-ttu-id="f64ad-124">[in]_LpPage_パラメーターが指す配列内の[DTPAGE](dtpage.md)構造体の数です。</span><span class="sxs-lookup"><span data-stu-id="f64ad-124">[in] Count of [DTPAGE](dtpage.md) structures in the array pointed to by the  _lpPage_ parameter.</span></span> 
    
 <span data-ttu-id="f64ad-125">_lpPage_</span><span class="sxs-lookup"><span data-stu-id="f64ad-125">_lpPage_</span></span>
  
> <span data-ttu-id="f64ad-126">[in]**DTPAGE**構造体を構築する、表示のテーブル ・ ページに関する情報を含む配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f64ad-126">[in] Pointer to an array of **DTPAGE** structures that contain information about the display table pages to be built.</span></span> 
    
 <span data-ttu-id="f64ad-127">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f64ad-127">_ulFlags_</span></span>
  
> <span data-ttu-id="f64ad-128">[in]フラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="f64ad-128">[in] Bitmask of flags.</span></span> <span data-ttu-id="f64ad-129">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="f64ad-129">The following flag can be set:</span></span>
    
<span data-ttu-id="f64ad-130">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f64ad-130">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f64ad-131">渡された文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="f64ad-131">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="f64ad-132">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="f64ad-132">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="f64ad-133">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="f64ad-133">_lppTable_</span></span>
  
> <span data-ttu-id="f64ad-134">[out][IMAPITable](imapitableiunknown.md)インターフェイスを公開する表示のテーブルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="f64ad-134">[out] Pointer to a pointer to the display table, which exposes the [IMAPITable](imapitableiunknown.md) interface.</span></span> 
    
 <span data-ttu-id="f64ad-135">_lppTblData_</span><span class="sxs-lookup"><span data-stu-id="f64ad-135">_lppTblData_</span></span>
  
> <span data-ttu-id="f64ad-136">[で [チェック アウト]_LppTable_パラメーターで返されるテーブルの[ITableData](itabledataiunknown.md)インターフェイスを公開するテーブルのデータ オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="f64ad-136">[in, out] Pointer to a pointer to a table data object exposing the [ITableData](itabledataiunknown.md) interface on the table returned in the  _lppTable_ parameter.</span></span> <span data-ttu-id="f64ad-137">テーブルのデータ オブジェクトが必要ない場合、ポインターの値ではなく、 _lppTblData_を NULL に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f64ad-137">If no table data object is desired,  _lppTblData_ should be set to NULL instead of a pointer value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f64ad-138">戻り値</span><span class="sxs-lookup"><span data-stu-id="f64ad-138">Return value</span></span>

<span data-ttu-id="f64ad-139">なし</span><span class="sxs-lookup"><span data-stu-id="f64ad-139">None</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f64ad-140">注釈</span><span class="sxs-lookup"><span data-stu-id="f64ad-140">Remarks</span></span>

<span data-ttu-id="f64ad-141">MAPI が to で指された_lpAllocateBuffer_、 _lpAllocateMore_、および多くのメモリの割り当てと解放のための_lpFreeBuffer_具体的にはオブジェクトのインターフェイスを呼び出すときにクライアント アプリケーションで使用するメモリの割り当て関数を使用してください。[IMAPIProp::GetProps](imapiprop-getprops.md) 、 [IMAPITable::QueryRows](imapitable-queryrows.md)などです。</span><span class="sxs-lookup"><span data-stu-id="f64ad-141">MAPI uses the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f64ad-142">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="f64ad-142">Notes to callers</span></span>

<span data-ttu-id="f64ad-143">ダイアログ リソースから読み取り可能なすべてのものを含みます。</span><span class="sxs-lookup"><span data-stu-id="f64ad-143">Everything possible is read from the dialog resource, including:</span></span>
  
- <span data-ttu-id="f64ad-144">ページのタイトルは、 _ulbLpszLabel_ 、 [DTBLPAGE](dtblpage.md)構造体のメンバー リソースのダイアログのタイトルから読み取る。</span><span class="sxs-lookup"><span data-stu-id="f64ad-144">The page title that is, the  _ulbLpszLabel_ member of the [DTBLPAGE](dtblpage.md) structure read from the dialog title in the resource.</span></span> 
    
- <span data-ttu-id="f64ad-145">すべてのコントロールのタイトルは、リソース内のコントロールのテキストから読み取るその他の制御構造の_ulbLpszLabel_メンバー。</span><span class="sxs-lookup"><span data-stu-id="f64ad-145">All control titles that is, the  _ulbLpszLabel_ members of other control structures read from the control text in the resource.</span></span> 
    
 <span data-ttu-id="f64ad-146">**BuildDisplayTable**は、 **BuildDisplayTable**の呼び出し側が動的にページまたはコントロールのタイトルを指定することはできませんが、ダイアログ リソースから情報を入力コントロールの構造体に渡されたものを上書きします。</span><span class="sxs-lookup"><span data-stu-id="f64ad-146">**BuildDisplayTable** overwrites anything passed in the input control structures with information from the dialog resource, which means the caller of **BuildDisplayTable** cannot dynamically specify page or control titles.</span></span> <span data-ttu-id="f64ad-147">呼び出し元を実行する必要がある**BuildDisplayTable**を持つことができる_lppTableData_で、テーブルのデータ オブジェクトを返すしでその行を変更します。または、ディスプレイ テーブル、テーブルのデータ オブジェクトに手動で構築されること代わりにことができます。</span><span class="sxs-lookup"><span data-stu-id="f64ad-147">Callers who need to do that can have **BuildDisplayTable** return the table data object in  _lppTableData_ and change rows in it; or they can build the display table by hand in a table data object instead.</span></span> 
  
<span data-ttu-id="f64ad-148">_LppTableData_が NULL に設定されていない場合、プロバイダーは、表示された表の処理が終了すると、テーブルのデータ オブジェクトを解放することを担当します。</span><span class="sxs-lookup"><span data-stu-id="f64ad-148">If  _lppTableData_ is not set to NULL, the provider is responsible for freeing the table data object when it is finished with the display table.</span></span> 
  

