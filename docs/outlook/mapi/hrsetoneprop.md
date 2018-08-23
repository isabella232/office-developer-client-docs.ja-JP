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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 31d2be027ef3b58fdd44e71c922677164d352feb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569128"
---
# <a name="hrsetoneprop"></a><span data-ttu-id="dde39-103">HrSetOneProp</span><span class="sxs-lookup"><span data-stu-id="dde39-103">HrSetOneProp</span></span>

  
  
<span data-ttu-id="dde39-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dde39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dde39-105">インターフェイスでは、プロパティ、つまり、 [IMAPIProp](imapipropiunknown.md)から派生したインターフェイスの 1 つのプロパティの値を変更または設定します。</span><span class="sxs-lookup"><span data-stu-id="dde39-105">Sets or changes the value of a single property on a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dde39-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="dde39-106">Header file:</span></span>  <br/> |<span data-ttu-id="dde39-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="dde39-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="dde39-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="dde39-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dde39-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dde39-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dde39-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="dde39-110">Called by:</span></span>  <br/> |<span data-ttu-id="dde39-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="dde39-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a><span data-ttu-id="dde39-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="dde39-112">Parameters</span></span>

 <span data-ttu-id="dde39-113">_pmp_</span><span class="sxs-lookup"><span data-stu-id="dde39-113">_pmp_</span></span>
  
> <span data-ttu-id="dde39-114">[in]プロパティの値を設定または変更するのになっている[IMAPIProp](imapipropiunknown.md)インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="dde39-114">[in] Pointer to an [IMAPIProp](imapipropiunknown.md) interface on which the property value is to be set or changed.</span></span> 
    
 <span data-ttu-id="dde39-115">_pprop_</span><span class="sxs-lookup"><span data-stu-id="dde39-115">_pprop_</span></span>
  
> <span data-ttu-id="dde39-116">[in]_Pmp_プロパティに設定する値を定義する[SPropValue](spropvalue.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="dde39-116">[in] Pointer to the [SPropValue](spropvalue.md) structure defining the value to be set on the  _pmp_ property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dde39-117">Return value</span><span class="sxs-lookup"><span data-stu-id="dde39-117">Return value</span></span>

<span data-ttu-id="dde39-118">なし。</span><span class="sxs-lookup"><span data-stu-id="dde39-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dde39-119">注釈</span><span class="sxs-lookup"><span data-stu-id="dde39-119">Remarks</span></span>

<span data-ttu-id="dde39-120">[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドとは異なり、 **HrSetOneProp**関数は決して警告を返します。</span><span class="sxs-lookup"><span data-stu-id="dde39-120">Unlike the [IMAPIProp::SetProps](imapiprop-setprops.md) method, the **HrSetOneProp** function never returns any warnings.</span></span> <span data-ttu-id="dde39-121">1 つのプロパティを設定しているため、単に成功または失敗します。</span><span class="sxs-lookup"><span data-stu-id="dde39-121">Because it sets only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="dde39-122">設定、または複数のプロパティを変更する、 **SetProps**が高速です。</span><span class="sxs-lookup"><span data-stu-id="dde39-122">For setting or changing multiple properties, **SetProps** is faster.</span></span> 
  
<span data-ttu-id="dde39-123">[HrGetOneProp](hrgetoneprop.md)関数を使用して 1 つのプロパティを取得することができます。</span><span class="sxs-lookup"><span data-stu-id="dde39-123">You can retrieve a single property with the [HrGetOneProp](hrgetoneprop.md) function.</span></span> 
  

