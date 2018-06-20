---
title: IMAPIPropGetPropList
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0457007334ad8cc69dade3abd5859dd0d5f7af7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800652"
---
# <a name="imapipropgetproplist"></a><span data-ttu-id="00814-103">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="00814-103">IMAPIProp::GetPropList</span></span>

  
  
<span data-ttu-id="00814-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="00814-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="00814-105">すべてのプロパティのプロパティ タグを返します。</span><span class="sxs-lookup"><span data-stu-id="00814-105">Returns property tags for all properties.</span></span> 
  
```cpp
HRESULT GetPropList(
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTagArray
);
```

## <a name="parameters"></a><span data-ttu-id="00814-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="00814-106">Parameters</span></span>

 <span data-ttu-id="00814-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="00814-107">_ulFlags_</span></span>
  
> <span data-ttu-id="00814-108">[in]返されるプロパティは、タグ内の文字列の書式を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="00814-108">[in] A bitmask of flags that controls the format for the strings in the returned property tags.</span></span> <span data-ttu-id="00814-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="00814-109">The following flag can be set:</span></span>
    
<span data-ttu-id="00814-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="00814-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="00814-111">関数が返す文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="00814-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="00814-112">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="00814-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="00814-113">_lppPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="00814-113">_lppPropTagArray_</span></span>
  
> <span data-ttu-id="00814-114">[out]オブジェクトのプロパティのすべてのタグを含むプロパティ タグ配列へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="00814-114">[out] A pointer to a pointer to the property tag array that contains tags for all of the object's properties.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="00814-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="00814-115">Return value</span></span>

<span data-ttu-id="00814-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="00814-116">S_OK</span></span> 
  
> <span data-ttu-id="00814-117">プロパティ タグのすべてが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="00814-117">All of the property tags were returned successfully.</span></span>
    
<span data-ttu-id="00814-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="00814-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="00814-119">か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装は、Unicode だけをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="00814-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="00814-120">備考</span><span class="sxs-lookup"><span data-stu-id="00814-120">Remarks</span></span>

<span data-ttu-id="00814-121">**IMAPIProp::GetPropList**メソッドは、現在のオブジェクトによってサポートされている各プロパティのプロパティ タグを取得します。</span><span class="sxs-lookup"><span data-stu-id="00814-121">The **IMAPIProp::GetPropList** method retrieves the property tag for each property currently supported by an object.</span></span> <span data-ttu-id="00814-122">オブジェクトは、任意のプロパティを現在サポートしていません、 **getproplist メソッド**は**あう**メンバーが 0 に設定するプロパティ タグ配列を返します。</span><span class="sxs-lookup"><span data-stu-id="00814-122">If the object does not currently support any properties, **GetPropList** returns a property tag array with the **cValues** member set to 0.</span></span> 
  
<span data-ttu-id="00814-123">**Getproplist メソッド**から返されるプロパティのスコープは、プロバイダーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="00814-123">The scope of properties returned by **GetPropList** varies from provider to provider.</span></span> <span data-ttu-id="00814-124">一部のサービス プロバイダーは、呼び出し元がアクセス権を持たないこれらのプロパティを除外します。</span><span class="sxs-lookup"><span data-stu-id="00814-124">Some service providers exclude those properties for which the caller does not have access.</span></span> <span data-ttu-id="00814-125">すべてのプロバイダーでは、 **PT_OBJECT**の種類のプロパティが返されます。</span><span class="sxs-lookup"><span data-stu-id="00814-125">All providers return properties of type **PT_OBJECT**.</span></span>
  
<span data-ttu-id="00814-126">オブジェクトが Unicode をサポートしていない場合、 **getproplist メソッド**は、オブジェクトに対して定義されている文字列のプロパティがない場合でも、MAPI_E_BAD_CHARWIDTH を返します。</span><span class="sxs-lookup"><span data-stu-id="00814-126">If the object does not support Unicode, **GetPropList** returns MAPI_E_BAD_CHARWIDTH, even if there are no string properties defined for the object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="00814-127">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="00814-127">Notes to implementers</span></span>

<span data-ttu-id="00814-128">リモート トランスポート プロバイダーは、ここで指定どおり正確に**getproplist メソッド**を実装します。</span><span class="sxs-lookup"><span data-stu-id="00814-128">Remote transport providers implement **GetPropList** exactly as specified here.</span></span> <span data-ttu-id="00814-129">特別な懸念事項はありません。</span><span class="sxs-lookup"><span data-stu-id="00814-129">There are no special concerns.</span></span> <span data-ttu-id="00814-130">実装では、同じように[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドでサポートされているプロパティの一覧を返しますは、もちろん。</span><span class="sxs-lookup"><span data-stu-id="00814-130">Your implementation should, of course, return the same list of properties as supported by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="00814-131">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="00814-131">Notes to callers</span></span>

<span data-ttu-id="00814-132">_LppPropTagArray_で指定されたプロパティ タグ配列を解放する[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="00814-132">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the property tag array pointed to by  _lppPropTagArray_.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="00814-133">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="00814-133">MFCMAPI reference</span></span>

<span data-ttu-id="00814-134">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="00814-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="00814-135">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="00814-135">**File**</span></span>|<span data-ttu-id="00814-136">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="00814-136">**Function**</span></span>|<span data-ttu-id="00814-137">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="00814-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="00814-138">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="00814-138">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="00814-139">GetPropsNULL</span><span class="sxs-lookup"><span data-stu-id="00814-139">GetPropsNULL</span></span>  <br/> |<span data-ttu-id="00814-140">MFCMAPI は、 **GetProps**に渡すプロパティの一覧を取得するのに**IMAPIProp::GetPropList**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="00814-140">MFCMAPI uses the **IMAPIProp::GetPropList** method to get a property list to pass to **GetProps**.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="00814-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="00814-141">See also</span></span>



[<span data-ttu-id="00814-142">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="00814-142">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="00814-143">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="00814-143">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="00814-144">IMAPIProp: IUnknown</span><span class="sxs-lookup"><span data-stu-id="00814-144">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


<span data-ttu-id="00814-145">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="00814-145">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

