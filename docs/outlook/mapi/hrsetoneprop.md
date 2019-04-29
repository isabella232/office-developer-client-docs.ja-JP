---
title: HrSetOneProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrSetOneProp
api_type:
- COM
ms.assetid: 14ae3242-fddf-4199-a9a7-4ab153b31064
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 37e6560d859ce4731b7a06e571eb38eb160c3686
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417659"
---
# <a name="hrsetoneprop"></a><span data-ttu-id="88939-103">HrSetOneProp</span><span class="sxs-lookup"><span data-stu-id="88939-103">HrSetOneProp</span></span>

  
  
<span data-ttu-id="88939-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88939-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88939-105">プロパティインターフェイスの1つのプロパティの値を設定または変更します。つまり、 [imapiprop](imapipropiunknown.md)から派生したインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="88939-105">Sets or changes the value of a single property on a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="88939-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="88939-106">Header file:</span></span>  <br/> |<span data-ttu-id="88939-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="88939-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="88939-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="88939-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="88939-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="88939-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="88939-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="88939-110">Called by:</span></span>  <br/> |<span data-ttu-id="88939-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="88939-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a><span data-ttu-id="88939-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="88939-112">Parameters</span></span>

 <span data-ttu-id="88939-113">_pmp_</span><span class="sxs-lookup"><span data-stu-id="88939-113">_pmp_</span></span>
  
> <span data-ttu-id="88939-114">順番プロパティ値を設定または変更する[imapiprop](imapipropiunknown.md)インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="88939-114">[in] Pointer to an [IMAPIProp](imapipropiunknown.md) interface on which the property value is to be set or changed.</span></span> 
    
 <span data-ttu-id="88939-115">_pprop_</span><span class="sxs-lookup"><span data-stu-id="88939-115">_pprop_</span></span>
  
> <span data-ttu-id="88939-116">順番_pmp_プロパティに設定する値を定義する[spropvalue](spropvalue.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="88939-116">[in] Pointer to the [SPropValue](spropvalue.md) structure defining the value to be set on the  _pmp_ property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="88939-117">Return value</span><span class="sxs-lookup"><span data-stu-id="88939-117">Return value</span></span>

<span data-ttu-id="88939-118">なし。</span><span class="sxs-lookup"><span data-stu-id="88939-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="88939-119">注釈</span><span class="sxs-lookup"><span data-stu-id="88939-119">Remarks</span></span>

<span data-ttu-id="88939-120">[imapiprop:: setprops](imapiprop-setprops.md)メソッドとは異なり、 **hrsetoneprop**関数は警告を返しません。</span><span class="sxs-lookup"><span data-stu-id="88939-120">Unlike the [IMAPIProp::SetProps](imapiprop-setprops.md) method, the **HrSetOneProp** function never returns any warnings.</span></span> <span data-ttu-id="88939-121">1つのプロパティしか設定しないため、成功または失敗のどちらかです。</span><span class="sxs-lookup"><span data-stu-id="88939-121">Because it sets only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="88939-122">複数のプロパティを設定または変更する場合は、 **setprops**の方が高速です。</span><span class="sxs-lookup"><span data-stu-id="88939-122">For setting or changing multiple properties, **SetProps** is faster.</span></span> 
  
<span data-ttu-id="88939-123">[hrgetoneprop](hrgetoneprop.md)関数を使用して、1つのプロパティを取得できます。</span><span class="sxs-lookup"><span data-stu-id="88939-123">You can retrieve a single property with the [HrGetOneProp](hrgetoneprop.md) function.</span></span> 
  

