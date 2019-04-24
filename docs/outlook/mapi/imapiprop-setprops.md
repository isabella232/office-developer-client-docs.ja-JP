---
title: imapipropsetprops
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 87709f8a77471637d7652982669bcba93ca2e1dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341014"
---
# <a name="imapipropsetprops"></a><span data-ttu-id="5e9d7-103">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="5e9d7-103">IMAPIProp::SetProps</span></span>

  
  
<span data-ttu-id="5e9d7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e9d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e9d7-105">1つまたは複数のプロパティを更新します。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-105">Updates one or more properties.</span></span>
  
```cpp
HRESULT SetProps(
  ULONG cValues,
  LPSPropValue lpPropArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="5e9d7-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e9d7-106">Parameters</span></span>

 <span data-ttu-id="5e9d7-107">_cvalues_</span><span class="sxs-lookup"><span data-stu-id="5e9d7-107">_cValues_</span></span>
  
> <span data-ttu-id="5e9d7-108">順番_lpproparray_パラメーターが指すプロパティ値の数。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-108">[in] The count of property values pointed to by the  _lpPropArray_ parameter.</span></span> <span data-ttu-id="5e9d7-109">_cvalues_パラメーターは0以外でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-109">The  _cValues_ parameter must not be 0.</span></span> 
    
 <span data-ttu-id="5e9d7-110">_lpproparray_</span><span class="sxs-lookup"><span data-stu-id="5e9d7-110">_lpPropArray_</span></span>
  
> <span data-ttu-id="5e9d7-111">順番更新するプロパティ値を含む[spropvalue](spropvalue.md)構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-111">[in] A pointer to an array of [SPropValue](spropvalue.md) structures that contain property values to be updated.</span></span> 
    
 <span data-ttu-id="5e9d7-112">_lppproblems 問題_</span><span class="sxs-lookup"><span data-stu-id="5e9d7-112">_lppProblems_</span></span>
  
> <span data-ttu-id="5e9d7-113">[入力]input の場合は、 [spropの配列](spropproblemarray.md)構造体へのポインターへのポインターを返します。それ以外の場合、エラー情報を必要としないことを示す NULL。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-113">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, indicating no need for error information.</span></span> <span data-ttu-id="5e9d7-114">_lppproblems_が入力の有効なポインターである場合、 **setprops**は、1つ以上のプロパティの更新中に発生したエラーに関する詳細情報を返します。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-114">If  _lppProblems_ is a valid pointer on input, **SetProps** returns detailed information about errors in updating one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5e9d7-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="5e9d7-115">Return value</span></span>

<span data-ttu-id="5e9d7-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="5e9d7-116">S_OK</span></span> 
  
> <span data-ttu-id="5e9d7-117">プロパティが正常に更新されました。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-117">The properties were successfully updated.</span></span>
    
<span data-ttu-id="5e9d7-118">次の値は、 **spropの配列**構造で返すことができますが、 **setprops**の戻り値としては返されません。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-118">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **SetProps**:</span></span>
  
<span data-ttu-id="5e9d7-119">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="5e9d7-119">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="5e9d7-120">MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-120">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="5e9d7-121">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="5e9d7-121">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="5e9d7-122">プロパティは読み取り専用で、オブジェクトを処理するサービスプロバイダーによって計算されるため、更新できません。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-122">The property cannot be updated because it is read-only, computed by the service provider that is responsible for the object.</span></span>
    
<span data-ttu-id="5e9d7-123">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="5e9d7-123">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="5e9d7-124">プロパティの種類が無効です。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-124">The property type is invalid.</span></span>
    
<span data-ttu-id="5e9d7-125">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="5e9d7-125">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="5e9d7-126">読み取り専用オブジェクトを変更しようとしたか、またはユーザーが十分なアクセス許可を持っていないオブジェクトにアクセスしようとしました。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-126">An attempt was made to modify a read-only object or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="5e9d7-127">MAPI_E_NOT_ENOUGH_MEMORY</span><span class="sxs-lookup"><span data-stu-id="5e9d7-127">MAPI_E_NOT_ENOUGH_MEMORY</span></span> 
  
> <span data-ttu-id="5e9d7-128">このプロパティは、リモートプロシージャコール (RPC) のバッファーサイズよりも大きいため、更新できません。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-128">The property cannot be updated because it is larger than the remote procedure call (RPC) buffer size.</span></span>
    
<span data-ttu-id="5e9d7-129">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="5e9d7-129">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="5e9d7-130">プロパティの型は、呼び出し元の実装で想定される型ではありません。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-130">The property type is not the type expected by the calling implementation.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="5e9d7-131">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="5e9d7-131">Notes to implementers</span></span>

<span data-ttu-id="5e9d7-132">**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) プロパティタグと、 **PT_ERROR**型のすべてのプロパティを無視します。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-132">Ignore the **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) property tag and all properties with a type of **PT_ERROR**.</span></span> <span data-ttu-id="5e9d7-133">**sprop問題の配列**構造で、変更を加えたり、問題を報告したりしないでください。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-133">Do not make changes or report problems in the **SPropProblemArray** structure.</span></span> 
  
<span data-ttu-id="5e9d7-134">プロパティ値の配列に**PT_OBJECT**型のプロパティが含まれている場合は、MAPI_E_INVALID_PARAMETER を返します。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-134">Return MAPI_E_INVALID_PARAMETER if a property of type **PT_OBJECT** is included in the property value array.</span></span> <span data-ttu-id="5e9d7-135">また、複数値のプロパティが配列に含まれており、その**cvalues**メンバーが0に設定されている場合にも、このエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-135">Also return this error if a multiple-value property is included in the array and its **cValues** member is set to 0.</span></span> 
  
<span data-ttu-id="5e9d7-136">呼び出しが全体的に成功しても、一部のプロパティの設定に問題がある場合は、S_OK を返し、 _lppproblems_パラメーターが指す**sprop問題の配列**構造の適切なエントリに問題に関する情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-136">If the call succeeds overall but there are problems with setting some of the properties, return S_OK and put information about the problems in the appropriate entry of the **SPropProblemArray** structure that the  _lppProblems_ parameter points to.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5e9d7-137">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="5e9d7-137">Notes to callers</span></span>

<span data-ttu-id="5e9d7-138">また、サービスプロバイダーによっては、プロパティの種類を変更できるようにするために、特定のプロパティ識別子で以前に使用されていたのとは異なる種類のプロパティタグを渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-138">Depending on the service provider, you might also be able to change the property type by passing a property tag that contains a different type than was previously used with a given property identifier.</span></span>
  
<span data-ttu-id="5e9d7-139">オブジェクトでサポートされていないプロパティのプロパティタグを指定し、 **setprops**の実装で新しいプロパティを作成できる場合、プロパティはオブジェクトに追加されます。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-139">If you include a property tag for a property that is unsupported by the object and the implementation of **SetProps** allows the creation of new properties, the property is added to the object.</span></span> <span data-ttu-id="5e9d7-140">新しいプロパティに使用されたプロパティ識別子に格納されていた以前の値は、すべて破棄されます。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-140">Any previous value stored with the property identifier that was used for the new property is discarded.</span></span> 
  
<span data-ttu-id="5e9d7-141">S_OK 戻り値は、すべてのプロパティが正常に更新されたことを保証するものではないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-141">Note that the S_OK return value does not guarantee that all of the properties were successfully updated.</span></span> <span data-ttu-id="5e9d7-142">一部のプロバイダーは、 **setprops**呼び出しを受信するまで、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)または[imapiprop:: GetProps](imapiprop-getprops.md)などのプロバイダーの介入を必要とする呼び出しを受け取るまでキャッシュします。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-142">Some providers cache **SetProps** calls until they receive a call that requires provider intervention, such as [IMAPIProp::SaveChanges](imapiprop-savechanges.md) or [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span> <span data-ttu-id="5e9d7-143">そのため、以降の呼び出しで**setprops**呼び出しに関連するエラー値を受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-143">Therefore, it is possible to receive error values that relate to the **SetProps** call with the later calls.</span></span> 
  
<span data-ttu-id="5e9d7-144">**setprops**が S_OK を返す場合は、個々のプロパティの更新時に問題が発生したことを確認するために、 _lppproblems_に示されている**sprop問題の配列**構造を確認します。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-144">If **SetProps** returns S_OK, check the **SPropProblemArray** structure pointed to by  _lppProblems_ for problems updating individual properties.</span></span> <span data-ttu-id="5e9d7-145">**setprops**がエラーを返す場合は、プロパティの問題の配列をチェックしません。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-145">If **SetProps** returns an error, do not check the property problem array.</span></span> <span data-ttu-id="5e9d7-146">代わりに、オブジェクトの[imapiprop:: GetLastError](imapiprop-getlasterror.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-146">Instead, call the object's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method.</span></span> 
  
<span data-ttu-id="5e9d7-147">大きなプロパティを更新する場合、 **setprops**は失敗して MAPI_E_NOT_ENOUGH_MEMORY を返します。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-147">When updating large properties, **SetProps** can fail and return MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="5e9d7-148">プロパティの最大サイズはありません。また、オブジェクトごとに異なる制限を設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-148">There is no maximum size for properties, and different objects can have different limits.</span></span> <span data-ttu-id="5e9d7-149">大きなプロパティを処理する場合は、 **setprops**がこのエラー値を返す場合、IID_IStream をインターフェイス識別子として使用して、 [imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出すように準備してください。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-149">If you deal with potentially large properties, be prepared to call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with IID_IStream as the interface identifier if **SetProps** returns this error value.</span></span> 
  
<span data-ttu-id="5e9d7-150">[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、 **spropの配列**構造を解放します。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-150">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the **SPropProblemArray** structure.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5e9d7-151">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="5e9d7-151">MFCMAPI reference</span></span>

<span data-ttu-id="5e9d7-152">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5e9d7-153">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="5e9d7-153">**File**</span></span>|<span data-ttu-id="5e9d7-154">**関数**</span><span class="sxs-lookup"><span data-stu-id="5e9d7-154">**Function**</span></span>|<span data-ttu-id="5e9d7-155">**コメント**</span><span class="sxs-lookup"><span data-stu-id="5e9d7-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5e9d7-156">propertyeditor .cpp</span><span class="sxs-lookup"><span data-stu-id="5e9d7-156">PropertyEditor.cpp</span></span>  <br/> |<span data-ttu-id="5e9d7-157">cpropertyeditor:: writespropvaluetoobject</span><span class="sxs-lookup"><span data-stu-id="5e9d7-157">CPropertyEditor::WriteSPropValueToObject</span></span>  <br/> |<span data-ttu-id="5e9d7-158">mfcmapi は、 **imapiprop:: setprops**メソッドを使用して、プロパティが編集された後、そのプロパティをオブジェクトに書き戻します。</span><span class="sxs-lookup"><span data-stu-id="5e9d7-158">MFCMAPI uses the **IMAPIProp::SetProps** method to write a property back to an object after the property has been edited.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5e9d7-159">関連項目</span><span class="sxs-lookup"><span data-stu-id="5e9d7-159">See also</span></span>



[<span data-ttu-id="5e9d7-160">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="5e9d7-160">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="5e9d7-161">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="5e9d7-161">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="5e9d7-162">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="5e9d7-162">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="5e9d7-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="5e9d7-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="5e9d7-164">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="5e9d7-164">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="5e9d7-165">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="5e9d7-165">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="5e9d7-166">SPropValue</span><span class="sxs-lookup"><span data-stu-id="5e9d7-166">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="5e9d7-167">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5e9d7-167">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)

