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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7f7c243995c633389ab8fa80a26dddd152347276
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565362"
---
# <a name="imapipropgetidsfromnames"></a><span data-ttu-id="61f9c-103">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="61f9c-103">IMAPIProp::GetIDsFromNames</span></span>

  
  
<span data-ttu-id="61f9c-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61f9c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61f9c-105">1 つまたは複数のプロパティ名に対応するプロパティの識別子を提供します。</span><span class="sxs-lookup"><span data-stu-id="61f9c-105">Provides the property identifiers that correspond to one or more property names.</span></span>
  
```cpp
HRESULT GetIDsFromNames(
  ULONG cPropNames,
  LPMAPINAMEID FAR * lppPropNames,
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTags
);
```

## <a name="parameters"></a><span data-ttu-id="61f9c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="61f9c-106">Parameters</span></span>

 <span data-ttu-id="61f9c-107">_cPropNames_</span><span class="sxs-lookup"><span data-stu-id="61f9c-107">_cPropNames_</span></span>
  
> <span data-ttu-id="61f9c-108">[in]_LppPropNames_パラメーターで指定されたプロパティ名の数。</span><span class="sxs-lookup"><span data-stu-id="61f9c-108">[in] The count of property names pointed to by the  _lppPropNames_ parameter.</span></span> <span data-ttu-id="61f9c-109">_LppPropNames_が NULL の場合は、 _cPropNames_パラメーターは 0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="61f9c-109">If  _lppPropNames_ is NULL, the  _cPropNames_ parameter must be 0.</span></span> 
    
 <span data-ttu-id="61f9c-110">_lppPropNames_</span><span class="sxs-lookup"><span data-stu-id="61f9c-110">_lppPropNames_</span></span>
  
> <span data-ttu-id="61f9c-111">[in]プロパティ名、または NULL の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="61f9c-111">[in] A pointer to an array of property names, or NULL.</span></span> <span data-ttu-id="61f9c-112">パラメーターに NULL は、オブジェクトに情報があるについては、すべてのプロパティ セットのすべてのプロパティ名のプロパティの識別子を要求します。</span><span class="sxs-lookup"><span data-stu-id="61f9c-112">Passing NULL requests property identifiers for all property names in all property sets about which the object has information.</span></span> <span data-ttu-id="61f9c-113">_LppPropNames_パラメーターには NULL 必要がありますできません_ulFlags_パラメーターで、タグのフラグが設定されている場合。</span><span class="sxs-lookup"><span data-stu-id="61f9c-113">The  _lppPropNames_ parameter must not be NULL if the MAPI_CREATE flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="61f9c-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="61f9c-114">_ulFlags_</span></span>
  
> <span data-ttu-id="61f9c-115">[in]プロパティ識別子が返される方法を示すフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="61f9c-115">[in] A bitmask of flags that indicates how the property identifiers should be returned.</span></span> <span data-ttu-id="61f9c-116">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="61f9c-116">The following flag can be set:</span></span>
    
<span data-ttu-id="61f9c-117">タグ</span><span class="sxs-lookup"><span data-stu-id="61f9c-117">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="61f9c-118">プロパティの識別子では、1 つがまだ割り当てられていない場合、 _lppPropNames_で指定されたプロパティ名の配列に含まれている名前の 1 つ以上が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="61f9c-118">Assigns a property identifier, if one has not yet been assigned, to one or more of the names included in the property name array pointed to by  _lppPropNames_.</span></span> <span data-ttu-id="61f9c-119">このフラグは、名前の識別子をマッピング テーブルで内部的に id を登録します。</span><span class="sxs-lookup"><span data-stu-id="61f9c-119">This flag internally registers the identifier in the name-to-identifier mapping table.</span></span>
    
 <span data-ttu-id="61f9c-120">_lppPropTags_</span><span class="sxs-lookup"><span data-stu-id="61f9c-120">_lppPropTags_</span></span>
  
