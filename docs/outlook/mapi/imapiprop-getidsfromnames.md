---
title: IMAPIPropGetIDsFromNames
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
# <a name="imapipropgetidsfromnames"></a><span data-ttu-id="4085a-103">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="4085a-103">IMAPIProp::GetIDsFromNames</span></span>

  
  
<span data-ttu-id="4085a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4085a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4085a-105">1 つ以上のプロパティ名に対応するプロパティ識別子を提供します。</span><span class="sxs-lookup"><span data-stu-id="4085a-105">Provides the property identifiers that correspond to one or more property names.</span></span>
  
```cpp
HRESULT GetIDsFromNames(
  ULONG cPropNames,
  LPMAPINAMEID FAR * lppPropNames,
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTags
);
```

## <a name="parameters"></a><span data-ttu-id="4085a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4085a-106">Parameters</span></span>

 <span data-ttu-id="4085a-107">_cPropNames_</span><span class="sxs-lookup"><span data-stu-id="4085a-107">_cPropNames_</span></span>
  
> <span data-ttu-id="4085a-108">[in]  _lppPropNames_ パラメーターが指すプロパティ名の数。</span><span class="sxs-lookup"><span data-stu-id="4085a-108">[in] The count of property names pointed to by the  _lppPropNames_ parameter.</span></span> <span data-ttu-id="4085a-109">_lppPropNames が_ NULL の場合 _、cPropNames_ パラメーターは 0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="4085a-109">If  _lppPropNames_ is NULL, the  _cPropNames_ parameter must be 0.</span></span> 
    
 <span data-ttu-id="4085a-110">_lppPropNames_</span><span class="sxs-lookup"><span data-stu-id="4085a-110">_lppPropNames_</span></span>
  
> <span data-ttu-id="4085a-111">[in]プロパティ名または NULL の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4085a-111">[in] A pointer to an array of property names, or NULL.</span></span> <span data-ttu-id="4085a-112">NULL を渡す場合は、オブジェクトが情報を持つすべてのプロパティ セットのすべてのプロパティ名のプロパティ識別子を要求します。</span><span class="sxs-lookup"><span data-stu-id="4085a-112">Passing NULL requests property identifiers for all property names in all property sets about which the object has information.</span></span> <span data-ttu-id="4085a-113">_ulFlags_ パラメーターにフラグを設定する場合 _、lppPropNames_ パラメーター MAPI_CREATE NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="4085a-113">The  _lppPropNames_ parameter must not be NULL if the MAPI_CREATE flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="4085a-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4085a-114">_ulFlags_</span></span>
  
> <span data-ttu-id="4085a-115">[in]プロパティ識別子を返す方法を示すフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="4085a-115">[in] A bitmask of flags that indicates how the property identifiers should be returned.</span></span> <span data-ttu-id="4085a-116">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="4085a-116">The following flag can be set:</span></span>
    
<span data-ttu-id="4085a-117">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="4085a-117">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="4085a-118">プロパティ識別子がまだ割り当てられていない場合は  _、lppPropNames_ によって指されるプロパティ名配列に含まれる 1 つ以上の名前に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="4085a-118">Assigns a property identifier, if one has not yet been assigned, to one or more of the names included in the property name array pointed to by  _lppPropNames_.</span></span> <span data-ttu-id="4085a-119">このフラグは、名前から識別子へのマッピング テーブルに識別子を内部的に登録します。</span><span class="sxs-lookup"><span data-stu-id="4085a-119">This flag internally registers the identifier in the name-to-identifier mapping table.</span></span>
    
 <span data-ttu-id="4085a-120">_lppPropTags_</span><span class="sxs-lookup"><span data-stu-id="4085a-120">_lppPropTags_</span></span>
  
> <span data-ttu-id="4085a-121">[out]既存のプロパティ識別子または新しく割り当てられたプロパティ識別子を含むプロパティ タグの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4085a-121">[out] A pointer to a pointer to an array of property tags that contains existing or newly assigned property identifiers.</span></span> <span data-ttu-id="4085a-122">この配列のプロパティ タグのプロパティの種類は、次の値 **にPT_UNSPECIFIED。**</span><span class="sxs-lookup"><span data-stu-id="4085a-122">The property types for the property tags in this array are set to **PT_UNSPECIFIED**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4085a-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="4085a-123">Return value</span></span>

