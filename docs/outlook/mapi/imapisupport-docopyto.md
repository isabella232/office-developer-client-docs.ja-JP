---
title: imapisupportdocopyto
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
# <a name="imapisupportdocopyto"></a><span data-ttu-id="10a0d-103">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="10a0d-103">IMAPISupport::DoCopyTo</span></span>

  
  
<span data-ttu-id="10a0d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10a0d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10a0d-105">明示的に除外されたプロパティを除き、1つのオブジェクトのすべてのプロパティを別のオブジェクトにコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="10a0d-105">Copies or moves all properties of one object, except for specifically excluded properties, to another object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="10a0d-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="10a0d-106">Parameters</span></span>

 <span data-ttu-id="10a0d-107">_lpsrcinterface_</span><span class="sxs-lookup"><span data-stu-id="10a0d-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="10a0d-108">順番コピーまたは移動するプロパティを持つオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="10a0d-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object that has the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="10a0d-109">_lpsrcobj_</span><span class="sxs-lookup"><span data-stu-id="10a0d-109">_lpSrcObj_</span></span>
  
> <span data-ttu-id="10a0d-110">順番コピーまたは移動するプロパティを持つオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="10a0d-110">[in] A pointer to the object that has the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="10a0d-111">_ciidExclude_</span><span class="sxs-lookup"><span data-stu-id="10a0d-111">_ciidExclude_</span></span>
  
> <span data-ttu-id="10a0d-112">順番プロパティをコピーまたは移動するときに除外するインターフェイスの数。</span><span class="sxs-lookup"><span data-stu-id="10a0d-112">[in] The count of interfaces to exclude when you copy or move properties.</span></span>
    
 <span data-ttu-id="10a0d-113">_rgiidExclude_</span><span class="sxs-lookup"><span data-stu-id="10a0d-113">_rgiidExclude_</span></span>
  
> <span data-ttu-id="10a0d-114">順番ターゲットオブジェクトに補足情報をコピーまたは移動するときに使用しないインターフェイスを示すインターフェイス識別子の配列。</span><span class="sxs-lookup"><span data-stu-id="10a0d-114">[in] An array of interface identifiers that indicates interfaces that should not be used when you copy or move supplemental information to the destination object.</span></span>
    
 <span data-ttu-id="10a0d-115">_lpexcludeprops_</span><span class="sxs-lookup"><span data-stu-id="10a0d-115">_lpExcludeProps_</span></span>
  
> <span data-ttu-id="10a0d-116">順番コピー操作または移動操作から除外する必要があるプロパティタグを識別するプロパティタグ配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="10a0d-116">[in] A pointer to a property tag array that identifies the property tags that should be excluded from the copy or move operation.</span></span> <span data-ttu-id="10a0d-117">_lpexcludeprops_パラメーターで NULL を渡すことは、オブジェクトのすべてのプロパティをコピーまたは移動する必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="10a0d-117">Passing NULL in the  _lpExcludeProps_ parameter indicates that all of the object's properties should be copied or moved.</span></span> <span data-ttu-id="10a0d-118">_lpexcludeprops_によって参照される[SPropTagArray](sproptagarray.md)構造の**cvalues**メンバが0に設定されている場合、 **docopyto**は MAPI_E_INVALID_PARAMETER を返します。</span><span class="sxs-lookup"><span data-stu-id="10a0d-118">**DoCopyTo** returns MAPI_E_INVALID_PARAMETER when the **cValues** member of the [SPropTagArray](sproptagarray.md) structure pointed to by  _lpExcludeProps_ is set to 0.</span></span> 
    
 <span data-ttu-id="10a0d-119">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="10a0d-119">_ulUIParam_</span></span>
  
> <span data-ttu-id="10a0d-120">順番進行状況インジケーターの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="10a0d-120">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="10a0d-121">_lpprogress_</span><span class="sxs-lookup"><span data-stu-id="10a0d-121">_lpProgress_</span></span>
  
