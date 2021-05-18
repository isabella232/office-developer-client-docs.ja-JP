---
title: IMAPIPropDeleteProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.DeleteProps
api_type:
- COM
ms.assetid: 5cc642de-21f0-4826-bf21-aac4bcfc1328
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5bfef87baa2dffa4605f9a7afa3833024f514430
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409238"
---
# <a name="imapipropdeleteprops"></a><span data-ttu-id="6421b-103">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="6421b-103">IMAPIProp::DeleteProps</span></span>

  
  
<span data-ttu-id="6421b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6421b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6421b-105">オブジェクトから 1 つ以上のプロパティを削除します。</span><span class="sxs-lookup"><span data-stu-id="6421b-105">Deletes one or more properties from an object.</span></span> 
  
```cpp
HRESULT DeleteProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="6421b-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6421b-106">Parameters</span></span>

 <span data-ttu-id="6421b-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="6421b-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="6421b-108">[in]削除するプロパティを示すプロパティ タグの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6421b-108">[in] A pointer to an array of property tags that indicate the properties to delete.</span></span> <span data-ttu-id="6421b-109">_lpPropTagArray_ が指す [SPropTagArray](sproptagarray.md)構造体の **cValues** メンバーは 0 にし _、lpPropTagArray_ パラメーター自体は NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="6421b-109">The **cValues** member of the [SPropTagArray](sproptagarray.md) structure pointed to by  _lpPropTagArray_ must not be zero, and the  _lpPropTagArray_ parameter itself must not be NULL.</span></span> 
    
 <span data-ttu-id="6421b-110">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="6421b-110">_lppProblems_</span></span>
  
> <span data-ttu-id="6421b-111">[in, out]入力時に [、SPropProblemArray](spropproblemarray.md) 構造体へのポインターを指すポインター。それ以外の場合は、エラー情報が不要な NULL を指定します。</span><span class="sxs-lookup"><span data-stu-id="6421b-111">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates that there is no need for error information.</span></span> <span data-ttu-id="6421b-112">_lppProblems が_ 入力の有効なポインターである場合 **、DeleteProps** は 1 つ以上のプロパティを削除するエラーに関する詳細情報を返します。</span><span class="sxs-lookup"><span data-stu-id="6421b-112">If  _lppProblems_ is a valid pointer on input, **DeleteProps** returns detailed information about errors in deleting one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6421b-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="6421b-113">Return value</span></span>

<span data-ttu-id="6421b-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="6421b-114">S_OK</span></span> 
  
> <span data-ttu-id="6421b-115">プロパティが正常に削除されました。</span><span class="sxs-lookup"><span data-stu-id="6421b-115">Properties were successfully deleted.</span></span>
    
<span data-ttu-id="6421b-116">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="6421b-116">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="6421b-117">呼び出し元には、プロパティを削除するためのアクセス許可が不十分です。</span><span class="sxs-lookup"><span data-stu-id="6421b-117">The caller has insufficient permissions to delete properties.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6421b-118">注釈</span><span class="sxs-lookup"><span data-stu-id="6421b-118">Remarks</span></span>

<span data-ttu-id="6421b-119">**IMAPIProp::D eleteProps** メソッドは、現在のオブジェクトから 1 つ以上のプロパティを削除します。</span><span class="sxs-lookup"><span data-stu-id="6421b-119">The **IMAPIProp::DeleteProps** method removes one or more properties from the current object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6421b-120">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="6421b-120">Notes to implementers</span></span>

<span data-ttu-id="6421b-121">すべてのオブジェクトからプロパティを削除できる必要はない。</span><span class="sxs-lookup"><span data-stu-id="6421b-121">You do not have to allow properties to be deleted from all objects.</span></span> <span data-ttu-id="6421b-122">オブジェクトが変更できない場合は **、DeleteProps** MAPI_E_NO_ACCESSを返します。</span><span class="sxs-lookup"><span data-stu-id="6421b-122">If the object is not modifiable, return MAPI_E_NO_ACCESS from the **DeleteProps** method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6421b-123">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="6421b-123">Notes to callers</span></span>

<span data-ttu-id="6421b-124">_lpPropTagArray_ パラメーターが指すプロパティ タグ配列内の各プロパティ タグのプロパティの種類を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6421b-124">You do not have to set the property type for each property tag in the property tag array pointed to by the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="6421b-125">プロパティの種類は無視されます。プロパティ識別子だけが使用されます。</span><span class="sxs-lookup"><span data-stu-id="6421b-125">Property types are ignored; only the property identifiers are used.</span></span> 
  
<span data-ttu-id="6421b-126">一部のオブジェクトは変更を許可していないので、これらのオブジェクトは **DeleteProps** メソッドMAPI_E_NO_ACCESS返します。</span><span class="sxs-lookup"><span data-stu-id="6421b-126">Be aware that some objects do not allow modification and that these objects return MAPI_E_NO_ACCESS from the **DeleteProps** method.</span></span> <span data-ttu-id="6421b-127">その他のオブジェクトでは、一部のプロパティを削除できますが、他のプロパティは削除されません。</span><span class="sxs-lookup"><span data-stu-id="6421b-127">Other objects allow some properties to be deleted, but not others.</span></span> <span data-ttu-id="6421b-128">プロパティの一部のみを削除する際に問題が発生した場合 **、DeleteProps** はプロパティをS_OK。</span><span class="sxs-lookup"><span data-stu-id="6421b-128">When there is a problem deleting only some of the properties, **DeleteProps** returns S_OK.</span></span> <span data-ttu-id="6421b-129">_lppProblems_ パラメーターで有効なポインターを渡した場合 **、DeleteProps** は、各プロパティの問題に関する詳細情報を含む **SPropProblemArray** 構造体にポインターを設定します。</span><span class="sxs-lookup"><span data-stu-id="6421b-129">If you have passed a valid pointer in the  _lppProblems_ parameter, **DeleteProps** will set the pointer to an **SPropProblemArray** structure that contains detailed information about the problems with each property.</span></span> <span data-ttu-id="6421b-130">たとえば、メッセージのすべてのプロパティを削除し、1 つ以上の添付ファイルに問題がある場合 **、SPropProblemArray** 構造体には **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) プロパティのエントリが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6421b-130">For example, if you are deleting all of the properties of a message and there is a problem with one or more of its attachments, the **SPropProblemArray** structure will contain an entry for the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="6421b-131">_lppProblems_ が指す構造は **、DeleteProps** が値を返す場合にのみ有効S_OK。</span><span class="sxs-lookup"><span data-stu-id="6421b-131">The structure pointed to by  _lppProblems_ is only valid if **DeleteProps** returns S_OK.</span></span> <span data-ttu-id="6421b-132">**DeleteProps がエラー** を返す場合は **、SPropProblemArray 構造体の使用を試み** ない。</span><span class="sxs-lookup"><span data-stu-id="6421b-132">If **DeleteProps** returns an error, do not attempt to use the **SPropProblemArray** structure.</span></span> <span data-ttu-id="6421b-133">代わりに、オブジェクトの [IMAPIProp::GetLastError](imapiprop-getlasterror.md) メソッドを呼び出して、エラーの詳細を取得します。</span><span class="sxs-lookup"><span data-stu-id="6421b-133">Instead, call the object's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method to obtain more information about the error.</span></span> 
  
<span data-ttu-id="6421b-134">MAPIFreeBuffer 関数を呼び出して、返された[SPropProblemArray 構造体を解放](mapifreebuffer.md)します。 </span><span class="sxs-lookup"><span data-stu-id="6421b-134">Free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6421b-135">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="6421b-135">MFCMAPI reference</span></span>

<span data-ttu-id="6421b-136">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6421b-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6421b-137">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="6421b-137">**File**</span></span>|<span data-ttu-id="6421b-138">**関数**</span><span class="sxs-lookup"><span data-stu-id="6421b-138">**Function**</span></span>|<span data-ttu-id="6421b-139">**コメント**</span><span class="sxs-lookup"><span data-stu-id="6421b-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6421b-140">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="6421b-140">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="6421b-141">DeleteProperty</span><span class="sxs-lookup"><span data-stu-id="6421b-141">DeleteProperty</span></span>  <br/> |<span data-ttu-id="6421b-142">MFCMAPI は **IMAPIProp::D eleteProps** メソッドを使用して、オブジェクトからプロパティを削除します。</span><span class="sxs-lookup"><span data-stu-id="6421b-142">MFCMAPI uses the **IMAPIProp::DeleteProps** method to delete a property from an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6421b-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="6421b-143">See also</span></span>



[<span data-ttu-id="6421b-144">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="6421b-144">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="6421b-145">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="6421b-145">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="6421b-146">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="6421b-146">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="6421b-147">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="6421b-147">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="6421b-148">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="6421b-148">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="6421b-149">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="6421b-149">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="6421b-150">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6421b-150">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


<span data-ttu-id="6421b-151">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="6421b-151">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

