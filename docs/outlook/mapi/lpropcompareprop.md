---
title: LPropCompareProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LPropCompareProp
api_type:
- COM
ms.assetid: f14ad568-fe45-4875-957d-415d39dc6f28
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7417ddeb814cafb954d5ab80a6dae771fd0f7a79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414614"
---
# <a name="lpropcompareprop"></a><span data-ttu-id="262d4-103">LPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="262d4-103">LPropCompareProp</span></span>

  
  
<span data-ttu-id="262d4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="262d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="262d4-105">2つのプロパティ値が等しいかどうかを比較します。</span><span class="sxs-lookup"><span data-stu-id="262d4-105">Compares two property values to determine whether they are equal.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="262d4-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="262d4-106">Header file:</span></span>  <br/> |<span data-ttu-id="262d4-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="262d4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="262d4-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="262d4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="262d4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="262d4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="262d4-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="262d4-110">Called by:</span></span>  <br/> |<span data-ttu-id="262d4-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="262d4-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG LPropCompareProp(
  LPSPropValue lpSPropValueA,
  LPSPropValue lpSPropValueB
);
```

## <a name="parameters"></a><span data-ttu-id="262d4-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="262d4-112">Parameters</span></span>

 <span data-ttu-id="262d4-113">_lpspropvaluea_</span><span class="sxs-lookup"><span data-stu-id="262d4-113">_lpSPropValueA_</span></span>
  
> <span data-ttu-id="262d4-114">順番比較する最初のプロパティ値を定義する[spropvalue](spropvalue.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="262d4-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value to be compared.</span></span> 
    
 <span data-ttu-id="262d4-115">_lpspropvalueb_</span><span class="sxs-lookup"><span data-stu-id="262d4-115">_lpSPropValueB_</span></span>
  
> <span data-ttu-id="262d4-116">順番比較する2番目のプロパティ値を定義する**spropvalue**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="262d4-116">[in] Pointer to an **SPropValue** structure defining the second property value to be compared.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="262d4-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="262d4-117">Return value</span></span>

 <span data-ttu-id="262d4-118">**lpropcompareprop**は、ほとんどのプロパティの種類について、次のいずれかの値を返します。</span><span class="sxs-lookup"><span data-stu-id="262d4-118">**LPropCompareProp** returns one of the following values for most property types:</span></span> 
  
- <span data-ttu-id="262d4-119">_lpspropvaluea_パラメーターによって指定された値が_lpspropvaluea_パラメーターによって示される値よりも小さい場合は、0未満です。</span><span class="sxs-lookup"><span data-stu-id="262d4-119">Less than zero if the value indicated by the  _lpSPropValueA_ parameter is less than that indicated by the  _lpSPropValueB_ parameter.</span></span> 
    
- <span data-ttu-id="262d4-120">_lpspropvaluea_で指定された値が_lpspropvaluea_で示される値よりも大きい場合は、0より大きい値を指定します。</span><span class="sxs-lookup"><span data-stu-id="262d4-120">Greater than zero if the value indicated by  _lpSPropValueA_ is greater than that indicated by  _lpSPropValueB_.</span></span>
    
- <span data-ttu-id="262d4-121">_lpspropvaluea_で指定された値が_lpspropvaluea_によって示される値と等しい場合は0。</span><span class="sxs-lookup"><span data-stu-id="262d4-121">Zero if the value indicated by  _lpSPropValueA_ equals the value indicated by  _lpSPropValueB_.</span></span> 
    
<span data-ttu-id="262d4-122">ブール型 (Boolean) やエラーの種類など、組み込みの順序付けを持たないプロパティの種類の場合、 **lpropcompareprop**関数は、2つのプロパティの値が等しくない場合に未定義の値を返します。</span><span class="sxs-lookup"><span data-stu-id="262d4-122">For property types that have no intrinsic ordering, such as Boolean or error types, the **LPropCompareProp** function returns an undefined value if the two property values are not equal.</span></span> <span data-ttu-id="262d4-123">この未定義の値は、0以外の呼び出しで一貫しています。</span><span class="sxs-lookup"><span data-stu-id="262d4-123">This undefined value is nonzero and consistent across calls.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="262d4-124">注釈</span><span class="sxs-lookup"><span data-stu-id="262d4-124">Remarks</span></span>

<span data-ttu-id="262d4-125">2つのプロパティの比較対象の型が同じ場合にのみ、 **lpropcompareprop**関数を使用してください。</span><span class="sxs-lookup"><span data-stu-id="262d4-125">Use the **LPropCompareProp** function only if the types of the two properties to be compared are the same.</span></span> 
  
<span data-ttu-id="262d4-126">**lpropcompareprop**を呼び出す前に、クライアントアプリケーションまたはサービスプロバイダーは、 [imapiprop:: GetProps](imapiprop-getprops.md)メソッドの呼び出しと比較するプロパティを最初に取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="262d4-126">Before calling **LPropCompareProp**, a client application or service provider must first retrieve the properties for comparison with a call to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="262d4-127">クライアントまたはプロバイダーが**lpropcompareprop**を呼び出すと、まず、プロパティの値の比較が有効であることを確認するために、最初にプロパティタグを調べます。</span><span class="sxs-lookup"><span data-stu-id="262d4-127">When a client or provider calls **LPropCompareProp**, the function first examines the property tags to make sure that the comparison of property values is valid.</span></span> <span data-ttu-id="262d4-128">次に、プロパティの値を比較し、適切な値を返します。</span><span class="sxs-lookup"><span data-stu-id="262d4-128">The function then compares the property values, returning an appropriate value.</span></span> 
  
<span data-ttu-id="262d4-129">プロパティの値が等しくない場合は、 **lpropcompareprop**によって、どちらが大きくなるかが決まります。</span><span class="sxs-lookup"><span data-stu-id="262d4-129">If the property values are unequal, **LPropCompareProp** determines which one is the greater.</span></span> <span data-ttu-id="262d4-130">**lpropcompareprop**と比較するプロパティは、同じオブジェクトに属している必要はありません。</span><span class="sxs-lookup"><span data-stu-id="262d4-130">The properties that **LPropCompareProp** compares do not have to belong to the same object.</span></span> 
  

