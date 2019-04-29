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
# <a name="imapipropgetnamesfromids"></a><span data-ttu-id="faf51-103">IMAPIProp::GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="faf51-103">IMAPIProp::GetNamesFromIDs</span></span>

  
  
<span data-ttu-id="faf51-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="faf51-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="faf51-105">1つまたは複数のプロパティ識別子に対応するプロパティ名を提供します。</span><span class="sxs-lookup"><span data-stu-id="faf51-105">Provides the property names that correspond to one or more property identifiers.</span></span>
  
```cpp
HRESULT GetNamesFromIDs(
  LPSPropTagArray FAR * lppPropTags,
  LPGUID lpPropSetGuid,
  ULONG ulFlags,
  ULONG FAR * lpcPropNames,
  LPMAPINAMEID FAR * FAR * lpppPropNames
);
```

## <a name="parameters"></a><span data-ttu-id="faf51-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="faf51-106">Parameters</span></span>

 <span data-ttu-id="faf51-107">_lppproptags_</span><span class="sxs-lookup"><span data-stu-id="faf51-107">_lppPropTags_</span></span>
  
> <span data-ttu-id="faf51-108">[入力]入力時に、プロパティタグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。それ以外の場合は NULL。すべての名前を返す必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="faf51-108">[in, out] On input, a pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags; otherwise, NULL, indicating that all names should be returned.</span></span> <span data-ttu-id="faf51-109">プロパティタグ配列の**cvalues**メンバーを0にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="faf51-109">The **cValues** member for the property tag array cannot be 0.</span></span> <span data-ttu-id="faf51-110">_lppproptags_が入力に有効なポインターである場合、 **GetNamesFromIDs**は、配列に含まれる各プロパティ識別子の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="faf51-110">If  _lppPropTags_ is a valid pointer on input, **GetNamesFromIDs** returns names for each property identifier included in the array.</span></span> 
    
 <span data-ttu-id="faf51-111">_lppropsetguid_</span><span class="sxs-lookup"><span data-stu-id="faf51-111">_lpPropSetGuid_</span></span>
  
