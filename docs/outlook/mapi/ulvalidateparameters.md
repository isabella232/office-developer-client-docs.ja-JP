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
# <a name="ulvalidateparameters"></a><span data-ttu-id="6b7a6-103">UlValidateParameters</span><span class="sxs-lookup"><span data-stu-id="6b7a6-103">UlValidateParameters</span></span>

  
  
<span data-ttu-id="6b7a6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b7a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b7a6-105">内部関数を呼び出して、クライアント アプリケーションがサービス プロバイダーと MAPI に渡したパラメーターを確認します。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b7a6-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="6b7a6-106">Header file:</span></span>  <br/> |<span data-ttu-id="6b7a6-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="6b7a6-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="6b7a6-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="6b7a6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6b7a6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6b7a6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6b7a6-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="6b7a6-110">Called by:</span></span>  <br/> |<span data-ttu-id="6b7a6-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="6b7a6-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="6b7a6-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6b7a6-112">Parameters</span></span>

 <span data-ttu-id="6b7a6-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="6b7a6-113">_eMethod_</span></span>
  
> <span data-ttu-id="6b7a6-114">[in]列挙で検証するメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="6b7a6-115">_First_</span><span class="sxs-lookup"><span data-stu-id="6b7a6-115">_First_</span></span>
  
> <span data-ttu-id="6b7a6-116">[in]スタックの最初の引数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6b7a6-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="6b7a6-117">Return value</span></span>

<span data-ttu-id="6b7a6-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="6b7a6-118">S_OK</span></span> 
  
> <span data-ttu-id="6b7a6-119">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="6b7a6-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="6b7a6-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="6b7a6-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="6b7a6-121">予期しない、または不明な発生源のエラーにより、操作が完了しなかっていません。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-121">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6b7a6-122">注釈</span><span class="sxs-lookup"><span data-stu-id="6b7a6-122">Remarks</span></span>

<span data-ttu-id="6b7a6-123">**UlValidateParameters** マクロは [、UlValidateParms](ulvalidateparms.md)マクロに取ってかえされています。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-123">The **UlValidateParameters** macro has been superseded by the [UlValidateParms](ulvalidateparms.md) macro.</span></span> <span data-ttu-id="6b7a6-124">**UlValidateParameters** は RISC プラットフォームで正しく動作し、コンパイルが行えなくなります。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-124">**UlValidateParameters** does not work correctly on RISC platforms and is now prevented from compiling on them.</span></span> <span data-ttu-id="6b7a6-125">Intel プラットフォームではコンパイルおよび正常に動作しますが、すべてのプラットフォームで **UlValidateParms** が推奨されます。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-125">It still compiles and works correctly on Intel platforms, but **UlValidateParms** is recommended on all platforms.</span></span> 
  

