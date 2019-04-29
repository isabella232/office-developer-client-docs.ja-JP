---
title: imapipropgetidsfromnames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetIDsFromNames
api_type:
- COM
ms.assetid: e3f501a4-a8ee-43d7-bd83-c94e7980c398
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 28880b818bc80e31cae0c695d4aac92eb9555cac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433585"
---
# <a name="imapipropgetidsfromnames"></a><span data-ttu-id="cc09a-103">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="cc09a-103">IMAPIProp::GetIDsFromNames</span></span>

  
  
<span data-ttu-id="cc09a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc09a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc09a-105">1つまたは複数のプロパティ名に対応するプロパティ識別子を提供します。</span><span class="sxs-lookup"><span data-stu-id="cc09a-105">Provides the property identifiers that correspond to one or more property names.</span></span>
  
```cpp
HRESULT GetIDsFromNames(
  ULONG cPropNames,
  LPMAPINAMEID FAR * lppPropNames,
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTags
);
```

## <a name="parameters"></a><span data-ttu-id="cc09a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cc09a-106">Parameters</span></span>

 <span data-ttu-id="cc09a-107">_cpropnames_</span><span class="sxs-lookup"><span data-stu-id="cc09a-107">_cPropNames_</span></span>
  
> <span data-ttu-id="cc09a-108">順番_lpppropnames_パラメーターによって示されるプロパティ名の数。</span><span class="sxs-lookup"><span data-stu-id="cc09a-108">[in] The count of property names pointed to by the  _lppPropNames_ parameter.</span></span> <span data-ttu-id="cc09a-109">_lpppropnames_が NULL の場合、 _cpropnames_パラメーターは0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="cc09a-109">If  _lppPropNames_ is NULL, the  _cPropNames_ parameter must be 0.</span></span> 
    
 <span data-ttu-id="cc09a-110">_lpppropnames_</span><span class="sxs-lookup"><span data-stu-id="cc09a-110">_lppPropNames_</span></span>
  
> <span data-ttu-id="cc09a-111">順番プロパティ名の配列へのポインター、または NULL。</span><span class="sxs-lookup"><span data-stu-id="cc09a-111">[in] A pointer to an array of property names, or NULL.</span></span> <span data-ttu-id="cc09a-112">オブジェクトが情報を持っているすべてのプロパティセット内のすべてのプロパティ名に対して NULL 要求のプロパティ識別子を渡す。</span><span class="sxs-lookup"><span data-stu-id="cc09a-112">Passing NULL requests property identifiers for all property names in all property sets about which the object has information.</span></span> <span data-ttu-id="cc09a-113">MAPI_CREATE フラグが_ulflags_パラメーターで設定されている場合、 _lpppropnames_パラメーターを NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="cc09a-113">The  _lppPropNames_ parameter must not be NULL if the MAPI_CREATE flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="cc09a-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cc09a-114">_ulFlags_</span></span>
  
> <span data-ttu-id="cc09a-115">順番プロパティ識別子を返す方法を示すフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="cc09a-115">[in] A bitmask of flags that indicates how the property identifiers should be returned.</span></span> <span data-ttu-id="cc09a-116">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="cc09a-116">The following flag can be set:</span></span>
    
<span data-ttu-id="cc09a-117">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="cc09a-117">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="cc09a-118">プロパティ識別子がまだ割り当てられていない場合は、その識別子を、 _lpppropnames_で指定されたプロパティ名の配列に含まれる1つ以上の名前に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="cc09a-118">Assigns a property identifier, if one has not yet been assigned, to one or more of the names included in the property name array pointed to by  _lppPropNames_.</span></span> <span data-ttu-id="cc09a-119">このフラグは、名前から識別子へのマッピングテーブルに、識別子を内部的に登録します。</span><span class="sxs-lookup"><span data-stu-id="cc09a-119">This flag internally registers the identifier in the name-to-identifier mapping table.</span></span>
    
 <span data-ttu-id="cc09a-120">_lppproptags_</span><span class="sxs-lookup"><span data-stu-id="cc09a-120">_lppPropTags_</span></span>
  