> <span data-ttu-id="10a0d-122">順番進行状況インジケーターの実装へのポインター。</span><span class="sxs-lookup"><span data-stu-id="10a0d-122">[in] A pointer to a progress indicator implementation.</span></span> <span data-ttu-id="10a0d-123">_lpprogress_パラメーターで NULL が渡された場合、MAPI は進行状況の実装を提供します。</span><span class="sxs-lookup"><span data-stu-id="10a0d-123">If NULL is passed in the  _lpProgress_ parameter, MAPI provides the progress implementation.</span></span> <span data-ttu-id="10a0d-124">MAPI_DIALOG フラグが_ulflags_パラメーターで設定されていない場合、 _lpprogress_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="10a0d-124">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="10a0d-125">_lpdestinterface_</span><span class="sxs-lookup"><span data-stu-id="10a0d-125">_lpDestInterface_</span></span>
  
> <span data-ttu-id="10a0d-126">順番コピーまたは移動したプロパティを受け取るためのオブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="10a0d-126">[in] A pointer to the interface identifier that represents the interface to be used to access the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="10a0d-127">_lpdestobj_</span><span class="sxs-lookup"><span data-stu-id="10a0d-127">_lpDestObj_</span></span>
  
> <span data-ttu-id="10a0d-128">順番コピーまたは移動したプロパティを受け取るオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="10a0d-128">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="10a0d-129">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="10a0d-129">_ulFlags_</span></span>
  
> <span data-ttu-id="10a0d-130">順番コピー操作または移動操作を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="10a0d-130">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="10a0d-131">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="10a0d-131">The following flags can be set:</span></span>
    
<span data-ttu-id="10a0d-132">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="10a0d-132">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="10a0d-133">進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="10a0d-133">Displays a progress indicator.</span></span> 
    
<span data-ttu-id="10a0d-134">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="10a0d-134">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="10a0d-135">**docopyto**はコピー操作ではなく移動操作を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="10a0d-135">**DoCopyTo** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="10a0d-136">このフラグが設定されて\*\*\*\* いない場合は、コピー操作が実行されます。</span><span class="sxs-lookup"><span data-stu-id="10a0d-136">When this flag is not set, **DoCopyTo** performs a copy operation.</span></span> 
    
<span data-ttu-id="10a0d-137">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="10a0d-137">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="10a0d-138">対象のオブジェクト内の既存のプロパティは、上書きしないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="10a0d-138">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="10a0d-139">このフラグが設定されていない場合、 **docopyto**は既存のプロパティを上書きします。</span><span class="sxs-lookup"><span data-stu-id="10a0d-139">When this flag is not set, **DoCopyTo** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="10a0d-140">_lppproblems 問題_</span><span class="sxs-lookup"><span data-stu-id="10a0d-140">_lppProblems_</span></span>
  
