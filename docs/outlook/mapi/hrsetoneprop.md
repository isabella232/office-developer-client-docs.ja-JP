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
ms.openlocfilehash: 9fae06b9e9d5ef4885d798825659fa3486ec9e72
ms.sourcegitcommit: fb521c23df785c9c3aefa5062272b2630a32e587
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/20/2021
ms.locfileid: "52589181"
---
# <a name="hrsetoneprop"></a><span data-ttu-id="b1e1a-103">HrSetOneProp</span><span class="sxs-lookup"><span data-stu-id="b1e1a-103">HrSetOneProp</span></span>

  
  
<span data-ttu-id="b1e1a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1e1a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1e1a-105">プロパティ インターフェイス [(IMAPIProp](imapipropiunknown.md)から派生したインターフェイス) の 1 つのプロパティの値を設定または変更します。</span><span class="sxs-lookup"><span data-stu-id="b1e1a-105">Sets or changes the value of a single property on a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b1e1a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="b1e1a-106">Header file:</span></span>  <br/> |<span data-ttu-id="b1e1a-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="b1e1a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b1e1a-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="b1e1a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b1e1a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b1e1a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b1e1a-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="b1e1a-110">Called by:</span></span>  <br/> |<span data-ttu-id="b1e1a-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="b1e1a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a><span data-ttu-id="b1e1a-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b1e1a-112">Parameters</span></span>

 <span data-ttu-id="b1e1a-113">_pmp_</span><span class="sxs-lookup"><span data-stu-id="b1e1a-113">_pmp_</span></span>
  
> <span data-ttu-id="b1e1a-114">[in]プロパティ値 [を設定または変更する IMAPIProp](imapipropiunknown.md) インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b1e1a-114">[in] Pointer to an [IMAPIProp](imapipropiunknown.md) interface on which the property value is to be set or changed.</span></span> 
    
 <span data-ttu-id="b1e1a-115">_pprop_</span><span class="sxs-lookup"><span data-stu-id="b1e1a-115">_pprop_</span></span>
  
> <span data-ttu-id="b1e1a-116">[in]_pmp_ プロパティに設定する値を定義する [SPropValue](spropvalue.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b1e1a-116">[in] Pointer to the [SPropValue](spropvalue.md) structure defining the value to be set on the  _pmp_ property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b1e1a-117">Return value</span><span class="sxs-lookup"><span data-stu-id="b1e1a-117">Return value</span></span>

<span data-ttu-id="b1e1a-118">なし。</span><span class="sxs-lookup"><span data-stu-id="b1e1a-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b1e1a-119">解説</span><span class="sxs-lookup"><span data-stu-id="b1e1a-119">Remarks</span></span>

<span data-ttu-id="b1e1a-120">[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドとは異なり **、HrSetOneProp** 関数は警告を返しません。</span><span class="sxs-lookup"><span data-stu-id="b1e1a-120">Unlike the [IMAPIProp::SetProps](imapiprop-setprops.md) method, the **HrSetOneProp** function never returns any warnings.</span></span> <span data-ttu-id="b1e1a-121">プロパティは 1 つしか設定しないので、単に成功または失敗します。</span><span class="sxs-lookup"><span data-stu-id="b1e1a-121">Because it sets only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="b1e1a-122">複数のプロパティを設定または変更する場合 **、SetProps の方が** 高速です。</span><span class="sxs-lookup"><span data-stu-id="b1e1a-122">For setting or changing multiple properties, **SetProps** is faster.</span></span> 
  
<span data-ttu-id="b1e1a-123">HrGetOneProp 関数を使用して [1 つのプロパティを取得](hrgetoneprop.md) できます。</span><span class="sxs-lookup"><span data-stu-id="b1e1a-123">You can retrieve a single property with the [HrGetOneProp](hrgetoneprop.md) function.</span></span> 
  