<span data-ttu-id="4085a-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="4085a-124">S_OK</span></span> 
  
> <span data-ttu-id="4085a-125">指定したプロパティ名の識別子が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="4085a-125">The identifiers for the specified property names were successfully returned.</span></span>
    
<span data-ttu-id="4085a-126">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="4085a-126">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="4085a-127">オブジェクトは名前付きプロパティをサポートしていない。</span><span class="sxs-lookup"><span data-stu-id="4085a-127">The object does not support named properties.</span></span>
    
<span data-ttu-id="4085a-128">MAPI_E_NOT_ENOUGH_MEMORY</span><span class="sxs-lookup"><span data-stu-id="4085a-128">MAPI_E_NOT_ENOUGH_MEMORY</span></span> 
  
> <span data-ttu-id="4085a-129">識別子を取得するために使用できるメモリが不足しています。</span><span class="sxs-lookup"><span data-stu-id="4085a-129">Insufficient memory was available to retrieve the identifiers.</span></span>
    
<span data-ttu-id="4085a-130">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="4085a-130">MAPI_E_TOO_BIG</span></span> 
  
> <span data-ttu-id="4085a-131">返されるプロパティ タグが多すぎるため、操作を実行できません。</span><span class="sxs-lookup"><span data-stu-id="4085a-131">The operation cannot be performed because it requires too many property tags to be returned.</span></span>
    
<span data-ttu-id="4085a-132">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="4085a-132">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="4085a-133">呼び出しは全体的に成功しましたが、1 つ以上のプロパティ識別子を返す必要がありました。</span><span class="sxs-lookup"><span data-stu-id="4085a-133">The call succeeded overall, but one or more property identifiers could not be returned.</span></span> <span data-ttu-id="4085a-134">使用できない各プロパティの対応するプロパティの種類は、PT_ERROR **に設定** され、その識別子は 0 に設定されます。</span><span class="sxs-lookup"><span data-stu-id="4085a-134">The corresponding property type for each unavailable property is set to **PT_ERROR** and its identifier to zero.</span></span> <span data-ttu-id="4085a-135">この警告が返された場合は、呼び出しを成功として処理します。</span><span class="sxs-lookup"><span data-stu-id="4085a-135">When this warning is returned, handle the call as successful.</span></span> <span data-ttu-id="4085a-136">この警告をテストするには、次のマクロ **HR_FAILED** します。</span><span class="sxs-lookup"><span data-stu-id="4085a-136">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="4085a-137">「エラー [処理のためのマクロの使用」を参照してください](using-macros-for-error-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="4085a-137">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4085a-138">注釈</span><span class="sxs-lookup"><span data-stu-id="4085a-138">Remarks</span></span>

<span data-ttu-id="4085a-139">**IMAPIProp::GetIDsFromNames** メソッドは、1 つ以上の名前付きプロパティのプロパティ識別子を保持するプロパティ タグの配列を取得します。</span><span class="sxs-lookup"><span data-stu-id="4085a-139">The **IMAPIProp::GetIDsFromNames** method retrieves an array of property tags that hold the property identifiers for one or more named properties.</span></span> <span data-ttu-id="4085a-140">**IMAPIProp::GetIDsFromNames** を呼び出して、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="4085a-140">**IMAPIProp::GetIDsFromNames** can be called to do the following:</span></span> 
  
- <span data-ttu-id="4085a-141">新しい名前の識別子を作成します。</span><span class="sxs-lookup"><span data-stu-id="4085a-141">Create identifiers for new names.</span></span>
    
- <span data-ttu-id="4085a-142">特定の名前の識別子を取得します。</span><span class="sxs-lookup"><span data-stu-id="4085a-142">Retrieve identifiers for specific names.</span></span>
    
- <span data-ttu-id="4085a-143">オブジェクトのマッピングに含まれるすべての名前付きプロパティの識別子を取得します。</span><span class="sxs-lookup"><span data-stu-id="4085a-143">Retrieve identifiers for all named properties that are included in the object's mapping.</span></span>
    
<span data-ttu-id="4085a-144">名前付きプロパティは、通常、フォルダーとメッセージのメッセージ ストア プロバイダーによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="4085a-144">Named properties are typically used by message store providers for folders and messages.</span></span> <span data-ttu-id="4085a-145">メッセージング ユーザーやプロファイル セクションなどの他のオブジェクトは、名前とプロパティ識別子の関連付けをサポートしていない可能性があります **。GetIDsFromNames** から MAPI_E_NO_SUPPORTを返す場合があります。</span><span class="sxs-lookup"><span data-stu-id="4085a-145">Other objects, such as messaging users and profile sections, might not support the association of names to property identifiers and might return MAPI_E_NO_SUPPORT from **GetIDsFromNames**.</span></span>
  
<span data-ttu-id="4085a-146">特定の名前の識別子を返すエラーがある場合 **、GetIDsFromNames** は MAPI_W_ERRORS_RETURNED を返し、名前に対応するプロパティ タグ配列エントリのプロパティの種類を PT_ERROR に設定し、識別子を **0** に設定します。</span><span class="sxs-lookup"><span data-stu-id="4085a-146">If there is an error that returns an identifier for a particular name, **GetIDsFromNames** returns MAPI_W_ERRORS_RETURNED and sets the property type in the property tag array entry that corresponds to the name to **PT_ERROR** and the identifier to zero.</span></span> 
  
<span data-ttu-id="4085a-147">名前から識別子へのマッピングは、オブジェクトのプロパティ ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md) **)** PR_MAPPING_SIGNATUREプロパティで表されます。</span><span class="sxs-lookup"><span data-stu-id="4085a-147">Name-to-identifier mapping is represented by an object's **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) property.</span></span> <span data-ttu-id="4085a-148">**PR_MAPPING_SIGNATURE** には、オブジェクトを担当するサービス プロバイダーを示す [MAPIUID](mapiuid.md) 構造が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="4085a-148">**PR_MAPPING_SIGNATURE** contains a [MAPIUID](mapiuid.md) structure that indicates the service provider responsible for the object.</span></span> <span data-ttu-id="4085a-149">2 つの **PR_MAPPING_SIGNATURE** プロパティが同じ場合は、これらのオブジェクトが同じ名前から識別子へのマッピングを使用すると仮定します。</span><span class="sxs-lookup"><span data-stu-id="4085a-149">If the **PR_MAPPING_SIGNATURE** property is the same for two objects, assume that these objects use the same name-to-identifier mapping.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4085a-150">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="4085a-150">Notes to implementers</span></span>

