---
title: IMAPISupportDoCopyTo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoCopyTo
api_type:
- COM
ms.assetid: 84019475-5176-4fc5-a3ee-871095077498
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6f6c802f1d5ead1750c05fafc54533487fe3732a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331809"
---
# <a name="imapisupportdocopyto"></a><span data-ttu-id="e8d1c-103">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="e8d1c-103">IMAPISupport::DoCopyTo</span></span>

  
  
<span data-ttu-id="e8d1c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8d1c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8d1c-105">特定の除外プロパティを除く、1 つのオブジェクトのすべてのプロパティを別のオブジェクトにコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-105">Copies or moves all properties of one object, except for specifically excluded properties, to another object.</span></span>
  
```cpp
HRESULT DoCopyTo(
  LPCIID lpSrcInterface,
  LPVOID lpSrcObj,
  ULONG ciidExclude,
  LPCIID rgiidExclude,
  LPSPropTagArray lpExcludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpDestInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="e8d1c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e8d1c-106">Parameters</span></span>

 <span data-ttu-id="e8d1c-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="e8d1c-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="e8d1c-108">[in]コピーまたは移動するプロパティを持つオブジェクトにアクセスするために使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object that has the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="e8d1c-109">_lpSrcObj_</span><span class="sxs-lookup"><span data-stu-id="e8d1c-109">_lpSrcObj_</span></span>
  
> <span data-ttu-id="e8d1c-110">[in]コピーまたは移動するプロパティを持つオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-110">[in] A pointer to the object that has the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="e8d1c-111">_ciidExclude_</span><span class="sxs-lookup"><span data-stu-id="e8d1c-111">_ciidExclude_</span></span>
  
> <span data-ttu-id="e8d1c-112">[in]プロパティをコピーまたは移動するときに除外するインターフェイスの数。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-112">[in] The count of interfaces to exclude when you copy or move properties.</span></span>
    
 <span data-ttu-id="e8d1c-113">_rgiidExclude_</span><span class="sxs-lookup"><span data-stu-id="e8d1c-113">_rgiidExclude_</span></span>
  
> <span data-ttu-id="e8d1c-114">[in]補足情報をコピーまたは移動先オブジェクトに移動するときに使用しないインターフェイスを示すインターフェイス識別子の配列。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-114">[in] An array of interface identifiers that indicates interfaces that should not be used when you copy or move supplemental information to the destination object.</span></span>
    
 <span data-ttu-id="e8d1c-115">_lpExcludeProps_</span><span class="sxs-lookup"><span data-stu-id="e8d1c-115">_lpExcludeProps_</span></span>
  
> <span data-ttu-id="e8d1c-116">[in]コピーまたは移動操作から除外する必要があるプロパティ タグを識別するプロパティ タグ配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-116">[in] A pointer to a property tag array that identifies the property tags that should be excluded from the copy or move operation.</span></span> <span data-ttu-id="e8d1c-117">_lpExcludeProps_ パラメーターに NULL を渡す場合は、オブジェクトのすべてのプロパティをコピーまたは移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-117">Passing NULL in the  _lpExcludeProps_ parameter indicates that all of the object's properties should be copied or moved.</span></span> <span data-ttu-id="e8d1c-118">**DoCopyTo** は **、lpExcludeProps** MAPI_E_INVALID_PARAMETER示す [SPropTagArray](sproptagarray.md) 構造体の  _cValues_ メンバーが 0 に設定されている場合に、この値を返します。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-118">**DoCopyTo** returns MAPI_E_INVALID_PARAMETER when the **cValues** member of the [SPropTagArray](sproptagarray.md) structure pointed to by  _lpExcludeProps_ is set to 0.</span></span> 
    
 <span data-ttu-id="e8d1c-119">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="e8d1c-119">_ulUIParam_</span></span>
  
> <span data-ttu-id="e8d1c-120">[in]進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-120">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="e8d1c-121">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="e8d1c-121">_lpProgress_</span></span>
  
> <span data-ttu-id="e8d1c-122">[in]進行状況インジケーターの実装へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-122">[in] A pointer to a progress indicator implementation.</span></span> <span data-ttu-id="e8d1c-123">_lpProgress_ パラメーターで NULL が渡された場合、MAPI は進行状況の実装を提供します。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-123">If NULL is passed in the  _lpProgress_ parameter, MAPI provides the progress implementation.</span></span> <span data-ttu-id="e8d1c-124">_lpProgress パラメーター_ は _、ulFlags_ パラメーター MAPI_DIALOGフラグが設定されていない限り、無視されます。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-124">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="e8d1c-125">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="e8d1c-125">_lpDestInterface_</span></span>
  
> <span data-ttu-id="e8d1c-126">[in]コピーまたは移動されたプロパティを受け取るオブジェクトにアクセスするために使用するインターフェイスを表すインターフェイス識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-126">[in] A pointer to the interface identifier that represents the interface to be used to access the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="e8d1c-127">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="e8d1c-127">_lpDestObj_</span></span>
  
> <span data-ttu-id="e8d1c-128">[in]コピーまたは移動されたプロパティを受け取るオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-128">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="e8d1c-129">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e8d1c-129">_ulFlags_</span></span>
  
> <span data-ttu-id="e8d1c-130">[in]コピーまたは移動操作を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-130">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="e8d1c-131">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-131">The following flags can be set:</span></span>
    
<span data-ttu-id="e8d1c-132">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="e8d1c-132">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="e8d1c-133">進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-133">Displays a progress indicator.</span></span> 
    
<span data-ttu-id="e8d1c-134">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="e8d1c-134">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="e8d1c-135">**DoCopyTo は** 、コピー操作の代わりに移動操作を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-135">**DoCopyTo** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="e8d1c-136">このフラグが設定されていない場合 **、DoCopyTo は** コピー操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-136">When this flag is not set, **DoCopyTo** performs a copy operation.</span></span> 
    
<span data-ttu-id="e8d1c-137">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="e8d1c-137">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="e8d1c-138">移動先オブジェクト内の既存のプロパティは上書きしないでください。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-138">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="e8d1c-139">このフラグを設定しない場合 **、DoCopyTo は** 既存のプロパティを上書きします。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-139">When this flag is not set, **DoCopyTo** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="e8d1c-140">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="e8d1c-140">_lppProblems_</span></span>
  
> <span data-ttu-id="e8d1c-141">[out]入力時に [、SPropProblemArray](spropproblemarray.md) 構造体へのポインターを指すポインター。それ以外の場合は、エラー情報を必要としない NULL を指定します。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-141">[out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates no need for error information.</span></span> <span data-ttu-id="e8d1c-142">_lppProblems が_ 入力の有効なポインターである場合 **、DoCopyTo** は 1 つ以上のプロパティをコピーするエラーに関する詳細情報を返します。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-142">If  _lppProblems_ is a valid pointer on input, **DoCopyTo** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e8d1c-143">戻り値</span><span class="sxs-lookup"><span data-stu-id="e8d1c-143">Return value</span></span>

<span data-ttu-id="e8d1c-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="e8d1c-144">S_OK</span></span> 
  
> <span data-ttu-id="e8d1c-145">プロパティが正常にコピーまたは移動されました。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-145">The properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="e8d1c-146">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="e8d1c-146">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="e8d1c-147">コピーまたは移動するプロパティは、コピー先オブジェクトに既に存在し、MAPI_NOREPLACEフラグが設定されます。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-147">A property to be copied or moved already exists in the destination object and the MAPI_NOREPLACE flag is set.</span></span> 
    
<span data-ttu-id="e8d1c-148">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="e8d1c-148">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="e8d1c-149">ソース オブジェクトには、直接または間接的に移動先オブジェクトが含まれる。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-149">The source object directly or indirectly contains the destination object.</span></span> <span data-ttu-id="e8d1c-150">この条件が検出される前に重要な作業が実行された可能性があります。そのため、ソース オブジェクトと移動先オブジェクトが部分的に変更される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-150">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="e8d1c-151">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="e8d1c-151">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="e8d1c-152">_lpSrcInterface_ パラメーターで識別されるインターフェイスは _、lpSrcObj_ によって指されるオブジェクトではサポートされていません。または _lpDestInterface_ パラメーターで識別されるインターフェイスは _、lpDestObj_ によって指されるオブジェクトではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-152">The interface identified by the  _lpSrcInterface_ parameter is not supported by the object pointed to by  _lpSrcObj_, or the interface identified by the  _lpDestInterface_ parameter is not supported by the object pointed to by  _lpDestObj_.</span></span> 
    
<span data-ttu-id="e8d1c-153">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="e8d1c-153">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="e8d1c-154">呼び出し元のアクセス許可が不十分なオブジェクトにアクセスしようとした。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-154">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="e8d1c-155">このエラーは、移動先オブジェクトがソース オブジェクトと同じ場合に返されます。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-155">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="e8d1c-156">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e8d1c-156">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="e8d1c-157">_lpSrcInterface パラメーター_ は NULL です。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-157">The  _lpSrcInterface_ parameter is NULL.</span></span> 
    
<span data-ttu-id="e8d1c-158">次の値は **、SPropProblemArray** 構造体で返されますが、DoCopyTo の戻り値 **として返す値として返す必要があります**。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-158">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **DoCopyTo**.</span></span> <span data-ttu-id="e8d1c-159">これらのエラーは、1 つのプロパティに適用されます。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-159">These errors apply to a single property.</span></span>
  
<span data-ttu-id="e8d1c-160">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="e8d1c-160">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="e8d1c-161">このフラグMAPI_UNICODE設定され **、DoCopyTo** が Unicode をサポートしていないか、または設定されていない場合MAPI_UNICODE **DoCopyTo** は Unicode のみをサポートします。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-161">Either the MAPI_UNICODE flag was set and **DoCopyTo** does not support Unicode, or MAPI_UNICODE was not set and **DoCopyTo** supports only Unicode.</span></span> 
    
<span data-ttu-id="e8d1c-162">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="e8d1c-162">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="e8d1c-163">プロパティは、読み取り専用プロパティなので、呼び出し元が変更することはできません。これは、移動先オブジェクトの所有者によって計算されます。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-163">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="e8d1c-164">このエラーは重大ではありません。呼び出し元は、コピー操作の続行を許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-164">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="e8d1c-165">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="e8d1c-165">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="e8d1c-166">プロパティの種類が無効です。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-166">The property type is invalid.</span></span>
    
<span data-ttu-id="e8d1c-167">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="e8d1c-167">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="e8d1c-168">プロパティの種類は、呼び出し元が予期する型ではありません。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-168">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e8d1c-169">注釈</span><span class="sxs-lookup"><span data-stu-id="e8d1c-169">Remarks</span></span>

<span data-ttu-id="e8d1c-170">**IMAPISupport::D oCopyTo** メソッドは、メッセージ ストア プロバイダーのサポート オブジェクトに実装されます。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-170">The **IMAPISupport::DoCopyTo** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="e8d1c-171">メッセージ ストア プロバイダーは **、DoCopyTo** を呼び出して、フォルダーとメッセージ [の IMAPIProp::CopyTo](imapiprop-copyto.md) メソッドを実装できます。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-171">Message store providers can call **DoCopyTo** to implement the [IMAPIProp::CopyTo](imapiprop-copyto.md) method for their folders and messages.</span></span> 
  
<span data-ttu-id="e8d1c-172">既定では **、DoCopyTo は** 1 つのオブジェクトのすべてのプロパティを別のオブジェクトにコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-172">By default, **DoCopyTo** copies or moves all of the properties of one object to another object.</span></span> <span data-ttu-id="e8d1c-173">ソース オブジェクト内のサブオブジェクトは、自動的に操作に含まれてコピーまたは移動されます。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-173">Any subobjects in the source object are automatically included in the operation and copied or moved in their entirety.</span></span> 
  
<span data-ttu-id="e8d1c-174">コピーまたは移動されたプロパティがコピー先オブジェクトに既に存在する場合、MAPI_NOREPLACE フラグが  _ulFlags_ パラメーターに設定されていない限り、既存のプロパティは新しいプロパティによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-174">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="e8d1c-175">上書きされない移動先オブジェクト内の既存の情報はそのまま残ります。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-175">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e8d1c-176">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="e8d1c-176">Notes to callers</span></span>

<span data-ttu-id="e8d1c-177">コピーまたは移動操作からプロパティを除外するには、プロパティ タグを  _lpExcludeProps パラメーターに含_ める必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-177">To exclude properties from the copy or move operation, include their property tags in the  _lpExcludeProps_ parameter.</span></span> <span data-ttu-id="e8d1c-178">[PROP_TAG](prop_tag.md)マクロを使用してプロパティ タグ配列内の特定の識別子からプロパティ タグを作成した結果を渡した場合、その識別子を持つすべてのプロパティは除外されます。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-178">If you pass the results of using the [PROP_TAG](prop_tag.md) macro to build a property tag from a specific identifier in the property tag array, all properties with that identifier will be excluded.</span></span> <span data-ttu-id="e8d1c-179">たとえば、プロパティ タグ配列の次のエントリでは、型に関係なく、識別子を持つすべてのプロパティ0x8002除外されます。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-179">For example, the following entry in the property tag array causes all properties with an identifier of 0x8002 to be excluded, regardless of type:</span></span> 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
<span data-ttu-id="e8d1c-180">メッセージを別のフォルダーにコピーするときにメッセージの配信時間をコピーしないようにするには、プロパティ タグ exclude 配列に **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) を指定します。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-180">To avoid copying a message's delivery time when you copy the message to a different folder, specify **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) in the property tag exclude array.</span></span> <span data-ttu-id="e8d1c-181">メッセージの受信者リストを除外するには、PR_MESSAGE_RECIPIENTS **(** [PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) プロパティを exclude 配列に追加します。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-181">To exclude a message's recipient list, add the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property to the exclude array.</span></span> <span data-ttu-id="e8d1c-182">メッセージの添付ファイルを除外するには、PR_MESSAGE_ATTACHMENTS **(** [PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) プロパティを配列に追加します。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-182">To exclude a message's attachments, add the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property to the array.</span></span>
  
<span data-ttu-id="e8d1c-183">同様に、フォルダーまたはアドレス帳コンテナーの階層またはコンテンツ テーブルのコピーまたは移動を防止するには、プロパティ タグの除外配列に **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) または **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-183">Similarly, to prevent the copying or moving of a folder or address book container's hierarchy or contents table, include **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag exclude array.</span></span>
  
<span data-ttu-id="e8d1c-184">_lppProblems_ パラメーター MAPI_E_COMPUTED **SPropProblemArray** 構造体で返されるエラーを無視します。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-184">Ignore MAPI_E_COMPUTED errors returned in the **SPropProblemArray** structure in the  _lppProblems_ parameter.</span></span> 
  
<span data-ttu-id="e8d1c-185">_lpSrcInterface_ がポイントするインターフェイス識別子は、通常 _、lpDestInterface_ がポイントするインターフェイス識別子と同じです。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-185">The interface identifier that  _lpSrcInterface_ points to is usually the same as the interface identifier that  _lpDestInterface_ points to.</span></span> 
  
<span data-ttu-id="e8d1c-186">_lpDestInterface_ で許容可能なインターフェイス識別子を渡し _、lpDestObj_ で無効なポインターを渡した場合、結果は予測できません。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-186">If you pass an acceptable interface identifier in  _lpDestInterface_ but an invalid pointer in  _lpDestObj_, the results are unpredictable.</span></span> <span data-ttu-id="e8d1c-187">ほとんどの場合、これはプロバイダーが失敗する原因になります。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-187">Most likely this will cause your provider to fail.</span></span> 
  
<span data-ttu-id="e8d1c-188">逆に、コピーまたは移動しない補足情報を認識している場合は  _、rgiidExclude_ パラメーターで渡された配列で除外するインターフェイスのインターフェイス識別子を追加します。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-188">Conversely, if you are aware of supplemental information that should not be copied or moved, add the interface identifiers for the interfaces to be excluded in the array passed in the  _rgiidExclude_ parameter.</span></span> <span data-ttu-id="e8d1c-189">たとえば、メッセージをコピーするが、メッセージ添付ファイルをコピーしない場合は  _、rgiidExclude_ 配列IID_IMessageを渡します。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-189">For example, if you are copying messages, but not any of their message attachments, pass IID_IMessage in the  _rgiidExclude_ array.</span></span> <span data-ttu-id="e8d1c-190">**DoCopyTo** は  _、rgiidExclude_ で認識されないインターフェイスを無視します。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-190">**DoCopyTo** ignores any interfaces listed in  _rgiidExclude_ that it does not recognize.</span></span> 
  
<span data-ttu-id="e8d1c-191">_rgiidExclude_ パラメーターを使用してインターフェイスを除外すると、そのインターフェイスから派生したインターフェイスもすべて除外されます。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-191">When you use the  _rgiidExclude_ parameter to exclude an interface, it also excludes all interfaces derived from that interface.</span></span> <span data-ttu-id="e8d1c-192">たとえば [、IMAPIContainer](imapicontainerimapiprop.md) インターフェイスを除外すると、プロバイダーの種類に応じてフォルダーまたはアドレス帳コンテナーが除外されます。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-192">For example, excluding the [IMAPIContainer](imapicontainerimapiprop.md) interface causes folders or address book containers to be excluded, depending on the type of provider.</span></span> <span data-ttu-id="e8d1c-193">[IMAPIProp](imapipropiunknown.md)または[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)は、多くのインターフェイスから派生しますので、除外しません。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-193">Do not exclude [IMAPIProp](imapipropiunknown.md) or [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) because so many interfaces derive from them.</span></span> 
  
 <span data-ttu-id="e8d1c-194">**DoCopyTo は** 、操作全体に適用されるグローバル エラーと、個々のプロパティに適用される個々のエラーを報告します。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-194">**DoCopyTo** reports global errors that apply to the operation as a whole, and individual errors that apply to individual properties.</span></span> <span data-ttu-id="e8d1c-195">これらの個々のエラーは **、SPropProblemArray 構造体に入** れ込まれています。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-195">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="e8d1c-196">プロパティの問題配列構造パラメーターに対して、有効なポインターではなく NULL を渡して、プロパティ レベルでエラー報告を抑制できます。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-196">You can suppress error reporting at the property level by passing NULL, rather than a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="e8d1c-197">エラーに関する情報を受け取る場合は _、lppProblems_ パラメーターに有効な **SPropProblemArray** 構造体ポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-197">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="e8d1c-198">**DoCopyTo が** プロパティを返S_OK、構造内の個々のプロパティで発生する可能性のあるエラーを確認します。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-198">When **DoCopyTo** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="e8d1c-199">**DoCopyTo が** エラーを返す場合 **、SPropProblemArray 構造体には情報は返** されません。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-199">When **DoCopyTo** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="e8d1c-200">代わりに [、IMAPISupport::GetLastError](imapisupport-getlasterror.md) メソッドを呼び出して、詳細なエラー情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-200">Instead, call the [IMAPISupport::GetLastError](imapisupport-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="e8d1c-201">**DoCopyTo が** 関数を返S_OK [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、返される **SPropProblemArray** 構造体を解放します。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-201">If **DoCopyTo** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="e8d1c-202">**DoCopyTo** 呼び出しでグローバル エラーが発生した場合は **、SPropProblemArray** 構造体を使用したり解放したりしません。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-202">If a global error occurs on the **DoCopyTo** call, do not use or free the **SPropProblemArray** structure.</span></span> <span data-ttu-id="e8d1c-203">プロバイダーは  _、DoCopyTo_ によって返される **SPropProblemArray** 構造体の **ulIndex メンバーを無視する必要があります**。</span><span class="sxs-lookup"><span data-stu-id="e8d1c-203">Providers should ignore the  _ulIndex_ member in **SPropProblemArray** structures returned by **DoCopyTo**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e8d1c-204">関連項目</span><span class="sxs-lookup"><span data-stu-id="e8d1c-204">See also</span></span>



[<span data-ttu-id="e8d1c-205">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="e8d1c-205">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="e8d1c-206">IMAPISupport::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="e8d1c-206">IMAPISupport::CopyFolder</span></span>](imapisupport-copyfolder.md)
  
[<span data-ttu-id="e8d1c-207">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="e8d1c-207">IMAPISupport::CopyMessages</span></span>](imapisupport-copymessages.md)
  
[<span data-ttu-id="e8d1c-208">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="e8d1c-208">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="e8d1c-209">PidTagContainerContents 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e8d1c-209">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="e8d1c-210">PidTagContainerHierarchy 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e8d1c-210">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="e8d1c-211">PidTagMessageAttachments 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e8d1c-211">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="e8d1c-212">PidTagMessageDeliveryTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e8d1c-212">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)
  
[<span data-ttu-id="e8d1c-213">PidTagMessageRecipients 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e8d1c-213">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="e8d1c-214">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="e8d1c-214">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="e8d1c-215">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="e8d1c-215">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="e8d1c-216">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e8d1c-216">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

