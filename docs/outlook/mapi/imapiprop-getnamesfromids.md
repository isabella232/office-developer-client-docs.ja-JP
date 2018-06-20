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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a2ec6def319b1f4686a61e9f97a936bfeba0d410
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800662"
---
# <a name="imapipropgetnamesfromids"></a><span data-ttu-id="49082-103">IMAPIProp::GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="49082-103">IMAPIProp::GetNamesFromIDs</span></span>

  
  
<span data-ttu-id="49082-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="49082-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="49082-105">1 つまたは複数のプロパティの識別子に対応するプロパティ名を提供します。</span><span class="sxs-lookup"><span data-stu-id="49082-105">Provides the property names that correspond to one or more property identifiers.</span></span>
  
```cpp
HRESULT GetNamesFromIDs(
  LPSPropTagArray FAR * lppPropTags,
  LPGUID lpPropSetGuid,
  ULONG ulFlags,
  ULONG FAR * lpcPropNames,
  LPMAPINAMEID FAR * FAR * lpppPropNames
);
```

## <a name="parameters"></a><span data-ttu-id="49082-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="49082-106">Parameters</span></span>

 <span data-ttu-id="49082-107">_lppPropTags_</span><span class="sxs-lookup"><span data-stu-id="49082-107">_lppPropTags_</span></span>
  
