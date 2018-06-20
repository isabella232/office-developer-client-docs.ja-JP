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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: fc6c12d914e581c3f975e94809f0bdea73020099
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804146"
---
# <a name="uladdref"></a><span data-ttu-id="b901b-103">UlAddRef</span><span class="sxs-lookup"><span data-stu-id="b901b-103">UlAddRef</span></span>

  
  
<span data-ttu-id="b901b-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b901b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b901b-105">OLE メソッド**IUnknown::AddRef**を起動する別の方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="b901b-105">Provides an alternative way to invoke the OLE method **IUnknown::AddRef**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b901b-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="b901b-106">Header file:</span></span>  <br/> |<span data-ttu-id="b901b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b901b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b901b-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="b901b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b901b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b901b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b901b-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b901b-110">Called by:</span></span>  <br/> |<span data-ttu-id="b901b-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="b901b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlAddRef(
  LPVOID punk
);
```

## <a name="parameters"></a><span data-ttu-id="b901b-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="b901b-112">Parameters</span></span>

 <span data-ttu-id="b901b-113">_パンク_</span><span class="sxs-lookup"><span data-stu-id="b901b-113">_punk_</span></span>
  
> <span data-ttu-id="b901b-114">[in]インターフェイスへのポインターは、任意の MAPI インターフェイスに、 **IUnknown**インターフェイスから派生します。</span><span class="sxs-lookup"><span data-stu-id="b901b-114">[in] Pointer to an interface derived from the **IUnknown** interface, in other words any MAPI interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b901b-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="b901b-115">Return value</span></span>

<span data-ttu-id="b901b-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="b901b-116">S_OK</span></span> 
  
> <span data-ttu-id="b901b-117">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="b901b-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="b901b-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="b901b-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="b901b-119">予期しない、または不明な発生元のエラーでは、操作を完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="b901b-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b901b-120">備考</span><span class="sxs-lookup"><span data-stu-id="b901b-120">Remarks</span></span>

 <span data-ttu-id="b901b-121">**UlAddRef**は、インターフェイスの参照カウントの新しい値では、 **IUnknown::AddRef**メソッドによって返される値を返します。</span><span class="sxs-lookup"><span data-stu-id="b901b-121">**UlAddRef** returns the value returned by the **IUnknown::AddRef** method, which is the new value of the reference count for the interface.</span></span> <span data-ttu-id="b901b-122">値は、0 以外の値です。</span><span class="sxs-lookup"><span data-stu-id="b901b-122">The value is nonzero.</span></span> 
  
<span data-ttu-id="b901b-123">**IUnknown::AddRef**の詳細については、 [IUnknown インターフェイスを実装する](implementing-the-iunknown-interface.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b901b-123">For more information about **IUnknown::AddRef**, see [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span></span> 
  

