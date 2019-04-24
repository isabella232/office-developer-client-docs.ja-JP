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
ms.openlocfilehash: e5adc7d0c317d8b803645d78227777998d7d241f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347839"
---
# <a name="hrgetoneprop"></a><span data-ttu-id="18801-103">HrGetOneProp</span><span class="sxs-lookup"><span data-stu-id="18801-103">HrGetOneProp</span></span>

  
  
<span data-ttu-id="18801-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18801-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18801-105">プロパティインターフェイス ( [imapiprop](imapipropiunknown.md)から派生したインターフェイス) から1つのプロパティの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="18801-105">Retrieves the value of a single property from a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="18801-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="18801-106">Header file:</span></span>  <br/> |<span data-ttu-id="18801-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="18801-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="18801-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="18801-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="18801-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="18801-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="18801-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="18801-110">Called by:</span></span>  <br/> |<span data-ttu-id="18801-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="18801-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a><span data-ttu-id="18801-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="18801-112">Parameters</span></span>

 <span data-ttu-id="18801-113">_pmp_</span><span class="sxs-lookup"><span data-stu-id="18801-113">_pmp_</span></span>
  
> <span data-ttu-id="18801-114">順番プロパティ値を取得する[imapiprop](imapipropiunknown.md)インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="18801-114">[in] Pointer to the [IMAPIProp](imapipropiunknown.md) interface from which the property value is to be retrieved.</span></span> 
    
 <span data-ttu-id="18801-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="18801-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="18801-116">順番取得するプロパティのプロパティタグ。</span><span class="sxs-lookup"><span data-stu-id="18801-116">[in] Property tag of the property to be retrieved.</span></span> 
    
 <span data-ttu-id="18801-117">_ppprop_</span><span class="sxs-lookup"><span data-stu-id="18801-117">_ppprop_</span></span>
  
> <span data-ttu-id="18801-118">読み上げ取得したプロパティ値を定義する、返された[spropvalue](spropvalue.md)構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="18801-118">[out] Pointer to a pointer to the returned [SPropValue](spropvalue.md) structure defining the retrieved property value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="18801-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="18801-119">Return value</span></span>

<span data-ttu-id="18801-120">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="18801-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="18801-121">要求されたプロパティは、指定したインターフェイスからは使用できません。</span><span class="sxs-lookup"><span data-stu-id="18801-121">The requested property is not available from the specified interface.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="18801-122">解説</span><span class="sxs-lookup"><span data-stu-id="18801-122">Remarks</span></span>

<span data-ttu-id="18801-123">[imapiprop:: GetProps](imapiprop-getprops.md)メソッドとは異なり、 **hrgetoneprop**関数は警告を返しません。</span><span class="sxs-lookup"><span data-stu-id="18801-123">Unlike the [IMAPIProp::GetProps](imapiprop-getprops.md) method, the **HrGetOneProp** function never returns any warning.</span></span> <span data-ttu-id="18801-124">プロパティを1つだけ取得するので、成功または失敗のどちらかです。</span><span class="sxs-lookup"><span data-stu-id="18801-124">Because it retrieves only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="18801-125">複数のプロパティを取得する場合、 **GetProps**の方が高速です。</span><span class="sxs-lookup"><span data-stu-id="18801-125">For retrieving multiple properties, **GetProps** is faster.</span></span> 
  
<span data-ttu-id="18801-126">[hrsetoneprop](hrsetoneprop.md)関数を使用して、1つのプロパティを設定または変更できます。</span><span class="sxs-lookup"><span data-stu-id="18801-126">You can set or change a single property with the [HrSetOneProp](hrsetoneprop.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="18801-127">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="18801-127">MFCMAPI reference</span></span>

<span data-ttu-id="18801-128">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="18801-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="18801-129">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="18801-129">**File**</span></span>|<span data-ttu-id="18801-130">**関数**</span><span class="sxs-lookup"><span data-stu-id="18801-130">**Function**</span></span>|<span data-ttu-id="18801-131">**コメント**</span><span class="sxs-lookup"><span data-stu-id="18801-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="18801-132">MAPIFunctions</span><span class="sxs-lookup"><span data-stu-id="18801-132">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="18801-133">GetMAPIObjectType</span><span class="sxs-lookup"><span data-stu-id="18801-133">GetMAPIObjectType</span></span>  <br/> |<span data-ttu-id="18801-134">mfcmapi は、 **hrgetoneprop**メソッドを使用して、オブジェクトの種類を取得します。</span><span class="sxs-lookup"><span data-stu-id="18801-134">MFCMAPI uses the **HrGetOneProp** method to retrieve the type of an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="18801-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="18801-135">See also</span></span>



<span data-ttu-id="18801-136">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="18801-136">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

