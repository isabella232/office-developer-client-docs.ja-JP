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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7b29eab30677dae7f720cecd9fde71e8bbbf752c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579719"
---
# <a name="validateparms"></a><span data-ttu-id="14bc6-103">ValidateParms</span><span class="sxs-lookup"><span data-stu-id="14bc6-103">ValidateParms</span></span>

  
  
<span data-ttu-id="14bc6-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="14bc6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="14bc6-105">パラメーターのクライアント アプリケーションがサービス プロバイダーに渡されますが確認するのには内部の関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="14bc6-105">Calls an internal function to check the parameters client applications have passed to service providers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="14bc6-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="14bc6-106">Header file:</span></span>  <br/> |<span data-ttu-id="14bc6-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="14bc6-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="14bc6-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="14bc6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="14bc6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="14bc6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="14bc6-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="14bc6-110">Called by:</span></span>  <br/> |<span data-ttu-id="14bc6-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="14bc6-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT ValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="14bc6-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14bc6-112">Parameters</span></span>

 <span data-ttu-id="14bc6-113">_」方法_</span><span class="sxs-lookup"><span data-stu-id="14bc6-113">_eMethod_</span></span>
  
> <span data-ttu-id="14bc6-114">[in]確認する方法を列挙型を指定します。</span><span class="sxs-lookup"><span data-stu-id="14bc6-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="14bc6-115">_First/先頭のレコード_</span><span class="sxs-lookup"><span data-stu-id="14bc6-115">_First_</span></span>
  
> <span data-ttu-id="14bc6-116">[in]スタック上の最初の引数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="14bc6-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="14bc6-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="14bc6-117">Return value</span></span>

<span data-ttu-id="14bc6-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="14bc6-118">S_OK</span></span> 
  
> <span data-ttu-id="14bc6-119">すべてのパラメーターは、有効です。</span><span class="sxs-lookup"><span data-stu-id="14bc6-119">All of the parameters are valid.</span></span> 
    
<span data-ttu-id="14bc6-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="14bc6-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="14bc6-121">1 つまたは複数のパラメーターが有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="14bc6-121">One or more of the parameters are not valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="14bc6-122">注釈</span><span class="sxs-lookup"><span data-stu-id="14bc6-122">Remarks</span></span>

<span data-ttu-id="14bc6-123">MAPI とサービスの間で渡されるパラメーターを正しくし、 [CheckParms](checkparms.md)マクロのデバッグ検証のみを行うプロバイダーと見なされます。</span><span class="sxs-lookup"><span data-stu-id="14bc6-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="14bc6-124">プロバイダーは、クライアント アプリケーションによって渡されるすべてのパラメーターを確認する必要がありますが、クライアントが MAPI およびプロバイダーのパラメーターが正しいことを想定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="14bc6-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="14bc6-125">戻り値をテストするのにには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="14bc6-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
 <span data-ttu-id="14bc6-126">**ValidateParms**は、呼び出し元のコードが C または C++ のどちらであるかに応じて異なる方法で呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="14bc6-126">**ValidateParms** is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="14bc6-127">C++ では、各メソッドの呼び出しに、c 言語では明示的になり、オブジェクトのアドレスを_この_と呼ばれる暗黙のパラメーターを渡します。</span><span class="sxs-lookup"><span data-stu-id="14bc6-127">C++ passes an implicit parameter known as  _this_ to each method call, which becomes explicit in C and is the address of the object.</span></span> <span data-ttu-id="14bc6-128">_」方法_では、最初のパラメーターを使用して、列挙子インターフェイスとメソッドの検証対象からは、スタックで見つけられるには、どのようなパラメーターを示します。</span><span class="sxs-lookup"><span data-stu-id="14bc6-128">The first parameter,  _eMethod_, is an enumerator made from the interface and method being validated and tells what parameters to expect to find on the stack.</span></span> <span data-ttu-id="14bc6-129">2 番目のパラメーターは、C および C++ では異なります。</span><span class="sxs-lookup"><span data-stu-id="14bc6-129">The second parameter is different for C and C++.</span></span> <span data-ttu-id="14bc6-130">C++ では、_最初_と呼びますが最初のパラメーターを検証するメソッド。</span><span class="sxs-lookup"><span data-stu-id="14bc6-130">In C++ it is called  _First_, and it is the first parameter to the method being validated.</span></span> <span data-ttu-id="14bc6-131">C 言語、 _ppThis_の 2 番目のパラメーターは、常にオブジェクト ポインターであるメソッドの最初のパラメーターのアドレスです。</span><span class="sxs-lookup"><span data-stu-id="14bc6-131">The second parameter for the C language,  _ppThis_, is the address of the first parameter to the method which is always an object pointer.</span></span> <span data-ttu-id="14bc6-132">どちらの場合も、2 番目のパラメーター、メソッドのパラメーター リストの先頭のアドレスでは、 _」方法_に基づく、スタックの下に移動し、パラメーターを検証します。</span><span class="sxs-lookup"><span data-stu-id="14bc6-132">In both cases, the second parameter gives the address of the beginning of the method's parameter list, and based on  _eMethod_, moves down the stack and validates the parameters.</span></span> 
  
