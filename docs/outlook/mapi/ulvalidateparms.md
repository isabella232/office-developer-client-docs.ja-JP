---
title: UlValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlValidateParms
api_type:
- COM
ms.assetid: 02c66b46-1f01-43fb-832c-bac27aaae19f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e0cdcb92238dd4dffbcd6514e698e5511b05bf45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419612"
---
# <a name="ulvalidateparms"></a><span data-ttu-id="f2727-103">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="f2727-103">UlValidateParms</span></span>

  
  
<span data-ttu-id="f2727-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2727-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2727-105">内部関数を呼び出して、クライアント アプリケーションがサービス プロバイダーと MAPI に渡したパラメーターを確認します。</span><span class="sxs-lookup"><span data-stu-id="f2727-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f2727-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f2727-106">Header file:</span></span>  <br/> |<span data-ttu-id="f2727-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="f2727-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="f2727-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="f2727-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f2727-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f2727-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f2727-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="f2727-110">Called by:</span></span>  <br/> |<span data-ttu-id="f2727-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="f2727-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="f2727-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f2727-112">Parameters</span></span>

 <span data-ttu-id="f2727-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="f2727-113">_eMethod_</span></span>
  
> <span data-ttu-id="f2727-114">[in]列挙で検証するメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="f2727-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="f2727-115">_First_</span><span class="sxs-lookup"><span data-stu-id="f2727-115">_First_</span></span>
  
> <span data-ttu-id="f2727-116">[in]スタックの最初の引数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f2727-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f2727-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="f2727-117">Return value</span></span>

<span data-ttu-id="f2727-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="f2727-118">S_OK</span></span> 
  
> <span data-ttu-id="f2727-119">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="f2727-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="f2727-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="f2727-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="f2727-121">エラーが発生すると、操作が完了しきれなかった。</span><span class="sxs-lookup"><span data-stu-id="f2727-121">An error prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f2727-122">注釈</span><span class="sxs-lookup"><span data-stu-id="f2727-122">Remarks</span></span>

<span data-ttu-id="f2727-123">MAPI とサービス プロバイダーの間で渡されるパラメーターは正しいと見なされ [、CheckParms](checkparms.md) マクロを使用してデバッグ検証のみを行います。</span><span class="sxs-lookup"><span data-stu-id="f2727-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="f2727-124">プロバイダーは、クライアント アプリケーションによって渡されるパラメーターを確認する必要がありますが、クライアントは MAPI パラメーターとプロバイダー パラメーターが正しいと想定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f2727-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="f2727-125">戻り値 **をHR_FAILED** するには、次のマクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="f2727-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
<span data-ttu-id="f2727-126">**UlValidateParms** マクロの呼び出し方法は、呼び出し元のコードが C か C++かによって異なります。</span><span class="sxs-lookup"><span data-stu-id="f2727-126">The **UlValidateParms** macro is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="f2727-127">このマクロは、HRESULT 値の代わりに ULONG を返す少数の **IUnknown** メソッドおよび MAPI メソッドのパラメーターを検証するために使用されます。 [ValidateParms マクロは](validateparms.md) 、他のすべてのユーザーに対して機能します。</span><span class="sxs-lookup"><span data-stu-id="f2727-127">This macro is used to validate parameters for the few **IUnknown** and MAPI methods that return ULONG instead of HRESULT values; the [ValidateParms](validateparms.md) macro works for all others.</span></span> 
  

