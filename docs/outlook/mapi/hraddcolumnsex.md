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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 566a9d23c46ec717eb5eed711fff801b15d49fc1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564235"
---
# <a name="hraddcolumnsex"></a><span data-ttu-id="ced04-103">HrAddColumnsEx</span><span class="sxs-lookup"><span data-stu-id="ced04-103">HrAddColumnsEx</span></span>

  
  
<span data-ttu-id="ced04-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ced04-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ced04-105">追加または既存のテーブルの先頭に列を移動します。</span><span class="sxs-lookup"><span data-stu-id="ced04-105">Adds or moves columns to the beginning of an existing table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ced04-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ced04-106">Header file:</span></span>  <br/> |<span data-ttu-id="ced04-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="ced04-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ced04-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="ced04-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ced04-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ced04-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ced04-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ced04-110">Called by:</span></span>  <br/> |<span data-ttu-id="ced04-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="ced04-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="ced04-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ced04-112">Parameters</span></span>

 <span data-ttu-id="ced04-113">_lptbl_</span><span class="sxs-lookup"><span data-stu-id="ced04-113">_lptbl_</span></span>
  
> <span data-ttu-id="ced04-114">[in]影響を MAPI テーブルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ced04-114">[in] Pointer to the MAPI table affected.</span></span> 
    
 <span data-ttu-id="ced04-115">_lpproptagColumnsNew_</span><span class="sxs-lookup"><span data-stu-id="ced04-115">_lpproptagColumnsNew_</span></span>
  
