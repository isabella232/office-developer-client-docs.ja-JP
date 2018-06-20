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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 8af0d5c6eaff0c1e01e01c24c46f299e0c637f68
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800320"
---
# <a name="hrsetoneprop"></a><span data-ttu-id="34ce4-103">HrSetOneProp</span><span class="sxs-lookup"><span data-stu-id="34ce4-103">HrSetOneProp</span></span>

  
  
<span data-ttu-id="34ce4-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="34ce4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="34ce4-105">インターフェイスでは、プロパティ、つまり、 [IMAPIProp](imapipropiunknown.md)から派生したインターフェイスの 1 つのプロパティの値を変更または設定します。</span><span class="sxs-lookup"><span data-stu-id="34ce4-105">Sets or changes the value of a single property on a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="34ce4-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="34ce4-106">Header file:</span></span>  <br/> |<span data-ttu-id="34ce4-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="34ce4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="34ce4-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="34ce4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="34ce4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="34ce4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="34ce4-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="34ce4-110">Called by:</span></span>  <br/> |<span data-ttu-id="34ce4-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="34ce4-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a><span data-ttu-id="34ce4-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="34ce4-112">Parameters</span></span>

 <span data-ttu-id="34ce4-113">_pmp_</span><span class="sxs-lookup"><span data-stu-id="34ce4-113">_pmp_</span></span>
  
> <span data-ttu-id="34ce4-114">[in]プロパティの値を設定または変更するのになっている[IMAPIProp](imapipropiunknown.md)インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="34ce4-114">[in] Pointer to an [IMAPIProp](imapipropiunknown.md) interface on which the property value is to be set or changed.</span></span> 
    
 <span data-ttu-id="34ce4-115">_pprop_</span><span class="sxs-lookup"><span data-stu-id="34ce4-115">_pprop_</span></span>
  
> <span data-ttu-id="34ce4-116">[in]_Pmp_プロパティに設定する値を定義する[SPropValue](spropvalue.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="34ce4-116">[in] Pointer to the [SPropValue](spropvalue.md) structure defining the value to be set on the  _pmp_ property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="34ce4-117">Return value</span><span class="sxs-lookup"><span data-stu-id="34ce4-117">Return value</span></span>

<span data-ttu-id="34ce4-118">なし。</span><span class="sxs-lookup"><span data-stu-id="34ce4-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="34ce4-119">備考</span><span class="sxs-lookup"><span data-stu-id="34ce4-119">Remarks</span></span>

<span data-ttu-id="34ce4-120">[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドとは異なり、 **HrSetOneProp**関数は決して警告を返します。</span><span class="sxs-lookup"><span data-stu-id="34ce4-120">Unlike the [IMAPIProp::SetProps](imapiprop-setprops.md) method, the **HrSetOneProp** function never returns any warnings.</span></span> <span data-ttu-id="34ce4-121">1 つのプロパティを設定しているため、単に成功または失敗します。</span><span class="sxs-lookup"><span data-stu-id="34ce4-121">Because it sets only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="34ce4-122">設定、または複数のプロパティを変更する、 **SetProps**が高速です。</span><span class="sxs-lookup"><span data-stu-id="34ce4-122">For setting or changing multiple properties, **SetProps** is faster.</span></span> 
  
<span data-ttu-id="34ce4-123">[HrGetOneProp](hrgetoneprop.md)関数を使用して 1 つのプロパティを取得することができます。</span><span class="sxs-lookup"><span data-stu-id="34ce4-123">You can retrieve a single property with the [HrGetOneProp](hrgetoneprop.md) function.</span></span> 
  

