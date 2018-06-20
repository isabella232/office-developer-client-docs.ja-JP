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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c79d9ebb5be1d8af6c9136514d8a2b695513f755
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800273"
---
# <a name="hraddcolumnsex"></a><span data-ttu-id="99cf4-103">HrAddColumnsEx</span><span class="sxs-lookup"><span data-stu-id="99cf4-103">HrAddColumnsEx</span></span>

  
  
<span data-ttu-id="99cf4-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="99cf4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="99cf4-105">追加または既存のテーブルの先頭に列を移動します。</span><span class="sxs-lookup"><span data-stu-id="99cf4-105">Adds or moves columns to the beginning of an existing table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="99cf4-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="99cf4-106">Header file:</span></span>  <br/> |<span data-ttu-id="99cf4-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="99cf4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="99cf4-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="99cf4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="99cf4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="99cf4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="99cf4-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="99cf4-110">Called by:</span></span>  <br/> |<span data-ttu-id="99cf4-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="99cf4-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="99cf4-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="99cf4-112">Parameters</span></span>

 <span data-ttu-id="99cf4-113">_lptbl_</span><span class="sxs-lookup"><span data-stu-id="99cf4-113">_lptbl_</span></span>
  
> <span data-ttu-id="99cf4-114">[in]影響を MAPI テーブルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="99cf4-114">[in] Pointer to the MAPI table affected.</span></span> 
    
 <span data-ttu-id="99cf4-115">_lpproptagColumnsNew_</span><span class="sxs-lookup"><span data-stu-id="99cf4-115">_lpproptagColumnsNew_</span></span>
  
