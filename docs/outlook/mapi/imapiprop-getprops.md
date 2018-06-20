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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 33351235db2a9a3f9d9b67f59e8356a0fa8abfa8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800656"
---
# <a name="imapipropgetprops"></a><span data-ttu-id="025ad-103">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="025ad-103">IMAPIProp::GetProps</span></span>

  
  
<span data-ttu-id="025ad-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="025ad-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="025ad-105">オブジェクトの 1 つまたは複数のプロパティのプロパティ値を取得します。</span><span class="sxs-lookup"><span data-stu-id="025ad-105">Retrieves the property value of one or more properties of an object.</span></span>
  
```cpp
HRESULT GetProps(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="025ad-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="025ad-106">Parameters</span></span>

 <span data-ttu-id="025ad-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="025ad-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="025ad-108">[in]取得するのには、値がプロパティを識別するプロパティ タグの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="025ad-108">[in] A pointer to an array of property tags that identify the properties whose values are to be retrieved.</span></span> <span data-ttu-id="025ad-109">_LpPropTagArray_パラメーターは、NULL であるか、オブジェクトのすべてのプロパティの値、返されることを示す 1 つまたは複数のプロパティ タグを含む[SPropTagArray](sproptagarray.md)構造体をポイントにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="025ad-109">The  _lpPropTagArray_ parameter must be either NULL, indicating that values for all properties of the object should be returned, or point to an [SPropTagArray](sproptagarray.md) structure that contains one or more property tags.</span></span> 
    
 <span data-ttu-id="025ad-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="025ad-110">_ulFlags_</span></span>
  
> <span data-ttu-id="025ad-111">[in]PT_UNSPECIFIED の種類のプロパティの形式を示すフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="025ad-111">[in] A bitmask of flags that indicates the format for properties that have the type PT_UNSPECIFIED.</span></span> <span data-ttu-id="025ad-112">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="025ad-112">The following flag can be set:</span></span>
    
<span data-ttu-id="025ad-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="025ad-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="025ad-114">Unicode 形式でこれらのプロパティの文字列値が返されます。</span><span class="sxs-lookup"><span data-stu-id="025ad-114">The string values for these properties should be returned in the Unicode format.</span></span> <span data-ttu-id="025ad-115">MAPI_UNICODE フラグが設定されていない場合、ANSI 形式の文字列値が返されます。</span><span class="sxs-lookup"><span data-stu-id="025ad-115">If the MAPI_UNICODE flag is not set, the string values should be returned in the ANSI format.</span></span>
    
 <span data-ttu-id="025ad-116">_lpcValues_</span><span class="sxs-lookup"><span data-stu-id="025ad-116">_lpcValues_</span></span>
  
> <span data-ttu-id="025ad-117">[out]_LppPropArray_パラメーターで指定されたプロパティの値の数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="025ad-117">[out] A pointer to a count of property values pointed to by the  _lppPropArray_ parameter.</span></span> <span data-ttu-id="025ad-118">_LppPropArray_が NULL の場合は、 _lpcValues_パラメーターの内容は 0 になります。</span><span class="sxs-lookup"><span data-stu-id="025ad-118">If  _lppPropArray_ is NULL, the content of the  _lpcValues_ parameter is zero.</span></span> 
    
 <span data-ttu-id="025ad-119">_lppPropArray_</span><span class="sxs-lookup"><span data-stu-id="025ad-119">_lppPropArray_</span></span>
  
> <span data-ttu-id="025ad-120">[out]取得したプロパティの値へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="025ad-120">[out] A pointer to a pointer to the retrieved property values.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="025ad-121">�߂�l</span><span class="sxs-lookup"><span data-stu-id="025ad-121">Return value</span></span>

<span data-ttu-id="025ad-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="025ad-122">S_OK</span></span> 
  
> <span data-ttu-id="025ad-123">プロパティの値が正常に取得されました。</span><span class="sxs-lookup"><span data-stu-id="025ad-123">The property values were successfully retrieved.</span></span>
    
<span data-ttu-id="025ad-124">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="025ad-124">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="025ad-125">呼び出しは完了しましたが、1 つまたは複数のプロパティにアクセスできませんでした。</span><span class="sxs-lookup"><span data-stu-id="025ad-125">The call succeeded overall, but one or more properties could not be accessed.</span></span> <span data-ttu-id="025ad-126">各使用できないプロパティのプロパティ値の**aulPropTag**メンバーには、PT_ERROR とゼロの識別子のプロパティ型があります。</span><span class="sxs-lookup"><span data-stu-id="025ad-126">The **aulPropTag** member of the property value for each unavailable property has a property type of PT_ERROR and an identifier of zero.</span></span> <span data-ttu-id="025ad-127">この警告が返されると、呼び出しを成功として処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="025ad-127">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="025ad-128">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="025ad-128">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="025ad-129">詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="025ad-129">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
<span data-ttu-id="025ad-130">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="025ad-130">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="025ad-131">**あう**、 **SPropTagArray**構造体のメンバー _lpPropTagArray_で示される 0 が渡されました。</span><span class="sxs-lookup"><span data-stu-id="025ad-131">Zero was passed in the **cValues** member of the **SPropTagArray** structure pointed to by  _lpPropTagArray_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="025ad-132">備考</span><span class="sxs-lookup"><span data-stu-id="025ad-132">Remarks</span></span>

<span data-ttu-id="025ad-133">**IMAPIProp::GetProps**メソッドは、オブジェクトの 1 つまたは複数のプロパティのプロパティ値を取得します。</span><span class="sxs-lookup"><span data-stu-id="025ad-133">The **IMAPIProp::GetProps** method obtains the property values of one or more properties of an object.</span></span> 
  
<span data-ttu-id="025ad-134">プロパティの値が同じ順序で返されます、要求された (つまり、プロパティ タグ配列内のプロパティの順序で示される_lpPropTagArray_と一致する_の lppPropArray で指定されたプロパティ値の構造体の配列内の順序_).</span><span class="sxs-lookup"><span data-stu-id="025ad-134">The property values are returned in the same order as they were requested (that is, the order of properties in the property tag array pointed to by  _lpPropTagArray_ matches the order in the array of property value structures pointed to by  _lppPropArray_).</span></span> 
  
<span data-ttu-id="025ad-135">プロパティ タグ配列の**aulPropTag**のメンバーで指定されたプロパティの型は、各プロパティ値の構造体のメンバー**の値**で返される値の型を指定します。</span><span class="sxs-lookup"><span data-stu-id="025ad-135">The property types specified in the **aulPropTag** members of the property tag array indicate the type of value that should be returned in the **Value** member of each property value structure.</span></span> <span data-ttu-id="025ad-136">ただし、呼び出し元がプロパティの型を把握していない場合、 **aulPropTag**メンバーの種類設定できます代わりに PT_UNSPECIFIED を。</span><span class="sxs-lookup"><span data-stu-id="025ad-136">However, if the caller does not know the type of a property, the type in the **aulPropTag** member can be set instead to PT_UNSPECIFIED.</span></span> <span data-ttu-id="025ad-137">値を取得するには、 **GetProps**は、 **aulPropTag**のメンバー、プロパティ、構造体のプロパティ値の正しい型を設定します。</span><span class="sxs-lookup"><span data-stu-id="025ad-137">In retrieving the value, **GetProps** sets the correct type in the **aulPropTag** member of the property value structure for the property.</span></span> 
  
<span data-ttu-id="025ad-138">エラー値が返される場合を除きに、 _lppPropArray_で返される**SPropValue**のプロパティ値が、要求された型と一致する型を持つ_lpPropTagArray_の**SPropTagArray**では、プロパティの型が指定されている場合その代わりに。</span><span class="sxs-lookup"><span data-stu-id="025ad-138">If property types are specified in the **SPropTagArray** in  _lpPropTagArray_, the property values in the **SPropValue** returned in  _lppPropArray_ have types that exactly match the requested types, unless an error value is returned instead.</span></span> 
  
<span data-ttu-id="025ad-139">文字列プロパティは、2 つのプロパティ タイプのいずれかを持つことができます: PT_UNICODE PT_STRING8 ANSI 形式を表す Unicode 形式を表す。</span><span class="sxs-lookup"><span data-stu-id="025ad-139">String properties can have one of two property types: PT_UNICODE to represent the Unicode format and PT_STRING8 to represent the ANSI format.</span></span> <span data-ttu-id="025ad-140">**GetProps**が文字列型のプロパティの適切な形式を判断できないときに、 _ulFlags_のパラメーターに MAPI_UNICODE フラグが設定されて、する場合は、Unicode 形式でその値を返します。</span><span class="sxs-lookup"><span data-stu-id="025ad-140">If the MAPI_UNICODE flag is set in the  _ulFlags_ parameter, whenever **GetProps** cannot determine the appropriate format for a string property, it returns its value in the Unicode format.</span></span> <span data-ttu-id="025ad-141">**GetProps**には、以下の状況で、正確な文字列プロパティの型を判断できません。</span><span class="sxs-lookup"><span data-stu-id="025ad-141">**GetProps** cannot determine an exact string property type in the following situations:</span></span> 
  
- <span data-ttu-id="025ad-142">_LpPropTagArray_パラメーターは、すべてのプロパティを要求するのには NULL に設定されています。</span><span class="sxs-lookup"><span data-stu-id="025ad-142">The  _lpPropTagArray_ parameter is set to NULL to request all properties.</span></span> 
    
- <span data-ttu-id="025ad-143">**AulPropTag**メンバーには、プロパティ タグ配列にそのプロパティの型としての PT_UNSPECIFIED の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="025ad-143">The **aulPropTag** member includes the value PT_UNSPECIFIED as its property type in the property tag array.</span></span> 
    
<span data-ttu-id="025ad-144">_LpPropTagArray_パラメーターが NULL に設定してすべてのオブジェクトのプロパティを取得、プロパティが存在しない場合は、 **GetProps**は次を行います。</span><span class="sxs-lookup"><span data-stu-id="025ad-144">If the  _lpPropTagArray_ parameter is set to NULL to retrieve all of the properties of the object and no properties exist, **GetProps** does the following:</span></span> 
  
- <span data-ttu-id="025ad-145">S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="025ad-145">Returns S_OK.</span></span>
    
- <span data-ttu-id="025ad-146">引数 count の値を**あう**プロパティ値構造体のメンバーを 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="025ad-146">Sets the count value in the **cValues** member of the property value structure to 0.</span></span> 
    
- <span data-ttu-id="025ad-147">_LpcValues_の内容を 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="025ad-147">Sets the contents of  _lpcValues_ to 0.</span></span> 
    
- <span data-ttu-id="025ad-148">_LppPropArray_を NULL に設定します。</span><span class="sxs-lookup"><span data-stu-id="025ad-148">Sets  _lppPropArray_ to NULL.</span></span> 
    
 <span data-ttu-id="025ad-149">**GetProps**に**あう**と複数値プロパティが 0 に設定を返す必要がありますされません。</span><span class="sxs-lookup"><span data-stu-id="025ad-149">**GetProps** must not return multiple-value properties with **cValues** set to 0.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="025ad-150">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="025ad-150">Notes to implementers</span></span>

<span data-ttu-id="025ad-151">[SPropValue](spropvalue.md)構造体_lpPropTagArray_; での最初にメモリを割り当てることの[MAPIAllocateBuffer](mapiallocatebuffer.md)関数を呼び出す構造体のメンバーに必要な追加のメモリを割り当てるには、 [MAPIAllocateMore](mapiallocatemore.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="025ad-151">Call the [MAPIAllocateBuffer](mapiallocatebuffer.md) function to allocate memory initially for the [SPropValue](spropvalue.md) structure pointed to by  _lpPropTagArray_; call [MAPIAllocateMore](mapiallocatemore.md) to allocate any additional memory needed for the structure's members.</span></span> 
  
<span data-ttu-id="025ad-152">要求されたプロパティの 1 つ以上の値を取得できない場合は、MAPI_W_ERRORS_RETURNED を返します。</span><span class="sxs-lookup"><span data-stu-id="025ad-152">Return MAPI_W_ERRORS_RETURNED if you cannot retrieve the value for one or more of the requested properties.</span></span> <span data-ttu-id="025ad-153">プロパティの値の構造に PT_ERROR に**aulPropTag**のメンバーと、エラーを説明するステータス コード**値**のメンバーの種類を設定します。</span><span class="sxs-lookup"><span data-stu-id="025ad-153">In the property value structure, set the type in the **aulPropTag** member to PT_ERROR and the **Value** member to a status code that describes the error.</span></span> <span data-ttu-id="025ad-154">などの文字列を Unicode に変換する必要がある、Unicode をサポートしていない場合、**値**メンバーを MAPI_E_BAD_CHARWIDTH に設定します。</span><span class="sxs-lookup"><span data-stu-id="025ad-154">For example, if you have to convert a string to Unicode and do not support Unicode, set the **Value** member to MAPI_E_BAD_CHARWIDTH.</span></span> <span data-ttu-id="025ad-155">プロパティが大きすぎる場合は、MAPI_E_NOT_ENOUGH_MEMORY に設定します。</span><span class="sxs-lookup"><span data-stu-id="025ad-155">If the property is too large, set it to MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="025ad-156">オブジェクトがプロパティをサポートしていない場合は、MAPI_E_NOT_FOUND を設定します。</span><span class="sxs-lookup"><span data-stu-id="025ad-156">If the object does not support the property, set it to MAPI_E_NOT_FOUND.</span></span> 
  
<span data-ttu-id="025ad-157">**GetProps**メソッドのリモート トランスポート プロバイダーの実装は、プロパティの呼び出し元によって要求されたフォルダーのプロパティの値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="025ad-157">A remote transport provider's implementation of the **GetProps** method must return the folder's property values for properties requested by the caller.</span></span> <span data-ttu-id="025ad-158">実装では、次の操作を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="025ad-158">Your implementation must do the following:</span></span> 
  
- <span data-ttu-id="025ad-159">呼び出し元に戻るし、その目的のために渡されたプロパティ値のポインター パラメーターにそのアドレスを格納するプロパティ値の配列を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="025ad-159">Allocate a property value array to return to the caller and store its address in the property value pointer parameter passed in for that purpose.</span></span>
    
- <span data-ttu-id="025ad-160">**GetProps**に渡されるプロパティ タグの配列に基づいて、プロパティ値の配列内のプロパティ タグに、フォルダーのプロパティからプロパティ タグをコピーします。</span><span class="sxs-lookup"><span data-stu-id="025ad-160">Copy the property tags from the folder's properties into the property tags in the property value array according to the array of property tags passed to **GetProps**.</span></span>
    
- <span data-ttu-id="025ad-161">**GetProps**に渡されるすべてのプロパティ タグのプロパティのデータ型が設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="025ad-161">Ensure that the property type is set for all property tags passed to **GetProps**.</span></span> <span data-ttu-id="025ad-162">ケース**GetProps**がそのプロパティ タグの適切なプロパティの型を設定する必要があります、PT_UNSPECIFIED のプロパティの型で呼び出し側が渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="025ad-162">The caller can pass in a property type of PT_UNSPECIFIED, in which case **GetProps** must set the correct property type for that property tag.</span></span> 
    
- <span data-ttu-id="025ad-163">に従って、タグ、プロパティ値の配列内の各プロパティの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="025ad-163">Set the value of each property in the property value array according to its tag.</span></span> <span data-ttu-id="025ad-164">など、この呼び出し元によって要求されたプロパティ タグが**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) の場合は、 **GetProps**は MAPI_FOLDER に値を設定できます。</span><span class="sxs-lookup"><span data-stu-id="025ad-164">For example, if the property tag requested by the caller is **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)), **GetProps** can set the value to MAPI_FOLDER.</span></span> 
    
- <span data-ttu-id="025ad-165">実装が処理しない任意のプロパティ タグの呼び出しが成功した場合は、PT_ERROR にこれらのプロパティのプロパティ タグを設定し、MAPI_E_NOT_FOUND をプロパティの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="025ad-165">If the caller passes in any property tags that your implementation does not handle, you can set the property tag to PT_ERROR for those properties, and set the property value to MAPI_E_NOT_FOUND.</span></span>
    
- <span data-ttu-id="025ad-166">エラーが発生した場合は、エラーが発生していない場合は S_OK、または MAPI_W_ERRORS_RETURNED を返します。</span><span class="sxs-lookup"><span data-stu-id="025ad-166">Return S_OK if no errors occurred or MAPI_W_ERRORS_RETURNED if there were errors.</span></span>
    
<span data-ttu-id="025ad-167">**GetProps**メソッドのリモート トランスポート プロバイダーの実装では、最低限次のプロパティをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="025ad-167">A remote transport provider's implementation of the **GetProps** method must support the following properties at a minimum:</span></span> 
  
- <span data-ttu-id="025ad-168">**PR_ACCESS**([PidTagAccess](pidtagaccess-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="025ad-168">**PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))</span></span>
    
- <span data-ttu-id="025ad-169">**PR_ACCESS_LEVEL**([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="025ad-169">**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))</span></span>
    
- <span data-ttu-id="025ad-170">**PR_ASSOC_CONTENT_COUNT**([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="025ad-170">**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="025ad-171">**PR_CONTENT_COUNT**([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="025ad-171">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="025ad-172">**PR_CREATION_TIME**([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="025ad-172">**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="025ad-173">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="025ad-173">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="025ad-174">**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="025ad-174">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
- <span data-ttu-id="025ad-175">**PR_FOLDER_TYPE**([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="025ad-175">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>
    
- <span data-ttu-id="025ad-176">**PR_OBJECT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="025ad-176">**PR_OBJECT_TYPE**</span></span>
    
- <span data-ttu-id="025ad-177">**PR_SUBFOLDERS**([PidTagSubfolders](pidtagsubfolders-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="025ad-177">**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="025ad-178">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="025ad-178">Notes to callers</span></span>

<span data-ttu-id="025ad-179">PT_OBJECT の種類のプロパティの場合に、 **GetProps**の代わりに[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="025ad-179">For properties of type PT_OBJECT, call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method instead of **GetProps**.</span></span> 
  
<span data-ttu-id="025ad-180">セキュリティで保護されたプロパティは、必要ありません**GetProps**を呼び出すと、 _lppPropTagArray_パラメーターを NULL に設定してしまいます。</span><span class="sxs-lookup"><span data-stu-id="025ad-180">For secure properties, do not expect to retrieve them by calling **GetProps** with the  _lppPropTagArray_ parameter set to NULL.</span></span> <span data-ttu-id="025ad-181">必要があります明示的に設定するセキュリティで保護されたプロパティの識別子のプロパティ タグ配列の**aulPropTag**メンバーに**GetProps**を呼び出すとします。</span><span class="sxs-lookup"><span data-stu-id="025ad-181">You must explicitly set a secure property's identifier in the **aulPropTag** member of its property tag array when you call **GetProps**.</span></span> <span data-ttu-id="025ad-182">サービス プロバイダーは、セキュリティで保護されたプロパティは利用可能な時期と方法です。</span><span class="sxs-lookup"><span data-stu-id="025ad-182">When and how a secure property is available is up to the service provider.</span></span> 
  
<span data-ttu-id="025ad-183">**GetProps** MAPI_W_ERRORS_RETURNED は s_ok を返す場合にのみ、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによって返された**SPropValue**構造体を解放します。</span><span class="sxs-lookup"><span data-stu-id="025ad-183">Free the returned **SPropValue** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function only if **GetProps** returns S_OK or MAPI_W_ERRORS_RETURNED.</span></span> 
  
<span data-ttu-id="025ad-184">**GetProps**では、1 つまたは複数のプロパティにアクセスできなかったために MAPI_W_ERRORS_RETURNED が返された場合は、返されるプロパティのプロパティ タグを確認してください。</span><span class="sxs-lookup"><span data-stu-id="025ad-184">If **GetProps** returns MAPI_W_ERRORS_RETURNED because it could not access one or more properties, check the property tags of the returned properties.</span></span> <span data-ttu-id="025ad-185">失敗したプロパティには、次の値がそのプロパティ値の構造体に設定があります。</span><span class="sxs-lookup"><span data-stu-id="025ad-185">The failed properties will have the following values set in their property value structure:</span></span> 
  
- <span data-ttu-id="025ad-186">PT_ERROR に**aulPropTag**メンバーのプロパティの型。</span><span class="sxs-lookup"><span data-stu-id="025ad-186">The property type in the **aulPropTag** member set to PT_ERROR.</span></span> 
    
- <span data-ttu-id="025ad-187">MAPI_E_NOT_FOUND など、エラーの状態コードを入力する設定**値**のメンバーのプロパティの値。</span><span class="sxs-lookup"><span data-stu-id="025ad-187">The property value in the **Value** member set to a status code for the error, such as MAPI_E_NOT_FOUND.</span></span> 
    
<span data-ttu-id="025ad-188">プロパティはプロパティの値の構造体で簡単に取得するには大きすぎるために失敗した MAPI_E_NOT_ENOUGH_MEMORY に設定されて、**値**のメンバーがあります。</span><span class="sxs-lookup"><span data-stu-id="025ad-188">Properties that fail because they are too large to conveniently be returned in the property value structure have their **Value** member set to MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="025ad-189">通常、この場合に型の文字列またはバイナリのプロパティを持つ PT_STRING8、PT_UNICODE、または PT_BINARY プロパティの値は 4 KB 以上です。</span><span class="sxs-lookup"><span data-stu-id="025ad-189">Typically, this occurs with string or binary properties of type PT_STRING8, PT_UNICODE, or PT_BINARY when the value of the property is 4 KB or larger.</span></span> <span data-ttu-id="025ad-190">大きなプロパティを取得するために**IMAPIProp::OpenProperty**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="025ad-190">Call **IMAPIProp::OpenProperty** to retrieve large properties.</span></span> 
  
<span data-ttu-id="025ad-191">**GetProps**のすべての実装では、文字列を Unicode と ANSI の両方の形式をサポートします。</span><span class="sxs-lookup"><span data-stu-id="025ad-191">Not all implementations of **GetProps** support both the Unicode and ANSI formats for character strings.</span></span> <span data-ttu-id="025ad-192">特定のプロパティには、文字列形式の変換が必要です、 **GetProps**がサポートできないと、プロパティの**値**のメンバーが MAPI_E_BAD_CHARWIDTH に設定されています。</span><span class="sxs-lookup"><span data-stu-id="025ad-192">When a particular property requires string format conversion and **GetProps** cannot support it, the **Value** member for the property is set to MAPI_E_BAD_CHARWIDTH.</span></span> 
  
<span data-ttu-id="025ad-193">PST をマウントする pst ファイルが SharePoint pst ファイルを確認して、このプロパティを要求するメッセージ ストアのオブジェクトの**GetProps**を呼び出し、 [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)を使用して。</span><span class="sxs-lookup"><span data-stu-id="025ad-193">To check if a PST is a SharePoint PST, mount the PST using [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md), then call **GetProps** on the message store object requesting this property.</span></span> <span data-ttu-id="025ad-194">、存在する場合は、SharePoint の pst ファイルが構成されていると見なすことがそれ以外の場合は、SharePoint の PST と pst ファイルが構成されていません。</span><span class="sxs-lookup"><span data-stu-id="025ad-194">If it exists, you can assume the PST has been configured for SharePoint; if not, the PST has not been configured as a SharePoint PST.</span></span> 
  
<span data-ttu-id="025ad-195">**GetProps**を使用してプロパティにアクセスする方法の詳細については、 [MAPI プロパティを取得する](retrieving-mapi-properties.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="025ad-195">For more information about how to use **GetProps** to access properties, see [Retrieving MAPI Properties](retrieving-mapi-properties.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="025ad-196">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="025ad-196">MFCMAPI reference</span></span>

<span data-ttu-id="025ad-197">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="025ad-197">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="025ad-198">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="025ad-198">**File**</span></span>|<span data-ttu-id="025ad-199">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="025ad-199">**Function**</span></span>|<span data-ttu-id="025ad-200">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="025ad-200">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="025ad-201">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="025ad-201">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="025ad-202">GetPropsNULL</span><span class="sxs-lookup"><span data-stu-id="025ad-202">GetPropsNULL</span></span>  <br/> |<span data-ttu-id="025ad-203">MFCMAPI では、 **IMAPIProp::GetProps**メソッドを使用して、NULL または_lpPropTagArray_パラメーターでは、 [IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドによって返される配列を渡すことによって、オブジェクトのすべてのプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="025ad-203">MFCMAPI uses the **IMAPIProp::GetProps** method to obtain all properties for an object by passing either NULL or the array returned by the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method in the  _lpPropTagArray_ parameter.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="025ad-204">関連項目</span><span class="sxs-lookup"><span data-stu-id="025ad-204">See also</span></span>



[<span data-ttu-id="025ad-205">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="025ad-205">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="025ad-206">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="025ad-206">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="025ad-207">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="025ad-207">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="025ad-208">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="025ad-208">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="025ad-209">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="025ad-209">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="025ad-210">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="025ad-210">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="025ad-211">SPropValue</span><span class="sxs-lookup"><span data-stu-id="025ad-211">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="025ad-212">IMAPIProp: IUnknown</span><span class="sxs-lookup"><span data-stu-id="025ad-212">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


<span data-ttu-id="025ad-213">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="025ad-213">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="025ad-214">MAPI プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="025ad-214">Retrieving MAPI Properties</span></span>](retrieving-mapi-properties.md)
  
[<span data-ttu-id="025ad-215">エラー処理のためのマクロを使用してください。</span><span class="sxs-lookup"><span data-stu-id="025ad-215">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

