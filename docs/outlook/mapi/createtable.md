---
title: CreateTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateTable
api_type:
- HeaderDef
ms.assetid: 106ce3d8-d0bf-4a0e-9a15-dc8988d0eb58
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e8c399569e68b8cb55d803733ed93105ea0be799
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332985"
---
# <a name="createtable"></a><span data-ttu-id="940a7-103">CreateTable</span><span class="sxs-lookup"><span data-stu-id="940a7-103">CreateTable</span></span>

  
  
<span data-ttu-id="940a7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="940a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="940a7-105">テーブルの内容を作成するために使用できる[itabledata](itabledataiunknown.md)オブジェクトの構造とオブジェクトハンドルを作成します。</span><span class="sxs-lookup"><span data-stu-id="940a7-105">Creates structures and an object handle for an [ITableData](itabledataiunknown.md) object which can be used to create table contents.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="940a7-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="940a7-106">Header file:</span></span>  <br/> |<span data-ttu-id="940a7-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="940a7-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="940a7-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="940a7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="940a7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="940a7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="940a7-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="940a7-110">Called by:</span></span>  <br/> |<span data-ttu-id="940a7-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="940a7-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE CreateTable(
  LPCIID lpInterface,
  ALLOCATEBUFFER FAR * lpAllocateBuffer,
  ALLOCATEMORE FAR * lpAllocateMore,
  FREEBUFFER FAR * lpFreeBuffer,
  LPVOID lpvReserved,
  ULONG ulTableType,
  ULONG ulPropTagIndexColumn,
  LPSPropTagArray lpSPropTagArrayColumns,
  LPTABLEDATA FAR * lppTableData
);
```

## <a name="parameters"></a><span data-ttu-id="940a7-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="940a7-112">Parameters</span></span>

 <span data-ttu-id="940a7-113">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="940a7-113">_lpInterface_</span></span>
  
> <span data-ttu-id="940a7-114">順番テーブルデータオブジェクトのインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="940a7-114">[in] Pointer to an interface identifier (IID) for the table data object.</span></span> <span data-ttu-id="940a7-115">有効なインターフェイス識別子は IID_IMAPITableData です。</span><span class="sxs-lookup"><span data-stu-id="940a7-115">The valid interface identifier is IID_IMAPITableData.</span></span> <span data-ttu-id="940a7-116">_lpinterface_パラメーターで NULL を渡すと、 _lppTableData_パラメーターで返されるテーブルデータオブジェクトも、テーブルデータオブジェクトの標準インターフェイスにキャストされます。</span><span class="sxs-lookup"><span data-stu-id="940a7-116">Passing NULL in the  _lpInterface_ parameter also causes the table data object returned in the  _lppTableData_ parameter to be cast to the standard interface for a table data object.</span></span> 
    
 <span data-ttu-id="940a7-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="940a7-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="940a7-118">順番メモリの割り当てに使用される[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="940a7-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="940a7-119">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="940a7-119">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="940a7-120">順番追加のメモリを割り当てるために使用される[MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="940a7-120">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="940a7-121">_lpfreebuffer_</span><span class="sxs-lookup"><span data-stu-id="940a7-121">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="940a7-122">順番メモリを解放するために使用される[MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="940a7-122">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="940a7-123">_lpvreserved_</span><span class="sxs-lookup"><span data-stu-id="940a7-123">_lpvReserved_</span></span>
  
> <span data-ttu-id="940a7-124">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="940a7-124">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="940a7-125">_ulTableType_</span><span class="sxs-lookup"><span data-stu-id="940a7-125">_ulTableType_</span></span>
  
> <span data-ttu-id="940a7-126">順番クライアントアプリケーションまたはサービスプロバイダーが[IMAPITable:: GetStatus](imapitable-getstatus.md)の一部として使用できるテーブルの種類。テーブルビューにデータを返します。</span><span class="sxs-lookup"><span data-stu-id="940a7-126">[in] A table type that is available to a client application or service provider as part of the [IMAPITable::GetStatus](imapitable-getstatus.md) return data on its table views.</span></span> <span data-ttu-id="940a7-127">使用可能な値は次のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="940a7-127">Possible values are:</span></span> 
    
<span data-ttu-id="940a7-128">TBLTYPE_DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="940a7-128">TBLTYPE_DYNAMIC</span></span> 
  
> <span data-ttu-id="940a7-129">テーブルの内容は動的であり、基になるデータの変更に応じて変更できます。</span><span class="sxs-lookup"><span data-stu-id="940a7-129">The table's contents are dynamic and can change as the underlying data changes.</span></span> 
    
<span data-ttu-id="940a7-130">TBLTYPE_KEYSET</span><span class="sxs-lookup"><span data-stu-id="940a7-130">TBLTYPE_KEYSET</span></span> 
  
> <span data-ttu-id="940a7-131">表の行は固定されていますが、これらの行の値は動的であり、基になるデータの変更として変更されることがあります。</span><span class="sxs-lookup"><span data-stu-id="940a7-131">The rows in the table are fixed, but the values in these rows are dynamic and can change as the underlying data changes.</span></span> 
    
<span data-ttu-id="940a7-132">TBLTYPE_SNAPSHOT</span><span class="sxs-lookup"><span data-stu-id="940a7-132">TBLTYPE_SNAPSHOT</span></span> 
  
> <span data-ttu-id="940a7-133">テーブルは静的であり、基になるデータが変更されても内容は変わりません。</span><span class="sxs-lookup"><span data-stu-id="940a7-133">The table is static and the contents do not change when the underlying data changes.</span></span> 
    
 <span data-ttu-id="940a7-134">_ulPropTagIndexColumn_</span><span class="sxs-lookup"><span data-stu-id="940a7-134">_ulPropTagIndexColumn_</span></span>
  
> <span data-ttu-id="940a7-135">順番テーブルデータを変更するときに使用する列のインデックス番号を指定します。</span><span class="sxs-lookup"><span data-stu-id="940a7-135">[in] Index number of the column for use when changing table data.</span></span> 
    
 <span data-ttu-id="940a7-136">_lpSPropTagArrayColumns_</span><span class="sxs-lookup"><span data-stu-id="940a7-136">_lpSPropTagArrayColumns_</span></span>
  
> <span data-ttu-id="940a7-137">順番オブジェクトがデータを保持するテーブルで必要なプロパティを示す、プロパティタグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="940a7-137">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating the properties required in the table for which the object holds data.</span></span> 
    
 <span data-ttu-id="940a7-138">_lppTableData_</span><span class="sxs-lookup"><span data-stu-id="940a7-138">_lppTableData_</span></span>
  
> <span data-ttu-id="940a7-139">読み上げ返されるテーブルデータオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="940a7-139">[out] Pointer to a pointer to the returned table data object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="940a7-140">戻り値</span><span class="sxs-lookup"><span data-stu-id="940a7-140">Return value</span></span>

<span data-ttu-id="940a7-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="940a7-141">S_OK</span></span> 
  
> <span data-ttu-id="940a7-142">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="940a7-142">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="940a7-143">解説</span><span class="sxs-lookup"><span data-stu-id="940a7-143">Remarks</span></span>

<span data-ttu-id="940a7-144">_lpAllocateBuffer_、 _lpAllocateMore_、および_lpfreebuffer_の入力パラメーターは、それぞれ、 [MAPIAllocateBuffer](mapiallocatebuffer.md)、 [MAPIAllocateMore](mapiallocatemore.md)、および[MAPIFreeBuffer](mapifreebuffer.md)関数を指しています。</span><span class="sxs-lookup"><span data-stu-id="940a7-144">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="940a7-145">**CreateTable**を呼び出すクライアントアプリケーションは、という名前の MAPI 関数へのポインターを渡します。サービスプロバイダーは、初期化呼び出しで受け取った、または[imapiallocルーチン](imapisupport-getmemallocroutines.md)メソッドへの呼び出しによって取得したこれらの関数にポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="940a7-145">A client application calling **CreateTable** passes in pointers to the MAPI functions just named; a service provider passes the pointers to these functions that it received in its initialization call or retrieved with a call to the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="940a7-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="940a7-146">See also</span></span>



[<span data-ttu-id="940a7-147">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="940a7-147">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

