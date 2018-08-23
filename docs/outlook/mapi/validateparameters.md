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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 662330a7b8c665471e9bbe6af27dff84ee68c8cf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586068"
---
# <a name="validateparameters"></a><span data-ttu-id="1818b-103">ValidateParameters</span><span class="sxs-lookup"><span data-stu-id="1818b-103">ValidateParameters</span></span>

  
  
<span data-ttu-id="1818b-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1818b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1818b-105">パラメーターのクライアント アプリケーションがサービス プロバイダーに渡されますが確認するのには内部の関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1818b-105">Calls an internal function to check the parameters client applications have passed to service providers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1818b-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="1818b-106">Header file:</span></span>  <br/> |<span data-ttu-id="1818b-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="1818b-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="1818b-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="1818b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1818b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1818b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1818b-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="1818b-110">Called by:</span></span>  <br/> |<span data-ttu-id="1818b-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="1818b-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT ValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="1818b-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1818b-112">Parameters</span></span>

 <span data-ttu-id="1818b-113">_」方法_</span><span class="sxs-lookup"><span data-stu-id="1818b-113">_eMethod_</span></span>
  
> <span data-ttu-id="1818b-114">[in]確認する方法を列挙型を指定します。</span><span class="sxs-lookup"><span data-stu-id="1818b-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="1818b-115">_First/先頭のレコード_</span><span class="sxs-lookup"><span data-stu-id="1818b-115">_First_</span></span>
  
> <span data-ttu-id="1818b-116">[in]スタック上の最初の引数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1818b-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1818b-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="1818b-117">Return value</span></span>

<span data-ttu-id="1818b-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="1818b-118">S_OK</span></span> 
  
> <span data-ttu-id="1818b-119">すべてのパラメーターは、有効です。</span><span class="sxs-lookup"><span data-stu-id="1818b-119">All of the parameters are valid.</span></span> 
    
<span data-ttu-id="1818b-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="1818b-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="1818b-121">1 つまたは複数のパラメーターが有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="1818b-121">One or more of the parameters are not valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1818b-122">注釈</span><span class="sxs-lookup"><span data-stu-id="1818b-122">Remarks</span></span>

<span data-ttu-id="1818b-123">[ValidateParms](validateparms.md)マクロでは、 **ValidateParameters**マクロを置き換えられています。</span><span class="sxs-lookup"><span data-stu-id="1818b-123">The **ValidateParameters** macro has been superseded by the [ValidateParms](validateparms.md) macro.</span></span> <span data-ttu-id="1818b-124">**ValidateParameters**は、RISC プラットフォームで正常に動作しないとしてコンパイルができなきます。</span><span class="sxs-lookup"><span data-stu-id="1818b-124">**ValidateParameters** does not work correctly on RISC platforms and is now prevented from compiling on them.</span></span> <span data-ttu-id="1818b-125">それをコンパイルし、インテルのプラットフォームで正常に動作しますが、すべてのプラットフォームで**ValidateParms**をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="1818b-125">It still compiles and works correctly on Intel platforms, but **ValidateParms** is recommended on all platforms.</span></span> 
  

