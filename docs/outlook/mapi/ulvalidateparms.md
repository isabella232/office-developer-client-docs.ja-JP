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
# <a name="ulvalidateparms"></a><span data-ttu-id="93f74-103">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="93f74-103">UlValidateParms</span></span>

  
  
<span data-ttu-id="93f74-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93f74-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93f74-105">内部関数を呼び出して、クライアントアプリケーションがサービスプロバイダーと MAPI に渡されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="93f74-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="93f74-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="93f74-106">Header file:</span></span>  <br/> |<span data-ttu-id="93f74-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="93f74-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="93f74-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="93f74-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="93f74-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="93f74-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="93f74-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="93f74-110">Called by:</span></span>  <br/> |<span data-ttu-id="93f74-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="93f74-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="93f74-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="93f74-112">Parameters</span></span>

 <span data-ttu-id="93f74-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="93f74-113">_eMethod_</span></span>
  
> <span data-ttu-id="93f74-114">順番検証するメソッドを列挙で指定します。</span><span class="sxs-lookup"><span data-stu-id="93f74-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="93f74-115">_First_</span><span class="sxs-lookup"><span data-stu-id="93f74-115">_First_</span></span>
  
> <span data-ttu-id="93f74-116">順番スタック上の最初の引数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="93f74-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="93f74-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="93f74-117">Return value</span></span>

<span data-ttu-id="93f74-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="93f74-118">S_OK</span></span> 
  
> <span data-ttu-id="93f74-119">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="93f74-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="93f74-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="93f74-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="93f74-121">エラーが発生したため、操作を完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="93f74-121">An error prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="93f74-122">注釈</span><span class="sxs-lookup"><span data-stu-id="93f74-122">Remarks</span></span>

<span data-ttu-id="93f74-123">MAPI プロバイダーとサービスプロバイダー間で渡されるパラメーターは正しいと見なされ、 [checkparms](checkparms.md)マクロを使用してのみ、デバッグ検証を行います。</span><span class="sxs-lookup"><span data-stu-id="93f74-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="93f74-124">プロバイダーは、クライアントアプリケーションによって渡されたすべてのパラメーターをチェックする必要がありますが、クライアントは MAPI および provider パラメーターが正しいと想定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93f74-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="93f74-125">**HR_FAILED**マクロを使用して、戻り値をテストします。</span><span class="sxs-lookup"><span data-stu-id="93f74-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
<span data-ttu-id="93f74-126">**ulvalidateparms**マクロは、呼び出し元のコードが C または C++ のどちらであるかによって、異なる方法で呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="93f74-126">The **UlValidateParms** macro is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="93f74-127">このマクロは、HRESULT 値ではなく ULONG を返すいくつかの**IUnknown**および MAPI メソッドのパラメーターを検証するために使用されます。[validateparms](validateparms.md)マクロは、他のすべてのユーザーに対して動作します。</span><span class="sxs-lookup"><span data-stu-id="93f74-127">This macro is used to validate parameters for the few **IUnknown** and MAPI methods that return ULONG instead of HRESULT values; the [ValidateParms](validateparms.md) macro works for all others.</span></span> 
  

