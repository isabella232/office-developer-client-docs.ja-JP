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
# <a name="imapipropgetprops"></a><span data-ttu-id="1c5c4-103">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="1c5c4-103">IMAPIProp::GetProps</span></span>

  
  
<span data-ttu-id="1c5c4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c5c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c5c4-105">オブジェクトの 1 つ以上のプロパティのプロパティ値を取得します。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-105">Retrieves the property value of one or more properties of an object.</span></span>
  
```cpp
HRESULT GetProps(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="1c5c4-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1c5c4-106">Parameters</span></span>

 <span data-ttu-id="1c5c4-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="1c5c4-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="1c5c4-108">[in]値を取得するプロパティを識別するプロパティ タグの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-108">[in] A pointer to an array of property tags that identify the properties whose values are to be retrieved.</span></span> <span data-ttu-id="1c5c4-109">_lpPropTagArray_ パラメーターは NULL で、オブジェクトのすべてのプロパティの値を返す必要があります、または 1 つ以上のプロパティ タグを含む [SPropTagArray](sproptagarray.md)構造体を指す必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-109">The  _lpPropTagArray_ parameter must be either NULL, indicating that values for all properties of the object should be returned, or point to an [SPropTagArray](sproptagarray.md) structure that contains one or more property tags.</span></span> 
    
 <span data-ttu-id="1c5c4-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1c5c4-110">_ulFlags_</span></span>
  
> <span data-ttu-id="1c5c4-111">[in]型を持つプロパティの形式を示すフラグのビットマスクPT_UNSPECIFIED。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-111">[in] A bitmask of flags that indicates the format for properties that have the type PT_UNSPECIFIED.</span></span> <span data-ttu-id="1c5c4-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-112">The following flag can be set:</span></span>
    
<span data-ttu-id="1c5c4-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1c5c4-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1c5c4-114">これらのプロパティの文字列値は、Unicode 形式で返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-114">The string values for these properties should be returned in the Unicode format.</span></span> <span data-ttu-id="1c5c4-115">このフラグMAPI_UNICODE設定しない場合は、ANSI 形式で文字列値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-115">If the MAPI_UNICODE flag is not set, the string values should be returned in the ANSI format.</span></span>
    
 <span data-ttu-id="1c5c4-116">_lpcValues_</span><span class="sxs-lookup"><span data-stu-id="1c5c4-116">_lpcValues_</span></span>
  
> <span data-ttu-id="1c5c4-117">[out]  _lppPropArray_ パラメーターが指すプロパティ値の数を指すポインター。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-117">[out] A pointer to a count of property values pointed to by the  _lppPropArray_ parameter.</span></span> <span data-ttu-id="1c5c4-118">_lppPropArray が_ NULL の場合 _、lpcValues_ パラメーターの内容は 0 です。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-118">If  _lppPropArray_ is NULL, the content of the  _lpcValues_ parameter is zero.</span></span> 
    
 <span data-ttu-id="1c5c4-119">_lppPropArray_</span><span class="sxs-lookup"><span data-stu-id="1c5c4-119">_lppPropArray_</span></span>
  
> <span data-ttu-id="1c5c4-120">[out]取得したプロパティ値へのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-120">[out] A pointer to a pointer to the retrieved property values.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1c5c4-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="1c5c4-121">Return value</span></span>

<span data-ttu-id="1c5c4-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="1c5c4-122">S_OK</span></span> 
  
> <span data-ttu-id="1c5c4-123">プロパティの値が正常に取得されました。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-123">The property values were successfully retrieved.</span></span>
    
<span data-ttu-id="1c5c4-124">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="1c5c4-124">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="1c5c4-125">呼び出しは全体的に成功しましたが、1 つ以上のプロパティにアクセスする必要がありました。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-125">The call succeeded overall, but one or more properties could not be accessed.</span></span> <span data-ttu-id="1c5c4-126">使用できない各プロパティのプロパティ値の **aulPropTag** メンバーには、プロパティの種類PT_ERROR識別子が 0 です。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-126">The **aulPropTag** member of the property value for each unavailable property has a property type of PT_ERROR and an identifier of zero.</span></span> <span data-ttu-id="1c5c4-127">この警告が返されると、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-127">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="1c5c4-128">この警告をテストするには、次のマクロ **HR_FAILED** します。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-128">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="1c5c4-129">詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-129">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
<span data-ttu-id="1c5c4-130">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1c5c4-130">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="1c5c4-131">_lpPropTagArray_ が指す **SPropTagArray** 構造体の **cValues** メンバーにゼロが渡されています。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-131">Zero was passed in the **cValues** member of the **SPropTagArray** structure pointed to by  _lpPropTagArray_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1c5c4-132">注釈</span><span class="sxs-lookup"><span data-stu-id="1c5c4-132">Remarks</span></span>

<span data-ttu-id="1c5c4-133">**IMAPIProp::GetProps** メソッドは、オブジェクトの 1 つ以上のプロパティのプロパティ値を取得します。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-133">The **IMAPIProp::GetProps** method obtains the property values of one or more properties of an object.</span></span> 
  
<span data-ttu-id="1c5c4-134">プロパティの値は、要求された順序と同じ順序で返されます (つまり  _、lpPropTagArray_ が指すプロパティ タグ配列内のプロパティの順序は  _、lppPropArray_ が指すプロパティ値構造体の配列の順序と一致します)。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-134">The property values are returned in the same order as they were requested (that is, the order of properties in the property tag array pointed to by  _lpPropTagArray_ matches the order in the array of property value structures pointed to by  _lppPropArray_).</span></span> 
  
<span data-ttu-id="1c5c4-135">プロパティ タグ配列の **aulPropTag** メンバーで指定されたプロパティ型は、各プロパティ値構造体の **Value** メンバーで返される値の種類を示します。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-135">The property types specified in the **aulPropTag** members of the property tag array indicate the type of value that should be returned in the **Value** member of each property value structure.</span></span> <span data-ttu-id="1c5c4-136">ただし、呼び出し元がプロパティの種類を知らない場合は **、aulPropTag** メンバーの型を代わりにプロパティにPT_UNSPECIFIED。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-136">However, if the caller does not know the type of a property, the type in the **aulPropTag** member can be set instead to PT_UNSPECIFIED.</span></span> <span data-ttu-id="1c5c4-137">値を取得する際に **、GetProps は** プロパティのプロパティ値構造体 **の aulPropTag** メンバーに正しい型を設定します。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-137">In retrieving the value, **GetProps** sets the correct type in the **aulPropTag** member of the property value structure for the property.</span></span> 
  
<span data-ttu-id="1c5c4-138">_lpPropTagArray の SPropTagArray_ でプロパティ型が指定されている場合 _、lppPropArray_ で返される **SPropValue** のプロパティ値には、エラー値が代わりに返されていない限り、要求された型と完全に一致する型があります。 </span><span class="sxs-lookup"><span data-stu-id="1c5c4-138">If property types are specified in the **SPropTagArray** in  _lpPropTagArray_, the property values in the **SPropValue** returned in  _lppPropArray_ have types that exactly match the requested types, unless an error value is returned instead.</span></span> 
  
<span data-ttu-id="1c5c4-139">文字列プロパティには、Unicode 形式を表すプロパティPT_UNICODE ANSI 形式を表PT_STRING8プロパティの 2 つのいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-139">String properties can have one of two property types: PT_UNICODE to represent the Unicode format and PT_STRING8 to represent the ANSI format.</span></span> <span data-ttu-id="1c5c4-140">_ulFlags_ パラメーターで MAPI_UNICODE フラグが設定されている場合 **、GetProps** が文字列プロパティの適切な形式を決定できない場合は常に、Unicode 形式で値を返します。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-140">If the MAPI_UNICODE flag is set in the  _ulFlags_ parameter, whenever **GetProps** cannot determine the appropriate format for a string property, it returns its value in the Unicode format.</span></span> <span data-ttu-id="1c5c4-141">**GetProps は** 、次の状況で正確な文字列プロパティの種類を特定できません。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-141">**GetProps** cannot determine an exact string property type in the following situations:</span></span> 
  
- <span data-ttu-id="1c5c4-142">_lpPropTagArray パラメーターは_ NULL に設定して、すべてのプロパティを要求します。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-142">The  _lpPropTagArray_ parameter is set to NULL to request all properties.</span></span> 
    
- <span data-ttu-id="1c5c4-143">**aulPropTag** メンバーには、プロパティ タグPT_UNSPECIFIEDプロパティの種類として指定された値が含まれます。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-143">The **aulPropTag** member includes the value PT_UNSPECIFIED as its property type in the property tag array.</span></span> 
    
<span data-ttu-id="1c5c4-144">_lpPropTagArray_ パラメーターが NULL に設定され、オブジェクトのすべてのプロパティを取得し、プロパティが存在しない場合 **、GetProps は** 次の処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-144">If the  _lpPropTagArray_ parameter is set to NULL to retrieve all of the properties of the object and no properties exist, **GetProps** does the following:</span></span> 
  
- <span data-ttu-id="1c5c4-145">値をS_OKします。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-145">Returns S_OK.</span></span>
    
- <span data-ttu-id="1c5c4-146">プロパティ値構造体の **cValues** メンバーの count 値を 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-146">Sets the count value in the **cValues** member of the property value structure to 0.</span></span> 
    
- <span data-ttu-id="1c5c4-147">_lpcValues の内容を_ 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-147">Sets the contents of  _lpcValues_ to 0.</span></span> 
    
- <span data-ttu-id="1c5c4-148">_lppPropArray を_ NULL に設定します。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-148">Sets  _lppPropArray_ to NULL.</span></span> 
    
 <span data-ttu-id="1c5c4-149">**GetProps は\*\*\*\*、cValues** を 0 に設定した複数値のプロパティを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-149">**GetProps** must not return multiple-value properties with **cValues** set to 0.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1c5c4-150">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="1c5c4-150">Notes to implementers</span></span>

<span data-ttu-id="1c5c4-151">[MAPIAllocateBuffer](mapiallocatebuffer.md)関数を呼び出して _、lpPropTagArray_ が指す [SPropValue](spropvalue.md)構造体のメモリを最初に割り当てる。[MAPIAllocateMore を呼](mapiallocatemore.md)び出して、構造体のメンバーに必要な追加のメモリを割り当てる。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-151">Call the [MAPIAllocateBuffer](mapiallocatebuffer.md) function to allocate memory initially for the [SPropValue](spropvalue.md) structure pointed to by  _lpPropTagArray_; call [MAPIAllocateMore](mapiallocatemore.md) to allocate any additional memory needed for the structure's members.</span></span> 
  
<span data-ttu-id="1c5c4-152">要求MAPI_W_ERRORS_RETURNEDプロパティの値を取得できない場合は、この値を返します。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-152">Return MAPI_W_ERRORS_RETURNED if you cannot retrieve the value for one or more of the requested properties.</span></span> <span data-ttu-id="1c5c4-153">プロパティ値構造で **、aulPropTag** メンバーの型を PT_ERROR に設定し **、Value** メンバーにエラーを説明する状態コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-153">In the property value structure, set the type in the **aulPropTag** member to PT_ERROR and the **Value** member to a status code that describes the error.</span></span> <span data-ttu-id="1c5c4-154">たとえば、文字列を Unicode に変換する必要がある場合、Unicode をサポートしていない場合は **、Value** メンバーを次の文字列にMAPI_E_BAD_CHARWIDTH。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-154">For example, if you have to convert a string to Unicode and do not support Unicode, set the **Value** member to MAPI_E_BAD_CHARWIDTH.</span></span> <span data-ttu-id="1c5c4-155">プロパティが大きすぎる場合は、プロパティを [プロパティ] MAPI_E_NOT_ENOUGH_MEMORY。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-155">If the property is too large, set it to MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="1c5c4-156">オブジェクトがプロパティをサポートしていない場合は、このプロパティを [プロパティ] MAPI_E_NOT_FOUND。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-156">If the object does not support the property, set it to MAPI_E_NOT_FOUND.</span></span> 
  
<span data-ttu-id="1c5c4-157">リモート トランスポート プロバイダーによる **GetProps** メソッドの実装では、呼び出し元が要求したプロパティのフォルダーのプロパティ値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-157">A remote transport provider's implementation of the **GetProps** method must return the folder's property values for properties requested by the caller.</span></span> <span data-ttu-id="1c5c4-158">実装では、次の操作を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-158">Your implementation must do the following:</span></span> 
  
- <span data-ttu-id="1c5c4-159">呼び出し元に返すプロパティ値配列を割り当て、その目的で渡されたプロパティ値ポインター パラメーターにアドレスを格納します。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-159">Allocate a property value array to return to the caller and store its address in the property value pointer parameter passed in for that purpose.</span></span>
    
- <span data-ttu-id="1c5c4-160">GetProps に渡されるプロパティ タグの配列に従って、フォルダーのプロパティからプロパティ値配列のプロパティ タグにプロパティ タグ **をコピーします**。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-160">Copy the property tags from the folder's properties into the property tags in the property value array according to the array of property tags passed to **GetProps**.</span></span>
    
- <span data-ttu-id="1c5c4-161">GetProps に渡されるすべてのプロパティ タグに対してプロパティの種類が **設定されている必要があります**。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-161">Ensure that the property type is set for all property tags passed to **GetProps**.</span></span> <span data-ttu-id="1c5c4-162">呼び出し元は、プロパティの種類のプロパティ PT_UNSPECIFIED渡すことができます。その場合 **、GetProps** は、そのプロパティ タグの正しいプロパティの種類を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-162">The caller can pass in a property type of PT_UNSPECIFIED, in which case **GetProps** must set the correct property type for that property tag.</span></span> 
    
- <span data-ttu-id="1c5c4-163">タグに従ってプロパティ値配列の各プロパティの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-163">Set the value of each property in the property value array according to its tag.</span></span> <span data-ttu-id="1c5c4-164">たとえば、呼び出し元から要求されたプロパティ タグが PR_OBJECT_TYPE **(** [PidTagObjectType)](pidtagobjecttype-canonical-property.md)の場合 **、GetProps** は値を MAPI_FOLDER に設定できます。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-164">For example, if the property tag requested by the caller is **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)), **GetProps** can set the value to MAPI_FOLDER.</span></span> 
    
- <span data-ttu-id="1c5c4-165">呼び出し元が実装で処理しないプロパティ タグを渡す場合は、それらのプロパティのプロパティ タグを PT_ERROR に設定し、プロパティ値を MAPI_E_NOT_FOUND に設定できます。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-165">If the caller passes in any property tags that your implementation does not handle, you can set the property tag to PT_ERROR for those properties, and set the property value to MAPI_E_NOT_FOUND.</span></span>
    
- <span data-ttu-id="1c5c4-166">エラー S_OKが発生した場合、またはエラーが発生MAPI_W_ERRORS_RETURNED場合は、エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-166">Return S_OK if no errors occurred or MAPI_W_ERRORS_RETURNED if there were errors.</span></span>
    
<span data-ttu-id="1c5c4-167">リモート トランスポート プロバイダーによる **GetProps** メソッドの実装では、少なくとも次のプロパティをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-167">A remote transport provider's implementation of the **GetProps** method must support the following properties at a minimum:</span></span> 
  
- <span data-ttu-id="1c5c4-168">**PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c5c4-168">**PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))</span></span>
    
- <span data-ttu-id="1c5c4-169">**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c5c4-169">**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))</span></span>
    
- <span data-ttu-id="1c5c4-170">**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c5c4-170">**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="1c5c4-171">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c5c4-171">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="1c5c4-172">**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c5c4-172">**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="1c5c4-173">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c5c4-173">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="1c5c4-174">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c5c4-174">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
- <span data-ttu-id="1c5c4-175">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c5c4-175">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>
    
- <span data-ttu-id="1c5c4-176">**PR_OBJECT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="1c5c4-176">**PR_OBJECT_TYPE**</span></span>
    
- <span data-ttu-id="1c5c4-177">**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c5c4-177">**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="1c5c4-178">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="1c5c4-178">Notes to callers</span></span>

<span data-ttu-id="1c5c4-179">型プロパティのプロパティPT_OBJECT、GetProps の代わりに [IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッド **を呼び出します**。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-179">For properties of type PT_OBJECT, call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method instead of **GetProps**.</span></span> 
  
<span data-ttu-id="1c5c4-180">セキュリティで保護されたプロパティの場合は _、lppPropTagArray_ パラメーターを NULL に設定して **GetProps** を呼び出して取得する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-180">For secure properties, do not expect to retrieve them by calling **GetProps** with the  _lppPropTagArray_ parameter set to NULL.</span></span> <span data-ttu-id="1c5c4-181">GetProps を呼び出す場合は、プロパティ タグ配列 **の aulPropTag** メンバーでセキュリティで保護されたプロパティの識別子を明示的に **設定する必要があります**。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-181">You must explicitly set a secure property's identifier in the **aulPropTag** member of its property tag array when you call **GetProps**.</span></span> <span data-ttu-id="1c5c4-182">セキュリティで保護されたプロパティを使用できる場合と方法は、サービス プロバイダーによって管理されます。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-182">When and how a secure property is available is up to the service provider.</span></span> 
  
<span data-ttu-id="1c5c4-183">**GetProps** が関数または関数を返す場合にのみ [、MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、返される **SPropValue** 構造体S_OK解放MAPI_W_ERRORS_RETURNED。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-183">Free the returned **SPropValue** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function only if **GetProps** returns S_OK or MAPI_W_ERRORS_RETURNED.</span></span> 
  
<span data-ttu-id="1c5c4-184">**GetProps** が 1 つMAPI_W_ERRORS_RETURNEDプロパティにアクセスできないため、プロパティを返す場合は、返されるプロパティのプロパティ タグを確認します。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-184">If **GetProps** returns MAPI_W_ERRORS_RETURNED because it could not access one or more properties, check the property tags of the returned properties.</span></span> <span data-ttu-id="1c5c4-185">失敗したプロパティには、プロパティ値構造に次の値が設定されます。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-185">The failed properties will have the following values set in their property value structure:</span></span> 
  
- <span data-ttu-id="1c5c4-186">**aulPropTag メンバーのプロパティ** の種類は、プロパティに設定PT_ERROR。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-186">The property type in the **aulPropTag** member set to PT_ERROR.</span></span> 
    
- <span data-ttu-id="1c5c4-187">Value メンバーのプロパティ **の値** は、エラーの状態コード (エラーなど) に設定MAPI_E_NOT_FOUND。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-187">The property value in the **Value** member set to a status code for the error, such as MAPI_E_NOT_FOUND.</span></span> 
    
<span data-ttu-id="1c5c4-188">プロパティ値構造体で返すには大きすぎるため失敗するプロパティには **、Value** メンバーが値に設定MAPI_E_NOT_ENOUGH_MEMORY。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-188">Properties that fail because they are too large to conveniently be returned in the property value structure have their **Value** member set to MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="1c5c4-189">通常、これは、プロパティの値が 4 KB 以上の場合に、PT_STRING8、PT_UNICODE、または PT_BINARY 型の文字列プロパティまたはバイナリ プロパティで発生します。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-189">Typically, this occurs with string or binary properties of type PT_STRING8, PT_UNICODE, or PT_BINARY when the value of the property is 4 KB or larger.</span></span> <span data-ttu-id="1c5c4-190">**IMAPIProp::OpenProperty を呼び出して、大** きなプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-190">Call **IMAPIProp::OpenProperty** to retrieve large properties.</span></span> 
  
<span data-ttu-id="1c5c4-191">**GetProps のすべての実装で、文字列** の Unicode 形式と ANSI 形式の両方がサポートされているという場合があります。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-191">Not all implementations of **GetProps** support both the Unicode and ANSI formats for character strings.</span></span> <span data-ttu-id="1c5c4-192">特定のプロパティで文字列形式の変換が必要で **、GetProps** でサポートできない場合は、プロパティの **Value** メンバーが文字列形式にMAPI_E_BAD_CHARWIDTH。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-192">When a particular property requires string format conversion and **GetProps** cannot support it, the **Value** member for the property is set to MAPI_E_BAD_CHARWIDTH.</span></span> 
  
<span data-ttu-id="1c5c4-193">PST が SharePoint PST である場合は [、IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)を使用して PST をマウントし、このプロパティを要求するメッセージ ストア オブジェクトで **GetProps** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-193">To check if a PST is a SharePoint PST, mount the PST using [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md), then call **GetProps** on the message store object requesting this property.</span></span> <span data-ttu-id="1c5c4-194">存在する場合は、PST がユーザーに対して構成SharePoint。指定されていない場合、PST は PST の構成SharePointされていません。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-194">If it exists, you can assume the PST has been configured for SharePoint; if not, the PST has not been configured as a SharePoint PST.</span></span> 
  
<span data-ttu-id="1c5c4-195">**GetProps** を使用してプロパティにアクセスする方法の詳細については、「MAPI プロパティの取得 [」を参照してください](retrieving-mapi-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-195">For more information about how to use **GetProps** to access properties, see [Retrieving MAPI Properties](retrieving-mapi-properties.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1c5c4-196">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="1c5c4-196">MFCMAPI reference</span></span>

<span data-ttu-id="1c5c4-197">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-197">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1c5c4-198">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="1c5c4-198">**File**</span></span>|<span data-ttu-id="1c5c4-199">**関数**</span><span class="sxs-lookup"><span data-stu-id="1c5c4-199">**Function**</span></span>|<span data-ttu-id="1c5c4-200">**コメント**</span><span class="sxs-lookup"><span data-stu-id="1c5c4-200">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1c5c4-201">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="1c5c4-201">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="1c5c4-202">GetPropsNULL</span><span class="sxs-lookup"><span data-stu-id="1c5c4-202">GetPropsNULL</span></span>  <br/> |<span data-ttu-id="1c5c4-203">MFCMAPI は **、IMAPIProp::GetProps** メソッドを使用して _、LPPropTagArray_ パラメーターで [IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドによって返される NULL または配列を渡して、オブジェクトのすべてのプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="1c5c4-203">MFCMAPI uses the **IMAPIProp::GetProps** method to obtain all properties for an object by passing either NULL or the array returned by the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method in the  _lpPropTagArray_ parameter.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1c5c4-204">関連項目</span><span class="sxs-lookup"><span data-stu-id="1c5c4-204">See also</span></span>



[<span data-ttu-id="1c5c4-205">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="1c5c4-205">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="1c5c4-206">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="1c5c4-206">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="1c5c4-207">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="1c5c4-207">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="1c5c4-208">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="1c5c4-208">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="1c5c4-209">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="1c5c4-209">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="1c5c4-210">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="1c5c4-210">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="1c5c4-211">SPropValue</span><span class="sxs-lookup"><span data-stu-id="1c5c4-211">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="1c5c4-212">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1c5c4-212">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


<span data-ttu-id="1c5c4-213">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="1c5c4-213">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="1c5c4-214">MAPI プロパティの取得</span><span class="sxs-lookup"><span data-stu-id="1c5c4-214">Retrieving MAPI Properties</span></span>](retrieving-mapi-properties.md)
  
[<span data-ttu-id="1c5c4-215">エラー処理にマクロを使用する</span><span class="sxs-lookup"><span data-stu-id="1c5c4-215">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

