---
title: ValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ValidateParms
api_type:
- COM
ms.assetid: 3ede1a35-4acc-4b8f-a1bd-027f35798a37
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f2669f703827924493387c4beac0b64b25672860
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436806"
---
# <a name="validateparms"></a><span data-ttu-id="25556-103">ValidateParms</span><span class="sxs-lookup"><span data-stu-id="25556-103">ValidateParms</span></span>

  
  
<span data-ttu-id="25556-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25556-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25556-105">内部関数を呼び出して、クライアントアプリケーションがサービスプロバイダーに渡されたパラメーターを確認します。</span><span class="sxs-lookup"><span data-stu-id="25556-105">Calls an internal function to check the parameters client applications have passed to service providers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="25556-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="25556-106">Header file:</span></span>  <br/> |<span data-ttu-id="25556-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="25556-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="25556-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="25556-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="25556-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="25556-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="25556-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="25556-110">Called by:</span></span>  <br/> |<span data-ttu-id="25556-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="25556-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT ValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="25556-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="25556-112">Parameters</span></span>

 <span data-ttu-id="25556-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="25556-113">_eMethod_</span></span>
  
> <span data-ttu-id="25556-114">順番検証するメソッドを列挙で指定します。</span><span class="sxs-lookup"><span data-stu-id="25556-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="25556-115">_First_</span><span class="sxs-lookup"><span data-stu-id="25556-115">_First_</span></span>
  
> <span data-ttu-id="25556-116">順番スタック上の最初の引数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="25556-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="25556-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="25556-117">Return value</span></span>

<span data-ttu-id="25556-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="25556-118">S_OK</span></span> 
  
> <span data-ttu-id="25556-119">すべてのパラメーターが有効です。</span><span class="sxs-lookup"><span data-stu-id="25556-119">All of the parameters are valid.</span></span> 
    
<span data-ttu-id="25556-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="25556-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="25556-121">1つ以上のパラメーターが無効です。</span><span class="sxs-lookup"><span data-stu-id="25556-121">One or more of the parameters are not valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="25556-122">注釈</span><span class="sxs-lookup"><span data-stu-id="25556-122">Remarks</span></span>

<span data-ttu-id="25556-123">MAPI プロバイダーとサービスプロバイダー間で渡されるパラメーターは正しいと見なされ、 [checkparms](checkparms.md)マクロを使用してのみ、デバッグ検証を行います。</span><span class="sxs-lookup"><span data-stu-id="25556-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="25556-124">プロバイダーは、クライアントアプリケーションによって渡されたすべてのパラメーターをチェックする必要がありますが、クライアントは MAPI および provider パラメーターが正しいと想定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="25556-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="25556-125">**HR_FAILED**マクロを使用して、戻り値をテストします。</span><span class="sxs-lookup"><span data-stu-id="25556-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
 <span data-ttu-id="25556-126">**validateparms**は、呼び出し元のコードが C または C++ のどちらであるかによって、異なる呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="25556-126">**ValidateParms** is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="25556-127">C++ は、 _this_という暗黙的なパラメーターを各メソッド呼び出しに渡します。これは、C で明示的になり、オブジェクトのアドレスです。</span><span class="sxs-lookup"><span data-stu-id="25556-127">C++ passes an implicit parameter known as  _this_ to each method call, which becomes explicit in C and is the address of the object.</span></span> <span data-ttu-id="25556-128">最初のパラメーター _eMethod_は、インターフェイスおよび検証されたメソッドからの列挙子です。スタック上で検索するパラメーターを示します。</span><span class="sxs-lookup"><span data-stu-id="25556-128">The first parameter,  _eMethod_, is an enumerator made from the interface and method being validated and tells what parameters to expect to find on the stack.</span></span> <span data-ttu-id="25556-129">2番目のパラメーターは、C および C++ とは異なります。</span><span class="sxs-lookup"><span data-stu-id="25556-129">The second parameter is different for C and C++.</span></span> <span data-ttu-id="25556-130">C++ では、_最初_に呼び出され、検証されるメソッドの最初のパラメーターです。</span><span class="sxs-lookup"><span data-stu-id="25556-130">In C++ it is called  _First_, and it is the first parameter to the method being validated.</span></span> <span data-ttu-id="25556-131">C 言語の2番目のパラメーター _ppthis_は、メソッドに対する最初のパラメーターのアドレスで、常にオブジェクトポインターです。</span><span class="sxs-lookup"><span data-stu-id="25556-131">The second parameter for the C language,  _ppThis_, is the address of the first parameter to the method which is always an object pointer.</span></span> <span data-ttu-id="25556-132">どちらの場合も、2番目のパラメーターによって、メソッドのパラメーターリストの先頭のアドレスが指定され、 _eMethod_に基づいてスタックが下に移動され、パラメーターが検証されます。</span><span class="sxs-lookup"><span data-stu-id="25556-132">In both cases, the second parameter gives the address of the beginning of the method's parameter list, and based on  _eMethod_, moves down the stack and validates the parameters.</span></span> 
  