> <span data-ttu-id="10a0d-141">読み上げinput の場合は、 [spropの配列](spropproblemarray.md)構造体へのポインターへのポインターを返します。それ以外の場合は、エラー情報を必要としないことを示す NULL。</span><span class="sxs-lookup"><span data-stu-id="10a0d-141">[out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates no need for error information.</span></span> <span data-ttu-id="10a0d-142">_lppproblems_が入力の有効なポインターである場合、 **docopyto**は、1つ以上のプロパティをコピーする際のエラーに関する詳細情報を返します。</span><span class="sxs-lookup"><span data-stu-id="10a0d-142">If  _lppProblems_ is a valid pointer on input, **DoCopyTo** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="10a0d-143">戻り値</span><span class="sxs-lookup"><span data-stu-id="10a0d-143">Return value</span></span>

<span data-ttu-id="10a0d-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="10a0d-144">S_OK</span></span> 
  
> <span data-ttu-id="10a0d-145">プロパティが正常にコピーまたは移動されました。</span><span class="sxs-lookup"><span data-stu-id="10a0d-145">The properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="10a0d-146">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="10a0d-146">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="10a0d-147">コピーまたは移動されるプロパティは、対象オブジェクトに既に存在し、MAPI_NOREPLACE フラグが設定されています。</span><span class="sxs-lookup"><span data-stu-id="10a0d-147">A property to be copied or moved already exists in the destination object and the MAPI_NOREPLACE flag is set.</span></span> 
    
<span data-ttu-id="10a0d-148">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="10a0d-148">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="10a0d-149">source オブジェクトは、直接または間接的に対象のオブジェクトを含みます。</span><span class="sxs-lookup"><span data-stu-id="10a0d-149">The source object directly or indirectly contains the destination object.</span></span> <span data-ttu-id="10a0d-150">この条件が検出される前に、重要な作業が実行されている可能性があるので、移行元と移行先のオブジェクトの一部が変更されている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="10a0d-150">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="10a0d-151">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="10a0d-151">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="10a0d-152">_lpsrcinterface_パラメーターで指定されたインターフェイスは、 _lpsrcobj_が指すオブジェクトではサポートされていません。 __ lpsrcinterface パラメーターによって識別されるインターフェイスは、lpsrcinterface が指すオブジェクトではサポートされていません。 __.</span><span class="sxs-lookup"><span data-stu-id="10a0d-152">The interface identified by the  _lpSrcInterface_ parameter is not supported by the object pointed to by  _lpSrcObj_, or the interface identified by the  _lpDestInterface_ parameter is not supported by the object pointed to by  _lpDestObj_.</span></span> 
    
<span data-ttu-id="10a0d-153">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="10a0d-153">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="10a0d-154">発信者が十分なアクセス許可を持っていないオブジェクトにアクセスしようとしました。</span><span class="sxs-lookup"><span data-stu-id="10a0d-154">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="10a0d-155">destination オブジェクトがソースオブジェクトと同じ場合、このエラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="10a0d-155">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="10a0d-156">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="10a0d-156">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="10a0d-157">_lpsrcinterface_パラメーターが NULL です。</span><span class="sxs-lookup"><span data-stu-id="10a0d-157">The  _lpSrcInterface_ parameter is NULL.</span></span> 
    
<span data-ttu-id="10a0d-158">次の値は、 **spropの配列**構造で返すことができますが、 **docopyto**の戻り値として返すことはできません。</span><span class="sxs-lookup"><span data-stu-id="10a0d-158">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **DoCopyTo**.</span></span> <span data-ttu-id="10a0d-159">これらのエラーは、1つのプロパティに適用されます。</span><span class="sxs-lookup"><span data-stu-id="10a0d-159">These errors apply to a single property.</span></span>
  
<span data-ttu-id="10a0d-160">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="10a0d-160">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="10a0d-161">MAPI_UNICODE フラグが設定されており、 **docopyto**が unicode をサポートしていないか、MAPI_UNICODE が設定されておらず、 **docopyto**で unicode のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="10a0d-161">Either the MAPI_UNICODE flag was set and **DoCopyTo** does not support Unicode, or MAPI_UNICODE was not set and **DoCopyTo** supports only Unicode.</span></span> 
    
<span data-ttu-id="10a0d-162">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="10a0d-162">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="10a0d-163">このプロパティは読み取り専用プロパティであるため、呼び出し元が変更することはできません。これは、対象オブジェクトの所有者によって計算されます。</span><span class="sxs-lookup"><span data-stu-id="10a0d-163">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="10a0d-164">このエラーは重大ではありません。呼び出し元がコピー操作を続行できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="10a0d-164">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="10a0d-165">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="10a0d-165">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="10a0d-166">プロパティの種類が無効です。</span><span class="sxs-lookup"><span data-stu-id="10a0d-166">The property type is invalid.</span></span>
    
<span data-ttu-id="10a0d-167">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="10a0d-167">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="10a0d-168">プロパティの型は、呼び出し元が想定した型ではありません。</span><span class="sxs-lookup"><span data-stu-id="10a0d-168">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="10a0d-169">解説</span><span class="sxs-lookup"><span data-stu-id="10a0d-169">Remarks</span></span>

<span data-ttu-id="10a0d-170">**imapisupport::D ocopyto**メソッドは、メッセージストアプロバイダーサポートオブジェクトに実装されています。</span><span class="sxs-lookup"><span data-stu-id="10a0d-170">The **IMAPISupport::DoCopyTo** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="10a0d-171">メッセージストアプロバイダーは、 **docopyto**を呼び出して、フォルダーとメッセージに[imapiprop:: CopyTo](imapiprop-copyto.md)メソッドを実装できます。</span><span class="sxs-lookup"><span data-stu-id="10a0d-171">Message store providers can call **DoCopyTo** to implement the [IMAPIProp::CopyTo](imapiprop-copyto.md) method for their folders and messages.</span></span> 
  
<span data-ttu-id="10a0d-172">既定では、 **docopyto**は、1つのオブジェクトのすべてのプロパティを別のオブジェクトにコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="10a0d-172">By default, **DoCopyTo** copies or moves all of the properties of one object to another object.</span></span> <span data-ttu-id="10a0d-173">source オブジェクト内のすべてのサブオブジェクトは、自動的に操作に含まれ、全体でコピーまたは移動されます。</span><span class="sxs-lookup"><span data-stu-id="10a0d-173">Any subobjects in the source object are automatically included in the operation and copied or moved in their entirety.</span></span> 
  
<span data-ttu-id="10a0d-174">コピーまたは移動されたプロパティのいずれかがコピー先オブジェクトに既に存在する場合、MAPI_NOREPLACE フラグが_ulflags_パラメーターで設定されていない限り、既存のプロパティは新しいプロパティによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="10a0d-174">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="10a0d-175">上書きされていない対象のオブジェクト内の既存の情報は、そのまま残ります。</span><span class="sxs-lookup"><span data-stu-id="10a0d-175">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="10a0d-176">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="10a0d-176">Notes to callers</span></span>

<span data-ttu-id="10a0d-177">コピー操作または移動操作からプロパティを除外するには、そのプロパティタグを_lpexcludeprops_パラメーターに含めます。</span><span class="sxs-lookup"><span data-stu-id="10a0d-177">To exclude properties from the copy or move operation, include their property tags in the  _lpExcludeProps_ parameter.</span></span> <span data-ttu-id="10a0d-178">[PROP_TAG](prop_tag.md)マクロを使用した結果を渡して、プロパティタグ配列の特定の識別子からプロパティタグを作成すると、その識別子を持つすべてのプロパティが除外されます。</span><span class="sxs-lookup"><span data-stu-id="10a0d-178">If you pass the results of using the [PROP_TAG](prop_tag.md) macro to build a property tag from a specific identifier in the property tag array, all properties with that identifier will be excluded.</span></span> <span data-ttu-id="10a0d-179">たとえば、次のエントリをプロパティタグ配列に配置すると、型に関係なく、0x8002 の識別子が含まれるすべてのプロパティが除外されます。</span><span class="sxs-lookup"><span data-stu-id="10a0d-179">For example, the following entry in the property tag array causes all properties with an identifier of 0x8002 to be excluded, regardless of type:</span></span> 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
<span data-ttu-id="10a0d-180">メッセージを別のフォルダーにコピーしたときにメッセージの配信時刻がコピーされないようにするには、property タグの除外配列で**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) を指定します。</span><span class="sxs-lookup"><span data-stu-id="10a0d-180">To avoid copying a message's delivery time when you copy the message to a different folder, specify **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) in the property tag exclude array.</span></span> <span data-ttu-id="10a0d-181">メッセージの宛先リストを除外するには、 **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) プロパティを exclude 配列に追加します。</span><span class="sxs-lookup"><span data-stu-id="10a0d-181">To exclude a message's recipient list, add the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property to the exclude array.</span></span> <span data-ttu-id="10a0d-182">メッセージの添付ファイルを除外するには、 **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) プロパティを配列に追加します。</span><span class="sxs-lookup"><span data-stu-id="10a0d-182">To exclude a message's attachments, add the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property to the array.</span></span>
  
