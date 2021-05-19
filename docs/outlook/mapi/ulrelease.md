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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 288e34a159db48b1344524b87f02b045259f1565
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415846"
---
# <a name="ulrelease"></a><span data-ttu-id="de35f-103">UlRelease</span><span class="sxs-lookup"><span data-stu-id="de35f-103">UlRelease</span></span>

  
  
<span data-ttu-id="de35f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de35f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de35f-105">OLE メソッド **IUnknown::Release を呼び出す別の方法を提供します**。</span><span class="sxs-lookup"><span data-stu-id="de35f-105">Provides an alternative way to invoke the OLE method **IUnknown::Release**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="de35f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="de35f-106">Header file:</span></span>  <br/> |<span data-ttu-id="de35f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="de35f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="de35f-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="de35f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="de35f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="de35f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="de35f-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="de35f-110">Called by:</span></span>  <br/> |<span data-ttu-id="de35f-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="de35f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlRelease(
  LPVOID punk
);
```

## <a name="parameters"></a><span data-ttu-id="de35f-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de35f-112">Parameters</span></span>

 <span data-ttu-id="de35f-113">_punk_</span><span class="sxs-lookup"><span data-stu-id="de35f-113">_punk_</span></span>
  
> <span data-ttu-id="de35f-114">[in] **IUnknown** インターフェイスから派生したインターフェイスへのポインター、つまり任意の MAPI インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="de35f-114">[in] Pointer to an interface derived from the **IUnknown** interface, in other words any MAPI interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="de35f-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="de35f-115">Return value</span></span>

<span data-ttu-id="de35f-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="de35f-116">S_OK</span></span> 
  
> <span data-ttu-id="de35f-117">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="de35f-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="de35f-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="de35f-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="de35f-119">予期しない、または不明な発生源のエラーにより、操作が完了しなかっていません。</span><span class="sxs-lookup"><span data-stu-id="de35f-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="de35f-120">注釈</span><span class="sxs-lookup"><span data-stu-id="de35f-120">Remarks</span></span>

<span data-ttu-id="de35f-121">参照カウントは、解放するオブジェクトへの既存のポインターの数です。</span><span class="sxs-lookup"><span data-stu-id="de35f-121">The reference count is the number of existing pointers to the object to be released.</span></span> 
  
<span data-ttu-id="de35f-122">punk _パラメーターが_ NULL の場合、関数は **IUnknown::Release** を呼び出さずに直ちに返します。</span><span class="sxs-lookup"><span data-stu-id="de35f-122">If the  _punk_ parameter is NULL, the function returns immediately without calling **IUnknown::Release**</span></span>
  
 <span data-ttu-id="de35f-123">**UlRelease** は **、IUnknown::Release** メソッドによって返される値を返します。これは、解放するオブジェクトの参照カウントと等しい場合があります。</span><span class="sxs-lookup"><span data-stu-id="de35f-123">**UlRelease** returns the value returned by the **IUnknown::Release** method, which can be equal to the reference count for the object to be released.</span></span> 
  
<span data-ttu-id="de35f-124">**IUnknown::Release** の詳細については [、「IUnknown インターフェイスの実装」を参照してください](implementing-the-iunknown-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="de35f-124">For more information about **IUnknown::Release**, see [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span></span> 
  

