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
# <a name="validateparms"></a><span data-ttu-id="f41cd-103">ValidateParms</span><span class="sxs-lookup"><span data-stu-id="f41cd-103">ValidateParms</span></span>

  
  
<span data-ttu-id="f41cd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f41cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f41cd-105">内部関数を呼び出して、クライアント アプリケーションがサービス プロバイダーに渡したパラメーターを確認します。</span><span class="sxs-lookup"><span data-stu-id="f41cd-105">Calls an internal function to check the parameters client applications have passed to service providers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f41cd-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f41cd-106">Header file:</span></span>  <br/> |<span data-ttu-id="f41cd-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="f41cd-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="f41cd-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="f41cd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f41cd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f41cd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f41cd-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="f41cd-110">Called by:</span></span>  <br/> |<span data-ttu-id="f41cd-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="f41cd-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT ValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="f41cd-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f41cd-112">Parameters</span></span>

 <span data-ttu-id="f41cd-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="f41cd-113">_eMethod_</span></span>
  
> <span data-ttu-id="f41cd-114">[in]列挙で検証するメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="f41cd-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="f41cd-115">_First_</span><span class="sxs-lookup"><span data-stu-id="f41cd-115">_First_</span></span>
  
> <span data-ttu-id="f41cd-116">[in]スタックの最初の引数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f41cd-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f41cd-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="f41cd-117">Return value</span></span>

<span data-ttu-id="f41cd-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="f41cd-118">S_OK</span></span> 
  
> <span data-ttu-id="f41cd-119">すべてのパラメーターが有効です。</span><span class="sxs-lookup"><span data-stu-id="f41cd-119">All of the parameters are valid.</span></span> 
    
<span data-ttu-id="f41cd-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="f41cd-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="f41cd-121">1 つ以上のパラメーターが無効です。</span><span class="sxs-lookup"><span data-stu-id="f41cd-121">One or more of the parameters are not valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f41cd-122">注釈</span><span class="sxs-lookup"><span data-stu-id="f41cd-122">Remarks</span></span>

<span data-ttu-id="f41cd-123">MAPI とサービス プロバイダーの間で渡されるパラメーターは正しいと見なされ [、CheckParms](checkparms.md) マクロを使用してデバッグ検証のみを行います。</span><span class="sxs-lookup"><span data-stu-id="f41cd-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="f41cd-124">プロバイダーは、クライアント アプリケーションによって渡されるパラメーターを確認する必要がありますが、クライアントは MAPI パラメーターとプロバイダー パラメーターが正しいと想定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f41cd-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="f41cd-125">戻り値 **をHR_FAILED** するには、次のマクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="f41cd-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
 <span data-ttu-id="f41cd-126">**ValidateParms は** 、呼び出し元のコードが C か C++ かによって呼び出し方法が異なります。</span><span class="sxs-lookup"><span data-stu-id="f41cd-126">**ValidateParms** is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="f41cd-127">C++ は、これを呼び出す暗黙的なパラメーターを各メソッド呼び出しに渡します。これは C では明示的になり、オブジェクトのアドレスです。</span><span class="sxs-lookup"><span data-stu-id="f41cd-127">C++ passes an implicit parameter known as  _this_ to each method call, which becomes explicit in C and is the address of the object.</span></span> <span data-ttu-id="f41cd-128">最初のパラメーター  _eMethod_ は、検証されるインターフェイスとメソッドから作成された列挙子であり、スタック上で検索する必要があるパラメーターを示します。</span><span class="sxs-lookup"><span data-stu-id="f41cd-128">The first parameter,  _eMethod_, is an enumerator made from the interface and method being validated and tells what parameters to expect to find on the stack.</span></span> <span data-ttu-id="f41cd-129">2 番目のパラメーターは、C と C++ では異なります。</span><span class="sxs-lookup"><span data-stu-id="f41cd-129">The second parameter is different for C and C++.</span></span> <span data-ttu-id="f41cd-130">C++ では First  _と呼び_、検証されるメソッドの最初のパラメーターです。</span><span class="sxs-lookup"><span data-stu-id="f41cd-130">In C++ it is called  _First_, and it is the first parameter to the method being validated.</span></span> <span data-ttu-id="f41cd-131">C 言語の 2 番目のパラメーター  _ppThis_ は、常にオブジェクト ポインターであるメソッドの最初のパラメーターのアドレスです。</span><span class="sxs-lookup"><span data-stu-id="f41cd-131">The second parameter for the C language,  _ppThis_, is the address of the first parameter to the method which is always an object pointer.</span></span> <span data-ttu-id="f41cd-132">どちらの場合も、2 番目のパラメーターはメソッドのパラメーター リストの先頭のアドレスを指定し  _、eMethod_ に基づいてスタックを下に移動し、パラメーターを検証します。</span><span class="sxs-lookup"><span data-stu-id="f41cd-132">In both cases, the second parameter gives the address of the beginning of the method's parameter list, and based on  _eMethod_, moves down the stack and validates the parameters.</span></span> 
  
