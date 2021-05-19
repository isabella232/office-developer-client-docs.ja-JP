---
title: IMAPIPropGetNamesFromIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetNamesFromIDs
api_type:
- COM
ms.assetid: 3efa4731-cf32-4a6c-9ba8-d059e58b0d98
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f6688afde9b36a7722eaaf768f091481c15b7308
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423574"
---
# <a name="imapipropgetnamesfromids"></a><span data-ttu-id="25521-103">IMAPIProp::GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="25521-103">IMAPIProp::GetNamesFromIDs</span></span>

  
  
<span data-ttu-id="25521-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25521-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25521-105">1 つ以上のプロパティ識別子に対応するプロパティ名を指定します。</span><span class="sxs-lookup"><span data-stu-id="25521-105">Provides the property names that correspond to one or more property identifiers.</span></span>
  
```cpp
HRESULT GetNamesFromIDs(
  LPSPropTagArray FAR * lppPropTags,
  LPGUID lpPropSetGuid,
  ULONG ulFlags,
  ULONG FAR * lpcPropNames,
  LPMAPINAMEID FAR * FAR * lpppPropNames
);
```

## <a name="parameters"></a><span data-ttu-id="25521-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="25521-106">Parameters</span></span>

 <span data-ttu-id="25521-107">_lppPropTags_</span><span class="sxs-lookup"><span data-stu-id="25521-107">_lppPropTags_</span></span>
  
> <span data-ttu-id="25521-108">[in, out]入力時に、プロパティ タグの配列を含む [SPropTagArray](sproptagarray.md) 構造体へのポインター。それ以外の場合は NULL で、すべての名前を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="25521-108">[in, out] On input, a pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags; otherwise, NULL, indicating that all names should be returned.</span></span> <span data-ttu-id="25521-109">プロパティ **タグ配列の cValues** メンバーは 0 にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="25521-109">The **cValues** member for the property tag array cannot be 0.</span></span> <span data-ttu-id="25521-110">_lppPropTags が_ 入力の有効なポインターである場合 **、GetNamesFromIDs は** 配列に含まれる各プロパティ識別子の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="25521-110">If  _lppPropTags_ is a valid pointer on input, **GetNamesFromIDs** returns names for each property identifier included in the array.</span></span> 
    
 <span data-ttu-id="25521-111">_lpPropSetGuid_</span><span class="sxs-lookup"><span data-stu-id="25521-111">_lpPropSetGuid_</span></span>
  
> <span data-ttu-id="25521-112">[in]プロパティ セットを識別する [GUID (GUID](guid.md) 構造) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="25521-112">[in] A pointer to a GUID, or [GUID](guid.md) structure, that identifies a property set.</span></span> <span data-ttu-id="25521-113">_lpPropSetGuid_ パラメーターは、有効なプロパティ セットをポイントするか、NULL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="25521-113">The  _lpPropSetGuid_ parameter can point to a valid property set or can be NULL.</span></span> 
    
 <span data-ttu-id="25521-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="25521-114">_ulFlags_</span></span>
  
> <span data-ttu-id="25521-115">[in]返される名前の種類を示すフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="25521-115">[in] A bitmask of flags that indicates the type of names to be returned.</span></span> <span data-ttu-id="25521-116">次のフラグを使用できます (両方のフラグが設定されている場合、名前は返されません)。</span><span class="sxs-lookup"><span data-stu-id="25521-116">The following flags can be used (if both flags are set, no names will be returned):</span></span>
    
<span data-ttu-id="25521-117">MAPI_NO_IDS</span><span class="sxs-lookup"><span data-stu-id="25521-117">MAPI_NO_IDS</span></span> 
  
> <span data-ttu-id="25521-118">Unicode 文字列として格納されている名前のみを返す要求。</span><span class="sxs-lookup"><span data-stu-id="25521-118">Requests that only names stored as Unicode strings be returned.</span></span> 
    
<span data-ttu-id="25521-119">MAPI_NO_STRINGS</span><span class="sxs-lookup"><span data-stu-id="25521-119">MAPI_NO_STRINGS</span></span> 
  
> <span data-ttu-id="25521-120">数値識別子として格納された名前のみを返す要求。</span><span class="sxs-lookup"><span data-stu-id="25521-120">Requests that only names stored as numeric identifiers be returned.</span></span> 
    
 <span data-ttu-id="25521-121">_lpcPropNames_</span><span class="sxs-lookup"><span data-stu-id="25521-121">_lpcPropNames_</span></span>
  
