---
title: UlValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlValidateParameters
api_type:
- COM
ms.assetid: fb9050c9-5797-44f0-8bf5-6264f4e6d7c3
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 465069f08e2026dcbf98e24f0f5f59e12ed17eca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431275"
---
# <a name="ulvalidateparameters"></a><span data-ttu-id="33b52-103">UlValidateParameters</span><span class="sxs-lookup"><span data-stu-id="33b52-103">UlValidateParameters</span></span>

  
  
<span data-ttu-id="33b52-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33b52-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33b52-105">内部関数を呼び出して、クライアントアプリケーションがサービスプロバイダーと MAPI に渡されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="33b52-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="33b52-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="33b52-106">Header file:</span></span>  <br/> |<span data-ttu-id="33b52-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="33b52-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="33b52-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="33b52-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="33b52-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="33b52-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="33b52-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="33b52-110">Called by:</span></span>  <br/> |<span data-ttu-id="33b52-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="33b52-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="33b52-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="33b52-112">Parameters</span></span>

 <span data-ttu-id="33b52-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="33b52-113">_eMethod_</span></span>
  
> <span data-ttu-id="33b52-114">順番検証するメソッドを列挙で指定します。</span><span class="sxs-lookup"><span data-stu-id="33b52-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="33b52-115">_First_</span><span class="sxs-lookup"><span data-stu-id="33b52-115">_First_</span></span>
  
> <span data-ttu-id="33b52-116">順番スタック上の最初の引数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="33b52-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="33b52-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="33b52-117">Return value</span></span>

<span data-ttu-id="33b52-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="33b52-118">S_OK</span></span> 
  
> <span data-ttu-id="33b52-119">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="33b52-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="33b52-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="33b52-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="33b52-121">予期しないまたは不明な配信元のエラーにより、操作が完了しませんでした。</span><span class="sxs-lookup"><span data-stu-id="33b52-121">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="33b52-122">注釈</span><span class="sxs-lookup"><span data-stu-id="33b52-122">Remarks</span></span>

<span data-ttu-id="33b52-123">ulvalidateparameters マクロは[ulvalidateparameters](ulvalidateparms.md)マクロによって置き換えられました。 \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="33b52-123">The **UlValidateParameters** macro has been superseded by the [UlValidateParms](ulvalidateparms.md) macro.</span></span> <span data-ttu-id="33b52-124">**ulvalidateparameters**は RISC プラットフォームでは正しく動作せず、これでコンパイルができなくなりました。</span><span class="sxs-lookup"><span data-stu-id="33b52-124">**UlValidateParameters** does not work correctly on RISC platforms and is now prevented from compiling on them.</span></span> <span data-ttu-id="33b52-125">これは依然としてコンパイルされており、Intel プラットフォームで正常に動作しますが、 **ulvalidateparms**をすべてのプラットフォームで使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="33b52-125">It still compiles and works correctly on Intel platforms, but **UlValidateParms** is recommended on all platforms.</span></span> 
  