> <span data-ttu-id="cc09a-121">読み上げ既存または新規に割り当てられたプロパティ識別子を含むプロパティタグの配列へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="cc09a-121">[out] A pointer to a pointer to an array of property tags that contains existing or newly assigned property identifiers.</span></span> <span data-ttu-id="cc09a-122">この配列の property タグのプロパティの種類は、 **PT_UNSPECIFIED**に設定されています。</span><span class="sxs-lookup"><span data-stu-id="cc09a-122">The property types for the property tags in this array are set to **PT_UNSPECIFIED**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cc09a-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc09a-123">Return value</span></span>

<span data-ttu-id="cc09a-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="cc09a-124">S_OK</span></span> 
  
> <span data-ttu-id="cc09a-125">指定したプロパティ名の識別子が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="cc09a-125">The identifiers for the specified property names were successfully returned.</span></span>
    
<span data-ttu-id="cc09a-126">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="cc09a-126">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="cc09a-127">オブジェクトは、名前付きプロパティをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="cc09a-127">The object does not support named properties.</span></span>
    
<span data-ttu-id="cc09a-128">MAPI_E_NOT_ENOUGH_MEMORY</span><span class="sxs-lookup"><span data-stu-id="cc09a-128">MAPI_E_NOT_ENOUGH_MEMORY</span></span> 
  
> <span data-ttu-id="cc09a-129">メモリが不足しているため、識別子を取得できませんでした。</span><span class="sxs-lookup"><span data-stu-id="cc09a-129">Insufficient memory was available to retrieve the identifiers.</span></span>
    
<span data-ttu-id="cc09a-130">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="cc09a-130">MAPI_E_TOO_BIG</span></span> 
  
> <span data-ttu-id="cc09a-131">返されるプロパティタグが多すぎるため、操作を実行できません。</span><span class="sxs-lookup"><span data-stu-id="cc09a-131">The operation cannot be performed because it requires too many property tags to be returned.</span></span>
    
<span data-ttu-id="cc09a-132">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="cc09a-132">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="cc09a-133">呼び出しは全体的に成功しましたが、1つ以上のプロパティ識別子を返すことができませんでした。</span><span class="sxs-lookup"><span data-stu-id="cc09a-133">The call succeeded overall, but one or more property identifiers could not be returned.</span></span> <span data-ttu-id="cc09a-134">使用できない各プロパティの対応するプロパティの種類が**PT_ERROR**に設定され、その識別子が0に設定されます。</span><span class="sxs-lookup"><span data-stu-id="cc09a-134">The corresponding property type for each unavailable property is set to **PT_ERROR** and its identifier to zero.</span></span> <span data-ttu-id="cc09a-135">この警告が返された場合は、呼び出しを成功として処理します。</span><span class="sxs-lookup"><span data-stu-id="cc09a-135">When this warning is returned, handle the call as successful.</span></span> <span data-ttu-id="cc09a-136">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="cc09a-136">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="cc09a-137">「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cc09a-137">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cc09a-138">注釈</span><span class="sxs-lookup"><span data-stu-id="cc09a-138">Remarks</span></span>

<span data-ttu-id="cc09a-139">**imapiprop:: getidsfromnames**メソッドは、1つ以上の名前付きプロパティのプロパティ識別子を保持するプロパティタグの配列を取得します。</span><span class="sxs-lookup"><span data-stu-id="cc09a-139">The **IMAPIProp::GetIDsFromNames** method retrieves an array of property tags that hold the property identifiers for one or more named properties.</span></span> <span data-ttu-id="cc09a-140">**imapiprop:: getidsfromnames**を呼び出して、次の操作を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="cc09a-140">**IMAPIProp::GetIDsFromNames** can be called to do the following:</span></span> 
  
- <span data-ttu-id="cc09a-141">新しい名前の識別子を作成します。</span><span class="sxs-lookup"><span data-stu-id="cc09a-141">Create identifiers for new names.</span></span>
    
- <span data-ttu-id="cc09a-142">特定の名前の識別子を取得します。</span><span class="sxs-lookup"><span data-stu-id="cc09a-142">Retrieve identifiers for specific names.</span></span>
    
- <span data-ttu-id="cc09a-143">オブジェクトのマッピングに含まれているすべての名前付きプロパティの識別子を取得します。</span><span class="sxs-lookup"><span data-stu-id="cc09a-143">Retrieve identifiers for all named properties that are included in the object's mapping.</span></span>
    