<span data-ttu-id="f41cd-133">**IMAPITable** や **IMAPIProp** などの一般的なインターフェイスを実装するプロバイダーは、すべてのプロバイダー間で一貫性を確保するために **、ValidateParms** 関数を使用してパラメーターを常にチェックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f41cd-133">Providers implementing common interfaces such as **IMAPITable** and **IMAPIProp** should always check parameters using the **ValidateParms** function in order to make sure consistency across all providers.</span></span> <span data-ttu-id="f41cd-134">必要に応じて、一部の複雑なパラメーター型を使用するために、追加のパラメーター検証関数が定義されています。</span><span class="sxs-lookup"><span data-stu-id="f41cd-134">Additional parameter validation functions have been defined for some complex parameter types to be used instead as appropriate.</span></span> <span data-ttu-id="f41cd-135">以下の機能については、リファレンス トピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f41cd-135">See the reference topics for the following functions:</span></span> 
  
- [<span data-ttu-id="f41cd-136">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="f41cd-136">FBadColumnSet</span></span>](fbadcolumnset.md)
    
- [<span data-ttu-id="f41cd-137">FBadEntryList</span><span class="sxs-lookup"><span data-stu-id="f41cd-137">FBadEntryList</span></span>](fbadentrylist.md)
    
- [<span data-ttu-id="f41cd-138">FBadProp</span><span class="sxs-lookup"><span data-stu-id="f41cd-138">FBadProp</span></span>](fbadprop.md)
    
- [<span data-ttu-id="f41cd-139">FBadProp</span><span class="sxs-lookup"><span data-stu-id="f41cd-139">FBadProp</span></span>](fbadprop.md)
    
- [<span data-ttu-id="f41cd-140">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="f41cd-140">FBadRestriction</span></span>](fbadrestriction.md)
    
- [<span data-ttu-id="f41cd-141">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="f41cd-141">FBadRestriction</span></span>](fbadrestriction.md)
    
- [<span data-ttu-id="f41cd-142">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="f41cd-142">FBadRglpszW</span></span>](fbadrglpszw.md)
    
- [<span data-ttu-id="f41cd-143">FBadRow</span><span class="sxs-lookup"><span data-stu-id="f41cd-143">FBadRow</span></span>](fbadrow.md)
    
- [<span data-ttu-id="f41cd-144">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="f41cd-144">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="f41cd-145">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="f41cd-145">FBadSortOrderSet</span></span>](fbadsortorderset.md)
    
<span data-ttu-id="f41cd-146">継承されたメソッドは、継承元のインターフェイスと同じパラメーター検証を使用します。</span><span class="sxs-lookup"><span data-stu-id="f41cd-146">Inherited methods use the same parameter validation as the interface from which they inherit.</span></span> <span data-ttu-id="f41cd-147">たとえば **、IMessage** と **IMAPIProp** のパラメーター チェックは同じにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f41cd-147">For example, the parameter checking for **IMessage** and **IMAPIProp** should be the same.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f41cd-148">関連項目</span><span class="sxs-lookup"><span data-stu-id="f41cd-148">See also</span></span>



[<span data-ttu-id="f41cd-149">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="f41cd-149">UlValidateParms</span></span>](ulvalidateparms.md)