> <span data-ttu-id="61f9c-121">[out]既存または新たに割り当てられたプロパティの識別子を含むプロパティ タグの配列へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="61f9c-121">[out] A pointer to a pointer to an array of property tags that contains existing or newly assigned property identifiers.</span></span> <span data-ttu-id="61f9c-122">この配列内のプロパティ タグのプロパティの型は、 **PT_UNSPECIFIED**に設定されます。</span><span class="sxs-lookup"><span data-stu-id="61f9c-122">The property types for the property tags in this array are set to **PT_UNSPECIFIED**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="61f9c-123">�߂�l</span><span class="sxs-lookup"><span data-stu-id="61f9c-123">Return value</span></span>

<span data-ttu-id="61f9c-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="61f9c-124">S_OK</span></span> 
  
> <span data-ttu-id="61f9c-125">指定したプロパティ名の識別子が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="61f9c-125">The identifiers for the specified property names were successfully returned.</span></span>
    
<span data-ttu-id="61f9c-126">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="61f9c-126">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="61f9c-127">オブジェクトは、名前付きプロパティをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="61f9c-127">The object does not support named properties.</span></span>
    
<span data-ttu-id="61f9c-128">MAPI_E_NOT_ENOUGH_MEMORY</span><span class="sxs-lookup"><span data-stu-id="61f9c-128">MAPI_E_NOT_ENOUGH_MEMORY</span></span> 
  
> <span data-ttu-id="61f9c-129">メモリ不足のためでは、識別子を取得できませんでした。</span><span class="sxs-lookup"><span data-stu-id="61f9c-129">Insufficient memory was available to retrieve the identifiers.</span></span>
    
<span data-ttu-id="61f9c-130">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="61f9c-130">MAPI_E_TOO_BIG</span></span> 
  
> <span data-ttu-id="61f9c-131">返される多くのプロパティ タグが必要なために、操作を実行できません。</span><span class="sxs-lookup"><span data-stu-id="61f9c-131">The operation cannot be performed because it requires too many property tags to be returned.</span></span>
    