<span data-ttu-id="cc09a-144">名前付きプロパティは、通常、フォルダーおよびメッセージのメッセージストアプロバイダーによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="cc09a-144">Named properties are typically used by message store providers for folders and messages.</span></span> <span data-ttu-id="cc09a-145">メッセージングユーザーやプロファイルセクションなど、他のオブジェクトは、名前とプロパティ識別子との関連付けをサポートしていない場合があり、 **getidsfromnames**から MAPI_E_NO_SUPPORT を返す場合があります。</span><span class="sxs-lookup"><span data-stu-id="cc09a-145">Other objects, such as messaging users and profile sections, might not support the association of names to property identifiers and might return MAPI_E_NO_SUPPORT from **GetIDsFromNames**.</span></span>
  
<span data-ttu-id="cc09a-146">特定の名前の識別子を返すエラーがある場合、 **getidsfromnames**は MAPI_W_ERRORS_RETURNED を返し、プロパティタグ配列エントリのプロパティの型を**PT_ERROR**に対応するプロパティタグ配列エントリに設定し、識別子を0に設定します。</span><span class="sxs-lookup"><span data-stu-id="cc09a-146">If there is an error that returns an identifier for a particular name, **GetIDsFromNames** returns MAPI_W_ERRORS_RETURNED and sets the property type in the property tag array entry that corresponds to the name to **PT_ERROR** and the identifier to zero.</span></span> 
  
<span data-ttu-id="cc09a-147">名前から識別子へのマッピングは、オブジェクトの**PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) プロパティによって表されます。</span><span class="sxs-lookup"><span data-stu-id="cc09a-147">Name-to-identifier mapping is represented by an object's **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) property.</span></span> <span data-ttu-id="cc09a-148">**PR_MAPPING_SIGNATURE**には、オブジェクトを処理するサービスプロバイダーを示す[MAPIUID](mapiuid.md)構造が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cc09a-148">**PR_MAPPING_SIGNATURE** contains a [MAPIUID](mapiuid.md) structure that indicates the service provider responsible for the object.</span></span> <span data-ttu-id="cc09a-149">2つのオブジェクトの**PR_MAPPING_SIGNATURE**プロパティが同じ場合は、これらのオブジェクトが同じ名前と識別子のマッピングを使用することを前提としています。</span><span class="sxs-lookup"><span data-stu-id="cc09a-149">If the **PR_MAPPING_SIGNATURE** property is the same for two objects, assume that these objects use the same name-to-identifier mapping.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="cc09a-150">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="cc09a-150">Notes to implementers</span></span>

<span data-ttu-id="cc09a-151">_lpppropnames_パラメーターによって指定されたプロパティタグ配列で返される識別子は、0x8000 ~ 0xFFFE の範囲内にある必要があります。</span><span class="sxs-lookup"><span data-stu-id="cc09a-151">The identifiers that you pass back in the property tag array pointed to by the  _lppPropNames_ parameter must be in the 0x8000 to 0xFFFE range.</span></span> <span data-ttu-id="cc09a-152">この配列のエントリは、 _lpppropnames_で指定されたプロパティ名配列で渡された名前と同じ順序にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cc09a-152">The entries in this array must be in the same order as the names passed in the property name array pointed to by  _lppPropNames_.</span></span> 
  
<span data-ttu-id="cc09a-153">コンテナーで名前付きプロパティをサポートする場合は、コンテナー内のすべてのオブジェクトに同じ名前と識別子のマッピングを使用します (つまり、メッセージストア内の各フォルダーまたはフォルダー内の各メッセージに対して異なるマッピングを使用しません)。</span><span class="sxs-lookup"><span data-stu-id="cc09a-153">If you support named properties on a container, use the same name-to-identifier mapping for all objects in your container (that is, do not use a different mapping for each folder in your message store or each message in your folder).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="cc09a-154">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="cc09a-154">Notes to callers</span></span>

