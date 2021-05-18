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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 87709f8a77471637d7652982669bcba93ca2e1dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412619"
---
# <a name="imapipropsetprops"></a><span data-ttu-id="bfeaa-103">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="bfeaa-103">IMAPIProp::SetProps</span></span>

  
  
<span data-ttu-id="bfeaa-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bfeaa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bfeaa-105">1 つ以上のプロパティを更新します。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-105">Updates one or more properties.</span></span>
  
```cpp
HRESULT SetProps(
  ULONG cValues,
  LPSPropValue lpPropArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="bfeaa-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bfeaa-106">Parameters</span></span>

 <span data-ttu-id="bfeaa-107">_cValues_</span><span class="sxs-lookup"><span data-stu-id="bfeaa-107">_cValues_</span></span>
  
> <span data-ttu-id="bfeaa-108">[in]  _lpPropArray_ パラメーターが指すプロパティ値の数。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-108">[in] The count of property values pointed to by the  _lpPropArray_ parameter.</span></span> <span data-ttu-id="bfeaa-109">_cValues パラメーター_ は 0 にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-109">The  _cValues_ parameter must not be 0.</span></span> 
    
 <span data-ttu-id="bfeaa-110">_lpPropArray_</span><span class="sxs-lookup"><span data-stu-id="bfeaa-110">_lpPropArray_</span></span>
  
> <span data-ttu-id="bfeaa-111">[in]更新するプロパティ値を含む [SPropValue](spropvalue.md) 構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-111">[in] A pointer to an array of [SPropValue](spropvalue.md) structures that contain property values to be updated.</span></span> 
    
 <span data-ttu-id="bfeaa-112">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="bfeaa-112">_lppProblems_</span></span>
  
> <span data-ttu-id="bfeaa-113">[in, out]入力時に [、SPropProblemArray](spropproblemarray.md) 構造体へのポインターを指すポインター。それ以外の場合は、エラー情報が不要であることを示す NULL。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-113">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, indicating no need for error information.</span></span> <span data-ttu-id="bfeaa-114">_lppProblems が_ 入力の有効なポインターである場合 **、SetProps** は 1 つ以上のプロパティを更新するエラーに関する詳細情報を返します。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-114">If  _lppProblems_ is a valid pointer on input, **SetProps** returns detailed information about errors in updating one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bfeaa-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="bfeaa-115">Return value</span></span>

<span data-ttu-id="bfeaa-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="bfeaa-116">S_OK</span></span> 
  
> <span data-ttu-id="bfeaa-117">プロパティが正常に更新されました。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-117">The properties were successfully updated.</span></span>
    
<span data-ttu-id="bfeaa-118">次の値は **、SPropProblemArray** 構造体で返されますが、SetProps の戻り値 **として返す値として返す必要があります**。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-118">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **SetProps**:</span></span>
  
<span data-ttu-id="bfeaa-119">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="bfeaa-119">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="bfeaa-120">このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定されていないMAPI_UNICODE実装が Unicode のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-120">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="bfeaa-121">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="bfeaa-121">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="bfeaa-122">プロパティは、オブジェクトを担当するサービス プロバイダーによって計算される読み取り専用のため、更新できません。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-122">The property cannot be updated because it is read-only, computed by the service provider that is responsible for the object.</span></span>
    
<span data-ttu-id="bfeaa-123">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="bfeaa-123">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="bfeaa-124">プロパティの種類が無効です。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-124">The property type is invalid.</span></span>
    
<span data-ttu-id="bfeaa-125">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="bfeaa-125">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="bfeaa-126">読み取り専用オブジェクトを変更しようとしたり、ユーザーのアクセス許可が不十分なオブジェクトにアクセスしようとしたりしました。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-126">An attempt was made to modify a read-only object or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="bfeaa-127">MAPI_E_NOT_ENOUGH_MEMORY</span><span class="sxs-lookup"><span data-stu-id="bfeaa-127">MAPI_E_NOT_ENOUGH_MEMORY</span></span> 
  
> <span data-ttu-id="bfeaa-128">リモート プロシージャ 呼び出し (RPC) バッファー サイズよりも大きいので、プロパティを更新できません。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-128">The property cannot be updated because it is larger than the remote procedure call (RPC) buffer size.</span></span>
    
<span data-ttu-id="bfeaa-129">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="bfeaa-129">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="bfeaa-130">プロパティの種類は、呼び出し元の実装で予期される型ではありません。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-130">The property type is not the type expected by the calling implementation.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="bfeaa-131">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="bfeaa-131">Notes to implementers</span></span>

<span data-ttu-id="bfeaa-132">プロパティ **タグPR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) プロパティ タグおよびプロパティの種類を持つすべてのプロパティを **無視** PT_ERROR。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-132">Ignore the **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) property tag and all properties with a type of **PT_ERROR**.</span></span> <span data-ttu-id="bfeaa-133">**SPropProblemArray** 構造体に変更を加え、問題を報告したりしない。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-133">Do not make changes or report problems in the **SPropProblemArray** structure.</span></span> 
  
<span data-ttu-id="bfeaa-134">プロパティMAPI_E_INVALID_PARAMETER値の配列 **に型の** プロパティPT_OBJECT含まれている場合は、この値を返します。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-134">Return MAPI_E_INVALID_PARAMETER if a property of type **PT_OBJECT** is included in the property value array.</span></span> <span data-ttu-id="bfeaa-135">配列に複数値のプロパティが含まれていて、その **cValues** メンバーが 0 に設定されている場合も、このエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-135">Also return this error if a multiple-value property is included in the array and its **cValues** member is set to 0.</span></span> 
  
<span data-ttu-id="bfeaa-136">呼び出しが全体的に成功したが、一部のプロパティの設定に問題がある場合は、S_OK を返し _、lppProblems_ パラメーターが示す **SPropProblemArray** 構造体の適切なエントリに問題に関する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-136">If the call succeeds overall but there are problems with setting some of the properties, return S_OK and put information about the problems in the appropriate entry of the **SPropProblemArray** structure that the  _lppProblems_ parameter points to.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="bfeaa-137">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="bfeaa-137">Notes to callers</span></span>

<span data-ttu-id="bfeaa-138">サービス プロバイダーによっては、特定のプロパティ識別子で以前に使用された型とは異なる型を含むプロパティ タグを渡して、プロパティの種類を変更できる場合があります。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-138">Depending on the service provider, you might also be able to change the property type by passing a property tag that contains a different type than was previously used with a given property identifier.</span></span>
  
<span data-ttu-id="bfeaa-139">オブジェクトでサポートされていないプロパティのプロパティ タグを含め **、SetProps** の実装によって新しいプロパティを作成できる場合、プロパティはオブジェクトに追加されます。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-139">If you include a property tag for a property that is unsupported by the object and the implementation of **SetProps** allows the creation of new properties, the property is added to the object.</span></span> <span data-ttu-id="bfeaa-140">新しいプロパティに使用されたプロパティ識別子と一緒に格納された以前の値は破棄されます。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-140">Any previous value stored with the property identifier that was used for the new property is discarded.</span></span> 
  
<span data-ttu-id="bfeaa-141">戻り値S_OK、すべてのプロパティが正常に更新されたことを保証するものではありません。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-141">Note that the S_OK return value does not guarantee that all of the properties were successfully updated.</span></span> <span data-ttu-id="bfeaa-142">一部のプロバイダーは [、IMAPIProp::SaveChanges](imapiprop-savechanges.md)や [IMAPIProp::GetProps](imapiprop-getprops.md)などのプロバイダーの介入を必要とする呼び出しを受信するまで **、SetProps** 呼び出しをキャッシュします。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-142">Some providers cache **SetProps** calls until they receive a call that requires provider intervention, such as [IMAPIProp::SaveChanges](imapiprop-savechanges.md) or [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span> <span data-ttu-id="bfeaa-143">したがって **、SetProps** 呼び出しに関連するエラー値を、後の呼び出しで受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-143">Therefore, it is possible to receive error values that relate to the **SetProps** call with the later calls.</span></span> 
  
<span data-ttu-id="bfeaa-144">**SetProps が** S_OKを返す場合は _、lppProblems_ が示す **SPropProblemArray** 構造体で、個々のプロパティの更新に関する問題を確認します。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-144">If **SetProps** returns S_OK, check the **SPropProblemArray** structure pointed to by  _lppProblems_ for problems updating individual properties.</span></span> <span data-ttu-id="bfeaa-145">**SetProps がエラー** を返す場合は、プロパティの問題の配列をチェックしない。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-145">If **SetProps** returns an error, do not check the property problem array.</span></span> <span data-ttu-id="bfeaa-146">代わりに、オブジェクトの [IMAPIProp::GetLastError メソッドを呼び出](imapiprop-getlasterror.md) します。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-146">Instead, call the object's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method.</span></span> 
  
<span data-ttu-id="bfeaa-147">大規模なプロパティを更新すると **、SetProps が** 失敗し、エラーが発生MAPI_E_NOT_ENOUGH_MEMORY。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-147">When updating large properties, **SetProps** can fail and return MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="bfeaa-148">プロパティの最大サイズはありません。また、オブジェクトによって制限が異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-148">There is no maximum size for properties, and different objects can have different limits.</span></span> <span data-ttu-id="bfeaa-149">潜在的に大きいプロパティを処理する場合は **、SetProps** がこのエラー値を返す場合、インターフェイス識別子として IID_IStream を使用して [IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出す準備をしてください。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-149">If you deal with potentially large properties, be prepared to call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with IID_IStream as the interface identifier if **SetProps** returns this error value.</span></span> 
  
<span data-ttu-id="bfeaa-150">[MAPIFreeBuffer 関数を呼び出](mapifreebuffer.md)して **、SPropProblemArray 構造体を解放** します。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-150">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the **SPropProblemArray** structure.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="bfeaa-151">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="bfeaa-151">MFCMAPI reference</span></span>

<span data-ttu-id="bfeaa-152">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bfeaa-153">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="bfeaa-153">**File**</span></span>|<span data-ttu-id="bfeaa-154">**関数**</span><span class="sxs-lookup"><span data-stu-id="bfeaa-154">**Function**</span></span>|<span data-ttu-id="bfeaa-155">**コメント**</span><span class="sxs-lookup"><span data-stu-id="bfeaa-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bfeaa-156">PropertyEditor.cpp</span><span class="sxs-lookup"><span data-stu-id="bfeaa-156">PropertyEditor.cpp</span></span>  <br/> |<span data-ttu-id="bfeaa-157">CPropertyEditor::WriteSPropValueToObject</span><span class="sxs-lookup"><span data-stu-id="bfeaa-157">CPropertyEditor::WriteSPropValueToObject</span></span>  <br/> |<span data-ttu-id="bfeaa-158">MFCMAPI は **IMAPIProp::SetProps** メソッドを使用して、プロパティの編集後にプロパティをオブジェクトに書き戻します。</span><span class="sxs-lookup"><span data-stu-id="bfeaa-158">MFCMAPI uses the **IMAPIProp::SetProps** method to write a property back to an object after the property has been edited.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bfeaa-159">関連項目</span><span class="sxs-lookup"><span data-stu-id="bfeaa-159">See also</span></span>



[<span data-ttu-id="bfeaa-160">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="bfeaa-160">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="bfeaa-161">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="bfeaa-161">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="bfeaa-162">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="bfeaa-162">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="bfeaa-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="bfeaa-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="bfeaa-164">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="bfeaa-164">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="bfeaa-165">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="bfeaa-165">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="bfeaa-166">SPropValue</span><span class="sxs-lookup"><span data-stu-id="bfeaa-166">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="bfeaa-167">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bfeaa-167">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)