> <span data-ttu-id="49082-108">[で [チェック アウト]プロパティ タグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインターの入力でそれ以外の場合、NULL の場合、すべての名前が返されることを示します。</span><span class="sxs-lookup"><span data-stu-id="49082-108">[in, out] On input, a pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags; otherwise, NULL, indicating that all names should be returned.</span></span> <span data-ttu-id="49082-109">プロパティ タグ配列の**あう**メンバーは、0 にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="49082-109">The **cValues** member for the property tag array cannot be 0.</span></span> <span data-ttu-id="49082-110">_LppPropTags_が入力時に有効なポインターである場合は、 **GetNamesFromIDs**は、配列に含まれている各プロパティの識別子の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="49082-110">If  _lppPropTags_ is a valid pointer on input, **GetNamesFromIDs** returns names for each property identifier included in the array.</span></span> 
    
 <span data-ttu-id="49082-111">_lpPropSetGuid_</span><span class="sxs-lookup"><span data-stu-id="49082-111">_lpPropSetGuid_</span></span>
  
> <span data-ttu-id="49082-112">[in]GUID、または[GUID](guid.md)へのポインター構造体、プロパティ セットを識別します。</span><span class="sxs-lookup"><span data-stu-id="49082-112">[in] A pointer to a GUID, or [GUID](guid.md) structure, that identifies a property set.</span></span> <span data-ttu-id="49082-113">_LpPropSetGuid_パラメーターは、有効なプロパティのセットを指すことができますか、NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="49082-113">The  _lpPropSetGuid_ parameter can point to a valid property set or can be NULL.</span></span> 
    
 <span data-ttu-id="49082-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="49082-114">_ulFlags_</span></span>
  
> <span data-ttu-id="49082-115">[in]返される名前の種類を示すフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="49082-115">[in] A bitmask of flags that indicates the type of names to be returned.</span></span> <span data-ttu-id="49082-116">次のフラグを使用することができます (両方のフラグが設定されている場合の名前は返されません)。</span><span class="sxs-lookup"><span data-stu-id="49082-116">The following flags can be used (if both flags are set, no names will be returned):</span></span>
    
<span data-ttu-id="49082-117">MAPI_NO_IDS</span><span class="sxs-lookup"><span data-stu-id="49082-117">MAPI_NO_IDS</span></span> 
  
> <span data-ttu-id="49082-118">Unicode 文字列として格納されている名前だけが返されるように要求します。</span><span class="sxs-lookup"><span data-stu-id="49082-118">Requests that only names stored as Unicode strings be returned.</span></span> 
    
<span data-ttu-id="49082-119">MAPI_NO_STRINGS</span><span class="sxs-lookup"><span data-stu-id="49082-119">MAPI_NO_STRINGS</span></span> 
  
> <span data-ttu-id="49082-120">数字の識別子として保存されている名前だけが返されるように要求します。</span><span class="sxs-lookup"><span data-stu-id="49082-120">Requests that only names stored as numeric identifiers be returned.</span></span> 
    
 <span data-ttu-id="49082-121">_lpcPropNames_</span><span class="sxs-lookup"><span data-stu-id="49082-121">_lpcPropNames_</span></span>
  
> <span data-ttu-id="49082-122">[out]_LppPropNames_パラメーターが指す配列内のプロパティ名のポインターの数へのポインターです。</span><span class="sxs-lookup"><span data-stu-id="49082-122">[out] A pointer to a count of the property name pointers in the array pointed to by the  _lppPropNames_ parameter.</span></span> 
    
 <span data-ttu-id="49082-123">_lpppPropNames_</span><span class="sxs-lookup"><span data-stu-id="49082-123">_lpppPropNames_</span></span>
  
> <span data-ttu-id="49082-124">[out]プロパティ名を格納する[MAPINAMEID](mapinameid.md)構造体へのポインターの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="49082-124">[out] A pointer to an array of pointers to [MAPINAMEID](mapinameid.md) structures that contains property names.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="49082-125">�߂�l</span><span class="sxs-lookup"><span data-stu-id="49082-125">Return value</span></span>

<span data-ttu-id="49082-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="49082-126">S_OK</span></span> 
  
> <span data-ttu-id="49082-127">プロパティ名が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="49082-127">The property names were successfully returned.</span></span> 
    
<span data-ttu-id="49082-128">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="49082-128">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="49082-129">オブジェクトは、名前付きプロパティをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="49082-129">The object does not support named properties.</span></span> 
    
<span data-ttu-id="49082-130">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="49082-130">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="49082-131">呼び出しは完了しましたが、1 つまたは複数のプロパティの名前は返されませんでした。</span><span class="sxs-lookup"><span data-stu-id="49082-131">The call succeeded overall, but names for one or more properties could not be returned.</span></span> <span data-ttu-id="49082-132">**PT_ERROR**のプロパティの型は、障害が発生したプロパティのプロパティ タグであります。</span><span class="sxs-lookup"><span data-stu-id="49082-132">The property tags for the failing properties have a property type of **PT_ERROR**.</span></span> <span data-ttu-id="49082-133">この警告が返されると、呼び出しを成功として処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="49082-133">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="49082-134">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="49082-134">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="49082-135">詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="49082-135">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> 
    
<span data-ttu-id="49082-136">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="49082-136">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="49082-137">_LppPropTags_で指定されたプロパティ タグ配列内のエントリの 1 つ以上の**あう**メンバーは 0 に設定されています。</span><span class="sxs-lookup"><span data-stu-id="49082-137">The **cValues** member of one or more of the entries in the property tag array pointed to by  _lppPropTags_ is set to 0.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="49082-138">備考</span><span class="sxs-lookup"><span data-stu-id="49082-138">Remarks</span></span>

<span data-ttu-id="49082-139">ほとんどのプロパティへのアクセスは、プロパティの識別子では、いくつかのプロパティを名前でアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="49082-139">While access to most properties is by property identifier, some properties can be accessed by name.</span></span> <span data-ttu-id="49082-140">次の操作には、 **IMAPIProp::GetNamesFromIDs**メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="49082-140">The **IMAPIProp::GetNamesFromIDs** method can be called to do the following:</span></span> 
  
- <span data-ttu-id="49082-141">特定のプロパティ セット内の特定のプロパティ識別子の名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="49082-141">Retrieve names for specific property identifiers in a specific property set.</span></span>
    
- <span data-ttu-id="49082-142">任意のプロパティ セット内の特定のプロパティの識別子の名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="49082-142">Retrieve names for specific property identifiers in any property set.</span></span>
    
- <span data-ttu-id="49082-143">オブジェクトのマッピングに含まれるすべての名前付きプロパティの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="49082-143">Retrieve names for all named properties that are included in the object's mapping.</span></span>
    
<span data-ttu-id="49082-144">**GetNamesFromIDs**がプロパティ セットとプロパティの型を無視し、すべての名前を返す 1 つまたは複数のプロパティの識別子を持つ有効なプロパティ タグ配列を指す_lppPropTags_と_lpPropSetGuid_を指す有効なプロパティを設定する場合指定した識別子にマップするとします。</span><span class="sxs-lookup"><span data-stu-id="49082-144">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers, and  _lpPropSetGuid_ points to a valid property set, **GetNamesFromIDs** ignores the property set and the property types and returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="49082-145">プロパティ識別子と_lpPropSetGuid_の 1 つまたは複数の有効なプロパティ タグ配列を_lppPropTags_ポイントの場合、 **GetNamesFromIDs**を NULL がすべての指定した識別子にマップされる名前を返します。</span><span class="sxs-lookup"><span data-stu-id="49082-145">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers and  _lpPropSetGuid_ is NULL, **GetNamesFromIDs** returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="49082-146">指定した識別子は、名前を持たない場合、 **GetNamesFromIDs**は_lpppPropNames_で返される構造体でその識別子の場所には NULL を返し、MAPI_W_ERRORS_RETURNED を返します。</span><span class="sxs-lookup"><span data-stu-id="49082-146">If a specified identifier does not have a name, **GetNamesFromIDs** returns NULL in that identifier's place in the structure returned in  _lpppPropNames_ and also returns MAPI_W_ERRORS_RETURNED.</span></span> 
  
<span data-ttu-id="49082-147">_LpPropSetGuid_と_lppPropTags_の両方が NULL の場合、 **GetNamesFromIDs**は新しいプロパティ タグ配列を割り当て、すべてのすべてのオブジェクトの名前付きプロパティの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="49082-147">If both  _lpPropSetGuid_ and  _lppPropTags_ are NULL, **GetNamesFromIDs** allocates a new property tag array and returns all of the names for all of the named properties for the object.</span></span> 
  
<span data-ttu-id="49082-148">返される名前がない場合は、おそらく、要求されたプロパティ セットのプロパティはありませんか、フラグで除外された型のすべてのプロパティは、 **GetNamesFromIDs**は、次の。</span><span class="sxs-lookup"><span data-stu-id="49082-148">When there are no names to be returned, perhaps because there are no properties in the requested property set or all of the properties are of a type excluded by the flags, **GetNamesFromIDs** does the following:</span></span> 
  
- <span data-ttu-id="49082-149">S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="49082-149">Returns S_OK.</span></span>
    
- <span data-ttu-id="49082-150">**あう**メンバーを 0 に設定する、新しい**SPropTagArray**構造を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="49082-150">Allocates a new **SPropTagArray** structure, setting the **cValues** member to 0.</span></span> 
    
- <span data-ttu-id="49082-151">_LpcPropNames_の内容を 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="49082-151">Sets the contents of  _lpcPropNames_ to 0.</span></span> 
    
- <span data-ttu-id="49082-152">_LpppPropNames_の内容を NULL に設定します。</span><span class="sxs-lookup"><span data-stu-id="49082-152">Sets the contents of  _lpppPropNames_ to NULL.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="49082-153">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="49082-153">Notes to implementers</span></span>

<span data-ttu-id="49082-154">_LpPropSetGuid_を指し、有効なプロパティのセット、 _lppPropTags_が NULL の場合、結果は定義されていません。</span><span class="sxs-lookup"><span data-stu-id="49082-154">If  _lpPropSetGuid_ points to a valid property set and  _lppPropTags_ is NULL, the result is undefined.</span></span> <span data-ttu-id="49082-155">次の方法のいずれかを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="49082-155">You can use one of the following strategies:</span></span> 
  
- <span data-ttu-id="49082-156">プロパティの設定を無視し、プロパティ タグ配列の識別子の名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="49082-156">Ignore the property set and return the names for the identifiers in the property tag array.</span></span>
    
- <span data-ttu-id="49082-157">プロパティ タグ配列の指定されたプロパティ セットに属しているだけの識別子の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="49082-157">Return the names for only the identifiers in the property tag array that belong to the specified property set.</span></span>
    
- <span data-ttu-id="49082-158">MAPI_E_INVALID_PARAMETER を返す呼び出しは失敗します。</span><span class="sxs-lookup"><span data-stu-id="49082-158">Fail the call, returning MAPI_E_INVALID_PARAMETER.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="49082-159">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="49082-159">Notes to callers</span></span>

<span data-ttu-id="49082-160">すべてのオブジェクトの名前付きプロパティを取得するには、まずオブジェクトの[IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドを呼び出すし、 **GetNamesFromIDs**の範囲は 0x8000 を超える返される識別子を渡します。</span><span class="sxs-lookup"><span data-stu-id="49082-160">To retrieve all of the named properties for an object, you must first call the object's [IMAPIProp::GetPropList](imapiprop-getproplist.md) method and then pass the returned identifiers that are above the 0x8000 range to **GetNamesFromIDs**.</span></span>
  
<span data-ttu-id="49082-161">予期しない結果を渡す場合は、有効なプロパティ セットが有効なプロパティ タグの配列ではありません、しておいてください。</span><span class="sxs-lookup"><span data-stu-id="49082-161">If you pass a valid property set but not a valid property tag array, be prepared for unpredictable results.</span></span> <span data-ttu-id="49082-162">**GetNamesFromIDs**の一部の実装では、プロパティの設定を無視し、プロパティ タグ配列の識別子の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="49082-162">Some implementations of **GetNamesFromIDs** ignore the property set and return the names for the identifiers in the property tag array.</span></span> <span data-ttu-id="49082-163">いくつかの実装では、MAPI_E_INVALID_PARAMETER を返します。</span><span class="sxs-lookup"><span data-stu-id="49082-163">Some implementations return MAPI_E_INVALID_PARAMETER.</span></span> <span data-ttu-id="49082-164">まだ他の実装では、プロパティ セット内のすべてのプロパティの識別子の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="49082-164">Still other implementations return names for identifiers of all properties in the property set.</span></span> <span data-ttu-id="49082-165">プロパティ セットの PS_PUBLIC_STRINGS 場合、 **GetNamesFromIDs**は、これまでに作成されたすべての名前を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="49082-165">If the property set is PS_PUBLIC_STRINGS, **GetNamesFromIDs** can return all names that were ever created.</span></span> <span data-ttu-id="49082-166">サービス プロバイダーがパブリック文字列に関連付けられている識別子のプロパティを格納するかどうかは、数量単価型ではありません。</span><span class="sxs-lookup"><span data-stu-id="49082-166">Whether the service provider stores a property under the identifiers associated with the public strings is immaterial.</span></span> 
  
<span data-ttu-id="49082-167">プロパティ名を持つが終了したら、任意の名前が返されたかどうかを決定する_lpcPropNames_パラメーターの内容を確認してください。</span><span class="sxs-lookup"><span data-stu-id="49082-167">When you are finished with the property names, check the contents of the  _lpcPropNames_ parameter to determine whether any names were returned.</span></span> <span data-ttu-id="49082-168">その場合は、正常な結果が返されるときに_lppPropTags_と_lpppPropNames_が指すメモリを解放する[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="49082-168">If so, call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the memory pointed to by  _lppPropTags_ and  _lpppPropNames_ when a successful result is returned.</span></span> <span data-ttu-id="49082-169">**MAPIFreeBuffer** 1 回の呼び出しはそれぞれのパラメーターに対して十分ですポインターの配列を走査し、各**MAPINAMEID**構造体を個別に解放する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="49082-169">One call to **MAPIFreeBuffer** is sufficient for each parameter; you do not have to traverse the array of pointers and free each **MAPINAMEID** structure individually.</span></span> 
  
<span data-ttu-id="49082-170">名前付きプロパティの詳細については、 [MAPI 名前付きプロパティ](mapi-named-properties.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="49082-170">For more information about named properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="49082-171">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="49082-171">MFCMAPI reference</span></span>

<span data-ttu-id="49082-172">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="49082-172">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="49082-173">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="49082-173">**File**</span></span>|<span data-ttu-id="49082-174">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="49082-174">**Function**</span></span>|<span data-ttu-id="49082-175">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="49082-175">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="49082-176">SingleMAPIPropListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="49082-176">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="49082-177">CSingleMAPIPropListCtrl::FindAllNamedProps</span><span class="sxs-lookup"><span data-stu-id="49082-177">CSingleMAPIPropListCtrl::FindAllNamedProps</span></span>  <br/> |<span data-ttu-id="49082-178">MFCMAPI では、 **IMAPIProp::GetNamesFromIDs**メソッドを使用して、以前にマップされている名前付きのプロパティを検索します。</span><span class="sxs-lookup"><span data-stu-id="49082-178">MFCMAPI uses the **IMAPIProp::GetNamesFromIDs** method to look up named properties that have previously been mapped.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="49082-179">関連項目</span><span class="sxs-lookup"><span data-stu-id="49082-179">See also</span></span>



[<span data-ttu-id="49082-180">GUID</span><span class="sxs-lookup"><span data-stu-id="49082-180">GUID</span></span>](guid.md)
  
[<span data-ttu-id="49082-181">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="49082-181">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)
  
[<span data-ttu-id="49082-182">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="49082-182">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="49082-183">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="49082-183">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="49082-184">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="49082-184">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="49082-185">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="49082-185">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="49082-186">IMAPIProp: IUnknown</span><span class="sxs-lookup"><span data-stu-id="49082-186">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


<span data-ttu-id="49082-187">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="49082-187">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="49082-188">MAPI ���O�t���v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="49082-188">MAPI Named Properties</span></span>](mapi-named-properties.md)
  
[<span data-ttu-id="49082-189">エラー処理のためのマクロを使用してください。</span><span class="sxs-lookup"><span data-stu-id="49082-189">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