> <span data-ttu-id="25521-122">[out]  _lppPropNames_ パラメーターが指す配列内のプロパティ名ポインターの数を指すポインター。</span><span class="sxs-lookup"><span data-stu-id="25521-122">[out] A pointer to a count of the property name pointers in the array pointed to by the  _lppPropNames_ parameter.</span></span> 
    
 <span data-ttu-id="25521-123">_lpppPropNames_</span><span class="sxs-lookup"><span data-stu-id="25521-123">_lpppPropNames_</span></span>
  
> <span data-ttu-id="25521-124">[out]プロパティ名を含む [MAPINAMEID](mapinameid.md) 構造体へのポインターの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="25521-124">[out] A pointer to an array of pointers to [MAPINAMEID](mapinameid.md) structures that contains property names.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="25521-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="25521-125">Return value</span></span>

<span data-ttu-id="25521-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="25521-126">S_OK</span></span> 
  
> <span data-ttu-id="25521-127">プロパティ名が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="25521-127">The property names were successfully returned.</span></span> 
    
<span data-ttu-id="25521-128">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="25521-128">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="25521-129">オブジェクトは名前付きプロパティをサポートしていない。</span><span class="sxs-lookup"><span data-stu-id="25521-129">The object does not support named properties.</span></span> 
    
<span data-ttu-id="25521-130">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="25521-130">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="25521-131">呼び出しは全体的に成功しましたが、1 つ以上のプロパティの名前を返す必要がありました。</span><span class="sxs-lookup"><span data-stu-id="25521-131">The call succeeded overall, but names for one or more properties could not be returned.</span></span> <span data-ttu-id="25521-132">失敗したプロパティのプロパティ タグには、プロパティの種類が **PT_ERROR。**</span><span class="sxs-lookup"><span data-stu-id="25521-132">The property tags for the failing properties have a property type of **PT_ERROR**.</span></span> <span data-ttu-id="25521-133">この警告が返されると、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="25521-133">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="25521-134">この警告をテストするには、次のマクロ **HR_FAILED** します。</span><span class="sxs-lookup"><span data-stu-id="25521-134">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="25521-135">詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="25521-135">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> 
    
<span data-ttu-id="25521-136">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="25521-136">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="25521-137">**lppPropTags** が指すプロパティ タグ配列内の 1 つ以上のエントリの _cValues_ メンバーは 0 に設定されます。</span><span class="sxs-lookup"><span data-stu-id="25521-137">The **cValues** member of one or more of the entries in the property tag array pointed to by  _lppPropTags_ is set to 0.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="25521-138">注釈</span><span class="sxs-lookup"><span data-stu-id="25521-138">Remarks</span></span>

<span data-ttu-id="25521-139">ほとんどのプロパティへのアクセスはプロパティ識別子によって行いますが、一部のプロパティには名前でアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="25521-139">While access to most properties is by property identifier, some properties can be accessed by name.</span></span> <span data-ttu-id="25521-140">**IMAPIProp::GetNamesFromIDs** メソッドを呼び出して、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="25521-140">The **IMAPIProp::GetNamesFromIDs** method can be called to do the following:</span></span> 
  
- <span data-ttu-id="25521-141">特定のプロパティ セット内の特定のプロパティ識別子の名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="25521-141">Retrieve names for specific property identifiers in a specific property set.</span></span>
    
- <span data-ttu-id="25521-142">任意のプロパティ セット内の特定のプロパティ識別子の名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="25521-142">Retrieve names for specific property identifiers in any property set.</span></span>
    
- <span data-ttu-id="25521-143">オブジェクトのマッピングに含まれるすべての名前付きプロパティの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="25521-143">Retrieve names for all named properties that are included in the object's mapping.</span></span>
    
<span data-ttu-id="25521-144">_lppPropTags_ が 1 つ以上のプロパティ識別子を持つ有効なプロパティ タグ配列をポイントし _、lpPropSetGuid_ が有効なプロパティ セットをポイントする場合 **、GetNamesFromIDs** はプロパティ セットとプロパティの種類を無視し、指定された識別子にマップされる名前をすべて返します。</span><span class="sxs-lookup"><span data-stu-id="25521-144">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers, and  _lpPropSetGuid_ points to a valid property set, **GetNamesFromIDs** ignores the property set and the property types and returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="25521-145">_lppPropTags_ が 1 つ以上のプロパティ識別子を持つ有効なプロパティ タグ配列をポイントし _、lpPropSetGuid_ が NULL の場合 **、GetNamesFromIDs** は、指定された識別子にマップされる名前をすべて返します。</span><span class="sxs-lookup"><span data-stu-id="25521-145">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers and  _lpPropSetGuid_ is NULL, **GetNamesFromIDs** returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="25521-146">指定した識別子に名前がない場合 **、GetNamesFromIDs** は  _、lpppPropNames_ で返される構造体内のその識別子の場所で NULL を返し、また、その識別子をMAPI_W_ERRORS_RETURNED。</span><span class="sxs-lookup"><span data-stu-id="25521-146">If a specified identifier does not have a name, **GetNamesFromIDs** returns NULL in that identifier's place in the structure returned in  _lpppPropNames_ and also returns MAPI_W_ERRORS_RETURNED.</span></span> 
  
