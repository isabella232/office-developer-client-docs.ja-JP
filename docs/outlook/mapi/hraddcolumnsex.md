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
ms.openlocfilehash: 9ca34fb2cce6e86c42e8e9525cd213f1008997d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348371"
---
# <a name="hraddcolumnsex"></a><span data-ttu-id="98eb9-103">HrAddColumnsEx</span><span class="sxs-lookup"><span data-stu-id="98eb9-103">HrAddColumnsEx</span></span>

  
  
<span data-ttu-id="98eb9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98eb9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98eb9-105">既存の表の先頭に列を追加または移動します。</span><span class="sxs-lookup"><span data-stu-id="98eb9-105">Adds or moves columns to the beginning of an existing table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="98eb9-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="98eb9-106">Header file:</span></span>  <br/> |<span data-ttu-id="98eb9-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="98eb9-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="98eb9-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="98eb9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="98eb9-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="98eb9-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="98eb9-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="98eb9-110">Called by:</span></span>  <br/> |<span data-ttu-id="98eb9-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="98eb9-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="98eb9-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="98eb9-112">Parameters</span></span>

 <span data-ttu-id="98eb9-113">_lptbl_</span><span class="sxs-lookup"><span data-stu-id="98eb9-113">_lptbl_</span></span>
  
> <span data-ttu-id="98eb9-114">順番影響を受ける MAPI テーブルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="98eb9-114">[in] Pointer to the MAPI table affected.</span></span> 
    
 <span data-ttu-id="98eb9-115">_lpproptagColumnsNew_</span><span class="sxs-lookup"><span data-stu-id="98eb9-115">_lpproptagColumnsNew_</span></span>
  