<span data-ttu-id="25556-133">**IMAPITable**や**imapiprop**などの一般的なインターフェイスを実装するプロバイダーは、すべてのプロバイダー間で一貫性を確保するために、必ず**validateparms**関数を使用してパラメーターをチェックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="25556-133">Providers implementing common interfaces such as **IMAPITable** and **IMAPIProp** should always check parameters using the **ValidateParms** function in order to make sure consistency across all providers.</span></span> <span data-ttu-id="25556-134">その代わりに使用されるように、いくつかの複雑なパラメーターの検証関数が定義されています。</span><span class="sxs-lookup"><span data-stu-id="25556-134">Additional parameter validation functions have been defined for some complex parameter types to be used instead as appropriate.</span></span> <span data-ttu-id="25556-135">次の関数については、リファレンストピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="25556-135">See the reference topics for the following functions:</span></span> 
  
- [<span data-ttu-id="25556-136">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="25556-136">FBadColumnSet</span></span>](fbadcolumnset.md)
    
- [<span data-ttu-id="25556-137">FBadEntryList</span><span class="sxs-lookup"><span data-stu-id="25556-137">FBadEntryList</span></span>](fbadentrylist.md)
    
- [<span data-ttu-id="25556-138">FBadProp</span><span class="sxs-lookup"><span data-stu-id="25556-138">FBadProp</span></span>](fbadprop.md)
    
- [<span data-ttu-id="25556-139">FBadProp</span><span class="sxs-lookup"><span data-stu-id="25556-139">FBadProp</span></span>](fbadprop.md)
    
- [<span data-ttu-id="25556-140">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="25556-140">FBadRestriction</span></span>](fbadrestriction.md)
    
- [<span data-ttu-id="25556-141">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="25556-141">FBadRestriction</span></span>](fbadrestriction.md)
    
- [<span data-ttu-id="25556-142">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="25556-142">FBadRglpszW</span></span>](fbadrglpszw.md)
    
- [<span data-ttu-id="25556-143">FBadRow</span><span class="sxs-lookup"><span data-stu-id="25556-143">FBadRow</span></span>](fbadrow.md)
    
- [<span data-ttu-id="25556-144">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="25556-144">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="25556-145">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="25556-145">FBadSortOrderSet</span></span>](fbadsortorderset.md)
    
<span data-ttu-id="25556-146">継承されたメソッドは、継承元のインターフェイスと同じパラメーター検証を使用します。</span><span class="sxs-lookup"><span data-stu-id="25556-146">Inherited methods use the same parameter validation as the interface from which they inherit.</span></span> <span data-ttu-id="25556-147">たとえば、 **IMessage**と**imapiprop**をチェックするパラメーターは同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="25556-147">For example, the parameter checking for **IMessage** and **IMAPIProp** should be the same.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="25556-148">関連項目</span><span class="sxs-lookup"><span data-stu-id="25556-148">See also</span></span>



[<span data-ttu-id="25556-149">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="25556-149">UlValidateParms</span></span>](ulvalidateparms.md)