<span data-ttu-id="25521-147">_lpPropSetGuid_ と _lppPropTags_ の両方が NULL の場合 **、GetNamesFromIDs** は新しいプロパティ タグ配列を割り当て、オブジェクトのすべての名前付きプロパティの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="25521-147">If both  _lpPropSetGuid_ and  _lppPropTags_ are NULL, **GetNamesFromIDs** allocates a new property tag array and returns all of the names for all of the named properties for the object.</span></span> 
  
<span data-ttu-id="25521-148">要求されたプロパティ セットにプロパティが存在しないか、すべてのプロパティがフラグによって除外された型である場合など、返される名前がない場合 **、GetNamesFromIDs** は次の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="25521-148">When there are no names to be returned, perhaps because there are no properties in the requested property set or all of the properties are of a type excluded by the flags, **GetNamesFromIDs** does the following:</span></span> 
  
- <span data-ttu-id="25521-149">値をS_OKします。</span><span class="sxs-lookup"><span data-stu-id="25521-149">Returns S_OK.</span></span>
    
- <span data-ttu-id="25521-150">新しい **SPropTagArray** 構造体を割り当て **、cValues** メンバーを 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="25521-150">Allocates a new **SPropTagArray** structure, setting the **cValues** member to 0.</span></span> 
    
- <span data-ttu-id="25521-151">_lpcPropNames の内容を_ 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="25521-151">Sets the contents of  _lpcPropNames_ to 0.</span></span> 
    
- <span data-ttu-id="25521-152">_lpppPropNames の内容を NULL に_ 設定します。</span><span class="sxs-lookup"><span data-stu-id="25521-152">Sets the contents of  _lpppPropNames_ to NULL.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="25521-153">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="25521-153">Notes to implementers</span></span>

<span data-ttu-id="25521-154">_lpPropSetGuid が有効_ なプロパティ セットをポイントし _、lppPropTags_ が NULL の場合、結果は未定義です。</span><span class="sxs-lookup"><span data-stu-id="25521-154">If  _lpPropSetGuid_ points to a valid property set and  _lppPropTags_ is NULL, the result is undefined.</span></span> <span data-ttu-id="25521-155">次のいずれかの方法を使用できます。</span><span class="sxs-lookup"><span data-stu-id="25521-155">You can use one of the following strategies:</span></span> 
  
- <span data-ttu-id="25521-156">プロパティ セットを無視し、プロパティ タグ配列内の識別子の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="25521-156">Ignore the property set and return the names for the identifiers in the property tag array.</span></span>
    
- <span data-ttu-id="25521-157">指定したプロパティ セットに属するプロパティ タグ配列内の識別子の名前のみを返します。</span><span class="sxs-lookup"><span data-stu-id="25521-157">Return the names for only the identifiers in the property tag array that belong to the specified property set.</span></span>
    
- <span data-ttu-id="25521-158">呼び出しに失敗し、MAPI_E_INVALID_PARAMETER。</span><span class="sxs-lookup"><span data-stu-id="25521-158">Fail the call, returning MAPI_E_INVALID_PARAMETER.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="25521-159">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="25521-159">Notes to callers</span></span>

<span data-ttu-id="25521-160">オブジェクトのすべての名前付きプロパティを取得するには、まずオブジェクトの [IMAPIProp::GetPropList](imapiprop-getproplist.md) メソッドを呼び出してから、0x8000 の範囲を超える返された識別子を **GetNamesFromIDs** に渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="25521-160">To retrieve all of the named properties for an object, you must first call the object's [IMAPIProp::GetPropList](imapiprop-getproplist.md) method and then pass the returned identifiers that are above the 0x8000 range to **GetNamesFromIDs**.</span></span>
  
