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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e0cdcb92238dd4dffbcd6514e698e5511b05bf45
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360495"
---
# <a name="ulvalidateparms"></a><span data-ttu-id="7fa17-103">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="7fa17-103">UlValidateParms</span></span>

  
  
<span data-ttu-id="7fa17-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7fa17-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7fa17-105">内部関数を呼び出して、クライアントアプリケーションがサービスプロバイダーと MAPI に渡されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="7fa17-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7fa17-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="7fa17-106">Header file:</span></span>  <br/> |<span data-ttu-id="7fa17-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="7fa17-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="7fa17-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="7fa17-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7fa17-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7fa17-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7fa17-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="7fa17-110">Called by:</span></span>  <br/> |<span data-ttu-id="7fa17-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="7fa17-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="7fa17-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7fa17-112">Parameters</span></span>

 <span data-ttu-id="7fa17-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="7fa17-113">_eMethod_</span></span>
  
> <span data-ttu-id="7fa17-114">順番検証するメソッドを列挙で指定します。</span><span class="sxs-lookup"><span data-stu-id="7fa17-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="7fa17-115">_First_</span><span class="sxs-lookup"><span data-stu-id="7fa17-115">_First_</span></span>
  
> <span data-ttu-id="7fa17-116">順番スタック上の最初の引数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7fa17-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7fa17-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="7fa17-117">Return value</span></span>

<span data-ttu-id="7fa17-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="7fa17-118">S_OK</span></span> 
  
> <span data-ttu-id="7fa17-119">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="7fa17-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="7fa17-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="7fa17-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="7fa17-121">エラーが発生したため、操作を完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="7fa17-121">An error prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7fa17-122">解説</span><span class="sxs-lookup"><span data-stu-id="7fa17-122">Remarks</span></span>

<span data-ttu-id="7fa17-123">MAPI プロバイダーとサービスプロバイダー間で渡されるパラメーターは正しいと見なされ、 [checkparms](checkparms.md)マクロを使用してのみ、デバッグ検証を行います。</span><span class="sxs-lookup"><span data-stu-id="7fa17-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="7fa17-124">プロバイダーは、クライアントアプリケーションによって渡されたすべてのパラメーターをチェックする必要がありますが、クライアントは MAPI および provider パラメーターが正しいと想定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7fa17-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="7fa17-125">**HR_FAILED**マクロを使用して、戻り値をテストします。</span><span class="sxs-lookup"><span data-stu-id="7fa17-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
<span data-ttu-id="7fa17-126">**ulvalidateparms**マクロは、呼び出し元のコードが C または C++ のどちらであるかによって、異なる方法で呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7fa17-126">The **UlValidateParms** macro is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="7fa17-127">このマクロは、HRESULT 値ではなく ULONG を返すいくつかの**IUnknown**および MAPI メソッドのパラメーターを検証するために使用されます。[validateparms](validateparms.md)マクロは、他のすべてのユーザーに対して動作します。</span><span class="sxs-lookup"><span data-stu-id="7fa17-127">This macro is used to validate parameters for the few **IUnknown** and MAPI methods that return ULONG instead of HRESULT values; the [ValidateParms](validateparms.md) macro works for all others.</span></span> 
  

