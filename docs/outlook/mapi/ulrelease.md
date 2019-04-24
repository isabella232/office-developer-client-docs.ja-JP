---
title: UlRelease
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlRelease
api_type:
- COM
ms.assetid: 95db96ef-f95f-41da-b216-f717c23bffd2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 288e34a159db48b1344524b87f02b045259f1565
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315296"
---
# <a name="ulrelease"></a><span data-ttu-id="b9b59-103">UlRelease</span><span class="sxs-lookup"><span data-stu-id="b9b59-103">UlRelease</span></span>

  
  
<span data-ttu-id="b9b59-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9b59-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9b59-105">OLE メソッド**IUnknown:: Release**を呼び出す別の方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="b9b59-105">Provides an alternative way to invoke the OLE method **IUnknown::Release**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b9b59-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="b9b59-106">Header file:</span></span>  <br/> |<span data-ttu-id="b9b59-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b9b59-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b9b59-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="b9b59-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b9b59-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b9b59-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b9b59-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="b9b59-110">Called by:</span></span>  <br/> |<span data-ttu-id="b9b59-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="b9b59-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlRelease(
  LPVOID punk
);
```

## <a name="parameters"></a><span data-ttu-id="b9b59-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b9b59-112">Parameters</span></span>

 <span data-ttu-id="b9b59-113">_パンク_</span><span class="sxs-lookup"><span data-stu-id="b9b59-113">_punk_</span></span>
  
> <span data-ttu-id="b9b59-114">順番**IUnknown**インターフェイスから派生したインターフェイスへのポインター、つまり任意の MAPI インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="b9b59-114">[in] Pointer to an interface derived from the **IUnknown** interface, in other words any MAPI interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b9b59-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="b9b59-115">Return value</span></span>

<span data-ttu-id="b9b59-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="b9b59-116">S_OK</span></span> 
  
> <span data-ttu-id="b9b59-117">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="b9b59-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="b9b59-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="b9b59-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="b9b59-119">予期しないまたは不明な配信元のエラーにより、操作が完了しませんでした。</span><span class="sxs-lookup"><span data-stu-id="b9b59-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b9b59-120">解説</span><span class="sxs-lookup"><span data-stu-id="b9b59-120">Remarks</span></span>

<span data-ttu-id="b9b59-121">参照カウントは、解放されるオブジェクトへの既存のポインターの数です。</span><span class="sxs-lookup"><span data-stu-id="b9b59-121">The reference count is the number of existing pointers to the object to be released.</span></span> 
  
<span data-ttu-id="b9b59-122">_punk_パラメーターが NULL の場合、この関数は**IUnknown:: Release**を呼び出すことなく、すぐに戻ります。</span><span class="sxs-lookup"><span data-stu-id="b9b59-122">If the  _punk_ parameter is NULL, the function returns immediately without calling **IUnknown::Release**</span></span>
  
 <span data-ttu-id="b9b59-123">**ulrelease**は、 **IUnknown:: Release**メソッドによって返された値を返します。これは、解放されるオブジェクトの参照カウントと同じにすることができます。</span><span class="sxs-lookup"><span data-stu-id="b9b59-123">**UlRelease** returns the value returned by the **IUnknown::Release** method, which can be equal to the reference count for the object to be released.</span></span> 
  
<span data-ttu-id="b9b59-124">**iunknown:: Release**の詳細については、「 [iunknown インターフェイスを実装する](implementing-the-iunknown-interface.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9b59-124">For more information about **IUnknown::Release**, see [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span></span> 
  