<span data-ttu-id="61f9c-132">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="61f9c-132">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="61f9c-133">呼び出しは完了しましたが、1 つまたは複数のプロパティの識別子は返されませんでした。</span><span class="sxs-lookup"><span data-stu-id="61f9c-133">The call succeeded overall, but one or more property identifiers could not be returned.</span></span> <span data-ttu-id="61f9c-134">使用できないプロパティごとに対応するプロパティの型は、 **PT_ERROR**とその id を 0 に設定されています。</span><span class="sxs-lookup"><span data-stu-id="61f9c-134">The corresponding property type for each unavailable property is set to **PT_ERROR** and its identifier to zero.</span></span> <span data-ttu-id="61f9c-135">この警告が返されると、その成功と呼び出しを処理します。</span><span class="sxs-lookup"><span data-stu-id="61f9c-135">When this warning is returned, handle the call as successful.</span></span> <span data-ttu-id="61f9c-136">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="61f9c-136">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="61f9c-137">[エラー処理のためのマクロを使用する](using-macros-for-error-handling.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="61f9c-137">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="61f9c-138">注釈</span><span class="sxs-lookup"><span data-stu-id="61f9c-138">Remarks</span></span>

<span data-ttu-id="61f9c-139">**IMAPIProp::GetIDsFromNames**メソッドは、1 つまたは複数の名前付きプロパティのプロパティの識別子を保持するプロパティ タグの配列を取得します。</span><span class="sxs-lookup"><span data-stu-id="61f9c-139">The **IMAPIProp::GetIDsFromNames** method retrieves an array of property tags that hold the property identifiers for one or more named properties.</span></span> <span data-ttu-id="61f9c-140">**IMAPIProp::GetIDsFromNames**は、次の操作を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="61f9c-140">**IMAPIProp::GetIDsFromNames** can be called to do the following:</span></span> 
  
- <span data-ttu-id="61f9c-141">新しい名前の識別子を作成します。</span><span class="sxs-lookup"><span data-stu-id="61f9c-141">Create identifiers for new names.</span></span>
    
- <span data-ttu-id="61f9c-142">特定の名前の識別子を取得します。</span><span class="sxs-lookup"><span data-stu-id="61f9c-142">Retrieve identifiers for specific names.</span></span>
    
- <span data-ttu-id="61f9c-143">オブジェクトのマッピングに含まれるすべての名前付きプロパティの識別子を取得します。</span><span class="sxs-lookup"><span data-stu-id="61f9c-143">Retrieve identifiers for all named properties that are included in the object's mapping.</span></span>
    
<span data-ttu-id="61f9c-144">名前付きプロパティは、通常、フォルダーやメッセージのメッセージ ストア プロバイダーが使用します。</span><span class="sxs-lookup"><span data-stu-id="61f9c-144">Named properties are typically used by message store providers for folders and messages.</span></span> <span data-ttu-id="61f9c-145">メッセージングのユーザーとプロファイルのセクションなど、他のオブジェクトは、プロパティの識別子を名前との関連付けをサポートしていない可能性があり、 **GetIDsFromNames**から MAPI_E_NO_SUPPORT を返すことがあります。</span><span class="sxs-lookup"><span data-stu-id="61f9c-145">Other objects, such as messaging users and profile sections, might not support the association of names to property identifiers and might return MAPI_E_NO_SUPPORT from **GetIDsFromNames**.</span></span>
  
<span data-ttu-id="61f9c-146">エラーを特定の名前の識別子を返す場合は、 **GetIDsFromNames** MAPI_W_ERRORS_RETURNED を返し**PT_ERROR**と id を 0 にする名前に対応するプロパティ タグ配列のエントリのプロパティの型を設定します。</span><span class="sxs-lookup"><span data-stu-id="61f9c-146">If there is an error that returns an identifier for a particular name, **GetIDsFromNames** returns MAPI_W_ERRORS_RETURNED and sets the property type in the property tag array entry that corresponds to the name to **PT_ERROR** and the identifier to zero.</span></span> 
  
<span data-ttu-id="61f9c-147">識別子に名前のマッピングは、オブジェクトの**PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) で表されます。</span><span class="sxs-lookup"><span data-stu-id="61f9c-147">Name-to-identifier mapping is represented by an object's **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) property.</span></span> <span data-ttu-id="61f9c-148">**PR_MAPPING_SIGNATURE**には、オブジェクトを担当するサービス プロバイダーを指定する[MAPIUID](mapiuid.md)構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="61f9c-148">**PR_MAPPING_SIGNATURE** contains a [MAPIUID](mapiuid.md) structure that indicates the service provider responsible for the object.</span></span> <span data-ttu-id="61f9c-149">**PR_MAPPING_SIGNATURE**プロパティ、2 つのオブジェクトに対して同じである場合は、これらのオブジェクトが同じ名前の識別子をマッピングを使用することを想定しています。</span><span class="sxs-lookup"><span data-stu-id="61f9c-149">If the **PR_MAPPING_SIGNATURE** property is the same for two objects, assume that these objects use the same name-to-identifier mapping.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="61f9c-150">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="61f9c-150">Notes to implementers</span></span>

<span data-ttu-id="61f9c-151">_LppPropNames_パラメーターで指定されたプロパティ タグ配列に渡された識別子は、0x8000 を 0 xfffe の範囲でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="61f9c-151">The identifiers that you pass back in the property tag array pointed to by the  _lppPropNames_ parameter must be in the 0x8000 to 0xFFFE range.</span></span> <span data-ttu-id="61f9c-152">この配列のエントリ必要があるプロパティ名の配列に渡された名前と同じ順序で指す_lppPropNames_です。</span><span class="sxs-lookup"><span data-stu-id="61f9c-152">The entries in this array must be in the same order as the names passed in the property name array pointed to by  _lppPropNames_.</span></span> 
  
<span data-ttu-id="61f9c-153">コンテナーの名前付きプロパティをサポートする場合は、同じ名前の識別子にマッピングを使用して、コンテナー内のすべてのオブジェクト (つまり、マッピングを使用しない、別のメッセージ ストア内の各フォルダーまたはフォルダー内の各メッセージの)。</span><span class="sxs-lookup"><span data-stu-id="61f9c-153">If you support named properties on a container, use the same name-to-identifier mapping for all objects in your container (that is, do not use a different mapping for each folder in your message store or each message in your folder).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="61f9c-154">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="61f9c-154">Notes to callers</span></span>