<span data-ttu-id="10a0d-183">同様に、フォルダーまたはアドレス帳コンテナーの階層またはコンテンツテーブルをコピーまたは移動できないようにするには、 **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) または**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) プロパティタグの除外配列。</span><span class="sxs-lookup"><span data-stu-id="10a0d-183">Similarly, to prevent the copying or moving of a folder or address book container's hierarchy or contents table, include **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag exclude array.</span></span>
  
<span data-ttu-id="10a0d-184">_lppproblems_パラメーターの**sprop問題の配列**構造で返された MAPI_E_COMPUTED エラーを無視します。</span><span class="sxs-lookup"><span data-stu-id="10a0d-184">Ignore MAPI_E_COMPUTED errors returned in the **SPropProblemArray** structure in the  _lppProblems_ parameter.</span></span> 
  
<span data-ttu-id="10a0d-185">_lpsrcinterface_が指すインターフェイス識別子は、通常、 _lpsrcinterface_が指すインターフェイス識別子と同じです。</span><span class="sxs-lookup"><span data-stu-id="10a0d-185">The interface identifier that  _lpSrcInterface_ points to is usually the same as the interface identifier that  _lpDestInterface_ points to.</span></span> 
  
<span data-ttu-id="10a0d-186">_lpdestinterface_で受け入れ可能なインターフェイス識別子が渡され、 _lpdestinterface_に無効なポインターが渡された場合、結果は予測できません。</span><span class="sxs-lookup"><span data-stu-id="10a0d-186">If you pass an acceptable interface identifier in  _lpDestInterface_ but an invalid pointer in  _lpDestObj_, the results are unpredictable.</span></span> <span data-ttu-id="10a0d-187">ほとんどの場合、プロバイダーが失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="10a0d-187">Most likely this will cause your provider to fail.</span></span> 
  
