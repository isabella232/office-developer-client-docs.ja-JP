---
title: ValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ValidateParameters
api_type:
- COM
ms.assetid: 80aadd11-5409-4636-8fad-fa2206336671
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b3862ea539907bb0570a0e845b09a15e7bed0507
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425204"
---
# <a name="validateparameters"></a><span data-ttu-id="0a2a2-103">ValidateParameters</span><span class="sxs-lookup"><span data-stu-id="0a2a2-103">ValidateParameters</span></span>

  
  
<span data-ttu-id="0a2a2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a2a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a2a2-105">内部関数を呼び出して、クライアント アプリケーションがサービス プロバイダーに渡したパラメーターを確認します。</span><span class="sxs-lookup"><span data-stu-id="0a2a2-105">Calls an internal function to check the parameters client applications have passed to service providers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0a2a2-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0a2a2-106">Header file:</span></span>  <br/> |<span data-ttu-id="0a2a2-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="0a2a2-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="0a2a2-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="0a2a2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0a2a2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0a2a2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0a2a2-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="0a2a2-110">Called by:</span></span>  <br/> |<span data-ttu-id="0a2a2-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="0a2a2-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT ValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="0a2a2-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0a2a2-112">Parameters</span></span>

 <span data-ttu-id="0a2a2-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="0a2a2-113">_eMethod_</span></span>
  
> <span data-ttu-id="0a2a2-114">[in]列挙で検証するメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="0a2a2-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="0a2a2-115">_First_</span><span class="sxs-lookup"><span data-stu-id="0a2a2-115">_First_</span></span>
  
> <span data-ttu-id="0a2a2-116">[in]スタックの最初の引数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0a2a2-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0a2a2-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="0a2a2-117">Return value</span></span>

<span data-ttu-id="0a2a2-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="0a2a2-118">S_OK</span></span> 
  
> <span data-ttu-id="0a2a2-119">すべてのパラメーターが有効です。</span><span class="sxs-lookup"><span data-stu-id="0a2a2-119">All of the parameters are valid.</span></span> 
    
<span data-ttu-id="0a2a2-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="0a2a2-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="0a2a2-121">1 つ以上のパラメーターが無効です。</span><span class="sxs-lookup"><span data-stu-id="0a2a2-121">One or more of the parameters are not valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0a2a2-122">注釈</span><span class="sxs-lookup"><span data-stu-id="0a2a2-122">Remarks</span></span>

<span data-ttu-id="0a2a2-123">**ValidateParameters マクロ** は [ValidateParms マクロに取ってかえ](validateparms.md)されています。</span><span class="sxs-lookup"><span data-stu-id="0a2a2-123">The **ValidateParameters** macro has been superseded by the [ValidateParms](validateparms.md) macro.</span></span> <span data-ttu-id="0a2a2-124">**ValidateParameters** は RISC プラットフォームで正しく動作し、コンパイルが行えなくなります。</span><span class="sxs-lookup"><span data-stu-id="0a2a2-124">**ValidateParameters** does not work correctly on RISC platforms and is now prevented from compiling on them.</span></span> <span data-ttu-id="0a2a2-125">Intel プラットフォームではコンパイルおよび正常に動作しますが **、ValidateParms は** すべてのプラットフォームで推奨されます。</span><span class="sxs-lookup"><span data-stu-id="0a2a2-125">It still compiles and works correctly on Intel platforms, but **ValidateParms** is recommended on all platforms.</span></span> 
  

