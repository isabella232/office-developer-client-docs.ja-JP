---
title: imapipropgetproplist
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetPropList
api_type:
- COM
ms.assetid: 0069c223-32bb-4286-b763-39fd45dc263b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f089fa2c608fb9fcb7deba2e061c5cf5886aa02f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414789"
---
# <a name="imapipropgetproplist"></a><span data-ttu-id="edef0-103">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="edef0-103">IMAPIProp::GetPropList</span></span>

  
  
<span data-ttu-id="edef0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="edef0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="edef0-105">すべてのプロパティのプロパティタグを返します。</span><span class="sxs-lookup"><span data-stu-id="edef0-105">Returns property tags for all properties.</span></span> 
  
```cpp
HRESULT GetPropList(
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTagArray
);
```

## <a name="parameters"></a><span data-ttu-id="edef0-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edef0-106">Parameters</span></span>

 <span data-ttu-id="edef0-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="edef0-107">_ulFlags_</span></span>
  
> <span data-ttu-id="edef0-108">順番返される property タグ内の文字列の形式を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="edef0-108">[in] A bitmask of flags that controls the format for the strings in the returned property tags.</span></span> <span data-ttu-id="edef0-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="edef0-109">The following flag can be set:</span></span>
    
<span data-ttu-id="edef0-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="edef0-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="edef0-111">返される文字列は、Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="edef0-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="edef0-112">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="edef0-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="edef0-113">_lppPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="edef0-113">_lppPropTagArray_</span></span>
  
> <span data-ttu-id="edef0-114">読み上げすべてのオブジェクトのプロパティのタグを含む、プロパティタグ配列へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="edef0-114">[out] A pointer to a pointer to the property tag array that contains tags for all of the object's properties.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="edef0-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="edef0-115">Return value</span></span>

<span data-ttu-id="edef0-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="edef0-116">S_OK</span></span> 
  
> <span data-ttu-id="edef0-117">すべてのプロパティタグが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="edef0-117">All of the property tags were returned successfully.</span></span>
    
<span data-ttu-id="edef0-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="edef0-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="edef0-119">MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="edef0-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="edef0-120">注釈</span><span class="sxs-lookup"><span data-stu-id="edef0-120">Remarks</span></span>

<span data-ttu-id="edef0-121">**imapiprop:: getproplist**メソッドは、オブジェクトで現在サポートされている各プロパティの property タグを取得します。</span><span class="sxs-lookup"><span data-stu-id="edef0-121">The **IMAPIProp::GetPropList** method retrieves the property tag for each property currently supported by an object.</span></span> <span data-ttu-id="edef0-122">オブジェクトが現在プロパティをサポートしていない場合、 **getproplist**は**cvalues**メンバーが0に設定されたプロパティタグ配列を返します。</span><span class="sxs-lookup"><span data-stu-id="edef0-122">If the object does not currently support any properties, **GetPropList** returns a property tag array with the **cValues** member set to 0.</span></span> 
  
<span data-ttu-id="edef0-123">**getproplist**によって返されるプロパティの範囲は、プロバイダーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="edef0-123">The scope of properties returned by **GetPropList** varies from provider to provider.</span></span> <span data-ttu-id="edef0-124">一部のサービスプロバイダーは、呼び出し元がアクセス権を持っていないプロパティを除外します。</span><span class="sxs-lookup"><span data-stu-id="edef0-124">Some service providers exclude those properties for which the caller does not have access.</span></span> <span data-ttu-id="edef0-125">すべてのプロバイダーは、 **PT_OBJECT**型のプロパティを返します。</span><span class="sxs-lookup"><span data-stu-id="edef0-125">All providers return properties of type **PT_OBJECT**.</span></span>
  
<span data-ttu-id="edef0-126">オブジェクトが Unicode をサポートしていない場合、オブジェクトに対して定義されている文字列プロパティがない場合でも、 **getproplist**は MAPI_E_BAD_CHARWIDTH を返します。</span><span class="sxs-lookup"><span data-stu-id="edef0-126">If the object does not support Unicode, **GetPropList** returns MAPI_E_BAD_CHARWIDTH, even if there are no string properties defined for the object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="edef0-127">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="edef0-127">Notes to implementers</span></span>

<span data-ttu-id="edef0-128">リモートトランスポートプロバイダーは、ここで指定されたとおりに**getproplist**を実装します。</span><span class="sxs-lookup"><span data-stu-id="edef0-128">Remote transport providers implement **GetPropList** exactly as specified here.</span></span> <span data-ttu-id="edef0-129">特別な問題はありません。</span><span class="sxs-lookup"><span data-stu-id="edef0-129">There are no special concerns.</span></span> <span data-ttu-id="edef0-130">もちろん、実装では、 [imapiprop:: GetProps](imapiprop-getprops.md)メソッドでサポートされているのと同じプロパティのリストを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="edef0-130">Your implementation should, of course, return the same list of properties as supported by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="edef0-131">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="edef0-131">Notes to callers</span></span>

<span data-ttu-id="edef0-132">[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、 _lppPropTagArray_によって示されるプロパティタグ配列を解放します。</span><span class="sxs-lookup"><span data-stu-id="edef0-132">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the property tag array pointed to by  _lppPropTagArray_.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="edef0-133">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="edef0-133">MFCMAPI reference</span></span>

<span data-ttu-id="edef0-134">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="edef0-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="edef0-135">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="edef0-135">**File**</span></span>|<span data-ttu-id="edef0-136">**関数**</span><span class="sxs-lookup"><span data-stu-id="edef0-136">**Function**</span></span>|<span data-ttu-id="edef0-137">**コメント**</span><span class="sxs-lookup"><span data-stu-id="edef0-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="edef0-138">MAPIFunctions</span><span class="sxs-lookup"><span data-stu-id="edef0-138">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="edef0-139">GetPropsNULL</span><span class="sxs-lookup"><span data-stu-id="edef0-139">GetPropsNULL</span></span>  <br/> |<span data-ttu-id="edef0-140">mfcmapi は、 **imapiprop:: getproplist**メソッドを使用して、 **GetProps**に渡すプロパティリストを取得します。</span><span class="sxs-lookup"><span data-stu-id="edef0-140">MFCMAPI uses the **IMAPIProp::GetPropList** method to get a property list to pass to **GetProps**.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="edef0-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="edef0-141">See also</span></span>



[<span data-ttu-id="edef0-142">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="edef0-142">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="edef0-143">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="edef0-143">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="edef0-144">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="edef0-144">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


<span data-ttu-id="edef0-145">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="edef0-145">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

