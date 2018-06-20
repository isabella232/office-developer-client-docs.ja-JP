---
title: HrGetOneProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrGetOneProp
api_type:
- HeaderDef
ms.assetid: 8d0a381a-e714-4663-9a57-b0e1cdbd6ba7
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4dcdce72781669988a0cb15eb9b3a7cd73494bfb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800315"
---
# <a name="hrgetoneprop"></a><span data-ttu-id="e4f4c-103">HrGetOneProp</span><span class="sxs-lookup"><span data-stu-id="e4f4c-103">HrGetOneProp</span></span>

  
  
<span data-ttu-id="e4f4c-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e4f4c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e4f4c-105">プロパティのインターフェイスから、つまり、 [IMAPIProp](imapipropiunknown.md)から派生したインターフェイスには、1 つのプロパティの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="e4f4c-105">Retrieves the value of a single property from a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e4f4c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e4f4c-106">Header file:</span></span>  <br/> |<span data-ttu-id="e4f4c-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="e4f4c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e4f4c-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="e4f4c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e4f4c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e4f4c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e4f4c-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e4f4c-110">Called by:</span></span>  <br/> |<span data-ttu-id="e4f4c-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e4f4c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a><span data-ttu-id="e4f4c-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="e4f4c-112">Parameters</span></span>

 <span data-ttu-id="e4f4c-113">_pmp_</span><span class="sxs-lookup"><span data-stu-id="e4f4c-113">_pmp_</span></span>
  
> <span data-ttu-id="e4f4c-114">[in][IMAPIProp](imapipropiunknown.md)インターフェイスを取得するプロパティの値は、元へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e4f4c-114">[in] Pointer to the [IMAPIProp](imapipropiunknown.md) interface from which the property value is to be retrieved.</span></span> 
    
 <span data-ttu-id="e4f4c-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="e4f4c-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="e4f4c-116">[in]取得するプロパティのプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="e4f4c-116">[in] Property tag of the property to be retrieved.</span></span> 
    
 <span data-ttu-id="e4f4c-117">_ppprop_</span><span class="sxs-lookup"><span data-stu-id="e4f4c-117">_ppprop_</span></span>
  
> <span data-ttu-id="e4f4c-118">[out]取得したプロパティ値を定義する、返される[SPropValue](spropvalue.md)構造へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e4f4c-118">[out] Pointer to a pointer to the returned [SPropValue](spropvalue.md) structure defining the retrieved property value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e4f4c-119">�߂�l</span><span class="sxs-lookup"><span data-stu-id="e4f4c-119">Return value</span></span>

<span data-ttu-id="e4f4c-120">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="e4f4c-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="e4f4c-121">要求されたプロパティは、指定されたインターフェイスからは使用できません。</span><span class="sxs-lookup"><span data-stu-id="e4f4c-121">The requested property is not available from the specified interface.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e4f4c-122">備考</span><span class="sxs-lookup"><span data-stu-id="e4f4c-122">Remarks</span></span>

<span data-ttu-id="e4f4c-123">、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドとは異なり、 **HrGetOneProp**関数は決して警告を返します。</span><span class="sxs-lookup"><span data-stu-id="e4f4c-123">Unlike the [IMAPIProp::GetProps](imapiprop-getprops.md) method, the **HrGetOneProp** function never returns any warning.</span></span> <span data-ttu-id="e4f4c-124">1 つのプロパティを取得するために単に成功または失敗します。</span><span class="sxs-lookup"><span data-stu-id="e4f4c-124">Because it retrieves only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="e4f4c-125">複数のプロパティを取得するため**GetProps**が高速です。</span><span class="sxs-lookup"><span data-stu-id="e4f4c-125">For retrieving multiple properties, **GetProps** is faster.</span></span> 
  
<span data-ttu-id="e4f4c-126">設定または[HrSetOneProp](hrsetoneprop.md)関数を使用して 1 つのプロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="e4f4c-126">You can set or change a single property with the [HrSetOneProp](hrsetoneprop.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e4f4c-127">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="e4f4c-127">MFCMAPI reference</span></span>

<span data-ttu-id="e4f4c-128">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="e4f4c-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e4f4c-129">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="e4f4c-129">**File**</span></span>|<span data-ttu-id="e4f4c-130">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="e4f4c-130">**Function**</span></span>|<span data-ttu-id="e4f4c-131">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="e4f4c-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e4f4c-132">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="e4f4c-132">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="e4f4c-133">GetMAPIObjectType</span><span class="sxs-lookup"><span data-stu-id="e4f4c-133">GetMAPIObjectType</span></span>  <br/> |<span data-ttu-id="e4f4c-134">MFCMAPI では、 **HrGetOneProp**メソッドを使用して、オブジェクトの種類を取得します。</span><span class="sxs-lookup"><span data-stu-id="e4f4c-134">MFCMAPI uses the **HrGetOneProp** method to retrieve the type of an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e4f4c-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="e4f4c-135">See also</span></span>



<span data-ttu-id="e4f4c-136">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="e4f4c-136">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

