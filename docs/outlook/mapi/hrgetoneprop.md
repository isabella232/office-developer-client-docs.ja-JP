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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4dcdce72781669988a0cb15eb9b3a7cd73494bfb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800315"
---
# <a name="hrgetoneprop"></a><span data-ttu-id="d8578-103">HrGetOneProp</span><span class="sxs-lookup"><span data-stu-id="d8578-103">HrGetOneProp</span></span>

  
  
<span data-ttu-id="d8578-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d8578-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d8578-105">プロパティのインターフェイスから、つまり、 [IMAPIProp](imapipropiunknown.md)から派生したインターフェイスには、1 つのプロパティの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="d8578-105">Retrieves the value of a single property from a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d8578-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="d8578-106">Header file:</span></span>  <br/> |<span data-ttu-id="d8578-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="d8578-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d8578-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="d8578-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d8578-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d8578-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d8578-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d8578-110">Called by:</span></span>  <br/> |<span data-ttu-id="d8578-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="d8578-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a><span data-ttu-id="d8578-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d8578-112">Parameters</span></span>

 <span data-ttu-id="d8578-113">_pmp_</span><span class="sxs-lookup"><span data-stu-id="d8578-113">_pmp_</span></span>
  
> <span data-ttu-id="d8578-114">[in][IMAPIProp](imapipropiunknown.md)インターフェイスを取得するプロパティの値は、元へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d8578-114">[in] Pointer to the [IMAPIProp](imapipropiunknown.md) interface from which the property value is to be retrieved.</span></span> 
    
 <span data-ttu-id="d8578-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="d8578-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="d8578-116">[in]取得するプロパティのプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="d8578-116">[in] Property tag of the property to be retrieved.</span></span> 
    
 <span data-ttu-id="d8578-117">_ppprop_</span><span class="sxs-lookup"><span data-stu-id="d8578-117">_ppprop_</span></span>
  
> <span data-ttu-id="d8578-118">[out]取得したプロパティ値を定義する、返される[SPropValue](spropvalue.md)構造へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d8578-118">[out] Pointer to a pointer to the returned [SPropValue](spropvalue.md) structure defining the retrieved property value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d8578-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="d8578-119">Return value</span></span>

<span data-ttu-id="d8578-120">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="d8578-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="d8578-121">要求されたプロパティは、指定されたインターフェイスからは使用できません。</span><span class="sxs-lookup"><span data-stu-id="d8578-121">The requested property is not available from the specified interface.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d8578-122">注釈</span><span class="sxs-lookup"><span data-stu-id="d8578-122">Remarks</span></span>

<span data-ttu-id="d8578-123">、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドとは異なり、 **HrGetOneProp**関数は決して警告を返します。</span><span class="sxs-lookup"><span data-stu-id="d8578-123">Unlike the [IMAPIProp::GetProps](imapiprop-getprops.md) method, the **HrGetOneProp** function never returns any warning.</span></span> <span data-ttu-id="d8578-124">1 つのプロパティを取得するために単に成功または失敗します。</span><span class="sxs-lookup"><span data-stu-id="d8578-124">Because it retrieves only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="d8578-125">複数のプロパティを取得するため**GetProps**が高速です。</span><span class="sxs-lookup"><span data-stu-id="d8578-125">For retrieving multiple properties, **GetProps** is faster.</span></span> 
  
<span data-ttu-id="d8578-126">設定または[HrSetOneProp](hrsetoneprop.md)関数を使用して 1 つのプロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="d8578-126">You can set or change a single property with the [HrSetOneProp](hrsetoneprop.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d8578-127">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="d8578-127">MFCMAPI reference</span></span>

<span data-ttu-id="d8578-128">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="d8578-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d8578-129">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="d8578-129">**File**</span></span>|<span data-ttu-id="d8578-130">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="d8578-130">**Function**</span></span>|<span data-ttu-id="d8578-131">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="d8578-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d8578-132">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="d8578-132">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="d8578-133">GetMAPIObjectType</span><span class="sxs-lookup"><span data-stu-id="d8578-133">GetMAPIObjectType</span></span>  <br/> |<span data-ttu-id="d8578-134">MFCMAPI では、 **HrGetOneProp**メソッドを使用して、オブジェクトの種類を取得します。</span><span class="sxs-lookup"><span data-stu-id="d8578-134">MFCMAPI uses the **HrGetOneProp** method to retrieve the type of an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d8578-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="d8578-135">See also</span></span>



<span data-ttu-id="d8578-136">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="d8578-136">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