<span data-ttu-id="4085a-151">_lppPropNames_ パラメーターが指すプロパティ タグ配列に戻す識別子は、0x8000から0xFFFEである必要があります。</span><span class="sxs-lookup"><span data-stu-id="4085a-151">The identifiers that you pass back in the property tag array pointed to by the  _lppPropNames_ parameter must be in the 0x8000 to 0xFFFE range.</span></span> <span data-ttu-id="4085a-152">この配列のエントリは  _、lppPropNames_ が指すプロパティ名配列で渡される名前と同じ順序である必要があります。</span><span class="sxs-lookup"><span data-stu-id="4085a-152">The entries in this array must be in the same order as the names passed in the property name array pointed to by  _lppPropNames_.</span></span> 
  
<span data-ttu-id="4085a-153">コンテナーで名前付きプロパティをサポートする場合は、コンテナー内のすべてのオブジェクトに対して同じ名前から識別子へのマッピングを使用します (つまり、メッセージ ストア内のフォルダーまたはフォルダー内の各メッセージに対して異なるマッピングを使用しない)。</span><span class="sxs-lookup"><span data-stu-id="4085a-153">If you support named properties on a container, use the same name-to-identifier mapping for all objects in your container (that is, do not use a different mapping for each folder in your message store or each message in your folder).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="4085a-154">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="4085a-154">Notes to callers</span></span>