> <span data-ttu-id="98eb9-116">順番表の先頭に追加または移動するプロパティのプロパティタグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="98eb9-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags for the properties to be added or moved to the beginning of the table.</span></span> 
    
 <span data-ttu-id="98eb9-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="98eb9-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="98eb9-118">順番メモリの割り当てに使用される[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="98eb9-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="98eb9-119">_lpfreebuffer_</span><span class="sxs-lookup"><span data-stu-id="98eb9-119">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="98eb9-120">順番メモリを解放するために使用される[MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="98eb9-120">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="98eb9-121">_lpfnFilterColumns_</span><span class="sxs-lookup"><span data-stu-id="98eb9-121">_lpfnFilterColumns_</span></span>
  
> <span data-ttu-id="98eb9-122">順番呼び出し元によって送信されたコールバック関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="98eb9-122">[in] Pointer to a callback function furnished by the caller.</span></span> <span data-ttu-id="98eb9-123">_lpfnFilterColumns_パラメーターが NULL に設定されている場合は、コールバックは行われません。</span><span class="sxs-lookup"><span data-stu-id="98eb9-123">If the  _lpfnFilterColumns_ parameter is set to NULL, no callback is made.</span></span> 
    
 <span data-ttu-id="98eb9-124">_ptaga_</span><span class="sxs-lookup"><span data-stu-id="98eb9-124">_ptaga_</span></span>
  
> <span data-ttu-id="98eb9-125">順番プロパティを追加または先頭に移動する前に、テーブルに既に存在しているプロパティタグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="98eb9-125">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the array of property tags already existing in the table before properties are added or moved to the beginning.</span></span> <span data-ttu-id="98eb9-126">**hraddcolumnsex**は、 _lpfnFilterColumns_によって参照されるコールバック関数へのパラメーターとしてこのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="98eb9-126">**HrAddColumnsEx** passes this pointer as the parameter to the callback function pointed to by  _lpfnFilterColumns_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="98eb9-127">戻り値</span><span class="sxs-lookup"><span data-stu-id="98eb9-127">Return value</span></span>

<span data-ttu-id="98eb9-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="98eb9-128">S_OK</span></span> 
  
> <span data-ttu-id="98eb9-129">呼び出しが成功し、指定された列が移動または追加されました。</span><span class="sxs-lookup"><span data-stu-id="98eb9-129">The call succeeded and the specified columns were moved or added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="98eb9-130">解説</span><span class="sxs-lookup"><span data-stu-id="98eb9-130">Remarks</span></span>

<span data-ttu-id="98eb9-131">_lpproptagColumnsNew_パラメーターを使用して**hraddcolumnsex**に渡されたプロパティは、次に[IMAPITable:: QueryRows](imapitable-queryrows.md)メソッドを呼び出したときに公開される最初のプロパティになります。</span><span class="sxs-lookup"><span data-stu-id="98eb9-131">The properties passed to **HrAddColumnsEx** using the  _lpproptagColumnsNew_ parameter become the first properties exposed on subsequent calls to the [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> <span data-ttu-id="98eb9-132">_lpproptagColumnsNew_パラメーターで指定されていないテーブル内のプロパティはすべて、追加されて移動されたプロパティの後に公開されます。</span><span class="sxs-lookup"><span data-stu-id="98eb9-132">Any properties previously in the table that were not specified in the  _lpproptagColumnsNew_ parameter are exposed after all the added and moved properties.</span></span> 
  
<span data-ttu-id="98eb9-133">**QueryRows**が呼び出されたときにテーブルのプロパティが未定義の場合は、プロパティの種類 PT_NULL およびプロパティ識別子 PROP_ID_NULL を使用して返されます。</span><span class="sxs-lookup"><span data-stu-id="98eb9-133">If any table properties are undefined when **QueryRows** is called, they are returned with property type PT_NULL and property identifier PROP_ID_NULL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="98eb9-134">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="98eb9-134">Notes to callers</span></span>

<span data-ttu-id="98eb9-135">**hraddcolumnsex**関数を使用すると、呼び出し元は、テーブル内に既に存在している列をフィルター処理するためのコールバック関数を与えることができます。たとえば、文字列をプロパティ型 PT_UNICODE から PT_STRING8 に変換します。</span><span class="sxs-lookup"><span data-stu-id="98eb9-135">The **HrAddColumnsEx** function allows the caller to furnish a callback function to filter the columns that were already in the table, for example to convert strings from property type PT_UNICODE to PT_STRING8.</span></span> <span data-ttu-id="98eb9-136">**hraddcolumnsex**は、コールバック関数へのパラメーターとして既に存在する列セットへのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="98eb9-136">**HrAddColumnsEx** passes a pointer to the previously existing column set as the parameter to the callback function.</span></span> <span data-ttu-id="98eb9-137">コールバック関数は、property タグ配列内のデータを変更できますが、新しいタグを追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="98eb9-137">The callback function can change data in the property tag array but cannot add new tags.</span></span> 
  
 <span data-ttu-id="98eb9-138">**hraddcolumnsex**は、最初にコールバック関数を呼び出し、次に、指定された列を追加または移動して、最後に[IMAPITable:: SetColumns](imapitable-setcolumns.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="98eb9-138">**HrAddColumnsEx** first calls the callback function if one is furnished, then adds or moves the specified columns, and finally calls [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span> 
  
<span data-ttu-id="98eb9-139">_lpAllocateBuffer_および_lpfreebuffer_入力パラメーターは、それぞれ[MAPIAllocateBuffer](mapiallocatebuffer.md)関数と[MAPIFreeBuffer](mapifreebuffer.md)関数をポイントします。</span><span class="sxs-lookup"><span data-stu-id="98eb9-139">The  _lpAllocateBuffer_ and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="98eb9-140">**hraddcolumnsex**に渡されるポインターの正確な値は、呼び出し元がクライアントアプリケーションであるかサービスプロバイダーであるかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="98eb9-140">The exact values of the pointers passed to **HrAddColumnsEx** depend on whether the caller is a client application or a service provider.</span></span> <span data-ttu-id="98eb9-141">クライアントは、指定された名前を持つ MAPI 関数へのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="98eb9-141">A client passes pointers to the MAPI functions with the specified names.</span></span> <span data-ttu-id="98eb9-142">サービスプロバイダーは、初期化呼び出しで受け取ったポインターまたは[imapisupport:: getmemallocroutines](imapisupport-getmemallocroutines.md)メソッドを呼び出して取得したポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="98eb9-142">A service provider passes the pointers it received in its initialization call or retrieved by calling the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="98eb9-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="98eb9-143">See also</span></span>



[<span data-ttu-id="98eb9-144">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="98eb9-144">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)

