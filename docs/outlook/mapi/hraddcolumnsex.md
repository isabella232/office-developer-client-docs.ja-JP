---
title: HrAddColumnsEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrAddColumnsEx
api_type:
- COM
ms.assetid: c0a65d2b-a9b8-4477-a1c7-18c8478126f6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9ca34fb2cce6e86c42e8e9525cd213f1008997d6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427480"
---
# <a name="hraddcolumnsex"></a><span data-ttu-id="fde3d-103">HrAddColumnsEx</span><span class="sxs-lookup"><span data-stu-id="fde3d-103">HrAddColumnsEx</span></span>

  
  
<span data-ttu-id="fde3d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fde3d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fde3d-105">既存のテーブルの先頭に列を追加または移動します。</span><span class="sxs-lookup"><span data-stu-id="fde3d-105">Adds or moves columns to the beginning of an existing table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fde3d-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="fde3d-106">Header file:</span></span>  <br/> |<span data-ttu-id="fde3d-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="fde3d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="fde3d-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="fde3d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fde3d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fde3d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fde3d-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="fde3d-110">Called by:</span></span>  <br/> |<span data-ttu-id="fde3d-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="fde3d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrAddColumnsEx(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  void (FAR * lpfnFilterColumns)(
  LPSPropTagArray ptaga)
);
```

## <a name="parameters"></a><span data-ttu-id="fde3d-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fde3d-112">Parameters</span></span>

 <span data-ttu-id="fde3d-113">_lptbl_</span><span class="sxs-lookup"><span data-stu-id="fde3d-113">_lptbl_</span></span>
  
> <span data-ttu-id="fde3d-114">[in]影響を受ける MAPI テーブルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="fde3d-114">[in] Pointer to the MAPI table affected.</span></span> 
    
 <span data-ttu-id="fde3d-115">_lpproptagColumnsNew_</span><span class="sxs-lookup"><span data-stu-id="fde3d-115">_lpproptagColumnsNew_</span></span>
  
> <span data-ttu-id="fde3d-116">[in]テーブルの先頭に追加または移動するプロパティのプロパティ タグの配列を含む [SPropTagArray](sproptagarray.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fde3d-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags for the properties to be added or moved to the beginning of the table.</span></span> 
    
 <span data-ttu-id="fde3d-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="fde3d-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="fde3d-118">[in]メモリの割 [り当てに使用する MAPIAllocateBuffer](mapiallocatebuffer.md) 関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fde3d-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="fde3d-119">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="fde3d-119">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="fde3d-120">[in]メモリを解放するために使用する [MAPIFreeBuffer](mapifreebuffer.md) 関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fde3d-120">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="fde3d-121">_lpfnFilterColumns_</span><span class="sxs-lookup"><span data-stu-id="fde3d-121">_lpfnFilterColumns_</span></span>
  
> <span data-ttu-id="fde3d-122">[in]呼び出し元によって提供されるコールバック関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fde3d-122">[in] Pointer to a callback function furnished by the caller.</span></span> <span data-ttu-id="fde3d-123">_lpfnFilterColumns パラメーター_ が NULL に設定されている場合、コールバックは実行できません。</span><span class="sxs-lookup"><span data-stu-id="fde3d-123">If the  _lpfnFilterColumns_ parameter is set to NULL, no callback is made.</span></span> 
    
 <span data-ttu-id="fde3d-124">_ptaga_</span><span class="sxs-lookup"><span data-stu-id="fde3d-124">_ptaga_</span></span>
  
> <span data-ttu-id="fde3d-125">[in]プロパティが先頭に追加または移動される前に、テーブルに既に存在するプロパティ タグの配列を含む [SPropTagArray](sproptagarray.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fde3d-125">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the array of property tags already existing in the table before properties are added or moved to the beginning.</span></span> <span data-ttu-id="fde3d-126">**HrAddColumnsEx** は、このポインターをパラメーターとして  _lpfnFilterColumns_ が指すコールバック関数に渡します。</span><span class="sxs-lookup"><span data-stu-id="fde3d-126">**HrAddColumnsEx** passes this pointer as the parameter to the callback function pointed to by  _lpfnFilterColumns_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fde3d-127">戻り値</span><span class="sxs-lookup"><span data-stu-id="fde3d-127">Return value</span></span>

<span data-ttu-id="fde3d-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="fde3d-128">S_OK</span></span> 
  
> <span data-ttu-id="fde3d-129">呼び出しが成功し、指定された列が移動または追加されました。</span><span class="sxs-lookup"><span data-stu-id="fde3d-129">The call succeeded and the specified columns were moved or added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fde3d-130">注釈</span><span class="sxs-lookup"><span data-stu-id="fde3d-130">Remarks</span></span>

<span data-ttu-id="fde3d-131">_lpproptagColumnsNew_ パラメーターを使用して **HrAddColumnsEx** に渡されるプロパティは [、IMAPITable::QueryRows](imapitable-queryrows.md)メソッドへの後続の呼び出しで公開される最初のプロパティになります。</span><span class="sxs-lookup"><span data-stu-id="fde3d-131">The properties passed to **HrAddColumnsEx** using the  _lpproptagColumnsNew_ parameter become the first properties exposed on subsequent calls to the [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> <span data-ttu-id="fde3d-132">_lpproptagColumnsNew_ パラメーターで指定されていないテーブル内のすべてのプロパティは、追加および移動されたプロパティの後で公開されます。</span><span class="sxs-lookup"><span data-stu-id="fde3d-132">Any properties previously in the table that were not specified in the  _lpproptagColumnsNew_ parameter are exposed after all the added and moved properties.</span></span> 
  
<span data-ttu-id="fde3d-133">**QueryRows** が呼び出された場合、テーブル プロパティが未定義の場合は、プロパティの種類とプロパティPT_NULLプロパティ識別子を使用して返PROP_ID_NULL。</span><span class="sxs-lookup"><span data-stu-id="fde3d-133">If any table properties are undefined when **QueryRows** is called, they are returned with property type PT_NULL and property identifier PROP_ID_NULL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="fde3d-134">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="fde3d-134">Notes to callers</span></span>

<span data-ttu-id="fde3d-135">**HrAddColumnsEx** 関数を使用すると、呼び出し元はコールバック関数を提供して、テーブル内に既に存在していた列をフィルター処理できます 。たとえば、文字列をプロパティ型 PT_UNICODE から PT_STRING8 に変換します。</span><span class="sxs-lookup"><span data-stu-id="fde3d-135">The **HrAddColumnsEx** function allows the caller to furnish a callback function to filter the columns that were already in the table, for example to convert strings from property type PT_UNICODE to PT_STRING8.</span></span> <span data-ttu-id="fde3d-136">**HrAddColumnsEx** は、パラメーターとして以前に既存の列セットへのポインターをコールバック関数に渡します。</span><span class="sxs-lookup"><span data-stu-id="fde3d-136">**HrAddColumnsEx** passes a pointer to the previously existing column set as the parameter to the callback function.</span></span> <span data-ttu-id="fde3d-137">コールバック関数は、プロパティ タグ配列のデータを変更できますが、新しいタグを追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="fde3d-137">The callback function can change data in the property tag array but cannot add new tags.</span></span> 
  
 <span data-ttu-id="fde3d-138">**HrAddColumnsEx** は、最初にコールバック関数が指定されている場合にコールバック関数を呼び出し、指定した列を追加または移動し、最後に [IMAPITable::SetColumns を呼び出します](imapitable-setcolumns.md)。</span><span class="sxs-lookup"><span data-stu-id="fde3d-138">**HrAddColumnsEx** first calls the callback function if one is furnished, then adds or moves the specified columns, and finally calls [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span> 
  
<span data-ttu-id="fde3d-139">_lpAllocateBuffer_ および _lpFreeBuffer_ 入力パラメーターは [、MAPIAllocateBuffer](mapiallocatebuffer.md)関数と [MAPIFreeBuffer](mapifreebuffer.md)関数をそれぞれ指します。</span><span class="sxs-lookup"><span data-stu-id="fde3d-139">The  _lpAllocateBuffer_ and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="fde3d-140">**HrAddColumnsEx** に渡されるポインターの正確な値は、呼び出し元がクライアント アプリケーションかサービス プロバイダーかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="fde3d-140">The exact values of the pointers passed to **HrAddColumnsEx** depend on whether the caller is a client application or a service provider.</span></span> <span data-ttu-id="fde3d-141">クライアントは、指定された名前を持つ MAPI 関数へのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="fde3d-141">A client passes pointers to the MAPI functions with the specified names.</span></span> <span data-ttu-id="fde3d-142">サービス プロバイダーは、初期化呼び出しで受信したポインターを渡したり [、IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) メソッドを呼び出して取得します。</span><span class="sxs-lookup"><span data-stu-id="fde3d-142">A service provider passes the pointers it received in its initialization call or retrieved by calling the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fde3d-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="fde3d-143">See also</span></span>



[<span data-ttu-id="fde3d-144">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="fde3d-144">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)