<span data-ttu-id="4085a-155">_lppPropTags_ が指すプロパティ タグ配列内の返される識別子のプロパティ型は **PT_UNSPECIFIED** に設定されますので、正確な型を取得するには [、IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="4085a-155">Because the property types for the returned identifiers in the property tag array pointed to by  _lppPropTags_ are set to **PT_UNSPECIFIED**, you will have to call the [IMAPIProp::SetProps](imapiprop-setprops.md) method to retrieve the accurate types.</span></span> 
  
<span data-ttu-id="4085a-156">名前付きプロパティを持つオブジェクトを移動またはコピーし、ソース オブジェクトと移動先オブジェクトのマッピングシグネチャが **異なる場合は、PR_MAPPING_SIGNATURE** プロパティの値で示されるマッピング署名が異なる場合は、これらの操作中に名前を保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4085a-156">If you move or copy objects with named properties, and the source and destination objects have different mapping signatures as indicated by the values of their **PR_MAPPING_SIGNATURE** properties, you must preserve the names during these operations.</span></span> <span data-ttu-id="4085a-157">プロパティ名を保持するには、対応するプロパティ識別子を、コピー先オブジェクトの名前と識別子のマッピングと一致する値に調整します。</span><span class="sxs-lookup"><span data-stu-id="4085a-157">To preserve property names, adjust the corresponding property identifiers to match the name-to-identifier mapping of the destination object.</span></span> 
  
<span data-ttu-id="4085a-158">一部のオブジェクトには、名前を付けできるプロパティ識別子の数に制限があります。</span><span class="sxs-lookup"><span data-stu-id="4085a-158">Some objects have a limit as to the number of property identifiers they can name.</span></span> <span data-ttu-id="4085a-159">**GetIDsFromNames** の呼び出しによってこの制限を超えた場合、メソッドは値を返MAPI_E_TOO_BIG。</span><span class="sxs-lookup"><span data-stu-id="4085a-159">If a call to **GetIDsFromNames** causes this limit to be exceeded, the method returns MAPI_E_TOO_BIG.</span></span> <span data-ttu-id="4085a-160">この場合、識別子によるクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="4085a-160">In this case, query by identifier.</span></span> 
  
<span data-ttu-id="4085a-161">詳細については、「MAPI 名前付き [プロパティ」を参照してください](mapi-named-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="4085a-161">For more information, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4085a-162">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="4085a-162">MFCMAPI reference</span></span>

<span data-ttu-id="4085a-163">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4085a-163">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4085a-164">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="4085a-164">**File**</span></span>|<span data-ttu-id="4085a-165">**関数**</span><span class="sxs-lookup"><span data-stu-id="4085a-165">**Function**</span></span>|<span data-ttu-id="4085a-166">**コメント**</span><span class="sxs-lookup"><span data-stu-id="4085a-166">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4085a-167">SingleMAPIPropListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="4085a-167">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="4085a-168">CSingleMAPIPropListCtrl::FindAllNamedPropsUsed</span><span class="sxs-lookup"><span data-stu-id="4085a-168">CSingleMAPIPropListCtrl::FindAllNamedPropsUsed</span></span>  <br/> |<span data-ttu-id="4085a-169">MFCMAPI は **IMAPIProp::GetIDsFromNames** メソッドを使用して、マップされた名前付きプロパティのプロパティ タグを取得します。</span><span class="sxs-lookup"><span data-stu-id="4085a-169">MFCMAPI uses the **IMAPIProp::GetIDsFromNames** method to obtain property tags for all named properties that have been mapped.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4085a-170">関連項目</span><span class="sxs-lookup"><span data-stu-id="4085a-170">See also</span></span>



[<span data-ttu-id="4085a-171">IMAPIProp::GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="4085a-171">IMAPIProp::GetNamesFromIDs</span></span>](imapiprop-getnamesfromids.md)
  
[<span data-ttu-id="4085a-172">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="4085a-172">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="4085a-173">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="4085a-173">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="4085a-174">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="4085a-174">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="4085a-175">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4085a-175">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


<span data-ttu-id="4085a-176">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="4085a-176">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="4085a-177">MAPI ���O�t���v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="4085a-177">MAPI Named Properties</span></span>](mapi-named-properties.md)
  
[<span data-ttu-id="4085a-178">エラー処理にマクロを使用する</span><span class="sxs-lookup"><span data-stu-id="4085a-178">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