<span data-ttu-id="14bc6-133">**IMAPITable**や**IMAPIProp**などの一般的なインターフェイスを実装するプロバイダーでは、すべてのプロバイダー間での整合性の確認を行うために、 **ValidateParms**関数を使用してパラメーターを常に確認しています。</span><span class="sxs-lookup"><span data-stu-id="14bc6-133">Providers implementing common interfaces such as **IMAPITable** and **IMAPIProp** should always check parameters using the **ValidateParms** function in order to make sure consistency across all providers.</span></span> <span data-ttu-id="14bc6-134">追加のパラメーターの検証関数は、必要に応じてその代わりに使用するいくつかの複雑なパラメーター型の定義されています。</span><span class="sxs-lookup"><span data-stu-id="14bc6-134">Additional parameter validation functions have been defined for some complex parameter types to be used instead as appropriate.</span></span> <span data-ttu-id="14bc6-135">次の関数のリファレンス トピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="14bc6-135">See the reference topics for the following functions:</span></span> 
  
- [<span data-ttu-id="14bc6-136">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="14bc6-136">FBadColumnSet</span></span>](fbadcolumnset.md)
    
- [<span data-ttu-id="14bc6-137">FBadEntryList</span><span class="sxs-lookup"><span data-stu-id="14bc6-137">FBadEntryList</span></span>](fbadentrylist.md)
    
- [<span data-ttu-id="14bc6-138">FBadProp</span><span class="sxs-lookup"><span data-stu-id="14bc6-138">FBadProp</span></span>](fbadprop.md)
    
- [<span data-ttu-id="14bc6-139">FBadProp</span><span class="sxs-lookup"><span data-stu-id="14bc6-139">FBadProp</span></span>](fbadprop.md)
    
- [<span data-ttu-id="14bc6-140">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="14bc6-140">FBadRestriction</span></span>](fbadrestriction.md)
    
- [<span data-ttu-id="14bc6-141">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="14bc6-141">FBadRestriction</span></span>](fbadrestriction.md)
    
- [<span data-ttu-id="14bc6-142">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="14bc6-142">FBadRglpszW</span></span>](fbadrglpszw.md)
    
- [<span data-ttu-id="14bc6-143">FBadRow</span><span class="sxs-lookup"><span data-stu-id="14bc6-143">FBadRow</span></span>](fbadrow.md)
    
- [<span data-ttu-id="14bc6-144">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="14bc6-144">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="14bc6-145">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="14bc6-145">FBadSortOrderSet</span></span>](fbadsortorderset.md)
    
<span data-ttu-id="14bc6-146">継承されたメソッドは、継承元となるインターフェイスとして同じパラメーターの検証を使用します。</span><span class="sxs-lookup"><span data-stu-id="14bc6-146">Inherited methods use the same parameter validation as the interface from which they inherit.</span></span> <span data-ttu-id="14bc6-147">**IMessage**および**IMAPIProp**をチェックするパラメーターは、同じにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="14bc6-147">For example, the parameter checking for **IMessage** and **IMAPIProp** should be the same.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="14bc6-148">関連項目</span><span class="sxs-lookup"><span data-stu-id="14bc6-148">See also</span></span>



[<span data-ttu-id="14bc6-149">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="14bc6-149">UlValidateParms</span></span>](ulvalidateparms.md)

