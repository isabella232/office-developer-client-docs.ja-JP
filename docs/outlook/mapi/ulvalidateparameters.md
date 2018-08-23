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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 297b5a516f8275b236092f9f385afcb673c95de0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585242"
---
# <a name="ulvalidateparameters"></a><span data-ttu-id="2a88a-103">UlValidateParameters</span><span class="sxs-lookup"><span data-stu-id="2a88a-103">UlValidateParameters</span></span>

  
  
<span data-ttu-id="2a88a-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a88a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a88a-105">パラメーターのクライアント アプリケーションが、サービス ・ プロバイダーおよび MAPI 経過をチェックする内部関数が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2a88a-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2a88a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2a88a-106">Header file:</span></span>  <br/> |<span data-ttu-id="2a88a-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="2a88a-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="2a88a-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="2a88a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2a88a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2a88a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2a88a-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2a88a-110">Called by:</span></span>  <br/> |<span data-ttu-id="2a88a-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="2a88a-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="2a88a-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2a88a-112">Parameters</span></span>

 <span data-ttu-id="2a88a-113">_」方法_</span><span class="sxs-lookup"><span data-stu-id="2a88a-113">_eMethod_</span></span>
  
> <span data-ttu-id="2a88a-114">[in]確認する方法を列挙型を指定します。</span><span class="sxs-lookup"><span data-stu-id="2a88a-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="2a88a-115">_First/先頭のレコード_</span><span class="sxs-lookup"><span data-stu-id="2a88a-115">_First_</span></span>
  
> <span data-ttu-id="2a88a-116">[in]スタック上の最初の引数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2a88a-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2a88a-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="2a88a-117">Return value</span></span>

<span data-ttu-id="2a88a-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="2a88a-118">S_OK</span></span> 
  
> <span data-ttu-id="2a88a-119">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="2a88a-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="2a88a-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="2a88a-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="2a88a-121">予期しない、または不明な発生元のエラーでは、操作を完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="2a88a-121">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2a88a-122">注釈</span><span class="sxs-lookup"><span data-stu-id="2a88a-122">Remarks</span></span>

<span data-ttu-id="2a88a-123">[UlValidateParms](ulvalidateparms.md)マクロでは、 **UlValidateParameters**マクロを置き換えられています。</span><span class="sxs-lookup"><span data-stu-id="2a88a-123">The **UlValidateParameters** macro has been superseded by the [UlValidateParms](ulvalidateparms.md) macro.</span></span> <span data-ttu-id="2a88a-124">**UlValidateParameters**は、RISC プラットフォームで正常に動作しないとしてコンパイルができなきます。</span><span class="sxs-lookup"><span data-stu-id="2a88a-124">**UlValidateParameters** does not work correctly on RISC platforms and is now prevented from compiling on them.</span></span> <span data-ttu-id="2a88a-125">それをコンパイルし、インテルのプラットフォームで正常に動作しますが、すべてのプラットフォームで**UlValidateParms**をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="2a88a-125">It still compiles and works correctly on Intel platforms, but **UlValidateParms** is recommended on all platforms.</span></span> 
  

