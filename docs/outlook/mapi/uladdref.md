---
title: UlAddRef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlAddRef
api_type:
- COM
ms.assetid: 9b897cbc-90b2-4c60-b5f1-dc78e7e7952d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f9e55153830dbe41a2b4a48454157c900d96cf90
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432836"
---
# <a name="uladdref"></a><span data-ttu-id="cc548-103">UlAddRef</span><span class="sxs-lookup"><span data-stu-id="cc548-103">UlAddRef</span></span>

  
  
<span data-ttu-id="cc548-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc548-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc548-105">OLE メソッド **IUnknown::AddRef を呼び出す別の方法を提供します**。</span><span class="sxs-lookup"><span data-stu-id="cc548-105">Provides an alternative way to invoke the OLE method **IUnknown::AddRef**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cc548-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="cc548-106">Header file:</span></span>  <br/> |<span data-ttu-id="cc548-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cc548-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="cc548-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="cc548-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="cc548-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="cc548-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="cc548-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="cc548-110">Called by:</span></span>  <br/> |<span data-ttu-id="cc548-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="cc548-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlAddRef(
  LPVOID punk
);
```

## <a name="parameters"></a><span data-ttu-id="cc548-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cc548-112">Parameters</span></span>

 <span data-ttu-id="cc548-113">_punk_</span><span class="sxs-lookup"><span data-stu-id="cc548-113">_punk_</span></span>
  
> <span data-ttu-id="cc548-114">[in] **IUnknown** インターフェイスから派生したインターフェイスへのポインター、つまり任意の MAPI インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="cc548-114">[in] Pointer to an interface derived from the **IUnknown** interface, in other words any MAPI interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cc548-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc548-115">Return value</span></span>

<span data-ttu-id="cc548-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="cc548-116">S_OK</span></span> 
  
> <span data-ttu-id="cc548-117">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="cc548-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="cc548-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="cc548-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="cc548-119">予期しない、または不明な発生源のエラーにより、操作が完了しなかっていません。</span><span class="sxs-lookup"><span data-stu-id="cc548-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cc548-120">注釈</span><span class="sxs-lookup"><span data-stu-id="cc548-120">Remarks</span></span>

 <span data-ttu-id="cc548-121">**UlAddRef** は、インターフェイスの参照カウントの新しい値である **IUnknown::AddRef** メソッドによって返される値を返します。</span><span class="sxs-lookup"><span data-stu-id="cc548-121">**UlAddRef** returns the value returned by the **IUnknown::AddRef** method, which is the new value of the reference count for the interface.</span></span> <span data-ttu-id="cc548-122">値は 0 以外です。</span><span class="sxs-lookup"><span data-stu-id="cc548-122">The value is nonzero.</span></span> 
  
<span data-ttu-id="cc548-123">**IUnknown::AddRef** の詳細については [、「IUnknown インターフェイスの実装」を参照してください](implementing-the-iunknown-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="cc548-123">For more information about **IUnknown::AddRef**, see [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span></span> 
  