<span data-ttu-id="61f9c-155">_LppPropTags_で指定されたプロパティ タグ配列で返される識別子のプロパティの型は、 **PT_UNSPECIFIED**に設定されているためには、正確な型を取得するために[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="61f9c-155">Because the property types for the returned identifiers in the property tag array pointed to by  _lppPropTags_ are set to **PT_UNSPECIFIED**, you will have to call the [IMAPIProp::SetProps](imapiprop-setprops.md) method to retrieve the accurate types.</span></span> 
  
<span data-ttu-id="61f9c-156">移動する、または名前付きプロパティを持つオブジェクトのコピーと、ソースと変換先オブジェクトの**PR_MAPPING_SIGNATURE**プロパティの値で示される別のマッピングのシグネチャを持つ、これらの操作中に名前を保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="61f9c-156">If you move or copy objects with named properties, and the source and destination objects have different mapping signatures as indicated by the values of their **PR_MAPPING_SIGNATURE** properties, you must preserve the names during these operations.</span></span> <span data-ttu-id="61f9c-157">プロパティ名を保持するには、目的のオブジェクトの識別子に名前のマッピングに一致するように対応するプロパティの識別子を調整します。</span><span class="sxs-lookup"><span data-stu-id="61f9c-157">To preserve property names, adjust the corresponding property identifiers to match the name-to-identifier mapping of the destination object.</span></span> 
  
<span data-ttu-id="61f9c-158">いくつかのオブジェクトには、プロパティ識別子の名前を数の制限があります。</span><span class="sxs-lookup"><span data-stu-id="61f9c-158">Some objects have a limit as to the number of property identifiers they can name.</span></span> <span data-ttu-id="61f9c-159">**GetIDsFromNames**への呼び出しでは、この制限を越えるが発生する場合は、MAPI_E_TOO_BIG を返します。</span><span class="sxs-lookup"><span data-stu-id="61f9c-159">If a call to **GetIDsFromNames** causes this limit to be exceeded, the method returns MAPI_E_TOO_BIG.</span></span> <span data-ttu-id="61f9c-160">この例では、識別子によってクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="61f9c-160">In this case, query by identifier.</span></span> 
  
<span data-ttu-id="61f9c-161">詳細については、 [MAPI 名前付きプロパティ](mapi-named-properties.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="61f9c-161">For more information, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="61f9c-162">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="61f9c-162">MFCMAPI reference</span></span>

<span data-ttu-id="61f9c-163">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="61f9c-163">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="61f9c-164">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="61f9c-164">**File**</span></span>|<span data-ttu-id="61f9c-165">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="61f9c-165">**Function**</span></span>|<span data-ttu-id="61f9c-166">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="61f9c-166">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="61f9c-167">SingleMAPIPropListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="61f9c-167">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="61f9c-168">CSingleMAPIPropListCtrl::FindAllNamedPropsUsed</span><span class="sxs-lookup"><span data-stu-id="61f9c-168">CSingleMAPIPropListCtrl::FindAllNamedPropsUsed</span></span>  <br/> |<span data-ttu-id="61f9c-169">MFCMAPI では、 **IMAPIProp::GetIDsFromNames**メソッドを使用して、マップされたすべての名前付きプロパティのプロパティ タグを取得します。</span><span class="sxs-lookup"><span data-stu-id="61f9c-169">MFCMAPI uses the **IMAPIProp::GetIDsFromNames** method to obtain property tags for all named properties that have been mapped.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="61f9c-170">関連項目</span><span class="sxs-lookup"><span data-stu-id="61f9c-170">See also</span></span>



[<span data-ttu-id="61f9c-171">IMAPIProp::GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="61f9c-171">IMAPIProp::GetNamesFromIDs</span></span>](imapiprop-getnamesfromids.md)
  
[<span data-ttu-id="61f9c-172">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="61f9c-172">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="61f9c-173">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="61f9c-173">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="61f9c-174">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="61f9c-174">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="61f9c-175">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="61f9c-175">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


<span data-ttu-id="61f9c-176">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="61f9c-176">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="61f9c-177">MAPI ���O�t���v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="61f9c-177">MAPI Named Properties</span></span>](mapi-named-properties.md)
  
[<span data-ttu-id="61f9c-178">エラー処理のためのマクロの使用</span><span class="sxs-lookup"><span data-stu-id="61f9c-178">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