<span data-ttu-id="25521-161">有効なプロパティ セットを渡すが、有効なプロパティ タグ配列を渡さない場合は、予期しない結果を得る準備をしてください。</span><span class="sxs-lookup"><span data-stu-id="25521-161">If you pass a valid property set but not a valid property tag array, be prepared for unpredictable results.</span></span> <span data-ttu-id="25521-162">**GetNamesFromIDs** の一部の実装では、プロパティ セットが無視され、プロパティ タグ配列内の識別子の名前が返されます。</span><span class="sxs-lookup"><span data-stu-id="25521-162">Some implementations of **GetNamesFromIDs** ignore the property set and return the names for the identifiers in the property tag array.</span></span> <span data-ttu-id="25521-163">一部の実装では、MAPI_E_INVALID_PARAMETER。</span><span class="sxs-lookup"><span data-stu-id="25521-163">Some implementations return MAPI_E_INVALID_PARAMETER.</span></span> <span data-ttu-id="25521-164">それ以外の実装では、プロパティ セット内のすべてのプロパティの識別子の名前が返されます。</span><span class="sxs-lookup"><span data-stu-id="25521-164">Still other implementations return names for identifiers of all properties in the property set.</span></span> <span data-ttu-id="25521-165">プロパティ セットが指定されているPS_PUBLIC_STRINGS **GetNamesFromIDs** は、これまでに作成された名前を返します。</span><span class="sxs-lookup"><span data-stu-id="25521-165">If the property set is PS_PUBLIC_STRINGS, **GetNamesFromIDs** can return all names that were ever created.</span></span> <span data-ttu-id="25521-166">サービス プロバイダーがパブリック文字列に関連付けられた識別子の下にプロパティを格納するかどうかは重要ではありません。</span><span class="sxs-lookup"><span data-stu-id="25521-166">Whether the service provider stores a property under the identifiers associated with the public strings is immaterial.</span></span> 
  
<span data-ttu-id="25521-167">プロパティ名が完成したら  _、lpcPropNames_ パラメーターの内容を確認して、名前が返されたかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="25521-167">When you are finished with the property names, check the contents of the  _lpcPropNames_ parameter to determine whether any names were returned.</span></span> <span data-ttu-id="25521-168">その場合は [、MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、成功した結果が返された場合に _lppPropTags と lpppPropNames_ が指すメモリを解放します。 </span><span class="sxs-lookup"><span data-stu-id="25521-168">If so, call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the memory pointed to by  _lppPropTags_ and  _lpppPropNames_ when a successful result is returned.</span></span> <span data-ttu-id="25521-169">**MAPIFreeBuffer の呼び出しは、パラメーター** ごとに 1 回で十分です。ポインターの配列を走査し、各 **MAPINAMEID** 構造体を個別に解放する必要はない。</span><span class="sxs-lookup"><span data-stu-id="25521-169">One call to **MAPIFreeBuffer** is sufficient for each parameter; you do not have to traverse the array of pointers and free each **MAPINAMEID** structure individually.</span></span> 
  
<span data-ttu-id="25521-170">名前付きプロパティの詳細については、「MAPI 名前付き [プロパティ」を参照してください](mapi-named-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="25521-170">For more information about named properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="25521-171">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="25521-171">MFCMAPI reference</span></span>

<span data-ttu-id="25521-172">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="25521-172">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="25521-173">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="25521-173">**File**</span></span>|<span data-ttu-id="25521-174">**関数**</span><span class="sxs-lookup"><span data-stu-id="25521-174">**Function**</span></span>|<span data-ttu-id="25521-175">**コメント**</span><span class="sxs-lookup"><span data-stu-id="25521-175">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="25521-176">SingleMAPIPropListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="25521-176">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="25521-177">CSingleMAPIPropListCtrl::FindAllNamedProps</span><span class="sxs-lookup"><span data-stu-id="25521-177">CSingleMAPIPropListCtrl::FindAllNamedProps</span></span>  <br/> |<span data-ttu-id="25521-178">MFCMAPI は **IMAPIProp::GetNamesFromIDs** メソッドを使用して、以前にマップされた名前付きプロパティを検索します。</span><span class="sxs-lookup"><span data-stu-id="25521-178">MFCMAPI uses the **IMAPIProp::GetNamesFromIDs** method to look up named properties that have previously been mapped.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="25521-179">関連項目</span><span class="sxs-lookup"><span data-stu-id="25521-179">See also</span></span>



[<span data-ttu-id="25521-180">GUID</span><span class="sxs-lookup"><span data-stu-id="25521-180">GUID</span></span>](guid.md)
  
[<span data-ttu-id="25521-181">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="25521-181">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)
  
[<span data-ttu-id="25521-182">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="25521-182">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="25521-183">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="25521-183">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="25521-184">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="25521-184">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="25521-185">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="25521-185">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="25521-186">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="25521-186">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


<span data-ttu-id="25521-187">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="25521-187">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="25521-188">MAPI ���O�t���v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="25521-188">MAPI Named Properties</span></span>](mapi-named-properties.md)
  
[<span data-ttu-id="25521-189">エラー処理にマクロを使用する</span><span class="sxs-lookup"><span data-stu-id="25521-189">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

