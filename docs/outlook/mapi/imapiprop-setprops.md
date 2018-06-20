---
title: IMAPIPropSetProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.SetProps
api_type:
- COM
ms.assetid: 49f007c9-42e5-4391-8b83-988c9b0ebdba
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 304295e3ac77fb67ec5875620a7a269377b542c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800658"
---
# <a name="imapipropsetprops"></a><span data-ttu-id="86ccf-103">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="86ccf-103">IMAPIProp::SetProps</span></span>

  
  
<span data-ttu-id="86ccf-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="86ccf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="86ccf-105">1 つまたは複数のプロパティを更新します。</span><span class="sxs-lookup"><span data-stu-id="86ccf-105">Updates one or more properties.</span></span>
  
```cpp
HRESULT SetProps(
  ULONG cValues,
  LPSPropValue lpPropArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="86ccf-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="86ccf-106">Parameters</span></span>

 <span data-ttu-id="86ccf-107">_あう_</span><span class="sxs-lookup"><span data-stu-id="86ccf-107">_cValues_</span></span>
  
> <span data-ttu-id="86ccf-108">[in]_LpPropArray_パラメーターで指定されたプロパティ値の数。</span><span class="sxs-lookup"><span data-stu-id="86ccf-108">[in] The count of property values pointed to by the  _lpPropArray_ parameter.</span></span> <span data-ttu-id="86ccf-109">_あう_パラメーターを 0 にする必要がありますはできません。</span><span class="sxs-lookup"><span data-stu-id="86ccf-109">The  _cValues_ parameter must not be 0.</span></span> 
    
 <span data-ttu-id="86ccf-110">_lpPropArray_</span><span class="sxs-lookup"><span data-stu-id="86ccf-110">_lpPropArray_</span></span>
  
> <span data-ttu-id="86ccf-111">[in]更新するプロパティの値を含む[SPropValue](spropvalue.md)構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="86ccf-111">[in] A pointer to an array of [SPropValue](spropvalue.md) structures that contain property values to be updated.</span></span> 
    
 <span data-ttu-id="86ccf-112">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="86ccf-112">_lppProblems_</span></span>
  
> <span data-ttu-id="86ccf-113">[で [チェック アウト][SPropProblemArray](spropproblemarray.md)構造体へのポインターへのポインターの入力でそれ以外の場合、NULL の場合、エラー情報の必要性がないことを示します。</span><span class="sxs-lookup"><span data-stu-id="86ccf-113">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, indicating no need for error information.</span></span> <span data-ttu-id="86ccf-114">_LppProblems_が入力時に有効なポインターである場合は、 **SetProps**は、1 つまたは複数のプロパティを更新中にエラーに関する詳細な情報を返します。</span><span class="sxs-lookup"><span data-stu-id="86ccf-114">If  _lppProblems_ is a valid pointer on input, **SetProps** returns detailed information about errors in updating one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="86ccf-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="86ccf-115">Return value</span></span>

<span data-ttu-id="86ccf-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="86ccf-116">S_OK</span></span> 
  
> <span data-ttu-id="86ccf-117">プロパティは正常に更新されました。</span><span class="sxs-lookup"><span data-stu-id="86ccf-117">The properties were successfully updated.</span></span>
    
<span data-ttu-id="86ccf-118">次の値が返される、 **SPropProblemArray**構造体には戻り値としてではなく**SetProps**。</span><span class="sxs-lookup"><span data-stu-id="86ccf-118">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **SetProps**:</span></span>
  
<span data-ttu-id="86ccf-119">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="86ccf-119">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="86ccf-120">か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装は、Unicode だけをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="86ccf-120">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="86ccf-121">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="86ccf-121">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="86ccf-122">読み取り専用オブジェクトを担当するサービス ・ プロバイダーによって計算されるため、プロパティを更新できません。</span><span class="sxs-lookup"><span data-stu-id="86ccf-122">The property cannot be updated because it is read-only, computed by the service provider that is responsible for the object.</span></span>
    
<span data-ttu-id="86ccf-123">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="86ccf-123">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="86ccf-124">プロパティの型が正しくありません。</span><span class="sxs-lookup"><span data-stu-id="86ccf-124">The property type is invalid.</span></span>
    
<span data-ttu-id="86ccf-125">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="86ccf-125">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="86ccf-126">しようとは、読み取り専用オブジェクトを変更するか、ユーザーが十分なアクセス許可を持っているオブジェクトへのアクセスにしました。</span><span class="sxs-lookup"><span data-stu-id="86ccf-126">An attempt was made to modify a read-only object or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="86ccf-127">MAPI_E_NOT_ENOUGH_MEMORY</span><span class="sxs-lookup"><span data-stu-id="86ccf-127">MAPI_E_NOT_ENOUGH_MEMORY</span></span> 
  
> <span data-ttu-id="86ccf-128">プロパティは、リモート プロシージャ コール (RPC) のバッファー サイズを超えているために更新できません。</span><span class="sxs-lookup"><span data-stu-id="86ccf-128">The property cannot be updated because it is larger than the remote procedure call (RPC) buffer size.</span></span>
    
<span data-ttu-id="86ccf-129">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="86ccf-129">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="86ccf-130">プロパティの型は、呼び出し元の実装の型ではありません。</span><span class="sxs-lookup"><span data-stu-id="86ccf-130">The property type is not the type expected by the calling implementation.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="86ccf-131">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="86ccf-131">Notes to implementers</span></span>

<span data-ttu-id="86ccf-132">**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) のプロパティ タグと**PT_ERROR**の型を持つすべてのプロパティを無視します。</span><span class="sxs-lookup"><span data-stu-id="86ccf-132">Ignore the **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) property tag and all properties with a type of **PT_ERROR**.</span></span> <span data-ttu-id="86ccf-133">**SPropProblemArray**構造の変更や問題の報告は行いません。</span><span class="sxs-lookup"><span data-stu-id="86ccf-133">Do not make changes or report problems in the **SPropProblemArray** structure.</span></span> 
  
<span data-ttu-id="86ccf-134">**PT_OBJECT**の型のプロパティは、プロパティ値の配列に含まれている場合は、MAPI_E_INVALID_PARAMETER を返します。</span><span class="sxs-lookup"><span data-stu-id="86ccf-134">Return MAPI_E_INVALID_PARAMETER if a property of type **PT_OBJECT** is included in the property value array.</span></span> <span data-ttu-id="86ccf-135">複数値プロパティは、配列と**あう**メンバーに含まれている場合、このエラーは 0 に設定を返します。</span><span class="sxs-lookup"><span data-stu-id="86ccf-135">Also return this error if a multiple-value property is included in the array and its **cValues** member is set to 0.</span></span> 
  
<span data-ttu-id="86ccf-136">全体の呼び出しが成功すると、一部のプロパティの設定に問題がある場合は、S_OK を返すし、 _lppProblems_パラメーターが指す**SPropProblemArray**構造体の適切なエントリで、問題に関する情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="86ccf-136">If the call succeeds overall but there are problems with setting some of the properties, return S_OK and put information about the problems in the appropriate entry of the **SPropProblemArray** structure that the  _lppProblems_ parameter points to.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="86ccf-137">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="86ccf-137">Notes to callers</span></span>

<span data-ttu-id="86ccf-138">サービス プロバイダーによって指定されたプロパティの識別子を使用していたよりも、別の種類を含むプロパティ タグを渡すことによってプロパティの型を変更することがあります。</span><span class="sxs-lookup"><span data-stu-id="86ccf-138">Depending on the service provider, you might also be able to change the property type by passing a property tag that contains a different type than was previously used with a given property identifier.</span></span>
  
<span data-ttu-id="86ccf-139">オブジェクトでサポートされていないプロパティのプロパティ タグを含めるし、 **SetProps**の実装では、新しいプロパティの作成、プロパティがオブジェクトに追加されます。</span><span class="sxs-lookup"><span data-stu-id="86ccf-139">If you include a property tag for a property that is unsupported by the object and the implementation of **SetProps** allows the creation of new properties, the property is added to the object.</span></span> <span data-ttu-id="86ccf-140">新しいプロパティのために使用されたプロパティの識別子が格納されている、以前の値は破棄されます。</span><span class="sxs-lookup"><span data-stu-id="86ccf-140">Any previous value stored with the property identifier that was used for the new property is discarded.</span></span> 
  
<span data-ttu-id="86ccf-141">S_OK の戻り値が正常に更新されたすべてのプロパティを保証していないことに注意します。</span><span class="sxs-lookup"><span data-stu-id="86ccf-141">Note that the S_OK return value does not guarantee that all of the properties were successfully updated.</span></span> <span data-ttu-id="86ccf-142">一部のプロバイダーは、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)や[IMAPIProp::GetProps](imapiprop-getprops.md)などのプロバイダーの介入が必要な呼び出しを受け取るまで、 **SetProps**呼び出しをキャッシュします。</span><span class="sxs-lookup"><span data-stu-id="86ccf-142">Some providers cache **SetProps** calls until they receive a call that requires provider intervention, such as [IMAPIProp::SaveChanges](imapiprop-savechanges.md) or [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span> <span data-ttu-id="86ccf-143">したがって、以降の呼び出しで**SetProps**の呼び出しに関連するエラー値を受け取ることが。</span><span class="sxs-lookup"><span data-stu-id="86ccf-143">Therefore, it is possible to receive error values that relate to the **SetProps** call with the later calls.</span></span> 
  
<span data-ttu-id="86ccf-144">**SetProps**には、S_OK が返された場合は、個々 のプロパティの更新に問題の_lppProblems_が指す**SPropProblemArray**の構造体を確認してください。</span><span class="sxs-lookup"><span data-stu-id="86ccf-144">If **SetProps** returns S_OK, check the **SPropProblemArray** structure pointed to by  _lppProblems_ for problems updating individual properties.</span></span> <span data-ttu-id="86ccf-145">**SetProps**がエラーを返した場合、プロパティの問題の配列をチェックすることはしません。</span><span class="sxs-lookup"><span data-stu-id="86ccf-145">If **SetProps** returns an error, do not check the property problem array.</span></span> <span data-ttu-id="86ccf-146">オブジェクトの[IMAPIProp::GetLastError](imapiprop-getlasterror.md)メソッドを呼び出す代わりに、します。</span><span class="sxs-lookup"><span data-stu-id="86ccf-146">Instead, call the object's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method.</span></span> 
  
<span data-ttu-id="86ccf-147">大きなプロパティを更新するとき**SetProps**は失敗し、MAPI_E_NOT_ENOUGH_MEMORY を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="86ccf-147">When updating large properties, **SetProps** can fail and return MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="86ccf-148">プロパティの最大サイズがないと、さまざまなオブジェクトは、さまざまな制限を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="86ccf-148">There is no maximum size for properties, and different objects can have different limits.</span></span> <span data-ttu-id="86ccf-149">大きな可能性のあるプロパティを扱う場合は、 **SetProps**がこのエラーの値を返す場合は、インターフェイス識別子として IID_IStream と[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出すように準備します。</span><span class="sxs-lookup"><span data-stu-id="86ccf-149">If you deal with potentially large properties, be prepared to call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with IID_IStream as the interface identifier if **SetProps** returns this error value.</span></span> 
  
<span data-ttu-id="86ccf-150">**SPropProblemArray**構造体を解放する[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="86ccf-150">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the **SPropProblemArray** structure.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="86ccf-151">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="86ccf-151">MFCMAPI reference</span></span>

<span data-ttu-id="86ccf-152">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="86ccf-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="86ccf-153">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="86ccf-153">**File**</span></span>|<span data-ttu-id="86ccf-154">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="86ccf-154">**Function**</span></span>|<span data-ttu-id="86ccf-155">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="86ccf-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="86ccf-156">PropertyEditor.cpp</span><span class="sxs-lookup"><span data-stu-id="86ccf-156">PropertyEditor.cpp</span></span>  <br/> |<span data-ttu-id="86ccf-157">CPropertyEditor::WriteSPropValueToObject</span><span class="sxs-lookup"><span data-stu-id="86ccf-157">CPropertyEditor::WriteSPropValueToObject</span></span>  <br/> |<span data-ttu-id="86ccf-158">MFCMAPI では、プロパティに書き込むオブジェクトのプロパティが編集された後に、 **IMAPIProp::SetProps**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="86ccf-158">MFCMAPI uses the **IMAPIProp::SetProps** method to write a property back to an object after the property has been edited.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="86ccf-159">関連項目</span><span class="sxs-lookup"><span data-stu-id="86ccf-159">See also</span></span>



[<span data-ttu-id="86ccf-160">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="86ccf-160">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="86ccf-161">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="86ccf-161">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="86ccf-162">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="86ccf-162">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="86ccf-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="86ccf-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="86ccf-164">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="86ccf-164">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="86ccf-165">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="86ccf-165">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="86ccf-166">SPropValue</span><span class="sxs-lookup"><span data-stu-id="86ccf-166">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="86ccf-167">IMAPIProp: IUnknown</span><span class="sxs-lookup"><span data-stu-id="86ccf-167">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)