> <span data-ttu-id="ced04-116">[in]追加されたり、テーブルの先頭に移動するにはプロパティのプロパティ タグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ced04-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags for the properties to be added or moved to the beginning of the table.</span></span> 
    
 <span data-ttu-id="ced04-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="ced04-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="ced04-118">[in]メモリの割り当てに使用する[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ced04-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="ced04-119">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="ced04-119">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="ced04-120">[in]メモリを解放するために使用する、 [MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ced04-120">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="ced04-121">_lpfnFilterColumns_</span><span class="sxs-lookup"><span data-stu-id="ced04-121">_lpfnFilterColumns_</span></span>
  
> <span data-ttu-id="ced04-122">[in]呼び出し元によって提供されるコールバック関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ced04-122">[in] Pointer to a callback function furnished by the caller.</span></span> <span data-ttu-id="ced04-123">_LpfnFilterColumns_パラメーターは、NULL に設定されている場合、コールバックは行われません。</span><span class="sxs-lookup"><span data-stu-id="ced04-123">If the  _lpfnFilterColumns_ parameter is set to NULL, no callback is made.</span></span> 
    
 <span data-ttu-id="ced04-124">_ptaga_</span><span class="sxs-lookup"><span data-stu-id="ced04-124">_ptaga_</span></span>
  
> <span data-ttu-id="ced04-125">[in]プロパティ タグのプロパティを追加または先頭に移動する前にテーブルの既存の配列を格納する[SPropTagArray](sproptagarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ced04-125">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the array of property tags already existing in the table before properties are added or moved to the beginning.</span></span> <span data-ttu-id="ced04-126">コールバック関数へのパラメーターとしては、このポインターが指す_lpfnFilterColumns_ **HrAddColumnsEx**のパス。</span><span class="sxs-lookup"><span data-stu-id="ced04-126">**HrAddColumnsEx** passes this pointer as the parameter to the callback function pointed to by  _lpfnFilterColumns_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ced04-127">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ced04-127">Return value</span></span>

<span data-ttu-id="ced04-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="ced04-128">S_OK</span></span> 
  
> <span data-ttu-id="ced04-129">呼び出しが成功し、指定された列の移動先または追加されました。</span><span class="sxs-lookup"><span data-stu-id="ced04-129">The call succeeded and the specified columns were moved or added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ced04-130">注釈</span><span class="sxs-lookup"><span data-stu-id="ced04-130">Remarks</span></span>

<span data-ttu-id="ced04-131">_LpproptagColumnsNew_パラメーターを使用して**HrAddColumnsEx**に渡されるプロパティは、 [IMAPITable::QueryRows](imapitable-queryrows.md)メソッドへの後続の呼び出しで公開されている最初のプロパティになります。</span><span class="sxs-lookup"><span data-stu-id="ced04-131">The properties passed to **HrAddColumnsEx** using the  _lpproptagColumnsNew_ parameter become the first properties exposed on subsequent calls to the [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> <span data-ttu-id="ced04-132">追加、移動、すべてのプロパティの後は、 _lpproptagColumnsNew_パラメーターで指定されていないテーブルの以前の任意のプロパティが公開されています。</span><span class="sxs-lookup"><span data-stu-id="ced04-132">Any properties previously in the table that were not specified in the  _lpproptagColumnsNew_ parameter are exposed after all the added and moved properties.</span></span> 
  
<span data-ttu-id="ced04-133">**QueryRows**が呼び出されたときに、テーブルのプロパティは定義されていません、PT_NULL プロパティの型およびプロパティの識別子 PROP_ID_NULL に返されます。</span><span class="sxs-lookup"><span data-stu-id="ced04-133">If any table properties are undefined when **QueryRows** is called, they are returned with property type PT_NULL and property identifier PROP_ID_NULL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ced04-134">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="ced04-134">Notes to callers</span></span>

<span data-ttu-id="ced04-135">**HrAddColumnsEx**関数は、既に PT_STRING8 プロパティの PT_UNICODE データ型から文字列に変換する例については、表にしていた列をフィルター処理するコールバック関数を提供する呼び出し元を使用できます。</span><span class="sxs-lookup"><span data-stu-id="ced04-135">The **HrAddColumnsEx** function allows the caller to furnish a callback function to filter the columns that were already in the table, for example to convert strings from property type PT_UNICODE to PT_STRING8.</span></span> <span data-ttu-id="ced04-136">**HrAddColumnsEx**は、コールバック関数へのパラメーターとして設定済みの既存の列へのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="ced04-136">**HrAddColumnsEx** passes a pointer to the previously existing column set as the parameter to the callback function.</span></span> <span data-ttu-id="ced04-137">コールバック関数は、プロパティ タグ配列内のデータを変更できますが、新しいタグを追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="ced04-137">The callback function can change data in the property tag array but cannot add new tags.</span></span> 
  
 <span data-ttu-id="ced04-138">**HrAddColumnsEx**は、1 つが提供され、追加または指定の列に移動し、最後に[IMAPITable::SetColumns](imapitable-setcolumns.md)を呼び出す場合に最初にコールバック関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ced04-138">**HrAddColumnsEx** first calls the callback function if one is furnished, then adds or moves the specified columns, and finally calls [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span> 
  
<span data-ttu-id="ced04-139">_LpAllocateBuffer_と_lpFreeBuffer_の入力パラメーターは、それぞれ、 [MAPIAllocateBuffer](mapiallocatebuffer.md)と[MAPIFreeBuffer](mapifreebuffer.md)関数をポイントします。</span><span class="sxs-lookup"><span data-stu-id="ced04-139">The  _lpAllocateBuffer_ and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="ced04-140">**HrAddColumnsEx**に渡されたポインターの正確な値は、呼び出し元が、クライアント アプリケーションまたはサービス プロバイダーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="ced04-140">The exact values of the pointers passed to **HrAddColumnsEx** depend on whether the caller is a client application or a service provider.</span></span> <span data-ttu-id="ced04-141">クライアントは、MAPI の関数を指定した名前にポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="ced04-141">A client passes pointers to the MAPI functions with the specified names.</span></span> <span data-ttu-id="ced04-142">ポインターの初期化の呼び出しで受信または[IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)メソッドを呼び出すことによって取得されたことをサービス プロバイダーに渡します。</span><span class="sxs-lookup"><span data-stu-id="ced04-142">A service provider passes the pointers it received in its initialization call or retrieved by calling the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ced04-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="ced04-143">See also</span></span>



[<span data-ttu-id="ced04-144">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="ced04-144">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)