<span data-ttu-id="10a0d-188">反対に、コピーまたは移動してはならない補足情報を認識している場合は、 _rgiidExclude_パラメーターで渡された配列で除外されるインターフェイスのインターフェイス識別子を追加します。</span><span class="sxs-lookup"><span data-stu-id="10a0d-188">Conversely, if you are aware of supplemental information that should not be copied or moved, add the interface identifiers for the interfaces to be excluded in the array passed in the  _rgiidExclude_ parameter.</span></span> <span data-ttu-id="10a0d-189">たとえば、メッセージをコピーするが、メッセージの添付ファイルをコピーしない場合は、 _rgiidExclude_配列に IID_IMessage を渡します。</span><span class="sxs-lookup"><span data-stu-id="10a0d-189">For example, if you are copying messages, but not any of their message attachments, pass IID_IMessage in the  _rgiidExclude_ array.</span></span> <span data-ttu-id="10a0d-190">\*\*\*\* _rgiidExclude_に一覧表示されているインターフェイスは無視されます。</span><span class="sxs-lookup"><span data-stu-id="10a0d-190">**DoCopyTo** ignores any interfaces listed in  _rgiidExclude_ that it does not recognize.</span></span> 
  
<span data-ttu-id="10a0d-191">_rgiidExclude_パラメーターを使用してインターフェイスを除外すると、そのインターフェイスから派生したすべてのインターフェイスも除外されます。</span><span class="sxs-lookup"><span data-stu-id="10a0d-191">When you use the  _rgiidExclude_ parameter to exclude an interface, it also excludes all interfaces derived from that interface.</span></span> <span data-ttu-id="10a0d-192">たとえば、 [IMAPIContainer](imapicontainerimapiprop.md)インターフェイスを除外すると、プロバイダーの種類に応じてフォルダーまたはアドレス帳コンテナーが除外されます。</span><span class="sxs-lookup"><span data-stu-id="10a0d-192">For example, excluding the [IMAPIContainer](imapicontainerimapiprop.md) interface causes folders or address book containers to be excluded, depending on the type of provider.</span></span> <span data-ttu-id="10a0d-193">[imapiprop](imapipropiunknown.md)または[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)から派生しているインターフェイスが多いため、これを除外しないでください。</span><span class="sxs-lookup"><span data-stu-id="10a0d-193">Do not exclude [IMAPIProp](imapipropiunknown.md) or [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) because so many interfaces derive from them.</span></span> 
  
 <span data-ttu-id="10a0d-194">**docopyto**は、操作全体に適用されるグローバルエラーと、個々のプロパティに適用される個々のエラーを報告します。</span><span class="sxs-lookup"><span data-stu-id="10a0d-194">**DoCopyTo** reports global errors that apply to the operation as a whole, and individual errors that apply to individual properties.</span></span> <span data-ttu-id="10a0d-195">これらの個々のエラーは、 **sprop問題の配列**構造に配置されます。</span><span class="sxs-lookup"><span data-stu-id="10a0d-195">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="10a0d-196">プロパティ問題の array 構造パラメーターに対して、有効なポインターではなく NULL を渡すことにより、プロパティレベルでエラー報告を抑制することができます。</span><span class="sxs-lookup"><span data-stu-id="10a0d-196">You can suppress error reporting at the property level by passing NULL, rather than a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="10a0d-197">エラーに関する情報を受信する必要がある場合は、 _lppproblems_パラメーターに有効な**sprop問題の配列**構造ポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="10a0d-197">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="10a0d-198">**docopyto**が S_OK を返す場合、構造内の個々のプロパティにエラーがあるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="10a0d-198">When **DoCopyTo** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="10a0d-199">**docopyto**がエラーを返す場合、 **sprop問題の配列**構造に情報は返されません。</span><span class="sxs-lookup"><span data-stu-id="10a0d-199">When **DoCopyTo** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="10a0d-200">代わりに、 [imapisupport:: GetLastError](imapisupport-getlasterror.md)メソッドを呼び出して詳細なエラー情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="10a0d-200">Instead, call the [IMAPISupport::GetLastError](imapisupport-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="10a0d-201">**docopyto**が S_OK を返す場合は、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによって返された**spropの配列**構造を解放します。</span><span class="sxs-lookup"><span data-stu-id="10a0d-201">If **DoCopyTo** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="10a0d-202">**docopyto**呼び出しでグローバルエラーが発生した場合は、sprop問題の**配列**構造を使用または解放しないでください。</span><span class="sxs-lookup"><span data-stu-id="10a0d-202">If a global error occurs on the **DoCopyTo** call, do not use or free the **SPropProblemArray** structure.</span></span> <span data-ttu-id="10a0d-203">プロバイダーは、 **docopyto**によって返される**spropの配列**構造で_ulindex_メンバーを無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="10a0d-203">Providers should ignore the  _ulIndex_ member in **SPropProblemArray** structures returned by **DoCopyTo**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="10a0d-204">関連項目</span><span class="sxs-lookup"><span data-stu-id="10a0d-204">See also</span></span>



[<span data-ttu-id="10a0d-205">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="10a0d-205">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="10a0d-206">IMAPISupport::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="10a0d-206">IMAPISupport::CopyFolder</span></span>](imapisupport-copyfolder.md)
  
[<span data-ttu-id="10a0d-207">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="10a0d-207">IMAPISupport::CopyMessages</span></span>](imapisupport-copymessages.md)
  
[<span data-ttu-id="10a0d-208">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="10a0d-208">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="10a0d-209">PidTagContainerContents 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="10a0d-209">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="10a0d-210">PidTagContainerHierarchy 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="10a0d-210">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="10a0d-211">PidTagMessageAttachments 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="10a0d-211">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="10a0d-212">PidTagMessageDeliveryTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="10a0d-212">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)
  
[<span data-ttu-id="10a0d-213">PidTagMessageRecipients 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="10a0d-213">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="10a0d-214">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="10a0d-214">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="10a0d-215">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="10a0d-215">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="10a0d-216">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="10a0d-216">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

