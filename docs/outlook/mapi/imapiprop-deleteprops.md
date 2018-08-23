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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8eb19f9a2d3458e153b0758b56c502ce612be0cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800667"
---
# <a name="imapipropdeleteprops"></a><span data-ttu-id="b6a05-103">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="b6a05-103">IMAPIProp::DeleteProps</span></span>

  
  
<span data-ttu-id="b6a05-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b6a05-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b6a05-105">オブジェクトから 1 つまたは複数のプロパティを削除します。</span><span class="sxs-lookup"><span data-stu-id="b6a05-105">Deletes one or more properties from an object.</span></span> 
  
```cpp
HRESULT DeleteProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="b6a05-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="b6a05-106">Parameters</span></span>

 <span data-ttu-id="b6a05-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="b6a05-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="b6a05-108">[in]削除するにはプロパティを指定するプロパティ タグの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b6a05-108">[in] A pointer to an array of property tags that indicate the properties to delete.</span></span> <span data-ttu-id="b6a05-109">_LpPropTagArray_で示される[SPropTagArray](sproptagarray.md)構造体の**あう**メンバーが 0 でなければできませんし、 _lpPropTagArray_パラメーター自体を NULL にする必要があることはできません。</span><span class="sxs-lookup"><span data-stu-id="b6a05-109">The **cValues** member of the [SPropTagArray](sproptagarray.md) structure pointed to by  _lpPropTagArray_ must not be zero, and the  _lpPropTagArray_ parameter itself must not be NULL.</span></span> 
    
 <span data-ttu-id="b6a05-110">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="b6a05-110">_lppProblems_</span></span>
  
> <span data-ttu-id="b6a05-111">[で [チェック アウト][SPropProblemArray](spropproblemarray.md)構造体へのポインターへのポインターの入力でそれ以外の場合、NULL、エラー情報の必要性がないことを示します。</span><span class="sxs-lookup"><span data-stu-id="b6a05-111">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates that there is no need for error information.</span></span> <span data-ttu-id="b6a05-112">_LppProblems_が入力時に有効なポインターである場合は、 **DeleteProps**は、1 つまたは複数のプロパティを削除中にエラーに関する詳細な情報を返します。</span><span class="sxs-lookup"><span data-stu-id="b6a05-112">If  _lppProblems_ is a valid pointer on input, **DeleteProps** returns detailed information about errors in deleting one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b6a05-113">�߂�l</span><span class="sxs-lookup"><span data-stu-id="b6a05-113">Return value</span></span>

<span data-ttu-id="b6a05-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="b6a05-114">S_OK</span></span> 
  
> <span data-ttu-id="b6a05-115">プロパティは正常に削除されました。</span><span class="sxs-lookup"><span data-stu-id="b6a05-115">Properties were successfully deleted.</span></span>
    
<span data-ttu-id="b6a05-116">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="b6a05-116">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="b6a05-117">呼び出し側では、プロパティを削除するのには十分なアクセス許可を持っています。</span><span class="sxs-lookup"><span data-stu-id="b6a05-117">The caller has insufficient permissions to delete properties.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b6a05-118">注釈</span><span class="sxs-lookup"><span data-stu-id="b6a05-118">Remarks</span></span>

<span data-ttu-id="b6a05-119">**IMAPIProp::DeleteProps**メソッドは、現在のオブジェクトから 1 つまたは複数のプロパティを削除します。</span><span class="sxs-lookup"><span data-stu-id="b6a05-119">The **IMAPIProp::DeleteProps** method removes one or more properties from the current object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b6a05-120">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="b6a05-120">Notes to implementers</span></span>

<span data-ttu-id="b6a05-121">すべてのオブジェクトから削除するプロパティを許可する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b6a05-121">You do not have to allow properties to be deleted from all objects.</span></span> <span data-ttu-id="b6a05-122">オブジェクトが変更可能でない場合は、 **DeleteProps**メソッドから MAPI_E_NO_ACCESS を返します。</span><span class="sxs-lookup"><span data-stu-id="b6a05-122">If the object is not modifiable, return MAPI_E_NO_ACCESS from the **DeleteProps** method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b6a05-123">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="b6a05-123">Notes to callers</span></span>

<span data-ttu-id="b6a05-124">_LpPropTagArray_パラメーターで指定されたプロパティ タグ配列内の各プロパティ タグのプロパティの型を設定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b6a05-124">You do not have to set the property type for each property tag in the property tag array pointed to by the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="b6a05-125">プロパティの型は無視されます。プロパティの識別子だけが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b6a05-125">Property types are ignored; only the property identifiers are used.</span></span> 
  
<span data-ttu-id="b6a05-126">いくつかのオブジェクトは、変更を許可しないことと、これらのオブジェクトの**DeleteProps**メソッドから MAPI_E_NO_ACCESS を返すことに注意します。</span><span class="sxs-lookup"><span data-stu-id="b6a05-126">Be aware that some objects do not allow modification and that these objects return MAPI_E_NO_ACCESS from the **DeleteProps** method.</span></span> <span data-ttu-id="b6a05-127">その他のオブジェクトは、いくつかのプロパティを削除するには、それ以外を使用します。</span><span class="sxs-lookup"><span data-stu-id="b6a05-127">Other objects allow some properties to be deleted, but not others.</span></span> <span data-ttu-id="b6a05-128">プロパティの一部のみを削除中に問題がある場合は、 **DeleteProps**は、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="b6a05-128">When there is a problem deleting only some of the properties, **DeleteProps** returns S_OK.</span></span> <span data-ttu-id="b6a05-129">_LppProblems_パラメーターに有効なポインターを渡した場合**DeleteProps**は各プロパティを使用して問題に関する詳細情報を含む**SPropProblemArray**構造体へのポインターを設定します。</span><span class="sxs-lookup"><span data-stu-id="b6a05-129">If you have passed a valid pointer in the  _lppProblems_ parameter, **DeleteProps** will set the pointer to an **SPropProblemArray** structure that contains detailed information about the problems with each property.</span></span> <span data-ttu-id="b6a05-130">などのすべてのメッセージのプロパティを削除する 1 つまたは複数の添付ファイルの問題がある場合は、 **SPropProblemArray**構造体エントリが記録の**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) プロパティです。</span><span class="sxs-lookup"><span data-stu-id="b6a05-130">For example, if you are deleting all of the properties of a message and there is a problem with one or more of its attachments, the **SPropProblemArray** structure will contain an entry for the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="b6a05-131">_LppProblems_が指す構造体は**DeleteProps**には、S_OK が返された場合です。</span><span class="sxs-lookup"><span data-stu-id="b6a05-131">The structure pointed to by  _lppProblems_ is only valid if **DeleteProps** returns S_OK.</span></span> <span data-ttu-id="b6a05-132">**DeleteProps**がエラーを返した場合に**SPropProblemArray**構造体を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="b6a05-132">If **DeleteProps** returns an error, do not attempt to use the **SPropProblemArray** structure.</span></span> <span data-ttu-id="b6a05-133">代わりに、エラーに関する詳細情報を取得するのには、オブジェクトの[IMAPIProp::GetLastError](imapiprop-getlasterror.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b6a05-133">Instead, call the object's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method to obtain more information about the error.</span></span> 
  
<span data-ttu-id="b6a05-134">[MAPIFreeBuffer](mapifreebuffer.md)関数の呼び出しによって返された**SPropProblemArray**構造体を解放します。</span><span class="sxs-lookup"><span data-stu-id="b6a05-134">Free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b6a05-135">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="b6a05-135">MFCMAPI reference</span></span>

<span data-ttu-id="b6a05-136">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="b6a05-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b6a05-137">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="b6a05-137">**File**</span></span>|<span data-ttu-id="b6a05-138">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="b6a05-138">**Function**</span></span>|<span data-ttu-id="b6a05-139">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="b6a05-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b6a05-140">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="b6a05-140">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="b6a05-141">DeleteProperty</span><span class="sxs-lookup"><span data-stu-id="b6a05-141">DeleteProperty</span></span>  <br/> |<span data-ttu-id="b6a05-142">MFCMAPI では、 **IMAPIProp::DeleteProps**メソッドを使用して、オブジェクトからプロパティを削除します。</span><span class="sxs-lookup"><span data-stu-id="b6a05-142">MFCMAPI uses the **IMAPIProp::DeleteProps** method to delete a property from an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b6a05-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="b6a05-143">See also</span></span>



[<span data-ttu-id="b6a05-144">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b6a05-144">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="b6a05-145">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="b6a05-145">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="b6a05-146">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="b6a05-146">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="b6a05-147">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="b6a05-147">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="b6a05-148">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="b6a05-148">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="b6a05-149">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="b6a05-149">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="b6a05-150">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b6a05-150">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


<span data-ttu-id="b6a05-151">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="b6a05-151">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

