---
title: IMAPIPropGetProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetProps
api_type:
- COM
ms.assetid: 1c7a9cd2-d765-4218-9aee-52df1a2aae6c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9b03775d495f7d1f51142eb0ed06fc9ecdf6d1a3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412458"
---
# <a name="imapipropgetprops"></a><span data-ttu-id="21ac1-103">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="21ac1-103">IMAPIProp::GetProps</span></span>

  
  
<span data-ttu-id="21ac1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21ac1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21ac1-105">オブジェクトの1つ以上のプロパティのプロパティ値を取得します。</span><span class="sxs-lookup"><span data-stu-id="21ac1-105">Retrieves the property value of one or more properties of an object.</span></span>
  
```cpp
HRESULT GetProps(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="21ac1-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="21ac1-106">Parameters</span></span>

 <span data-ttu-id="21ac1-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="21ac1-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="21ac1-108">順番値を取得するプロパティを識別するプロパティタグの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="21ac1-108">[in] A pointer to an array of property tags that identify the properties whose values are to be retrieved.</span></span> <span data-ttu-id="21ac1-109">_lpPropTagArray_パラメーターは、オブジェクトのすべてのプロパティの値を返す必要があるか、または1つ以上の property タグを含む[SPropTagArray](sproptagarray.md)構造をポイントする必要があることを示す NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="21ac1-109">The  _lpPropTagArray_ parameter must be either NULL, indicating that values for all properties of the object should be returned, or point to an [SPropTagArray](sproptagarray.md) structure that contains one or more property tags.</span></span> 
    
 <span data-ttu-id="21ac1-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="21ac1-110">_ulFlags_</span></span>
  
> <span data-ttu-id="21ac1-111">順番PT_UNSPECIFIED 型のプロパティの形式を示すフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="21ac1-111">[in] A bitmask of flags that indicates the format for properties that have the type PT_UNSPECIFIED.</span></span> <span data-ttu-id="21ac1-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="21ac1-112">The following flag can be set:</span></span>
    
<span data-ttu-id="21ac1-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="21ac1-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="21ac1-114">これらのプロパティの文字列値は、Unicode 形式で返される必要があります。</span><span class="sxs-lookup"><span data-stu-id="21ac1-114">The string values for these properties should be returned in the Unicode format.</span></span> <span data-ttu-id="21ac1-115">MAPI_UNICODE フラグが設定されていない場合、文字列値は ANSI 形式で返されます。</span><span class="sxs-lookup"><span data-stu-id="21ac1-115">If the MAPI_UNICODE flag is not set, the string values should be returned in the ANSI format.</span></span>
    
 <span data-ttu-id="21ac1-116">_lpcValues_</span><span class="sxs-lookup"><span data-stu-id="21ac1-116">_lpcValues_</span></span>
  
> <span data-ttu-id="21ac1-117">読み上げ_lppproparray_パラメーターが指すプロパティ値の数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="21ac1-117">[out] A pointer to a count of property values pointed to by the  _lppPropArray_ parameter.</span></span> <span data-ttu-id="21ac1-118">_lppproparray_が NULL の場合、 _lpcValues_パラメーターの内容は0になります。</span><span class="sxs-lookup"><span data-stu-id="21ac1-118">If  _lppPropArray_ is NULL, the content of the  _lpcValues_ parameter is zero.</span></span> 
    
 <span data-ttu-id="21ac1-119">_lppproparray_</span><span class="sxs-lookup"><span data-stu-id="21ac1-119">_lppPropArray_</span></span>
  
> <span data-ttu-id="21ac1-120">読み上げ取得したプロパティ値へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="21ac1-120">[out] A pointer to a pointer to the retrieved property values.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="21ac1-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="21ac1-121">Return value</span></span>

<span data-ttu-id="21ac1-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="21ac1-122">S_OK</span></span> 
  
> <span data-ttu-id="21ac1-123">プロパティの値が正常に取得されました。</span><span class="sxs-lookup"><span data-stu-id="21ac1-123">The property values were successfully retrieved.</span></span>
    
<span data-ttu-id="21ac1-124">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="21ac1-124">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="21ac1-125">呼び出しは全体的に成功しましたが、1つ以上のプロパティにアクセスできませんでした。</span><span class="sxs-lookup"><span data-stu-id="21ac1-125">The call succeeded overall, but one or more properties could not be accessed.</span></span> <span data-ttu-id="21ac1-126">使用できない各プロパティのプロパティ値の**aulPropTag**メンバには、プロパティの種類が PT_ERROR で、識別子が0になっています。</span><span class="sxs-lookup"><span data-stu-id="21ac1-126">The **aulPropTag** member of the property value for each unavailable property has a property type of PT_ERROR and an identifier of zero.</span></span> <span data-ttu-id="21ac1-127">この警告が返された場合、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="21ac1-127">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="21ac1-128">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="21ac1-128">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="21ac1-129">詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="21ac1-129">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
<span data-ttu-id="21ac1-130">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="21ac1-130">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="21ac1-131">_lpPropTagArray_で参照されている**SPropTagArray**構造の**cvalues**メンバーに0が渡されました。</span><span class="sxs-lookup"><span data-stu-id="21ac1-131">Zero was passed in the **cValues** member of the **SPropTagArray** structure pointed to by  _lpPropTagArray_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="21ac1-132">注釈</span><span class="sxs-lookup"><span data-stu-id="21ac1-132">Remarks</span></span>

<span data-ttu-id="21ac1-133">**imapiprop:: GetProps**メソッドは、オブジェクトの1つ以上のプロパティのプロパティ値を取得します。</span><span class="sxs-lookup"><span data-stu-id="21ac1-133">The **IMAPIProp::GetProps** method obtains the property values of one or more properties of an object.</span></span> 
  
<span data-ttu-id="21ac1-134">プロパティ値は、要求されたときと同じ順序で返されます (つまり、 _lpPropTagArray_によって参照されているプロパティタグ配列内のプロパティの順序は、lppproparray が指すプロパティ値構造の配列内の順序と一致します) __).</span><span class="sxs-lookup"><span data-stu-id="21ac1-134">The property values are returned in the same order as they were requested (that is, the order of properties in the property tag array pointed to by  _lpPropTagArray_ matches the order in the array of property value structures pointed to by  _lppPropArray_).</span></span> 
  
<span data-ttu-id="21ac1-135">property タグ配列の**aulPropTag**メンバーで指定されているプロパティの種類は、各プロパティの値構造の**value**メンバーで返される値の種類を示します。</span><span class="sxs-lookup"><span data-stu-id="21ac1-135">The property types specified in the **aulPropTag** members of the property tag array indicate the type of value that should be returned in the **Value** member of each property value structure.</span></span> <span data-ttu-id="21ac1-136">ただし、呼び出し元がプロパティの型を知らない場合は、代わりに**aulPropTag**メンバーの型を PT_UNSPECIFIED に設定できます。</span><span class="sxs-lookup"><span data-stu-id="21ac1-136">However, if the caller does not know the type of a property, the type in the **aulPropTag** member can be set instead to PT_UNSPECIFIED.</span></span> <span data-ttu-id="21ac1-137">**GetProps**は、値を取得するときに、プロパティのプロパティ値構造の**aulPropTag**メンバーで適切な型を設定します。</span><span class="sxs-lookup"><span data-stu-id="21ac1-137">In retrieving the value, **GetProps** sets the correct type in the **aulPropTag** member of the property value structure for the property.</span></span> 
  
<span data-ttu-id="21ac1-138">プロパティの種類が_lpPropTagArray_の**SPropTagArray**で指定されている場合、 _lppproparray_に返される**spropvalue**のプロパティ値は、エラー値が返されない限り、要求された型と正確に一致する型を持っています。その代わりに。</span><span class="sxs-lookup"><span data-stu-id="21ac1-138">If property types are specified in the **SPropTagArray** in  _lpPropTagArray_, the property values in the **SPropValue** returned in  _lppPropArray_ have types that exactly match the requested types, unless an error value is returned instead.</span></span> 
  
<span data-ttu-id="21ac1-139">文字列プロパティには、次の2つのプロパティの種類のいずれかを指定できます: PT_UNICODE は、UNICODE 形式と PT_STRING8 を表す ANSI 形式を表します。</span><span class="sxs-lookup"><span data-stu-id="21ac1-139">String properties can have one of two property types: PT_UNICODE to represent the Unicode format and PT_STRING8 to represent the ANSI format.</span></span> <span data-ttu-id="21ac1-140">MAPI_UNICODE フラグが_ulflags_パラメーターで設定されている場合は、 **GetProps**が文字列プロパティの適切な形式を決定できないときに、その値を UNICODE 形式で返します。</span><span class="sxs-lookup"><span data-stu-id="21ac1-140">If the MAPI_UNICODE flag is set in the  _ulFlags_ parameter, whenever **GetProps** cannot determine the appropriate format for a string property, it returns its value in the Unicode format.</span></span> <span data-ttu-id="21ac1-141">**GetProps**は、次の状況では、正確な文字列プロパティの種類を特定できません。</span><span class="sxs-lookup"><span data-stu-id="21ac1-141">**GetProps** cannot determine an exact string property type in the following situations:</span></span> 
  
- <span data-ttu-id="21ac1-142">_lpPropTagArray_パラメーターは、すべてのプロパティを要求するために NULL に設定されています。</span><span class="sxs-lookup"><span data-stu-id="21ac1-142">The  _lpPropTagArray_ parameter is set to NULL to request all properties.</span></span> 
    
- <span data-ttu-id="21ac1-143">**aulPropTag**メンバーには、プロパティのタグ配列に、プロパティの型として PT_UNSPECIFIED 値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="21ac1-143">The **aulPropTag** member includes the value PT_UNSPECIFIED as its property type in the property tag array.</span></span> 
    
<span data-ttu-id="21ac1-144">オブジェクトのすべてのプロパティを取得するために_lpPropTagArray_パラメーターが NULL に設定されていて、プロパティが存在しない場合、 **GetProps**は次の処理を行います。</span><span class="sxs-lookup"><span data-stu-id="21ac1-144">If the  _lpPropTagArray_ parameter is set to NULL to retrieve all of the properties of the object and no properties exist, **GetProps** does the following:</span></span> 
  
- <span data-ttu-id="21ac1-145">S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="21ac1-145">Returns S_OK.</span></span>
    
- <span data-ttu-id="21ac1-146">プロパティ値構造の**cvalues**メンバーの count 値を0に設定します。</span><span class="sxs-lookup"><span data-stu-id="21ac1-146">Sets the count value in the **cValues** member of the property value structure to 0.</span></span> 
    
- <span data-ttu-id="21ac1-147">_lpcValues_の内容を0に設定します。</span><span class="sxs-lookup"><span data-stu-id="21ac1-147">Sets the contents of  _lpcValues_ to 0.</span></span> 
    
- <span data-ttu-id="21ac1-148">_lppproparray_を NULL に設定します。</span><span class="sxs-lookup"><span data-stu-id="21ac1-148">Sets  _lppPropArray_ to NULL.</span></span> 
    
 <span data-ttu-id="21ac1-149">**GetProps**は、 **cvalues**が0に設定された複数値のプロパティを返すことはできません。</span><span class="sxs-lookup"><span data-stu-id="21ac1-149">**GetProps** must not return multiple-value properties with **cValues** set to 0.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="21ac1-150">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="21ac1-150">Notes to implementers</span></span>

<span data-ttu-id="21ac1-151">[MAPIAllocateBuffer](mapiallocatebuffer.md)関数を呼び出して、 _lpPropTagArray_によってポイントされている[spropvalue](spropvalue.md)構造体の初期メモリを割り当てます。[MAPIAllocateMore](mapiallocatemore.md)を呼び出して、構造体のメンバーに必要な追加メモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="21ac1-151">Call the [MAPIAllocateBuffer](mapiallocatebuffer.md) function to allocate memory initially for the [SPropValue](spropvalue.md) structure pointed to by  _lpPropTagArray_; call [MAPIAllocateMore](mapiallocatemore.md) to allocate any additional memory needed for the structure's members.</span></span> 
  
<span data-ttu-id="21ac1-152">要求された1つ以上のプロパティの値を取得できない場合は、MAPI_W_ERRORS_RETURNED を返します。</span><span class="sxs-lookup"><span data-stu-id="21ac1-152">Return MAPI_W_ERRORS_RETURNED if you cannot retrieve the value for one or more of the requested properties.</span></span> <span data-ttu-id="21ac1-153">プロパティ値の構造で、 **aulPropTag**メンバーの型を PT_ERROR に設定し、 **value**メンバーを、エラーを説明する状態コードに設定します。</span><span class="sxs-lookup"><span data-stu-id="21ac1-153">In the property value structure, set the type in the **aulPropTag** member to PT_ERROR and the **Value** member to a status code that describes the error.</span></span> <span data-ttu-id="21ac1-154">たとえば、文字列を unicode に変換する必要があり、unicode をサポートしていない場合は、 **Value**メンバーを MAPI_E_BAD_CHARWIDTH に設定します。</span><span class="sxs-lookup"><span data-stu-id="21ac1-154">For example, if you have to convert a string to Unicode and do not support Unicode, set the **Value** member to MAPI_E_BAD_CHARWIDTH.</span></span> <span data-ttu-id="21ac1-155">プロパティが大きすぎる場合は、MAPI_E_NOT_ENOUGH_MEMORY に設定します。</span><span class="sxs-lookup"><span data-stu-id="21ac1-155">If the property is too large, set it to MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="21ac1-156">オブジェクトがプロパティをサポートしていない場合は、MAPI_E_NOT_FOUND に設定します。</span><span class="sxs-lookup"><span data-stu-id="21ac1-156">If the object does not support the property, set it to MAPI_E_NOT_FOUND.</span></span> 
  
<span data-ttu-id="21ac1-157">リモートトランスポートプロバイダーの**GetProps**メソッドの実装は、呼び出し元によって要求されたプロパティのフォルダーのプロパティ値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="21ac1-157">A remote transport provider's implementation of the **GetProps** method must return the folder's property values for properties requested by the caller.</span></span> <span data-ttu-id="21ac1-158">実装では、次のことを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="21ac1-158">Your implementation must do the following:</span></span> 
  
- <span data-ttu-id="21ac1-159">呼び出し元に返されるプロパティ値の配列を割り当て、そのアドレスを、その目的のために渡されたプロパティ値ポインターパラメーターに格納します。</span><span class="sxs-lookup"><span data-stu-id="21ac1-159">Allocate a property value array to return to the caller and store its address in the property value pointer parameter passed in for that purpose.</span></span>
    
- <span data-ttu-id="21ac1-160">**GetProps**に渡されたプロパティタグの配列に従って、フォルダーのプロパティのプロパティタグを、プロパティの値の配列のプロパティタグにコピーします。</span><span class="sxs-lookup"><span data-stu-id="21ac1-160">Copy the property tags from the folder's properties into the property tags in the property value array according to the array of property tags passed to **GetProps**.</span></span>
    
- <span data-ttu-id="21ac1-161">**GetProps**に渡されるすべてのプロパティタグについて、プロパティの型が設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="21ac1-161">Ensure that the property type is set for all property tags passed to **GetProps**.</span></span> <span data-ttu-id="21ac1-162">呼び出し元は、PT_UNSPECIFIED のプロパティの種類を渡すことができます。この場合、 **GetProps**は、そのプロパティタグに適切なプロパティの種類を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="21ac1-162">The caller can pass in a property type of PT_UNSPECIFIED, in which case **GetProps** must set the correct property type for that property tag.</span></span> 
    
- <span data-ttu-id="21ac1-163">プロパティ値配列の各プロパティの値をタグに従って設定します。</span><span class="sxs-lookup"><span data-stu-id="21ac1-163">Set the value of each property in the property value array according to its tag.</span></span> <span data-ttu-id="21ac1-164">たとえば、呼び出し元によって要求されたプロパティタグが**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) である場合、 **GetProps**は値を MAPI_FOLDER に設定できます。</span><span class="sxs-lookup"><span data-stu-id="21ac1-164">For example, if the property tag requested by the caller is **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)), **GetProps** can set the value to MAPI_FOLDER.</span></span> 
    
- <span data-ttu-id="21ac1-165">呼び出し元が、実装で処理されていないプロパティタグを渡した場合は、そのプロパティのプロパティタグを PT_ERROR に設定し、プロパティ値を MAPI_E_NOT_FOUND に設定します。</span><span class="sxs-lookup"><span data-stu-id="21ac1-165">If the caller passes in any property tags that your implementation does not handle, you can set the property tag to PT_ERROR for those properties, and set the property value to MAPI_E_NOT_FOUND.</span></span>
    
- <span data-ttu-id="21ac1-166">エラーが発生しなかった場合は S_OK を返し、エラーが発生した場合は MAPI_W_ERRORS_RETURNED を返します。</span><span class="sxs-lookup"><span data-stu-id="21ac1-166">Return S_OK if no errors occurred or MAPI_W_ERRORS_RETURNED if there were errors.</span></span>
    
<span data-ttu-id="21ac1-167">リモートトランスポートプロバイダーの**GetProps**メソッドの実装では、少なくとも次のプロパティをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="21ac1-167">A remote transport provider's implementation of the **GetProps** method must support the following properties at a minimum:</span></span> 
  
- <span data-ttu-id="21ac1-168">**PR_ACCESS**([PidTagAccess](pidtagaccess-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21ac1-168">**PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))</span></span>
    
- <span data-ttu-id="21ac1-169">**PR_ACCESS_LEVEL**([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21ac1-169">**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))</span></span>
    
- <span data-ttu-id="21ac1-170">**PR_ASSOC_CONTENT_COUNT**([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21ac1-170">**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="21ac1-171">**PR_CONTENT_COUNT**([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21ac1-171">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="21ac1-172">**PR_CREATION_TIME**([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21ac1-172">**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="21ac1-173">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21ac1-173">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="21ac1-174">**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21ac1-174">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
- <span data-ttu-id="21ac1-175">**PR_FOLDER_TYPE**([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21ac1-175">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>
    
- <span data-ttu-id="21ac1-176">**PR_OBJECT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="21ac1-176">**PR_OBJECT_TYPE**</span></span>
    
- <span data-ttu-id="21ac1-177">**PR_SUBFOLDERS**([PidTagSubfolders](pidtagsubfolders-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="21ac1-177">**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="21ac1-178">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="21ac1-178">Notes to callers</span></span>

<span data-ttu-id="21ac1-179">PT_OBJECT 型のプロパティの場合は、 **GetProps**ではなく、 [imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="21ac1-179">For properties of type PT_OBJECT, call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method instead of **GetProps**.</span></span> 
  
<span data-ttu-id="21ac1-180">セキュリティで保護されたプロパティの場合は、 _lppPropTagArray_パラメーターを NULL に設定して**GetProps**を呼び出すことによって、プロパティを取得する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="21ac1-180">For secure properties, do not expect to retrieve them by calling **GetProps** with the  _lppPropTagArray_ parameter set to NULL.</span></span> <span data-ttu-id="21ac1-181">**GetProps**を呼び出すときには、そのプロパティタグ配列の**aulPropTag**メンバーで、セキュリティで保護されたプロパティの識別子を明示的に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="21ac1-181">You must explicitly set a secure property's identifier in the **aulPropTag** member of its property tag array when you call **GetProps**.</span></span> <span data-ttu-id="21ac1-182">セキュリティで保護されたプロパティを使用可能にする時期と方法は、サービスプロバイダーによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="21ac1-182">When and how a secure property is available is up to the service provider.</span></span> 
  
<span data-ttu-id="21ac1-183">**GetProps**が S_OK または MAPI_W_ERRORS_RETURNED を返す場合にのみ、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことで、返される**spropvalue**構造を解放します。</span><span class="sxs-lookup"><span data-stu-id="21ac1-183">Free the returned **SPropValue** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function only if **GetProps** returns S_OK or MAPI_W_ERRORS_RETURNED.</span></span> 
  
<span data-ttu-id="21ac1-184">1つ以上のプロパティにアクセスできなかったために**GetProps**が MAPI_W_ERRORS_RETURNED を返す場合は、返されたプロパティのプロパティタグを確認してください。</span><span class="sxs-lookup"><span data-stu-id="21ac1-184">If **GetProps** returns MAPI_W_ERRORS_RETURNED because it could not access one or more properties, check the property tags of the returned properties.</span></span> <span data-ttu-id="21ac1-185">失敗したプロパティの値は、プロパティの値の構造に次の値が設定されます。</span><span class="sxs-lookup"><span data-stu-id="21ac1-185">The failed properties will have the following values set in their property value structure:</span></span> 
  
- <span data-ttu-id="21ac1-186">**aulPropTag**メンバーのプロパティの型が PT_ERROR に設定されます。</span><span class="sxs-lookup"><span data-stu-id="21ac1-186">The property type in the **aulPropTag** member set to PT_ERROR.</span></span> 
    
- <span data-ttu-id="21ac1-187">**value**メンバーのプロパティ値がエラーの状態コードに設定されています (MAPI_E_NOT_FOUND など)。</span><span class="sxs-lookup"><span data-stu-id="21ac1-187">The property value in the **Value** member set to a status code for the error, such as MAPI_E_NOT_FOUND.</span></span> 
    
<span data-ttu-id="21ac1-188">プロパティの値の構造体に返されるのが非常に大きいために失敗するプロパティは、その**値**のメンバーが MAPI_E_NOT_ENOUGH_MEMORY に設定されています。</span><span class="sxs-lookup"><span data-stu-id="21ac1-188">Properties that fail because they are too large to conveniently be returned in the property value structure have their **Value** member set to MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="21ac1-189">通常、このエラーは、プロパティの値が 4 KB 以上の場合に、PT_STRING8、PT_UNICODE、または PT_BINARY 型の文字列またはバイナリのプロパティを使用して発生します。</span><span class="sxs-lookup"><span data-stu-id="21ac1-189">Typically, this occurs with string or binary properties of type PT_STRING8, PT_UNICODE, or PT_BINARY when the value of the property is 4 KB or larger.</span></span> <span data-ttu-id="21ac1-190">大きなプロパティを取得するには、 **imapiprop:: openproperty**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="21ac1-190">Call **IMAPIProp::OpenProperty** to retrieve large properties.</span></span> 
  
<span data-ttu-id="21ac1-191">**GetProps**のすべての実装で、文字列の Unicode 形式と ANSI 形式の両方をサポートしているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="21ac1-191">Not all implementations of **GetProps** support both the Unicode and ANSI formats for character strings.</span></span> <span data-ttu-id="21ac1-192">特定のプロパティが文字列形式の変換を必要とし、 **GetProps**がそれをサポートできない場合、プロパティの**値**のメンバーは MAPI_E_BAD_CHARWIDTH に設定されます。</span><span class="sxs-lookup"><span data-stu-id="21ac1-192">When a particular property requires string format conversion and **GetProps** cannot support it, the **Value** member for the property is set to MAPI_E_BAD_CHARWIDTH.</span></span> 
  
<span data-ttu-id="21ac1-193">pst が SharePoint pst であるかどうかを確認するには、 [imapisession:: openmsgstore](imapisession-openmsgstore.md)を使用して pst をマウントし、このプロパティを要求しているメッセージストアオブジェクトで**GetProps**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="21ac1-193">To check if a PST is a SharePoint PST, mount the PST using [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md), then call **GetProps** on the message store object requesting this property.</span></span> <span data-ttu-id="21ac1-194">存在する場合は、SharePoint 用に PST が構成されていると想定できます。含まれていない場合、pst は SharePoint pst として構成されていません。</span><span class="sxs-lookup"><span data-stu-id="21ac1-194">If it exists, you can assume the PST has been configured for SharePoint; if not, the PST has not been configured as a SharePoint PST.</span></span> 
  
<span data-ttu-id="21ac1-195">**GetProps**を使用してプロパティにアクセスする方法の詳細については、「 [MAPI プロパティの取得](retrieving-mapi-properties.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="21ac1-195">For more information about how to use **GetProps** to access properties, see [Retrieving MAPI Properties](retrieving-mapi-properties.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="21ac1-196">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="21ac1-196">MFCMAPI reference</span></span>

<span data-ttu-id="21ac1-197">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="21ac1-197">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="21ac1-198">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="21ac1-198">**File**</span></span>|<span data-ttu-id="21ac1-199">**関数**</span><span class="sxs-lookup"><span data-stu-id="21ac1-199">**Function**</span></span>|<span data-ttu-id="21ac1-200">**コメント**</span><span class="sxs-lookup"><span data-stu-id="21ac1-200">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="21ac1-201">MAPIFunctions</span><span class="sxs-lookup"><span data-stu-id="21ac1-201">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="21ac1-202">GetPropsNULL</span><span class="sxs-lookup"><span data-stu-id="21ac1-202">GetPropsNULL</span></span>  <br/> |<span data-ttu-id="21ac1-203">mfcmapi は、 **imapiprop:: GetProps**メソッドを使用して、オブジェクトのすべてのプロパティを取得します。 NULL または、 _lpPropTagArray_パラメーターの[imapiprop:: getproplist](imapiprop-getproplist.md)メソッドによって返される配列を渡します。</span><span class="sxs-lookup"><span data-stu-id="21ac1-203">MFCMAPI uses the **IMAPIProp::GetProps** method to obtain all properties for an object by passing either NULL or the array returned by the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method in the  _lpPropTagArray_ parameter.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="21ac1-204">関連項目</span><span class="sxs-lookup"><span data-stu-id="21ac1-204">See also</span></span>



[<span data-ttu-id="21ac1-205">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="21ac1-205">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="21ac1-206">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="21ac1-206">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="21ac1-207">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="21ac1-207">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="21ac1-208">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="21ac1-208">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="21ac1-209">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="21ac1-209">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="21ac1-210">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="21ac1-210">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="21ac1-211">SPropValue</span><span class="sxs-lookup"><span data-stu-id="21ac1-211">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="21ac1-212">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="21ac1-212">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


<span data-ttu-id="21ac1-213">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="21ac1-213">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="21ac1-214">MAPI プロパティの取得</span><span class="sxs-lookup"><span data-stu-id="21ac1-214">Retrieving MAPI Properties</span></span>](retrieving-mapi-properties.md)
  
[<span data-ttu-id="21ac1-215">エラー処理にマクロを使用する</span><span class="sxs-lookup"><span data-stu-id="21ac1-215">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