<span data-ttu-id="cc09a-155">_lppproptags_によって参照されるプロパティタグの配列で返される識別子のプロパティの種類は**PT_UNSPECIFIED**に設定されているため、 [imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出して正確な型を取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cc09a-155">Because the property types for the returned identifiers in the property tag array pointed to by  _lppPropTags_ are set to **PT_UNSPECIFIED**, you will have to call the [IMAPIProp::SetProps](imapiprop-setprops.md) method to retrieve the accurate types.</span></span> 
  
<span data-ttu-id="cc09a-156">名前付きプロパティを持つオブジェクトを移動またはコピーするときに、source オブジェクトと destination オブジェクトのマッピングシグネチャがそれぞれの**PR_MAPPING_SIGNATURE**プロパティの値で示されている場合は、これらの操作の間に名前を保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cc09a-156">If you move or copy objects with named properties, and the source and destination objects have different mapping signatures as indicated by the values of their **PR_MAPPING_SIGNATURE** properties, you must preserve the names during these operations.</span></span> <span data-ttu-id="cc09a-157">プロパティ名を保持するには、対応するプロパティ識別子を、対象のオブジェクトの名前から識別子へのマッピングと一致するように調整します。</span><span class="sxs-lookup"><span data-stu-id="cc09a-157">To preserve property names, adjust the corresponding property identifiers to match the name-to-identifier mapping of the destination object.</span></span> 
  
<span data-ttu-id="cc09a-158">一部のオブジェクトには、名前を付けることができるプロパティ識別子の数に制限があります。</span><span class="sxs-lookup"><span data-stu-id="cc09a-158">Some objects have a limit as to the number of property identifiers they can name.</span></span> <span data-ttu-id="cc09a-159">**getidsfromnames**を呼び出すとこの制限を超えると、メソッドは MAPI_E_TOO_BIG を返します。</span><span class="sxs-lookup"><span data-stu-id="cc09a-159">If a call to **GetIDsFromNames** causes this limit to be exceeded, the method returns MAPI_E_TOO_BIG.</span></span> <span data-ttu-id="cc09a-160">この場合は、識別子でクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="cc09a-160">In this case, query by identifier.</span></span> 
  
<span data-ttu-id="cc09a-161">詳細については、「 [MAPI の名前付きプロパティ](mapi-named-properties.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cc09a-161">For more information, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cc09a-162">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="cc09a-162">MFCMAPI reference</span></span>

<span data-ttu-id="cc09a-163">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cc09a-163">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cc09a-164">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="cc09a-164">**File**</span></span>|<span data-ttu-id="cc09a-165">**関数**</span><span class="sxs-lookup"><span data-stu-id="cc09a-165">**Function**</span></span>|<span data-ttu-id="cc09a-166">**コメント**</span><span class="sxs-lookup"><span data-stu-id="cc09a-166">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cc09a-167">SingleMAPIPropListCtrl</span><span class="sxs-lookup"><span data-stu-id="cc09a-167">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="cc09a-168">CSingleMAPIPropListCtrl:: findallnamedpropsused</span><span class="sxs-lookup"><span data-stu-id="cc09a-168">CSingleMAPIPropListCtrl::FindAllNamedPropsUsed</span></span>  <br/> |<span data-ttu-id="cc09a-169">mfcmapi は、 **imapiprop:: getidsfromnames**メソッドを使用して、マップされているすべての名前付きプロパティのプロパティタグを取得します。</span><span class="sxs-lookup"><span data-stu-id="cc09a-169">MFCMAPI uses the **IMAPIProp::GetIDsFromNames** method to obtain property tags for all named properties that have been mapped.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cc09a-170">関連項目</span><span class="sxs-lookup"><span data-stu-id="cc09a-170">See also</span></span>



[<span data-ttu-id="cc09a-171">IMAPIProp::GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="cc09a-171">IMAPIProp::GetNamesFromIDs</span></span>](imapiprop-getnamesfromids.md)
  
[<span data-ttu-id="cc09a-172">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="cc09a-172">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="cc09a-173">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="cc09a-173">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="cc09a-174">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="cc09a-174">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="cc09a-175">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cc09a-175">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


<span data-ttu-id="cc09a-176">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="cc09a-176">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="cc09a-177">MAPI ���O�t���v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cc09a-177">MAPI Named Properties</span></span>](mapi-named-properties.md)
  
[<span data-ttu-id="cc09a-178">エラー処理にマクロを使用する</span><span class="sxs-lookup"><span data-stu-id="cc09a-178">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