> <span data-ttu-id="99cf4-116">[in]追加されたり、テーブルの先頭に移動するにはプロパティのプロパティ タグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="99cf4-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags for the properties to be added or moved to the beginning of the table.</span></span> 
    
 <span data-ttu-id="99cf4-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="99cf4-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="99cf4-118">[in]メモリの割り当てに使用する[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="99cf4-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="99cf4-119">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="99cf4-119">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="99cf4-120">[in]メモリを解放するために使用する、 [MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="99cf4-120">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="99cf4-121">_lpfnFilterColumns_</span><span class="sxs-lookup"><span data-stu-id="99cf4-121">_lpfnFilterColumns_</span></span>
  
> <span data-ttu-id="99cf4-122">[in]呼び出し元によって提供されるコールバック関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="99cf4-122">[in] Pointer to a callback function furnished by the caller.</span></span> <span data-ttu-id="99cf4-123">_LpfnFilterColumns_パラメーターは、NULL に設定されている場合、コールバックは行われません。</span><span class="sxs-lookup"><span data-stu-id="99cf4-123">If the  _lpfnFilterColumns_ parameter is set to NULL, no callback is made.</span></span> 
    
 <span data-ttu-id="99cf4-124">_ptaga_</span><span class="sxs-lookup"><span data-stu-id="99cf4-124">_ptaga_</span></span>
  
> <span data-ttu-id="99cf4-125">[in]プロパティ タグのプロパティを追加または先頭に移動する前にテーブルの既存の配列を格納する[SPropTagArray](sproptagarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="99cf4-125">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the array of property tags already existing in the table before properties are added or moved to the beginning.</span></span> <span data-ttu-id="99cf4-126">コールバック関数へのパラメーターとしては、このポインターが指す_lpfnFilterColumns_ **HrAddColumnsEx**のパス。</span><span class="sxs-lookup"><span data-stu-id="99cf4-126">**HrAddColumnsEx** passes this pointer as the parameter to the callback function pointed to by  _lpfnFilterColumns_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="99cf4-127">�߂�l</span><span class="sxs-lookup"><span data-stu-id="99cf4-127">Return value</span></span>

<span data-ttu-id="99cf4-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="99cf4-128">S_OK</span></span> 
  
> <span data-ttu-id="99cf4-129">呼び出しが成功し、指定された列の移動先または追加されました。</span><span class="sxs-lookup"><span data-stu-id="99cf4-129">The call succeeded and the specified columns were moved or added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="99cf4-130">備考</span><span class="sxs-lookup"><span data-stu-id="99cf4-130">Remarks</span></span>

<span data-ttu-id="99cf4-131">_LpproptagColumnsNew_パラメーターを使用して**HrAddColumnsEx**に渡されるプロパティは、 [IMAPITable::QueryRows](imapitable-queryrows.md)メソッドへの後続の呼び出しで公開されている最初のプロパティになります。</span><span class="sxs-lookup"><span data-stu-id="99cf4-131">The properties passed to **HrAddColumnsEx** using the  _lpproptagColumnsNew_ parameter become the first properties exposed on subsequent calls to the [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> <span data-ttu-id="99cf4-132">追加、移動、すべてのプロパティの後は、 _lpproptagColumnsNew_パラメーターで指定されていないテーブルの以前の任意のプロパティが公開されています。</span><span class="sxs-lookup"><span data-stu-id="99cf4-132">Any properties previously in the table that were not specified in the  _lpproptagColumnsNew_ parameter are exposed after all the added and moved properties.</span></span> 
  
<span data-ttu-id="99cf4-133">**QueryRows**が呼び出されたときに、テーブルのプロパティは定義されていません、PT_NULL プロパティの型およびプロパティの識別子 PROP_ID_NULL に返されます。</span><span class="sxs-lookup"><span data-stu-id="99cf4-133">If any table properties are undefined when **QueryRows** is called, they are returned with property type PT_NULL and property identifier PROP_ID_NULL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="99cf4-134">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="99cf4-134">Notes to callers</span></span>

<span data-ttu-id="99cf4-135">**HrAddColumnsEx**関数は、既に PT_STRING8 プロパティの PT_UNICODE データ型から文字列に変換する例については、表にしていた列をフィルター処理するコールバック関数を提供する呼び出し元を使用できます。</span><span class="sxs-lookup"><span data-stu-id="99cf4-135">The **HrAddColumnsEx** function allows the caller to furnish a callback function to filter the columns that were already in the table, for example to convert strings from property type PT_UNICODE to PT_STRING8.</span></span> <span data-ttu-id="99cf4-136">**HrAddColumnsEx**は、コールバック関数へのパラメーターとして設定済みの既存の列へのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="99cf4-136">**HrAddColumnsEx** passes a pointer to the previously existing column set as the parameter to the callback function.</span></span> <span data-ttu-id="99cf4-137">コールバック関数は、プロパティ タグ配列内のデータを変更できますが、新しいタグを追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="99cf4-137">The callback function can change data in the property tag array but cannot add new tags.</span></span> 
  
 <span data-ttu-id="99cf4-138">**HrAddColumnsEx**は、1 つが提供され、追加または指定の列に移動し、最後に[IMAPITable::SetColumns](imapitable-setcolumns.md)を呼び出す場合に最初にコールバック関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="99cf4-138">**HrAddColumnsEx** first calls the callback function if one is furnished, then adds or moves the specified columns, and finally calls [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span> 
  
<span data-ttu-id="99cf4-139">_LpAllocateBuffer_と_lpFreeBuffer_の入力パラメーターは、それぞれ、 [MAPIAllocateBuffer](mapiallocatebuffer.md)と[MAPIFreeBuffer](mapifreebuffer.md)関数をポイントします。</span><span class="sxs-lookup"><span data-stu-id="99cf4-139">The  _lpAllocateBuffer_ and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="99cf4-140">**HrAddColumnsEx**に渡されたポインターの正確な値は、呼び出し元が、クライアント アプリケーションまたはサービス プロバイダーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="99cf4-140">The exact values of the pointers passed to **HrAddColumnsEx** depend on whether the caller is a client application or a service provider.</span></span> <span data-ttu-id="99cf4-141">クライアントは、MAPI の関数を指定した名前にポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="99cf4-141">A client passes pointers to the MAPI functions with the specified names.</span></span> <span data-ttu-id="99cf4-142">ポインターの初期化の呼び出しで受信または[IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)メソッドを呼び出すことによって取得されたことをサービス プロバイダーに渡します。</span><span class="sxs-lookup"><span data-stu-id="99cf4-142">A service provider passes the pointers it received in its initialization call or retrieved by calling the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="99cf4-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="99cf4-143">See also</span></span>



[<span data-ttu-id="99cf4-144">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="99cf4-144">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)