> <span data-ttu-id="faf51-112">順番プロパティセットを識別する guid または[guid](guid.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="faf51-112">[in] A pointer to a GUID, or [GUID](guid.md) structure, that identifies a property set.</span></span> <span data-ttu-id="faf51-113">_lppropsetguid_パラメーターは、有効なプロパティセットを指すことも、NULL にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="faf51-113">The  _lpPropSetGuid_ parameter can point to a valid property set or can be NULL.</span></span> 
    
 <span data-ttu-id="faf51-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="faf51-114">_ulFlags_</span></span>
  
> <span data-ttu-id="faf51-115">順番返される名前の種類を示すフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="faf51-115">[in] A bitmask of flags that indicates the type of names to be returned.</span></span> <span data-ttu-id="faf51-116">次のフラグを使用できます (両方のフラグが設定されている場合、名前は返されません)。</span><span class="sxs-lookup"><span data-stu-id="faf51-116">The following flags can be used (if both flags are set, no names will be returned):</span></span>
    
<span data-ttu-id="faf51-117">MAPI_NO_IDS</span><span class="sxs-lookup"><span data-stu-id="faf51-117">MAPI_NO_IDS</span></span> 
  
> <span data-ttu-id="faf51-118">Unicode 文字列として格納されている名前のみを返すように要求します。</span><span class="sxs-lookup"><span data-stu-id="faf51-118">Requests that only names stored as Unicode strings be returned.</span></span> 
    
<span data-ttu-id="faf51-119">MAPI_NO_STRINGS</span><span class="sxs-lookup"><span data-stu-id="faf51-119">MAPI_NO_STRINGS</span></span> 
  
> <span data-ttu-id="faf51-120">数値識別子として格納されている名前のみを返すように要求します。</span><span class="sxs-lookup"><span data-stu-id="faf51-120">Requests that only names stored as numeric identifiers be returned.</span></span> 
    
 <span data-ttu-id="faf51-121">_lpcPropNames_</span><span class="sxs-lookup"><span data-stu-id="faf51-121">_lpcPropNames_</span></span>
  
> <span data-ttu-id="faf51-122">読み上げ_lpppropnames_パラメーターによって指定された配列内のプロパティ名ポインターの数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="faf51-122">[out] A pointer to a count of the property name pointers in the array pointed to by the  _lppPropNames_ parameter.</span></span> 
    
 <span data-ttu-id="faf51-123">_lpppPropNames_</span><span class="sxs-lookup"><span data-stu-id="faf51-123">_lpppPropNames_</span></span>
  
> <span data-ttu-id="faf51-124">読み上げプロパティ名を含む[mapinameid](mapinameid.md)構造体へのポインターの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="faf51-124">[out] A pointer to an array of pointers to [MAPINAMEID](mapinameid.md) structures that contains property names.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="faf51-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="faf51-125">Return value</span></span>

<span data-ttu-id="faf51-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="faf51-126">S_OK</span></span> 
  
> <span data-ttu-id="faf51-127">プロパティ名が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="faf51-127">The property names were successfully returned.</span></span> 
    
<span data-ttu-id="faf51-128">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="faf51-128">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="faf51-129">オブジェクトは、名前付きプロパティをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="faf51-129">The object does not support named properties.</span></span> 
    
<span data-ttu-id="faf51-130">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="faf51-130">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="faf51-131">呼び出しは全体的に成功しましたが、1つ以上のプロパティの名前を返すことができませんでした。</span><span class="sxs-lookup"><span data-stu-id="faf51-131">The call succeeded overall, but names for one or more properties could not be returned.</span></span> <span data-ttu-id="faf51-132">失敗したプロパティのプロパティタグには、 **PT_ERROR**というプロパティの種類があります。</span><span class="sxs-lookup"><span data-stu-id="faf51-132">The property tags for the failing properties have a property type of **PT_ERROR**.</span></span> <span data-ttu-id="faf51-133">この警告が返された場合、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="faf51-133">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="faf51-134">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="faf51-134">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="faf51-135">詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="faf51-135">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> 
    
<span data-ttu-id="faf51-136">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="faf51-136">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="faf51-137">_lppproptags_によって示されるプロパティタグ配列内の1つ以上のエントリの**cvalues**メンバーが0に設定されています。</span><span class="sxs-lookup"><span data-stu-id="faf51-137">The **cValues** member of one or more of the entries in the property tag array pointed to by  _lppPropTags_ is set to 0.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="faf51-138">注釈</span><span class="sxs-lookup"><span data-stu-id="faf51-138">Remarks</span></span>

<span data-ttu-id="faf51-139">ほとんどのプロパティはプロパティ識別子によってアクセスできますが、名前によってアクセスできるプロパティもあります。</span><span class="sxs-lookup"><span data-stu-id="faf51-139">While access to most properties is by property identifier, some properties can be accessed by name.</span></span> <span data-ttu-id="faf51-140">**imapiprop:: GetNamesFromIDs**メソッドを呼び出すと、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="faf51-140">The **IMAPIProp::GetNamesFromIDs** method can be called to do the following:</span></span> 
  
- <span data-ttu-id="faf51-141">特定のプロパティセット内の特定のプロパティ識別子の名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="faf51-141">Retrieve names for specific property identifiers in a specific property set.</span></span>
    
- <span data-ttu-id="faf51-142">任意のプロパティセット内の特定のプロパティ識別子の名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="faf51-142">Retrieve names for specific property identifiers in any property set.</span></span>
    
- <span data-ttu-id="faf51-143">オブジェクトのマッピングに含まれているすべての名前付きプロパティの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="faf51-143">Retrieve names for all named properties that are included in the object's mapping.</span></span>
    
<span data-ttu-id="faf51-144">_lppproptags_が1つまたは複数のプロパティ識別子を持つ有効なプロパティタグ配列を指しており、 _lppropsetguid_が有効なプロパティセットをポイントしている場合、 **GetNamesFromIDs**はプロパティセットとプロパティの型を無視し、すべての名前を返します。指定した識別子にマップされます。</span><span class="sxs-lookup"><span data-stu-id="faf51-144">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers, and  _lpPropSetGuid_ points to a valid property set, **GetNamesFromIDs** ignores the property set and the property types and returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="faf51-145">_lppproptags_が、1つまたは複数のプロパティ識別子を持つ有効なプロパティタグ配列を指しており、 _lppropsetguid_が NULL の場合、 **GetNamesFromIDs**は指定された識別子にマップされているすべての名前を返します。</span><span class="sxs-lookup"><span data-stu-id="faf51-145">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers and  _lpPropSetGuid_ is NULL, **GetNamesFromIDs** returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="faf51-146">指定した識別子に名前が含まれていない場合、 **GetNamesFromIDs**はその識別子が_lpppPropNames_で返される構造内で NULL を返し、MAPI_W_ERRORS_RETURNED も返します。</span><span class="sxs-lookup"><span data-stu-id="faf51-146">If a specified identifier does not have a name, **GetNamesFromIDs** returns NULL in that identifier's place in the structure returned in  _lpppPropNames_ and also returns MAPI_W_ERRORS_RETURNED.</span></span> 
  
<span data-ttu-id="faf51-147">_lppropsetguid_と_lppproptags_の両方が NULL の場合、 **GetNamesFromIDs**は新しいプロパティタグ配列を割り当て、オブジェクトのすべての名前付きプロパティの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="faf51-147">If both  _lpPropSetGuid_ and  _lppPropTags_ are NULL, **GetNamesFromIDs** allocates a new property tag array and returns all of the names for all of the named properties for the object.</span></span> 
  
<span data-ttu-id="faf51-148">返される名前がない場合は、要求されたプロパティセットにプロパティが存在しないか、またはすべてのプロパティがフラグによって除外される型であるため、 **GetNamesFromIDs**は次の処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="faf51-148">When there are no names to be returned, perhaps because there are no properties in the requested property set or all of the properties are of a type excluded by the flags, **GetNamesFromIDs** does the following:</span></span> 
  
- <span data-ttu-id="faf51-149">S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="faf51-149">Returns S_OK.</span></span>
    
- <span data-ttu-id="faf51-150">**cvalues**メンバーを0に設定して、新しい**SPropTagArray**構造を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="faf51-150">Allocates a new **SPropTagArray** structure, setting the **cValues** member to 0.</span></span> 
    
- <span data-ttu-id="faf51-151">_lpcPropNames_の内容を0に設定します。</span><span class="sxs-lookup"><span data-stu-id="faf51-151">Sets the contents of  _lpcPropNames_ to 0.</span></span> 
    
- <span data-ttu-id="faf51-152">_lpppPropNames_の内容を NULL に設定します。</span><span class="sxs-lookup"><span data-stu-id="faf51-152">Sets the contents of  _lpppPropNames_ to NULL.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="faf51-153">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="faf51-153">Notes to implementers</span></span>

<span data-ttu-id="faf51-154">_lppropsetguid_が有効なプロパティセットを指しており、 _lppproptags_が NULL の場合、結果は未定義となります。</span><span class="sxs-lookup"><span data-stu-id="faf51-154">If  _lpPropSetGuid_ points to a valid property set and  _lppPropTags_ is NULL, the result is undefined.</span></span> <span data-ttu-id="faf51-155">次のいずれかの方法を使用できます。</span><span class="sxs-lookup"><span data-stu-id="faf51-155">You can use one of the following strategies:</span></span> 
  
- <span data-ttu-id="faf51-156">プロパティセットを無視し、プロパティタグ配列の識別子の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="faf51-156">Ignore the property set and return the names for the identifiers in the property tag array.</span></span>
    
- <span data-ttu-id="faf51-157">指定したプロパティセットに属するプロパティタグ配列内の識別子の名前のみを返します。</span><span class="sxs-lookup"><span data-stu-id="faf51-157">Return the names for only the identifiers in the property tag array that belong to the specified property set.</span></span>
    
- <span data-ttu-id="faf51-158">呼び出しを失敗させ、MAPI_E_INVALID_PARAMETER を返します。</span><span class="sxs-lookup"><span data-stu-id="faf51-158">Fail the call, returning MAPI_E_INVALID_PARAMETER.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="faf51-159">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="faf51-159">Notes to callers</span></span>

<span data-ttu-id="faf51-160">オブジェクトのすべての名前付きプロパティを取得するには、最初にオブジェクトの[imapiprop:: getproplist](imapiprop-getproplist.md)メソッドを呼び出してから、0x8000 の範囲の上にある返された識別子を**GetNamesFromIDs**に渡します。</span><span class="sxs-lookup"><span data-stu-id="faf51-160">To retrieve all of the named properties for an object, you must first call the object's [IMAPIProp::GetPropList](imapiprop-getproplist.md) method and then pass the returned identifiers that are above the 0x8000 range to **GetNamesFromIDs**.</span></span>
  
<span data-ttu-id="faf51-161">有効なプロパティセットを渡すが、有効なプロパティタグ配列を渡さない場合は、予期しない結果を得るために準備してください。</span><span class="sxs-lookup"><span data-stu-id="faf51-161">If you pass a valid property set but not a valid property tag array, be prepared for unpredictable results.</span></span> <span data-ttu-id="faf51-162">**GetNamesFromIDs**の一部の実装では、プロパティセットを無視して、プロパティタグの配列内の識別子の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="faf51-162">Some implementations of **GetNamesFromIDs** ignore the property set and return the names for the identifiers in the property tag array.</span></span> <span data-ttu-id="faf51-163">一部の実装は MAPI_E_INVALID_PARAMETER を返します。</span><span class="sxs-lookup"><span data-stu-id="faf51-163">Some implementations return MAPI_E_INVALID_PARAMETER.</span></span> <span data-ttu-id="faf51-164">その他の実装では、プロパティセット内のすべてのプロパティの識別子の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="faf51-164">Still other implementations return names for identifiers of all properties in the property set.</span></span> <span data-ttu-id="faf51-165">プロパティセットが PS_PUBLIC_STRINGS の場合、 **GetNamesFromIDs**は作成されたすべての名前を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="faf51-165">If the property set is PS_PUBLIC_STRINGS, **GetNamesFromIDs** can return all names that were ever created.</span></span> <span data-ttu-id="faf51-166">パブリック文字列に関連付けられた識別子の下に、サービスプロバイダーがプロパティを格納するかどうかは、immaterial になります。</span><span class="sxs-lookup"><span data-stu-id="faf51-166">Whether the service provider stores a property under the identifiers associated with the public strings is immaterial.</span></span> 
  
<span data-ttu-id="faf51-167">プロパティ名の指定が終了したら、 _lpcPropNames_パラメーターの内容を確認して、名前が返されたかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="faf51-167">When you are finished with the property names, check the contents of the  _lpcPropNames_ parameter to determine whether any names were returned.</span></span> <span data-ttu-id="faf51-168">その場合は、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、正常な結果が返されたときに、 _lppproptags_および_lpppPropNames_が指すメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="faf51-168">If so, call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the memory pointed to by  _lppPropTags_ and  _lpppPropNames_ when a successful result is returned.</span></span> <span data-ttu-id="faf51-169">**MAPIFreeBuffer**の1回の呼び出しでは、各パラメーターに対して十分です。ポインターの配列をスキャンして、各**mapinameid**構造を個別に解放する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="faf51-169">One call to **MAPIFreeBuffer** is sufficient for each parameter; you do not have to traverse the array of pointers and free each **MAPINAMEID** structure individually.</span></span> 
  
<span data-ttu-id="faf51-170">名前付きプロパティの詳細については、「 [MAPI の名前付きプロパティ](mapi-named-properties.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="faf51-170">For more information about named properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="faf51-171">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="faf51-171">MFCMAPI reference</span></span>

<span data-ttu-id="faf51-172">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="faf51-172">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="faf51-173">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="faf51-173">**File**</span></span>|<span data-ttu-id="faf51-174">**関数**</span><span class="sxs-lookup"><span data-stu-id="faf51-174">**Function**</span></span>|<span data-ttu-id="faf51-175">**コメント**</span><span class="sxs-lookup"><span data-stu-id="faf51-175">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="faf51-176">SingleMAPIPropListCtrl</span><span class="sxs-lookup"><span data-stu-id="faf51-176">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="faf51-177">CSingleMAPIPropListCtrl:: findallnamedprops</span><span class="sxs-lookup"><span data-stu-id="faf51-177">CSingleMAPIPropListCtrl::FindAllNamedProps</span></span>  <br/> |<span data-ttu-id="faf51-178">mfcmapi は、 **imapiprop:: GetNamesFromIDs**メソッドを使用して、以前にマップされていた名前付きプロパティを検索します。</span><span class="sxs-lookup"><span data-stu-id="faf51-178">MFCMAPI uses the **IMAPIProp::GetNamesFromIDs** method to look up named properties that have previously been mapped.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="faf51-179">関連項目</span><span class="sxs-lookup"><span data-stu-id="faf51-179">See also</span></span>



[<span data-ttu-id="faf51-180">GUID</span><span class="sxs-lookup"><span data-stu-id="faf51-180">GUID</span></span>](guid.md)
  
[<span data-ttu-id="faf51-181">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="faf51-181">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)
  
[<span data-ttu-id="faf51-182">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="faf51-182">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="faf51-183">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="faf51-183">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="faf51-184">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="faf51-184">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="faf51-185">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="faf51-185">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="faf51-186">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="faf51-186">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


<span data-ttu-id="faf51-187">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="faf51-187">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="faf51-188">MAPI ���O�t���v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="faf51-188">MAPI Named Properties</span></span>](mapi-named-properties.md)
  
[<span data-ttu-id="faf51-189">エラー処理にマクロを使用する</span><span class="sxs-lookup"><span data-stu-id="faf51-189">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

