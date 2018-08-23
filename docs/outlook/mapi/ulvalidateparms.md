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
ms.openlocfilehash: 12b1655b1e6786d2ebc985e834b635679e59f7d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804166"
---
# <a name="ulvalidateparms"></a><span data-ttu-id="bcb42-103">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="bcb42-103">UlValidateParms</span></span>

  
  
<span data-ttu-id="bcb42-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bcb42-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bcb42-105">パラメーターのクライアント アプリケーションが、サービス ・ プロバイダーおよび MAPI 経過をチェックする内部関数が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="bcb42-105">Calls an internal function to check the parameters client applications have passed to service providers and MAPI.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bcb42-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="bcb42-106">Header file:</span></span>  <br/> |<span data-ttu-id="bcb42-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="bcb42-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="bcb42-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="bcb42-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bcb42-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="bcb42-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="bcb42-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="bcb42-110">Called by:</span></span>  <br/> |<span data-ttu-id="bcb42-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="bcb42-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT UlValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="bcb42-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bcb42-112">Parameters</span></span>

 <span data-ttu-id="bcb42-113">_」方法_</span><span class="sxs-lookup"><span data-stu-id="bcb42-113">_eMethod_</span></span>
  
> <span data-ttu-id="bcb42-114">[in]確認する方法を列挙型を指定します。</span><span class="sxs-lookup"><span data-stu-id="bcb42-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="bcb42-115">_First/先頭のレコード_</span><span class="sxs-lookup"><span data-stu-id="bcb42-115">_First_</span></span>
  
> <span data-ttu-id="bcb42-116">[in]スタック上の最初の引数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="bcb42-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bcb42-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="bcb42-117">Return value</span></span>

<span data-ttu-id="bcb42-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="bcb42-118">S_OK</span></span> 
  
> <span data-ttu-id="bcb42-119">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="bcb42-119">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="bcb42-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="bcb42-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="bcb42-121">エラーの操作を完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="bcb42-121">An error prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bcb42-122">注釈</span><span class="sxs-lookup"><span data-stu-id="bcb42-122">Remarks</span></span>

<span data-ttu-id="bcb42-123">MAPI とサービスの間で渡されるパラメーターを正しくし、 [CheckParms](checkparms.md)マクロのデバッグ検証のみを行うプロバイダーと見なされます。</span><span class="sxs-lookup"><span data-stu-id="bcb42-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="bcb42-124">プロバイダーは、クライアント アプリケーションによって渡されるすべてのパラメーターを確認する必要がありますが、クライアントが MAPI およびプロバイダーのパラメーターが正しいことを想定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bcb42-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="bcb42-125">戻り値をテストするのにには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="bcb42-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
<span data-ttu-id="bcb42-126">**UlValidateParms**マクロは、呼び出し元のコードが C または C++ のどちらであるかに応じて異なる方法で呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="bcb42-126">The **UlValidateParms** macro is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="bcb42-127">HRESULT 値の代わりに ULONG を返すいくつかの**IUnknown**と MAPI メソッドのパラメーターを検証するためにこのマクロを使用します。[ValidateParms](validateparms.md)マクロは、他のすべてのユーザーに対して機能します。</span><span class="sxs-lookup"><span data-stu-id="bcb42-127">This macro is used to validate parameters for the few **IUnknown** and MAPI methods that return ULONG instead of HRESULT values; the [ValidateParms](validateparms.md) macro works for all others.</span></span> 
  

