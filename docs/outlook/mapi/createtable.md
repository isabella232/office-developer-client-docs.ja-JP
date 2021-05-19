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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e8c399569e68b8cb55d803733ed93105ea0be799
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435013"
---
# <a name="createtable"></a><span data-ttu-id="4b261-103">CreateTable</span><span class="sxs-lookup"><span data-stu-id="4b261-103">CreateTable</span></span>

  
  
<span data-ttu-id="4b261-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b261-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b261-105">テーブルの内容を作成するために使用できる [ITableData](itabledataiunknown.md) オブジェクトの構造とオブジェクト ハンドルを作成します。</span><span class="sxs-lookup"><span data-stu-id="4b261-105">Creates structures and an object handle for an [ITableData](itabledataiunknown.md) object which can be used to create table contents.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4b261-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="4b261-106">Header file:</span></span>  <br/> |<span data-ttu-id="4b261-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="4b261-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="4b261-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="4b261-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4b261-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4b261-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4b261-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="4b261-110">Called by:</span></span>  <br/> |<span data-ttu-id="4b261-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="4b261-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="4b261-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4b261-112">Parameters</span></span>

 <span data-ttu-id="4b261-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="4b261-113">_lpInterface_</span></span>
  
> <span data-ttu-id="4b261-114">[in]テーブル データ オブジェクトのインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4b261-114">[in] Pointer to an interface identifier (IID) for the table data object.</span></span> <span data-ttu-id="4b261-115">有効なインターフェイス識別子はIID_IMAPITableData。</span><span class="sxs-lookup"><span data-stu-id="4b261-115">The valid interface identifier is IID_IMAPITableData.</span></span> <span data-ttu-id="4b261-116">_lpInterface_ パラメーターに NULL を渡すと _、lppTableData_ パラメーターで返されるテーブル データ オブジェクトがテーブル データ オブジェクトの標準インターフェイスにキャストされます。</span><span class="sxs-lookup"><span data-stu-id="4b261-116">Passing NULL in the  _lpInterface_ parameter also causes the table data object returned in the  _lppTableData_ parameter to be cast to the standard interface for a table data object.</span></span> 
    
 <span data-ttu-id="4b261-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="4b261-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="4b261-118">[in]メモリの割 [り当てに使用する MAPIAllocateBuffer](mapiallocatebuffer.md) 関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4b261-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="4b261-119">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="4b261-119">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="4b261-120">[in]追加のメモリ [の割り当てに使用する MAPIAllocateMore](mapiallocatemore.md) 関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4b261-120">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="4b261-121">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="4b261-121">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="4b261-122">[in]メモリを解放するために使用する [MAPIFreeBuffer](mapifreebuffer.md) 関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4b261-122">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="4b261-123">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="4b261-123">_lpvReserved_</span></span>
  
> <span data-ttu-id="4b261-124">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="4b261-124">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="4b261-125">_ulTableType_</span><span class="sxs-lookup"><span data-stu-id="4b261-125">_ulTableType_</span></span>
  
> <span data-ttu-id="4b261-126">[in] [IMAPITable::GetStatus](imapitable-getstatus.md) の一部としてクライアント アプリケーションまたはサービス プロバイダーが使用できるテーブルの種類は、そのテーブル ビューのデータを返します。</span><span class="sxs-lookup"><span data-stu-id="4b261-126">[in] A table type that is available to a client application or service provider as part of the [IMAPITable::GetStatus](imapitable-getstatus.md) return data on its table views.</span></span> <span data-ttu-id="4b261-127">使用可能な値は次のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="4b261-127">Possible values are:</span></span> 
    
<span data-ttu-id="4b261-128">TBLTYPE_DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="4b261-128">TBLTYPE_DYNAMIC</span></span> 
  
> <span data-ttu-id="4b261-129">テーブルの内容は動的であり、基になるデータの変更に応じ変更できます。</span><span class="sxs-lookup"><span data-stu-id="4b261-129">The table's contents are dynamic and can change as the underlying data changes.</span></span> 
    
<span data-ttu-id="4b261-130">TBLTYPE_KEYSET</span><span class="sxs-lookup"><span data-stu-id="4b261-130">TBLTYPE_KEYSET</span></span> 
  
> <span data-ttu-id="4b261-131">テーブル内の行は固定されますが、これらの行の値は動的であり、基になるデータが変更されるに従って変更される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4b261-131">The rows in the table are fixed, but the values in these rows are dynamic and can change as the underlying data changes.</span></span> 
    
<span data-ttu-id="4b261-132">TBLTYPE_SNAPSHOT</span><span class="sxs-lookup"><span data-stu-id="4b261-132">TBLTYPE_SNAPSHOT</span></span> 
  
> <span data-ttu-id="4b261-133">テーブルは静的であり、基になるデータが変更された場合、内容は変更されません。</span><span class="sxs-lookup"><span data-stu-id="4b261-133">The table is static and the contents do not change when the underlying data changes.</span></span> 
    
 <span data-ttu-id="4b261-134">_ulPropTagIndexColumn_</span><span class="sxs-lookup"><span data-stu-id="4b261-134">_ulPropTagIndexColumn_</span></span>
  
> <span data-ttu-id="4b261-135">[in]テーブル データを変更するときに使用する列のインデックス番号。</span><span class="sxs-lookup"><span data-stu-id="4b261-135">[in] Index number of the column for use when changing table data.</span></span> 
    
 <span data-ttu-id="4b261-136">_lpSPropTagArrayColumns_</span><span class="sxs-lookup"><span data-stu-id="4b261-136">_lpSPropTagArrayColumns_</span></span>
  
> <span data-ttu-id="4b261-137">[in]オブジェクトがデータを保持するテーブルで必要なプロパティを示すプロパティ タグの配列を含む [SPropTagArray](sproptagarray.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4b261-137">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating the properties required in the table for which the object holds data.</span></span> 
    
 <span data-ttu-id="4b261-138">_lppTableData_</span><span class="sxs-lookup"><span data-stu-id="4b261-138">_lppTableData_</span></span>
  
> <span data-ttu-id="4b261-139">[out]返されるテーブル データ オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="4b261-139">[out] Pointer to a pointer to the returned table data object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4b261-140">戻り値</span><span class="sxs-lookup"><span data-stu-id="4b261-140">Return value</span></span>

<span data-ttu-id="4b261-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="4b261-141">S_OK</span></span> 
  
> <span data-ttu-id="4b261-142">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="4b261-142">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4b261-143">注釈</span><span class="sxs-lookup"><span data-stu-id="4b261-143">Remarks</span></span>

<span data-ttu-id="4b261-144">_lpAllocateBuffer_ _、lpAllocateMore、lpFreeBuffer_ 入力パラメーターは [、MAPIAllocateBuffer、MAPIAllocateMore、MAPIFreeBuffer](mapiallocatebuffer.md)関数をそれぞれ指します。  [](mapiallocatemore.md) [](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="4b261-144">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="4b261-145">CreateTable を呼び **出すクライアント アプリケーション** は、という名前の MAPI 関数へのポインターを渡します。サービス プロバイダーは、初期化呼び出しで受け取った、 [または IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) メソッドへの呼び出しで取得したこれらの関数へのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="4b261-145">A client application calling **CreateTable** passes in pointers to the MAPI functions just named; a service provider passes the pointers to these functions that it received in its initialization call or retrieved with a call to the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4b261-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="4b261-146">See also</span></span>



[<span data-ttu-id="4b261-147">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4b261-147">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

